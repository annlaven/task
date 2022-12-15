1)	# Сортирвка пузырьком. issorted, sortperm!, sort!. Сортировка по значению функции.
function bubblesort!(a)
n = length(a)
for k in 1:n-1
is_sorted = true
for i in 1:n-k
if a[i]>a[i+1]
a[i], a[i+1] = a[i+1], a[i]
is_sorted = false
end
end
if is_sorted
break
end
end
return a
end
bubblesort(a) = bubblesort!(deepcopy(a))
реализация функции issorted
function issorted(A)
for i in 1:length(A)-1
if A[i+1]<A[i]
return false
end
end
return true
end

 
