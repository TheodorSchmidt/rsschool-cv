1. Bogdan Zakharov
2. Phone number: +79050312252, Email: bogdan_zakharov_99@mail.ru
3. I want to become a front-end developer. I have no work experience, but I have ambitions and a desire to learn new things. My strengths are self-critical attitude, thoroughness, diligence.
4. Basics of C++, C#, SQL, Python and more.
5. Code examples:
```
void IntegralRect(const double a, const double b, const double h, double *res) {
	int i, n;
	double sum;
	double x;
	n = (int)((b - a) / h);
	sum = 0.0;
#pragma omp parallel for private(x) reduction(+:sum)
	for (i = 0; i < n; i++) {
		x = a + i * h + h / 2.0;
		sum += fun(x) * h;
	}
	*res = sum;
}

void IntegralSimpson(const double a, const double b, const double h, double* res) {
	double temp = a;
	double x;
	double sum = fun(a) + fun(b);
	int n = (int)((b - a) / (2 * h));
	double sum1 = 0;
#pragma omp parallel for private(x) reduction(+: sum1)
	for (int i = 1; i < n; i++) {
		x = a + (2.0 * i - 1) * h;
		sum1 += fun(x);
	}
	sum += 4 * sum1;
	double sum2 = 0;
#pragma omp parallel for private(x) reduction(+: sum2)
	for (int i = 1; i < n - 1; i++) {
		x = a + 2.0 * i * h;
		sum2 += fun(x);
	}
	sum += 2 * sum2;
	sum *= h / 3;
	*res = sum;
}
```
7. I have no work experience
8. I am studying at the 3rd year of the CSIT department of Saratov State University
9. B1. I am getting additional education in the field of translator in professional communication.
