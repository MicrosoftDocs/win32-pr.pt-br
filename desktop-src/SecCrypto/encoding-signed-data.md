---
description: Descreve o procedimento para codificar uma mensagem assinada.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Codificando dados assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4a542fe0890a6ee9d51ebc1a5ee6b98bab4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170921"
---
# <a name="encoding-signed-data"></a>Codificando dados assinados

Os [*dados assinados*](../secgloss/s-gly.md) consistem no conteúdo de qualquer tipo e [*hashes*](../secgloss/h-gly.md) de mensagens criptografadas do conteúdo por zero ou mais assinantes. O hash resultante pode confirmar que a mensagem original não foi modificada desde a assinatura e que as pessoas ou entidades em particular assinaram os dados.

A ilustração a seguir descreve o procedimento para codificar uma mensagem assinada. A lista após a ilustração descreve as etapas.

Uma mensagem pode ter vários assinantes, algoritmos de hash e certificados. Embora a ilustração mostre somente certificados, [*CRLs*](../secgloss/c-gly.md)e [*CTLs*](../secgloss/c-gly.md) podem usar o mesmo processo. Elas se ajustarão à ilustração sempre que os certificados forem mostrados.

![Codificando uma mensagem assinada](images/signmsg2.png)

O processo geral de codificação de [*dados assinados*](../secgloss/s-gly.md) é o seguinte.

**Para codificar dados assinados**

1.  Os dados são criados (se necessário) e um ponteiro para ele é recuperado.
2.  Um [*repositório de certificados*](../secgloss/c-gly.md) é aberto que contém o certificado do signatário.
3.  A chave privada para o certificado é recuperada. Há duas propriedades que devem ser definidas no certificado antes de usá-lo. Uma é usada para vincular um certificado a um CSP específico e, dentro desse CSP, a um contêiner de [*chave*](../secgloss/k-gly.md)privada específico. O outro é usado para indicar qual algoritmo de hash deve ser usado quando uma operação de [*hash*](../secgloss/h-gly.md) é chamada. Essas necessidades só precisam ser definidas uma vez.
4.  A propriedade de um certificado determina o algoritmo de hash.
5.  Um hash dos dados é criado enviando os dados por meio da função de hash.
6.  A assinatura é criada criptografando-se o hash usando a chave privada, obtida por meio de uma propriedade no certificado.
7.  Os dados a seguir estão incluídos na mensagem assinada concluída:
    -   Os dados originais a serem assinados
    -   Os algoritmos de hash
    -   As assinaturas
    -   As estruturas de informações do Assinante, que incluem o identificador de signatário (emissor do certificado e número de série)
    -   Os certificados do signatário (opcional)

Este procedimento ilustra um caso simples. Casos mais complexos envolvem atributos autenticados incluídos na mensagem. Quando o tipo de conteúdo é qualquer coisa, exceto uma cadeia de caracteres de **byte** , ou há pelo menos um atributo autenticado junto com qualquer tipo de dados, há dois atributos autenticados padrão necessários: o tipo de conteúdo (dados) e o hash do conteúdo. Sob essas circunstâncias, a [*CryptoAPI*](../secgloss/c-gly.md) fornece automaticamente esses dois atributos necessários. As funções da mensagem de nível baixo aplicam hash aos atributos autenticados, criptografam o hash com a chave privada e fornecem isso como a assinatura.

Use as funções de mensagem de baixo nível para realizar as tarefas listadas, usando o procedimento a seguir.

**Para codificar uma mensagem assinada**

1.  Crie ou recupere o conteúdo.
2.  Obter um provedor criptográfico.
3.  Obtenha os certificados de signatário.
4.  Inicialize a estrutura de [**\_ informações de \_ codificação \_ do signatário CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) .
5.  Inicialize a estrutura de [**\_ \_ \_ informações de codificação assinada do CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .
6.  Chame [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obter o tamanho do blob de mensagens codificadas. Aloque memória para ele.
7.  Chame [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando CMSG \_ assinado para *dwMsgType* e um ponteiro para [**CMSG \_ informações de \_ codificação \_ assinadas**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) para *pvMsgEncodeInfo* para obter um identificador para a mensagem aberta.
8.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando o identificador recuperado na etapa 7 e um ponteiro para os dados que serão assinados e codificados. Essa função pode ser chamada quantas vezes forem necessárias para concluir o processo de codificação.
9.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador recuperado na etapa 7 e os tipos de parâmetro apropriados para acessar os dados desejados e codificados. Por exemplo, passe \_ o parâmetro de conteúdo CMSG \_ para obter um ponteiro para toda a mensagem [*PKCS \# 7*](../secgloss/p-gly.md) .

    Se o resultado dessa codificação for ser usado como os [*dados internos*](../secgloss/i-gly.md) para outra mensagem codificada, como uma mensagem envelopada, o \_ parâmetro CMSG Bare \_ Content \_ param deverá ser passado. Para ver um exemplo que mostra isso, consulte [código alternativo para codificar uma mensagem envelopada](alternate-code-for-encoding-an-enveloped-message.md).

10. Feche a mensagem chamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

O resultado desse procedimento é uma mensagem codificada que contém os dados originais, o hash criptografado desses dados (assinatura) e as informações do signatário. Também há um ponteiro para o BLOB desejado e codificado.

Para obter detalhes de codificação C, consulte [exemplo c programa: assinatura, codificação, decodificação e verificação de uma mensagem](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
