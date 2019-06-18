# 2phase-LBM-DNS
This project will reproduce the lattice Boltzmann method with DNS (direct numerical simulation) for the gas-solid two-phase flow using c language.
***
### 1. File structure as follows:
		+ CalcSolidConcentrationInterp
		  - Calc20131129.m ---> Calculate the overlap area of the circle and square
		  - dat.txt ---> results obained from the above program
		  - ReadData.cpp ---> reading dat.txt and do bilinear interpolation
		  - readme.txt ---> detailed description for files in this folder
		+ LBMDNS.cpp ---> main program using c program
		+ SolidConcentration.txt ---> solid concentration data
### 2. Functions in LBMDNS.cpp:
		+ void EsDataRead() ---> read solid concentration into ESMatrix
		+ double EsInterp(double x,double y) ---> calculate solid concentration using bilinear interpolation
		+ void SetLBMParameter() ---> D2Q9
		+ double f_equ(double ux, double uy, double rho, int b) ---> calculate the value of the equilibrium distribution function