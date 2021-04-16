---
description: Detalha o procedimento para codificar uma mensagem geral.
ms.assetid: 554cab0d-cfa2-46a7-80d9-f41430eb4b47
title: Procedimento para codificar e decodificar mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49da09c2318fffd3d1c92d6012055172709609a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761393"
---
# <a name="procedure-for-encoding-and-decoding-messages"></a>Procedimento para codificar e decodificar mensagens

O procedimento para codificar uma mensagem geral é o seguinte.

**Para codificar uma mensagem**

1.  Inicialize as estruturas de dados apropriadas para o tipo de dados desejado.
2.  Chame [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando os argumentos necessários. Ao chamar **CryptMsgOpenToEncode**, se os dados a serem fornecidos ao [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) já tiverem sido codificados por mensagem, passe o identificador de objeto apropriado em *pszInnerContentObjID* (por exemplo, "1.2.840.113549.1.7.2" para szOID \_ RSA \_ signedData). Se *pszInnerContentObjID* for **NULL**, presume-se que o tipo de [*conteúdo interno*](../secgloss/i-gly.md) não tenha sido codificado anteriormente e que seja processado adequadamente.
3.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) quantas vezes forem necessárias para concluir a mensagem. Na última chamada, defina o parâmetro *fFinal* como **true**. (Para obter detalhes, consulte **CryptMsgUpdate**).
4.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para obter um ponteiro para os parâmetros desejados, como o conteúdo. Para codificar dados gerais simples, use \_ o parâmetro de conteúdo CMSG \_ para o *dwParamtype*.
5.  Feche a mensagem chamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Esse procedimento resulta em uma mensagem codificada de um tipo especificado nas chamadas de função.

O procedimento para decodificar uma mensagem geral é o seguinte.

**Para decodificar uma mensagem**

1.  Determine o comprimento necessário para que o buffer Mantenha os dados codificados usando [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).
2.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando os argumentos necessários. Para manter a compatibilidade com o Internet Explorer versão 3,0, o parâmetro *dwMsgType* é fornecido. Os dados assinados criados no Internet Explorer 3,0 não contêm informações de cabeçalho. Portanto, se essa mensagem for extraída de assinaturas de arquivo, o tipo de mensagem deverá ser passado para a função. Se zero for passado para o parâmetro *dwMsgType* , a função lerá o tipo de mensagem do cabeçalho na mensagem. Se o cabeçalho estiver ausente, a chamada de função falhará. Se for bem-sucedido, será retornado um identificador para a mensagem aberta.
3.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez. Isso faz com que as ações apropriadas sejam executadas na mensagem, dependendo do tipo de mensagem.
4.  Para o processamento adicional da mensagem, como a descriptografia adicional ou a verificação de assinatura, chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando a ação desejada em *dwCtrlType*.
5.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para obter um ponteiro para os parâmetros desejados, como o conteúdo. Para decodificar dados gerais simples, use \_ o parâmetro de conteúdo CMSG \_ para o parâmetro *dwParamtype* .
6.  Chame [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para fechar a mensagem.

Para obter um exemplo que implementa essas etapas, consulte [exemplo C programa: codificação e decodificação de dados](example-c-program-encoding-and-decoding-data.md). Para obter procedimentos e um exemplo demonstrando o processo de codificação, decodificação e verificação da assinatura de uma mensagem assinada, consulte [exemplo C programa: assinatura, codificação, decodificação e verificação de uma mensagem](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
