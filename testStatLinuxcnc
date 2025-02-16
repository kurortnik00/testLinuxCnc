import linuxcnc

# Создаем объекты для взаимодействия с LinuxCNC
s = linuxcnc.stat()  # Для чтения состояния
c = linuxcnc.command()  # Для отправки команд

# Обновляем состояние
s.poll()

# Выводим текущее состояние
print("Текущий режим:", s.task_mode)
print("Текущее состояние:", s.task_state)
print("Текущая позиция:", s.position)

# Пример отправки команды
try:
    c.mode(linuxcnc.MODE_AUTO)  # Переключение в автоматический режим
    c.wait_complete()  # Ожидание завершения команды
    print("Режим изменен на Auto")
except linuxcnc.error as e:
    print("Ошибка:", e)