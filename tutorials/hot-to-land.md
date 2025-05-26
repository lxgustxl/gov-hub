## 🎨 Tutorial: Como mexer com a **Landing Page** (Vite + Tailwind)

Este tutorial orienta como instalar, configurar, rodar e contribuir com a **Landing Page** do projeto, que utiliza **Vite** com **Tailwind CSS**.

---

### ✅ Pré-requisitos

* **Node.js** e **npm** instalados
* **Git** (para clonar o repositório)
* Dependências do Vite e Tailwind

---

### ✅ Passo 1: Navegar até a pasta da landing page

A landing page está localizada dentro da pasta:

```
docs/land/
```

Acesse-a via terminal:

```bash
cd docs/land
```

---

### ✅ Passo 2: Instalar as dependências

Na pasta `docs/land`, execute:

```bash
npm install
```

Isso irá instalar as dependências necessárias para o **Vite** e **Tailwind CSS**.

---

### ✅ Passo 3: Executar a landing page localmente

Ainda na pasta `docs/land`, rode o comando:

```bash
npm run dev
```

➡️ O Vite iniciará um servidor local.
➡️ Acesse no navegador: [http://127.0.0.1:5173](http://127.0.0.1:5173) (ou a porta exibida no terminal).

> 📌 Esse comando é recomendado para desenvolvimento, pois permite **hot reload** (atualização automática ao salvar arquivos).

---

### ✅ Passo 4: Fazer alterações na landing page

As principais pastas/arquivos para editar são:

```
docs/land/
├── src/             # Componentes e lógica principal
├── public/          # Arquivos estáticos
├── index.html       # Estrutura principal da página
├── style.css        # Arquivo de estilos base
├── tailwind.config.js # Configuração do Tailwind CSS
└── vite.config.js   # Configuração do Vite
```

Edite o que for necessário e salve: o Vite irá atualizar automaticamente no navegador.

---

### ✅ Passo 5: Gerar o build para produção

Para gerar os arquivos otimizados da landing page, execute:

```bash
npm run build
```

➡️ Os arquivos finais serão gerados automaticamente na pasta:

```
docs/land/dist/
```

Esses arquivos são **referenciados automaticamente** pelo **MkDocs** ao rodar `mkdocs serve` ou `mkdocs build`.

**Importante:** após qualquer alteração no código da landing page, é **obrigatório rodar** `npm run build` para atualizar os arquivos estáticos utilizados no MkDocs.

---

### ✅ Passo 6: Atualizar visualização via MkDocs

Se estiver rodando o **MkDocs** com:

```bash
mkdocs serve
```

➡️ Precisa abrir **um segundo terminal**, acessar `docs/land` e rodar `npm run build` sempre que fizer alterações na landing page.

Assim o MkDocs irá renderizar corretamente a versão atualizada da landing.

---

### ✅ Estrutura relevante para a landing page

```
docs/
└── land/
    ├── dist/              # Arquivos estáticos gerados pelo build
    ├── node_modules/      # Dependências
    ├── public/            # Arquivos públicos
    ├── src/               # Código-fonte
    ├── index.html         # Estrutura da página
    ├── package.json       # Scripts e dependências
    ├── tailwind.config.js # Configuração do Tailwind
    └── vite.config.js     # Configuração do Vite
```

---

### ✅ Boas práticas

✔️ Sempre rode `npm run build` após alterações importantes.
✔️ Mantenha imagens e assets públicos dentro da pasta `public/`.
✔️ Use `npm run dev` para desenvolvimento local com **hot reload**.

---

**✅ Pronto!** Agora você sabe como mexer com a **Landing Page** do Gov Hub BR utilizando **Vite** e **Tailwind CSS**.