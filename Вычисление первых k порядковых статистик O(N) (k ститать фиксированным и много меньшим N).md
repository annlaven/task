# 14)Вычисление первых k порядковых статистик O(N) (k ститать фиксированным и много меньшим N)

function minimums(array, k)
N = length(array)
k_minimums = sort(array[1:k])
i = k
# ИНВАРИАНТ: issorted(k_mins) && k_mins - содержит k наименьших элементов в
array[1:i]
while i < length(array)
i += 1
if array[i] < k_minimums[end]
k_minimums[end] = array[i]
insert_end!(k_minimums)
end
end
return k_minimums
end
function insert_end!(array)::Nothing
j = length(array)
while j>1 && array[j-1] > array[j]
array[j-1], array[j] = array[j], array[j-1]
j -= 1
end
end
