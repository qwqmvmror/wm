def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        # 提前退出冒泡循环的标志位
        swapped = False
        # 每次比较相邻的两个元素
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                # 交换元素
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True
        # 如果没有发生交换，说明已经有序，提前退出
        if not swapped:
            break
    return arr

# 测试代码
if __name__ == "__main__":
    # 输入一个未排序的列表
    unsorted_list = [64, 34, 25, 12, 22, 11, 90]
    print("未排序的列表:", unsorted_list)
    
    # 调用冒泡排序函数
    sorted_list = bubble_sort(unsorted_list)
    print("排序后的列表:", sorted_list)