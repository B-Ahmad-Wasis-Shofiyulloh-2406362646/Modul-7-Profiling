<details>
<summary>Testing awal GUI dan CLI</summary>

### Test 1: All Students Endpoint (`/all-student`)

![All Student GUI Test](assets/images/all-student-gui.png)

**JMeter CLI result:**

![All Student CLI Test](assets/images/all-student-cli.png)

### Test 2: All Student Names Endpoint (`/all-student-name`)

![All Student Names GUI Test](assets/images/all-student-name-gui.png)

**JMeter CLI result:**

![All Student Names CLI Test](assets/images/all-student-name-cli.png)

### Test 3: Highest GPA Endpoint (`/highest-gpa`)

![Highest GPA GUI Test](assets/images/highest-gpa-gui.png)

**JMeter CLI result:**

![Highest GPA CLI Test](assets/images/highest-gpa-cli.png)

</details>

<details>
<summary>Perbandingan setelah optimisasi</summary>

### Test 1: All Students Endpoint (`/all-student`)

![All Student GUI Test](assets/images/all-student-gui.png)

**After:**

![All Student After Optimization](assets/images/all-student-after.png)

Query yang dioptimalkan mengurangi pemanggilan berulang dengan mengambil data yang dibutuhkan dalam satu query database.

### Test 2: All Student Names Endpoint (`/all-student-name`)

![All Student Names GUI Test](assets/images/all-student-name-gui.png)

**After:**

![All Student Names After Optimization](assets/images/all-student-name-after.png)

Query nama yang dioptimalkan menghindari pemuatan entity yang tidak perlu dan hanya mengembalikan nama mahasiswa.

### Test 3: Highest GPA Endpoint (`/highest-gpa`)

![Highest GPA GUI Test](assets/images/highest-gpa-gui.png)

**After:**

![Highest GPA After Optimization](assets/images/highest-gpa-after.png)

Pencarian GPA tertinggi sekarang menangani nilai yang sama dengan aman dan mengembalikan satu hasil yang deterministik.

### Conclusion

Optimisasi ini meningkatkan waktu respons dengan mengurangi overhead query dan membatasi pekerjaan database pada setiap endpoint.

</details>