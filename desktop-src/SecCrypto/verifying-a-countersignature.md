---
description: Explica como verificar uma contrasignature usando CryptMsgVerifyCountersignatureEncoded.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Verificando uma Countersignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23163c7b1d4345908b24fed36b6fa23bdf2cf7c46dd3faa1beaa99c76d6f0ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896237"
---
# <a name="verifying-a-countersignature"></a>Verificando uma Countersignature

**Para verificar uma countersignature**

1.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obter um handle para a mensagem assinada.
2.  Obter um ponteiro para o certificado do contador [**(INFORMAÇÕES DE \_ CERTIFICADO).**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)
3.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar as informações do signante da mensagem.
4.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar [*a countersignature*](../secgloss/c-gly.md) da mensagem.
5.  Chame [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) para verificar a countersignature.

Se a chamada de função [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) for bem-sucedida, [*a countersignature*](../secgloss/c-gly.md) será verificada.

 

 
