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
# <a name="verifying-a-countersignature"></a><span data-ttu-id="77793-103">Verificando uma referenda</span><span class="sxs-lookup"><span data-stu-id="77793-103">Verifying a Countersignature</span></span>

<span data-ttu-id="77793-104">**Para verificar uma referenda**</span><span class="sxs-lookup"><span data-stu-id="77793-104">**To verify a countersignature**</span></span>

1.  <span data-ttu-id="77793-105">Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obter um identificador para a mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="77793-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="77793-106">Obtenha um ponteiro para o certificado do assinante ( [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span><span class="sxs-lookup"><span data-stu-id="77793-106">Get a pointer to the countersigner's certificate ( [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span></span>
3.  <span data-ttu-id="77793-107">Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar as informações de signatário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="77793-107">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the signer information from the message.</span></span>
4.  <span data-ttu-id="77793-108">Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar a [*referenda*](../secgloss/c-gly.md) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="77793-108">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the [*countersignature*](../secgloss/c-gly.md) from the message.</span></span>
5.  <span data-ttu-id="77793-109">Chame [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) para verificar a referenda.</span><span class="sxs-lookup"><span data-stu-id="77793-109">Call [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) to verify the countersignature.</span></span>

<span data-ttu-id="77793-110">Se a chamada de função [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) for realizada com sucesso, a [*referenda*](../secgloss/c-gly.md) será verificada.</span><span class="sxs-lookup"><span data-stu-id="77793-110">If the [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) function call succeeds, the [*countersignature*](../secgloss/c-gly.md) is verified.</span></span>

 

 
