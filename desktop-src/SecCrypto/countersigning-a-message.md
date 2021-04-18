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
# <a name="countersigning-a-message"></a><span data-ttu-id="6cafa-103">Como assinar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="6cafa-103">Countersigning a Message</span></span>

<span data-ttu-id="6cafa-104">**Para referendar uma mensagem assinada usando CryptMsgCountersign**</span><span class="sxs-lookup"><span data-stu-id="6cafa-104">**To countersign a signed message by using CryptMsgCountersign**</span></span>

1.  <span data-ttu-id="6cafa-105">Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obter um identificador para a mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="6cafa-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="6cafa-106">Inicialize uma estrutura de [**\_ informações de \_ codificação \_ de signatário CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para o signatário.</span><span class="sxs-lookup"><span data-stu-id="6cafa-106">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
3.  <span data-ttu-id="6cafa-107">Adicione a estrutura de [**\_ informações de \_ codificação \_ do assinante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a uma matriz de signatários (apenas um único signatário tem suporte no momento).</span><span class="sxs-lookup"><span data-stu-id="6cafa-107">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
4.  <span data-ttu-id="6cafa-108">Chame [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) para adicionar a referenda ou referendas.</span><span class="sxs-lookup"><span data-stu-id="6cafa-108">Call [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) to add the countersignature or countersignatures.</span></span>

<span data-ttu-id="6cafa-109">Se todas as chamadas de função forem bem sucedidos, a mensagem original agora terá uma [*referenda*](../secgloss/c-gly.md) inclusa como um atributo não autenticado.</span><span class="sxs-lookup"><span data-stu-id="6cafa-109">If all of the function calls succeed, the original message now has a [*countersignature*](../secgloss/c-gly.md) included as an unauthenticated attribute.</span></span>

<span data-ttu-id="6cafa-110">**Para referendar uma mensagem assinada usando CryptMsgCountersignEncoded**</span><span class="sxs-lookup"><span data-stu-id="6cafa-110">**To countersign a signed message by using CryptMsgCountersignEncoded**</span></span>

1.  <span data-ttu-id="6cafa-111">Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obter um identificador para a mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="6cafa-111">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="6cafa-112">Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar as informações de signatário codificado da mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="6cafa-112">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the encoded signer information of the signed message.</span></span>
3.  <span data-ttu-id="6cafa-113">Inicialize uma estrutura de [**\_ informações de \_ codificação \_ de signatário CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para o signatário.</span><span class="sxs-lookup"><span data-stu-id="6cafa-113">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
4.  <span data-ttu-id="6cafa-114">Adicione a estrutura de [**\_ informações de \_ codificação \_ do assinante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a uma matriz de signatários (apenas um único signatário tem suporte no momento).</span><span class="sxs-lookup"><span data-stu-id="6cafa-114">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
5.  <span data-ttu-id="6cafa-115">Chame [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) para criar o atributo de referenda codificado.</span><span class="sxs-lookup"><span data-stu-id="6cafa-115">Call [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) to create the encoded countersignature attribute.</span></span>
6.  <span data-ttu-id="6cafa-116">Chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) para adicionar o atributo de referenda à mensagem original como um atributo não autenticado.</span><span class="sxs-lookup"><span data-stu-id="6cafa-116">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) to add the countersignature attribute to the original message as an unauthenticated attribute.</span></span>

<span data-ttu-id="6cafa-117">Se todas as chamadas de função forem realizadas com sucesso, um atributo de [*referenda*](../secgloss/c-gly.md) será adicionado à mensagem original.</span><span class="sxs-lookup"><span data-stu-id="6cafa-117">If all of the function calls succeed, a [*countersignature*](../secgloss/c-gly.md) attribute is added to the original message.</span></span>

 

 
