# Bebracci-sequence
The Bebracci Sequence is a fast-growing integer recurrence sequence initialized by seeds b(-2)=1, b(-1)=2, b(0)=4, and b(1)=6. For indices n ≥ 2, terms compound via the cross-product recurrence formula b(n) = b(n-1)·b(n-2) + b(n-3)·b(n-4). The sequence yields b(2)=26 and b(3)=164, exhibiting hyper-exponential growth suited for googology.

the code is:def generate_bebracci(terms):
    b = {
        -2: 1,
        -1: 2,
        0: 4,
        1: 6
    }
    
    for n in range(2, terms + 1):
        b[n] = (b[n-1] * b[n-2]) + (b[n-3] * b[n-4])
        
    return b

# Test the function by generating up to b(7)
sequence = generate_bebracci(7)
for index in sorted(sequence.keys()):
    print(f"b({index}) = {sequence[index]}")



     try it in phyton or like pydroid if your mobile
