# Lista do mercado (Vercel + Firebase, acesso por link)

Qualquer pessoa que abrir o link consegue ver e editar a lista, sem criar conta.
Na primeira vez, o app só pergunta o nome da pessoa.

## 1. Firebase (banco)
1. Acesse https://console.firebase.google.com e crie um projeto (pode desativar o Google Analytics).
2. Em **Build > Authentication > Get started > Sign-in method**, ative **Anônimo**.
3. Em **Build > Firestore Database > Criar banco de dados**, escolha a região `southamerica-east1 (São Paulo)` e o modo de produção.
4. Na aba **Regras** do Firestore, cole o conteúdo de `firestore.rules` e clique em **Publicar**.
5. Em **Configurações do projeto > Geral > Seus apps**, clique no ícone `</>` para registrar um app da Web. Copie o objeto `firebaseConfig` para o arquivo `firebase-config.js`.

## 2. Vercel (site)
1. Crie um repositório no GitHub e envie os arquivos desta pasta.
2. Em https://vercel.com, entre com o GitHub, clique em **Add New > Project** e importe o repositório.
3. Em **Framework Preset** deixe **Other**, sem comando de build. Clique em **Deploy**.
4. Copie o endereço gerado (ex.: `lista-mercado.vercel.app`). Esse é o link para compartilhar.

## 3. Liberar o domínio
No Firebase, em **Authentication > Settings > Authorized domains**, adicione o endereço da Vercel.

## 4. Primeiro uso
Abra o link, digite seu nome, vá na aba **Lista base** e toque em **Carregar lista base padrão**.
Para compartilhar, mande o link ou use **Orçamento > Copiar link**.

## Atenção
Quem tiver o link pode adicionar, marcar e apagar itens. Compartilhe só com quem faz compra com você.
Para dificultar que alguém encontre o site por acaso, use um nome de projeto pouco óbvio na Vercel
(ex.: `lista-casa-7k2m.vercel.app` em vez de `lista-mercado.vercel.app`).
