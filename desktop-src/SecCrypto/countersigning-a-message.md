---
description: Explica como referendar uma mensagem usando CryptMsgCountersign.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Como assinar uma mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756559"
---
# <a name="countersigning-a-message"></a>Como assinar uma mensagem

**Para referendar uma mensagem assinada usando CryptMsgCountersign**

1.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obter um identificador para a mensagem assinada.
2.  Inicialize uma estrutura de [**\_ informações de \_ codificação \_ de signatário CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para o signatário.
3.  Adicione a estrutura de [**\_ informações de \_ codificação \_ do assinante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a uma matriz de signatários (apenas um único signatário tem suporte no momento).
4.  Chame [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) para adicionar a referenda ou referendas.

Se todas as chamadas de função forem bem sucedidos, a mensagem original agora terá uma [*referenda*](../secgloss/c-gly.md) inclusa como um atributo não autenticado.

**Para referendar uma mensagem assinada usando CryptMsgCountersignEncoded**

1.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obter um identificador para a mensagem assinada.
2.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar as informações de signatário codificado da mensagem assinada.
3.  Inicialize uma estrutura de [**\_ informações de \_ codificação \_ de signatário CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para o signatário.
4.  Adicione a estrutura de [**\_ informações de \_ codificação \_ do assinante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a uma matriz de signatários (apenas um único signatário tem suporte no momento).
5.  Chame [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) para criar o atributo de referenda codificado.
6.  Chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) para adicionar o atributo de referenda à mensagem original como um atributo não autenticado.

Se todas as chamadas de função forem realizadas com sucesso, um atributo de [*referenda*](../secgloss/c-gly.md) será adicionado à mensagem original.

 

 
