 ## Assinaturas Chave GPG


Lista as chaves geradas:

    gpg --list-secret-keys --keyid-format LONG


Gera uma nova chave

    gpg --full-generate-key


Exporta chave

    gpg --armor --export [CHAVE_ID]

Adiciona configuração no git para assinar

    git config --global user.signingkey [CHAVE_ID]


Adiciona no bash / profile variavel de ambiente

    export GPG_TTY=$(tty)

Define por padrão para assinar todos os commits

    git config --global commit.gpgsign true
    git config --global tag.gpgsign true