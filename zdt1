import numpy as np
from scipy import integrate

class ZDT1:
    def len():
        return np.sqrt(5)/2+np.log(2+np.sqrt(5))/4

    def y(x):
        return (1-x)*(1-x)
    
    def dsigma(x):
        return np.sqrt(1+(2*x-2)**2)

def exact_igd(sol, k=15):
    return integrate.romberg(lambda x: np.min(np.linalg.norm(
        sol - np.array([ZDT1.y(x), x]), axis=1))*ZDT1.dsigma(x), 0, 1, divmax=k, show=False) / ZDT1.len()

sols = np.random.rand(50, 2) + 1 # solution set
print(exact_igd(sols))
