---
description: Ilustra o procedimento para codificar uma mensagem assinada.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Codificando dados assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e5c3ab338c4e7b251416f1a488747eb0c9b897c1fa02082afcb580cb12341b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874836"
---
# <a name="encoding-signed-data"></a>Codificando dados assinados

[*Os dados assinados*](../secgloss/s-gly.md) consistem em conteúdo de qualquer tipo e [*hashes*](../secgloss/h-gly.md) de mensagens criptografadas do conteúdo por zero ou mais signatários. O hash resultante pode confirmar que a mensagem original não foi modificada desde a assinatura e que determinadas pessoas ou entidades assinaram os dados.

A ilustração a seguir ilustra o procedimento para codificar uma mensagem assinada. A lista a seguir à ilustração descreve as etapas.

Uma mensagem pode ter vários signatários, algoritmos de hash e certificados. Embora a ilustração mostre apenas certificados, [*AS CRLs*](../secgloss/c-gly.md)e [*CTLs*](../secgloss/c-gly.md) podem usar o mesmo processo. Eles se ajustariam à ilustração sempre que os certificados são mostrados.

![codificando uma mensagem assinada](images/signmsg2.png)

O processo geral para codificar dados [*assinados*](../secgloss/s-gly.md) é o seguinte.

**Para codificar dados assinados**

1.  Os dados são criados (se necessário) e um ponteiro para eles é recuperado.
2.  Um [*armazenamento de*](../secgloss/c-gly.md) certificados é aberto que contém o certificado do signante.
3.  A chave privada do certificado é recuperada. Há duas propriedades que devem ser definidas no certificado antes de usá-la. Um é usado para ligar um certificado a um CSP específico e, dentro desse CSP, a um contêiner de [*chave privada específico.*](../secgloss/k-gly.md) O outro é usado para indicar qual algoritmo de hash deve ser usado quando uma operação [*de hash*](../secgloss/h-gly.md) é chamada. Eles só precisam ser definidos uma vez.
4.  A propriedade de um certificado determina o algoritmo de hash.
5.  Um hash dos dados é criado enviando os dados por meio da função de hash.
6.  A assinatura é criada criptografando o hash usando a chave privada, obtida por meio de uma propriedade no certificado.
7.  Os seguintes dados estão incluídos na mensagem assinada concluída:
    -   Os dados originais a serem assinados
    -   Os algoritmos de hash
    -   As assinaturas
    -   As estruturas de informações do signante, que incluem o identificador do signante (emissor do certificado e número de série)
    -   Certificados do signante (opcional)

Este procedimento ilustra um caso simples. Casos mais complexos envolvem atributos autenticados incluídos na mensagem. Quando o tipo de conteúdo é qualquer coisa, menos uma cadeia de caracteres **BYTE** ou há pelo menos um atributo autenticado junto com qualquer tipo de dados, há dois atributos autenticados padrão necessários: o tipo de conteúdo (dados) e o hash do conteúdo. Nessas circunstâncias, o [*CryptoAPI*](../secgloss/c-gly.md) fornece automaticamente esses dois atributos necessários. As funções de mensagem de baixo nível hash os atributos autenticados, criptografam o hash com a chave privada e fornecem isso como a assinatura.

Use as funções de mensagem de baixo nível para realizar as tarefas listadas, usando o procedimento a seguir.

**Para codificar uma mensagem assinada**

1.  Crie ou recupere o conteúdo.
2.  Obter um provedor criptográfico.
3.  Obter os certificados de signante.
4.  Inicialize a estrutura DE INFORMAÇÕES DE CODIFICAÇÃO DO [**\_ SIGNER \_ \_ DO CMSG.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info)
5.  Inicialize a estrutura [**DE INFORMAÇÕES DE \_ \_ CODIFICAÇÃO ASSINADA \_ DO CMSG.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)
6.  Chame [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obter o tamanho do BLOB da mensagem codificada. Alocar memória para ele.
7.  Chame [**CryptMsgOpenToEncode,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)passando CMSG SIGNED para dwMsgType e um ponteiro para INFORMAÇÕES DE CODIFICAÇÃO ASSINADA DO \_  [**CMSG \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) para *pvMsgEncodeInfo* para obter um alçamento para a mensagem aberta.
8.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando o handle recuperado na etapa 7 e um ponteiro para os dados que devem ser assinados e codificados. Essa função pode ser chamada quantas vezes for necessário para concluir o processo de codificação.
9.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o handle recuperado na etapa 7 e os tipos de parâmetro apropriados para acessar os dados codificados desejados. Por exemplo, passe CMSG CONTENT PARAM para \_ obter um ponteiro para toda a mensagem \_ [*PKCS \# 7.*](../secgloss/p-gly.md)

    Se o resultado dessa codificação for ser [](../secgloss/i-gly.md) usado como os dados internos de outra mensagem codificada, como uma mensagem envelheçada, o parâmetro PARAM BARE CONTENT DO CMSG deverá \_ ser \_ \_ passado. Para ver um exemplo mostrando isso, consulte [Código alternativo para codificar uma mensagem enveloada](alternate-code-for-encoding-an-enveloped-message.md).

10. Feche a mensagem chamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

O resultado desse procedimento é uma mensagem codificada que contém os dados originais, o hash criptografado desses dados (assinatura) e as informações do signante. Também há um ponteiro para o BLOB codificado desejado.

Para obter detalhes de codificação em C, consulte Programa C de [exemplo: assinatura, codificação,](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)decodificação e verificação de uma mensagem .

 

 
