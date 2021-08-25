---
description: Descreve as etapas a serem tomadas para criptografar uma mensagem com as Funções de Criptografia Base.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Criptografando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d2a7fde500397959f0a2352b3f8ddb4fa662209afb251ddceaa8774048f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874446"
---
# <a name="encrypting-data"></a>Criptografando dados

O procedimento a seguir descreve as etapas a serem seguidas para criptografar uma mensagem com as Funções de Criptografia Base. Para criptografar mensagens usando padrões PKCS 7, consulte Funções de mensagem de nível baixo \# e Funções de mensagem [simplificadas](cryptography-functions.md) [](cryptography-functions.md) .

**Para criptografar uma mensagem**

1.  Gere uma chave de sessão usando a [**função CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)

    Fazer essa chamada gera uma chave aleatória e retorna um handle para que a chave possa ser usada para criptografar e descriptografar dados. O algoritmo de criptografia a ser usado também é especificado neste ponto. Como CryptoAPI não permite que os aplicativos usem algoritmos de chave pública para criptografar dados em massa, especifique um algoritmo simétrico como RC2 ou RC4 com a [**chamada CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)

2.  Como alternativa, use a [**função CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) para transformar uma senha em uma chave adequada para criptografia.

    Se um aplicativo precisar criptografar a mensagem para que qualquer pessoa com uma senha especificada possa descriptografar os dados, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) para transformar a senha em uma chave adequada para criptografia.

    > [!Note]  
    > Nesse caso, essa função é chamada em vez da [**função CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) e as chamadas [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) subsequentes não são necessárias.

     

3.  Se necessário, de definir propriedades criptográficas extras da chave usando a [**função CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)

    Depois que a chave tiver sido gerada, as propriedades criptográficas extras da chave poderão ser definidas com a [**função CryptSetKeyParam.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) Essa função permite que diferentes seções do arquivo sejam criptografadas com diferentes sais de chave e fornece uma maneira de alterar o modo de codificação ou o vetor de inicialização da chave. Esses parâmetros podem ser usados para fazer com que a criptografia esteja em conformidade com um padrão de criptografia de dados específico.

4.  Criptografe os dados no arquivo com a [**função CryptEncrypt.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt)

    A [**função CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) pega a chave de sessão que foi gerada na etapa anterior e criptografa um buffer de dados.

    > [!Note]  
    > À medida que os dados são criptografados, os dados podem ser ligeiramente expandidos pelo algoritmo de criptografia. O aplicativo é responsável por lembrar o comprimento dos dados criptografados para que o comprimento apropriado possa ser especificado posteriormente para a [**função CryptDecrypt.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt)

     

5.  Opcionalmente, use [**a função CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) para permitir que o usuário atual descriptografe os dados no futuro.

    Para permitir que o usuário atual descriptografe os dados no futuro, a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) é usada para salvar a chave de descriptografia em um formulário criptografado (um BLOB de chave) que só pode ser descriptografado com a chave privada do usuário. Essa função requer a chave pública de troca de chaves do usuário para essa finalidade, que pode ser obtida usando a [**função CryptGetUserKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) A **função CryptExportKey** retornará um BLOB de chave que deve ser armazenado pelo aplicativo para uso na descriptografia do arquivo

> [!Note]  
> Se o aplicativo tiver certificados (ou chaves públicas) para outros usuários, ele poderá permitir que outros usuários descriptografem o arquivo executando chamadas [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) para cada usuário que deve receber acesso. Os BLOBs de chave retornados devem ser armazenados pelo aplicativo, como na etapa 5.

 

## <a name="creating-an-encrypted-message"></a>Criando uma mensagem criptografada

As funções de mensagem simplificadas facilitam a criptografia e a descriptografia de dados. A ilustração a seguir ilustra as tarefas individuais que devem ser realizadas para criptografar uma mensagem. As etapas são descritas na lista a seguir.

![criptografando uma mensagem](images/encmsg.png)

**Para criptografar uma mensagem**

1.  Obter um ponteiro para a mensagem de texto não criptografado.
2.  Gere uma chave simétrica (sessão).
3.  Usando a chave simétrica e o algoritmo de criptografia especificado, criptografe os dados da mensagem.
4.  Abra um armazenamento de certificados.
5.  Obter o certificado do destinatário.
6.  Obter a chave pública do certificado do destinatário.
7.  Usando a chave pública do destinatário, criptografe a chave simétrica.
8.  Obter o identificador do destinatário do certificado do destinatário.
9.  Inclua o seguinte na mensagem enveloada digitalmente: o algoritmo de criptografia de dados, os dados criptografados, a chave simétrica criptografada e o identificador do destinatário.

 

 



