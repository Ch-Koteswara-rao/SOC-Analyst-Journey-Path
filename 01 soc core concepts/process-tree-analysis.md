# Process Tree Analysis

Process tree analysis is used to understand how processes start and interact with each other on a system. It helps identify suspicious execution patterns and trace the origin of malicious activity.

Every process has a parent process that started it. By examining these relationships, analysts can determine whether execution behavior is normal or potentially malicious.

---

## 🌳 Process Relationship

A process tree shows the chain of execution from the original process to its child processes.

This structure helps visualize how activity originated and what actions followed.

Example:

```
explorer.exe
 └── chrome.exe
```

This indicates the user launched Chrome from the system interface, which is expected behavior.

---

## 🔍 Identifying Suspicious Execution

Malicious activity often appears when trusted applications launch unexpected processes. Attackers use legitimate programs to execute hidden commands.

Analyst actions:

- Identify the parent process that initiated execution
- Check whether the child process is expected behavior
- Look for unusual process chains involving scripting engines or system tools
- Trace execution back to its origin

Example:

```
winword.exe
 └── powershell.exe
```

This indicates PowerShell was launched from Microsoft Word, which is not typical and may suggest malicious macro execution.

---

## ⚠️ Recognizing Malicious Process Chains

Certain process chains are commonly associated with attacks. These patterns may indicate unauthorized command execution.

Example:

```
winword.exe
 └── powershell.exe
      └── cmd.exe
```

This sequence shows a document launching command-line activity, which is abnormal and requires investigation.

---

## 🧠 Analyst Investigation Focus

When reviewing process trees, analysts focus on:

- Unexpected parent-child relationships
- Execution originating from user directories
- Script interpreters launched by non-administrative applications
- Processes that initiate network communication after execution

These indicators help determine whether activity is legitimate or malicious.

---

## Example of Normal vs Suspicious Behavior

Normal execution:

```
explorer.exe → notepad.exe
```

Suspicious execution:

```
winword.exe → powershell.exe → external connection
```

The second chain indicates abnormal behavior and requires escalation.

---

## Key Understanding

- Process trees show how execution originates and progresses
- Parent-child relationships help identify attack entry points
- Suspicious process chains indicate potential compromise
- Process analysis is critical for detecting malicious execution
