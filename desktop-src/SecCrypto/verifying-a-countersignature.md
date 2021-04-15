---
description: Explica como verificar uma referenda usando o CryptMsgVerifyCountersignatureEncoded.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Verificando uma referenda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761391"
---
# <a name="verifying-a-countersignature"></a>Verificando uma referenda

**Para verificar uma referenda**

1.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obter um identificador para a mensagem assinada.
2.  Obtenha um ponteiro para o certificado do assinante ( [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).
3.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar as informações de signatário da mensagem.
4.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar a [*referenda*](../secgloss/c-gly.md) da mensagem.
5.  Chame [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) para verificar a referenda.

Se a chamada de função [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) for realizada com sucesso, a [*referenda*](../secgloss/c-gly.md) será verificada.

 

 
