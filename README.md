
python --version
# vagy
python3 --version
**2. Virtuális környezet létrehozása (ajánlott, de opcionális):**

python -m venv pytorch_env
cd pytorch_env
# Aktiválás Windows-on:
pytorch_env\Scripts\activate
# Aktiválás Linux/Mac:
source pytorch_env/bin/activate

### 👉 **3. PyTorch telepítése:**

🔹 **CPU verzió (ha nincs GPU-d):**

pip install torch torchvision torchaudio
```

🔹 **GPU-s verzió (ha van NVIDIA GPU-d):**
Először ellenőrizd a CUDA verziót itt: https://pytorch.org/get-started/locally/

Példa telepítés CUDA 12-vel:
```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

### 👉 **4. Ellenőrzés: Sikeres telepítés?**

Futtasd a következő Python kódot:
```python
import torch
print(torch.__version__)
print("CUDA elérhető?" , torch.cuda.is_available())
```

Ha ez működik, akkor ✔️ PyTorch készen áll!

---

## **2. Első egyszerű példa – Tenszorok**

Próbáljuk ki az első PyTorch kódot:

```python
import torch

# Készítsünk egy 2x3-as tenszort véletlen számokkal
t = torch.rand(2, 3)
print("Tenzor:")
print(t)

# Egyszerű művelet: adjunk hozzá 1-et minden elemhez
t_plus_one = t + 1
print("Tenzor + 1:")
print(t_plus_one)
```

Kimenet például:
```
Tenzor:
tensor([[0.7452, 0.1623, 0.9394],
        [0.8741, 0.3034, 0.7689]])
Tenzor + 1:
tensor([[1.7452, 1.1623, 1.9394],
        [1.8741, 1.3034, 1.7689]])
`
