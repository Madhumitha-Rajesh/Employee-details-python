# Employee-details-python

def get_employee_details():
    name=input("Enter Employee Name:")
    emp_id=input("Enter Employee ID:")
    dept=input("Enter department:")
    bas_sal=float(input("Enter Basic Salary:"))
    return name,emp_id,dept,bas_sal

def calc_sal(basic_sal):
    hra=bas_sal*0.20
    da=bas_sal*0.10
    pf=bas_sal*0.12
    gross_sal=bas_sal+hra+da
    net_sal=gross_sal-pf
    return hra,da,pf,gross_sal,net_sal


def print_sal_slip(name,emp_id,dept,bas,hra,da,pf,gross,net):
    print("\n ================= EMPLOYEE SALARY SLIP===============")
    print("Employee Name: ",name)
    print("Employee ID: ",emp_id)
    print("Department: ",dept)
    print("--------------------------------------------------------")
    print("Basic Salary: Rs.",bas_sal)
    print("HRA(20%): Rs.",da)
    print("DA (10%)        : Rs.", da)
    print("PF Deduction    : Rs.", pf)
    print("--------------------------------------------------------")
    print("Gross Salary    : Rs.", gross)
    print("Net Salary      : Rs.", net)
    print("========================================================")

name, emp_id, dept, bas_sal = get_employee_details()
hra, da, pf, gross, net = calc_sal(bas_sal)
print_sal_slip(name,emp_id,dept,bas_sal,hra,da,pf,gross,net)

Output:

Enter Employee Name:Sakthi
Enter Employee ID:S2204564
Enter department:Marketing
Enter Basic Salary:75000

 ================= EMPLOYEE SALARY SLIP===============
Employee Name:  Sakthi
Employee ID:  S2204564
Department:  Marketing
--------------------------------------------------------
Basic Salary: Rs. 75000.0
HRA(20%): Rs. 7500.0
DA (10%)        : Rs. 7500.0
PF Deduction    : Rs. 9000.0
--------------------------------------------------------
Gross Salary    : Rs. 97500.0
Net Salary      : Rs. 88500.0
========================================================




