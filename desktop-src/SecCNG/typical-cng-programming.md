---
description: A API CNG implementa um modelo de provedor extensível que permite carregar um provedor especificando o algoritmo criptográfico necessário em vez de um provedor específico.
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: Programação CNG típica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1cd45c68d7c34c3815008690b49cabfefff437222b29512abbf858cf3b370f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905517"
---
# <a name="typical-cng-programming"></a>Programação CNG típica

A API CNG implementa um modelo de provedor extensível que permite carregar um provedor especificando o algoritmo criptográfico necessário em vez de um provedor específico. A vantagem é que um provedor de algoritmo pode ser substituído ou atualizado e você não precisará alterar seu código de qualquer forma para usar o novo provedor. Além disso, se algum algoritmo for determinado como não seguro no futuro, uma versão mais segura desse algoritmo poderá ser instalada sem afetar seu código. A maioria das APIs CNG requer um provedor ou um objeto criado por um provedor.

As etapas típicas envolvidas no uso da API CNG para operações primitivas de criptografia são as seguintes:

1.  Abrindo o provedor de algoritmos
2.  Obtendo ou definindo propriedades de algoritmo
3.  Criando ou importando uma chave
4.  Executando operações criptográficas
5.  Fechando o provedor de algoritmos

Para obter mais informações, consulte exemplos de programação.

## <a name="opening-the-algorithm-provider"></a>Abrindo o provedor de algoritmos

A função [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) fornece um identificador de provedor de algoritmo que é usado em APIs CNG subsequentes, como [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) ou [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair).

## <a name="getting-or-setting-algorithm-properties"></a>Obtendo ou definindo propriedades de algoritmo

Você pode usar o identificador do provedor de algoritmos para obter detalhes de implementação para o algoritmo, como o tamanho da chave ou o modo atual de operação. Use a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obter propriedades específicas.

Você também pode modificar as propriedades do algoritmo. Por exemplo, se você quiser usar o encadeamento de codificação de bloco ECB com AES, defina a **propriedade \_ \_ modo de encadeamento BCRYPT** de um algoritmo AES para **o \_ modo de cadeia BCrypt \_ \_ ECB**; a propriedade é atribuída a todas as chaves AES criadas usando esse identificador de algoritmo, sem a necessidade de configurar cada chave AES. Use a função [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para modificar essas propriedades.

## <a name="creating-or-importing-a-key"></a>Criando ou importando uma chave

Dependendo do tipo de algoritmo usado, talvez seja necessário criar ou carregar uma chave. Por exemplo, a função [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) usa um identificador de chave para o primeiro parâmetro. Se você quiser que essa função criptografe dados com um algoritmo de criptografia simétrica como AES, primeiro você deve obter uma chave. A forma como você obtém a chave depende do tipo de algoritmo que está sendo usado e da origem da chave.

Você pode criar chaves efêmeras com as funções [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) e [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) . Você também pode importar chaves efêmeras de um BLOB de memória com as funções [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) e [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) .

Para chaves persistentes, você usa as funções de armazenamento de chaves para carregar um provedor de armazenamento de chaves e, em seguida, criar ou carregar as chaves. Você também pode usar essas funções para criar ou carregar chaves efêmeras passando **NULL** para qualquer nome de contêiner. para obter mais informações sobre as funções de armazenamento de chaves, consulte [funções de Armazenamento de chave CNG](cng-key-storage-functions.md).

## <a name="performing-cryptographic-operations"></a>Executando operações criptográficas

Agora você está pronto para executar a operação criptográfica, como criptografar ou descriptografar dados usando as funções [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) ou [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) , respectivamente.

## <a name="closing-the-algorithm-provider"></a>Fechando o provedor de algoritmos

Quando o provedor não for mais necessário, você deve passar o identificador para a função [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) para fechar o provedor. Isso faz com que o provedor libere todos os recursos que foram alocados para essa instância do provedor de algoritmo. Depois que um identificador de provedor é fechado, ele não pode ser reutilizado.

O carregamento de um provedor pode ser um processo relativamente demorado. Portanto, você deve armazenar em cache quaisquer identificadores de provedor que serão referenciados várias vezes durante o tempo de vida do seu aplicativo.

## <a name="programming-examples"></a>Exemplos de programação

Os exemplos a seguir descrevem como executar operações criptográficas específicas usando a CNG.

-   [Criando um hash com CNG](creating-a-hash-with-cng.md)
-   [Assinando dados com CNG](signing-data-with-cng.md)
-   [Criptografando dados com CNG](encrypting-data-with-cng.md)

 

 



