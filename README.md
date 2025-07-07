
## 📘 Ansible: File Module Example

### 🧾 Playbook: `02_file_module.yml`

This playbook demonstrates the use of the `file` module to create files on Docker containers using Ansible.

---

### 🔍 What Happens:

1. **The playbook targets the host group `ansible_nodes`**, defined in `inventory.ini` with `docker` connection type.

2. **It performs 3 tasks:**

   * 🟢 `Create a hello.txt file`

     * Creates the file `/tmp/hello.txt` on all hosts.

   * 🟡 `Create multiple files with loop`

     * Creates `/tmp/loop1.txt`, `/tmp/loop2.txt`, `/tmp/loop3.txt` on each container using a `loop:`.

   * 🔵 `Create a file only on ansible-node1`

     * Creates `/tmp/special.txt` only on `ansible-node1` using a `when:` condition.

---

### 📂 File Structure:

```
ansible/
├── inventory.ini
├── playbooks/
│   └── 02_file_module.yml
```

---

### 🧠 Key Concepts Covered:

* Usage of `file` module (`ansible.builtin.file`)
* Creating a file
* Looping with `loop`
* Conditional execution with `when:`

---

### ▶️ Run Command:

```bash
ansible-playbook -i inventory.ini playbooks/02_file_module.yml
```

---

✅ Ready for the next step: **Variables**
