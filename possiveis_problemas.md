ionic cap add android

Caso o comando acima não funcione

Verificar com package.json e colocar o ^ antes do número da versão

@capacitor/app
@capacitor/core
@capacitor/cli

e rodar o comando npm install @capacitor/android
# ########################################
ionic build            # cria a pasta dist
npx cap add android    # Adiciona a pasta do android no projeto
npx cap copy           # copia os arquivos da dist para o android
npx cap sync           # Sincroniza alguma alteração realizada na pasta dist
npx cap open android   # abre o projeto no android studio
