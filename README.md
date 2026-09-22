# GABEFIT

Protótipo web de acompanhamento de alimentação, calorias, treino, histórico e composição corporal.

## Publicar gratuitamente com GitHub Pages

1. Crie um repositório público no GitHub, por exemplo `gabefit`.
2. Envie todos os arquivos deste projeto para a branch `main`.
3. Abra `Settings > Pages` no repositório.
4. Em `Build and deployment`, selecione `GitHub Actions`.
5. O workflow `.github/workflows/pages.yml` fará o deploy automaticamente.
6. O endereço será semelhante a `https://SEU-USUARIO.github.io/gabefit/`.

O GABEFIT atual funciona como protótipo estático: os dados ficam no navegador via `localStorage`. Isso significa que, nesta versão, os dados não sincronizam entre computador e celular.

## Próxima etapa: banco e login

Para transformar o protótipo em aplicação multi-dispositivo, a arquitetura recomendada é:
- GitHub Pages para o frontend estático;
- Supabase Auth para login;
- Supabase/Postgres para perfil, refeições, metas, treinos e histórico;
- uma função de backend/Edge Function para chamadas à API de IA.

Nunca coloque uma chave secreta de servidor da OpenAI ou uma chave `service_role` do Supabase no JavaScript publicado no navegador.
