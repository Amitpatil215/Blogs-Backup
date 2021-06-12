## Convert TimeOfDay To DateTime in Dart

```timeOfDayToDateTime()``` function converts ```TimeOfDay``` object to ```DateTime```. You can optionally pass ```DateTime``` value to merge with particular date. 

```dart
DateTime timeOfDayToDateTime(TimeOfDay timeOfDay, {DateTime? dateTime}) {
  if (dateTime != null) {
    return DateTime(dateTime.year, dateTime.month, dateTime.day, timeOfDay.hour,
        timeOfDay.minute);
  } else {
    final now = DateTime.now();
    return DateTime(
        now.year, now.month, now.day, timeOfDay.hour, timeOfDay.minute);
  }
}
```

#### Example (Merge with current date)

```dart
void main() {
	final timeofday=TimeOfDay(hour:4,minute: 22);
	print(timeOfDayToDateTime(timeofday));
}

// Output
2021-06-12 04:22:00.000
```

#### Example (Merge with custom date)

```dart
void main() {
	final timeofday=TimeOfDay(hour:4, minute: 22);
	final dateTime= DateTime(2022, 5, 21);
	print(timeOfDayToDateTime(timeofday, dateTime:dateTime));
}

// Output
2022-05-21 04:22:00.000
```