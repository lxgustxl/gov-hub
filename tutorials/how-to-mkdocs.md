## 📄 Tutorial: Como mexer com a **Documentação** (MkDocs)

Este tutorial orienta como instalar, configurar, rodar e contribuir com a **documentação** do projeto, que utiliza o **MkDocs** com o tema **Material**.

---

### ✅ Pré-requisitos

* **Python 3.x** instalado
* **pip** (gerenciador de pacotes do Python)
* **Git** (para clonar o repositório)

---

### ✅ Passo 1: Instalar as dependências

Na raiz do projeto, instale as dependências necessárias para o MkDocs:

```bash
pip install -r requirements.txt
```

---

### ✅ Passo 2: Executar a documentação localmente

Na raiz do projeto, rode o seguinte comando:

```bash
mkdocs serve
```

> Isso irá iniciar um servidor local.

Acesse no navegador:
➡️ [http://127.0.0.1:8000](http://127.0.0.1:8000)

Por padrão, a **landing page** será carregada e, ao clicar em **"Docs"** no menu de navegação, você será redirecionado para a documentação gerada pelo MkDocs.

---

### ✅ Passo 3: Fazer alterações na documentação

Os arquivos de documentação estão organizados na pasta:

```
docs/
```

Cada seção corresponde a um arquivo Markdown `.md`.

Exemplos:

* `docs/index.md` - Página de redirecionamento para a landing page  
* `docs/home.md` – Página inicial da documentação  
* `docs/sobre-projeto/` – Informações detalhadas sobre o propósito, objetivos, equipe e sistemas estruturantes do projeto  
* `docs/replicacao/` – Guia prático para replicação do projeto em outros órgãos, incluindo pré-requisitos, arquitetura de solução, integração de dados e templates de dashboards  

Edite ou adicione arquivos `.md` conforme a necessidade.

---

### ✅ Passo 4: Gerar o site estático

Após as alterações, para gerar os arquivos estáticos da documentação, execute:

```bash
mkdocs build
```

Os arquivos gerados ficam na pasta:

```
site/
```

Essa pasta pode ser publicada em servidores como **GitHub Pages**.

---

### ✅ Estrutura relevante para a documentação

```
docs/  
├── assets/            # Imagens e arquivos auxiliares utilizados na documentação  
│   ├── images/       # Imagens gerais  
│   └── stylesheets/  # Arquivos CSS personalizados  
├── blog/              # Publicações e anotações complementares  
├── contributing/      # Guia de contribuição com diversos tópicos técnicos  
├── land/              # Código-fonte da landing page (baseado em Vite + Tailwind)  
├── replicacao/        # Guia prático para replicação do projeto em outros órgãos  
├── schema/            # Arquivos relacionados aos esquemas e extensões de dados  
├── setup/             # Arquivos de configuração e instalação  
├── sobre-projeto/     # Propósito, objetivos, equipe e sistemas estruturantes  
├── getting-started.md # Guia rápido de início  
├── guia-usuario.md    # Orientações para novos usuários  
├── home.md            # Página inicial da documentação  
├── index.md           # Página de redirecionamento para a landing page  
└── schema.json        # Arquivo de esquema JSON global  
```

**Customizações de layout** → `material/overrides/` → Contém templates (`home.html`, `main.html`) e hooks para personalização do tema **Material for MkDocs**.

📌 **Importante**:

* A pasta `material/overrides/` **não está dentro de `docs/`**, mas sim na raiz do projeto, ao lado das pastas `docs/`, `site/` e `src/`.
* A landing page está localizada em `docs/land` e é gerenciada separadamente com Vite.

---

### ✅ Boas práticas

✔️ Utilize `mkdocs serve` para visualizar alterações em tempo real
✔️ Mantenha imagens e arquivos estáticos em `docs/assets/`

---

**✅ Pronto!** Agora você sabe como mexer com a **documentação** do Gov Hub BR utilizando **MkDocs**.

---