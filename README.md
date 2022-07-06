#예산

def solution(d, budget):
    answer = 0
    d.sort()
    for i in range(len(d)):
        if budget- d[i] >= 0:
            print(budget)
            budget -= d[i]
            answer +=1
        else:
            break
    return answer

#print(solution([2,3,3,3],	10))
#ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

def solution(d, budget):
    d.sort()
    while budget < sum(d):
        d.pop()
    return len(d)
