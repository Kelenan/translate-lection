# translate-lection
разбор задачи с функцией и массивом

//void (пустота) - процедура которая похожа на функцию, но не возвращает никаких значений
void FillArray(int[] collection) // обозначаем процедуру с названием FillArray (заполнения массива) на вход данной процедуры должен поступать массив
{
    int length = collection.Length;   // целочисленная переменная length (длина) в которую помещаем значение метода Length (возвращает длину или количество элементов массива)
    int index = 0;
    while (index < length)
    {
       collection[index] = new Random() .Next(1, 10);
        //index = index +1
        index ++;
    }
}

void PrintArray(int[] col) // процедура с названием PrintArray(печать массива) для вывода массива в консоле
{
    int count = col.Length; //count - подсчет
    int position = 0;
    while (position < count)
    {
        Console.WriteLine(col[position]);
        position ++;
    }
}

int indexOF(int[] collection, int find) // функция целочисленного числа с названием indexOF, на вход поступают2 переменные: 1 массив, 2 элемент индекс которого мы должны найти
{
    int count = collection.Length; 
    int index = 0;
    int position = -1;
    while (index < count)
    {
        if(collection[index]== find)
        {
            position = index; 
            break; // прерывание цикла
        }
        index++;
    }
    return position; //возвращает значение того же типа данных как и функция, после выполнения данной функции
}

int [] array = new int [10];

FillArray(array); // на вход процедуры мы впускаем массив под названием array который назначили выше
array[4] = 4;
array[6] = 4;

PrintArray(array);
Console.WriteLine();

int pos = indexOF(array, 444);
Console.WriteLine(pos);
