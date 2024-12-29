# ssh-keygen

## Passo a Passo Simples para Criar uma Nova Chave SSH

## Windows

### Iniciar o processo de geração da chave: Execute o comando no PowerShell:
 ```
ssh-keygen -t rsa -b 4096 -C "chave_ssh"
```

O argumento `-C "chave_ssh"` adiciona um comentário para identificação.

### Especificar o local para salvar a chave:

O prompt sugere o local padrão `(C:\Users\pedro silva/.ssh/id_rsa)`.

Como já existia uma chave nesse local, você digitou:
```
C:\Users\pedro silva\.ssh\chave_ssh
```
Isso garantiu que uma nova chave fosse criada com o nome `chave_ssh`.

### Definir uma senha (opcional):

Foi solicitado que você definisse uma senha para a chave privada.

Caso tenha escolhido não definir, apenas pressionou Enter.

### Salvar a chave com sucesso:

Após confirmar o nome e a senha, a chave foi salva:

Chave privada: `C:\Users\pedro silva\.ssh\chave_ssh`

Chave pública: `C:\Users\pedro silva\.ssh\chave_ssh.pub`

### Verificar o resultado:

O PowerShell exibiu informações sobre a chave criada:

- Fingerprint da chave: Uma impressão digital única da chave.

- Randomart image: Uma representação visual para verificar a autenticidade.

### Capturar as chaves

Use aspas ao redor do caminho completo do arquivo:
```
cat "C:\Users\pedro silva\.ssh\chave_ssh.pub"
```
ou 
```
cat "C:\Users\pedro silva\.ssh\chave_ssh"
```

⚠️ Atenção: Nunca compartilhe sua chave privada!

## Linux

### Iniciar o processo de geração da chave: Abra o terminal no Linux e execute o comando:

```
ssh-keygen -t rsa -b 4096 -C "chave_ssh"
```

- O argumento -C "chave_ssh" adiciona um comentário para facilitar a identificação da chave.

### Especificar o local para salvar a chave:

- O terminal sugere um local padrão (geralmente /home/seu_usuario/.ssh/id_rsa).
- Caso já exista uma chave no local padrão, você pode fornecer um novo caminho, por exemplo:

```
/home/pedro/.ssh/chave_ssh
```

- Isso criará uma nova chave com o nome chave_ssh.

### Definir uma senha (opcional):

- Durante o processo, será solicitado que você defina uma senha para proteger a chave privada.
- Caso não deseje definir uma senha, apenas pressione Enter.

### Salvar a chave com sucesso:

- Após confirmar o nome e a senha, as chaves serão geradas e salvas nos seguintes arquivos:
  - Chave privada: `/home/pedro/.ssh/chave_ssh`
  - Chave pública: `/home/pedro/.ssh/chave_ssh.pub`

### Verificar o resultado:

- O terminal exibirá informações sobre a chave criada:
  - Fingerprint: Uma impressão digital única da chave.
  - Randomart image: Uma representação visual usada para validar a autenticidade.

### Capturar as chaves:

- Para exibir o conteúdo da chave pública, execute:
```
cat /home/pedro/.ssh/chave_ssh.pub
```
- Para exibir o conteúdo da chave privada, execute:
```
cat /home/pedro/.ssh/chave_ssh
```
⚠️ Atenção: Nunca compartilhe sua chave privada!
