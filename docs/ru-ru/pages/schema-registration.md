# Регистрация схемы

Теперь, нам необходимо зарегистрировать нашу схему, чтобы `kindagoose` смог превратить её в модель, поддерживающую
инъекцию зависимостей `NestJS`! Чтобы зарегистрировать схему, вам необходимо вызвать метод `forFeature`
у `KindagooseModule`:

```typescript
@Module({
  imports: [
    KindagooseModule.forFeature([
      { schema: User },
    ]),
  ],
  controllers: [UsersController],
  providers: [UsersService],
})
export class UsersModule {}
```

!> Заметьте, что для каждого модуля схемы регистрируются отдельно. Вы не можете зарегистрировать схему один раз и
глобально, вы должны использовать `forFeature` всякий раз, как ваш модуль требует какую-либо модель. Также стоит
взглянуть на сигнатуру `forFeature` — метод принимает в себя неограниченное количество объектов
типа `SchemaRegistrationOptions`, поэтому, вам не стоит дублировать его вызовы.