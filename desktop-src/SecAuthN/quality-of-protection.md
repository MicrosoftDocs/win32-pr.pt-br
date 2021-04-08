---
description: A qualidade de proteção, identificada pela diretiva QoP, é especificada pela primeira vez pelo servidor no desafio de resumo e, em seguida, confirmada pelo cliente na resposta de desafio.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualidade da proteção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011558"
---
# <a name="quality-of-protection"></a><span data-ttu-id="57b3d-103">Qualidade da proteção</span><span class="sxs-lookup"><span data-stu-id="57b3d-103">Quality of Protection</span></span>

<span data-ttu-id="57b3d-104">A qualidade de proteção, identificada pela diretiva QoP, é especificada pela primeira vez pelo servidor no desafio de resumo e, em seguida, confirmada pelo cliente na resposta de desafio.</span><span class="sxs-lookup"><span data-stu-id="57b3d-104">The quality of protection, identified by the qop directive, is first specified by the server in the Digest challenge, and then confirmed by the client in the challenge response.</span></span> <span data-ttu-id="57b3d-105">Se o cliente exigir uma qualidade de proteção para a qual o servidor não oferece suporte, o cliente deverá encerrar a autenticação.</span><span class="sxs-lookup"><span data-stu-id="57b3d-105">If the client requires a quality of protection that the server does not support, the client must terminate the authentication.</span></span>

<span data-ttu-id="57b3d-106">Os valores possíveis para a diretiva QoP são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="57b3d-106">The possible values for the qop directive are described in the following table.</span></span>



| <span data-ttu-id="57b3d-107">Valor</span><span class="sxs-lookup"><span data-stu-id="57b3d-107">Value</span></span>                   | <span data-ttu-id="57b3d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="57b3d-108">Description</span></span>                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b3d-109">propósito</span><span class="sxs-lookup"><span data-stu-id="57b3d-109">"auth"</span></span>                  | <span data-ttu-id="57b3d-110">Somente autenticação.</span><span class="sxs-lookup"><span data-stu-id="57b3d-110">Authentication only.</span></span>                                                                                                                         |
| <span data-ttu-id="57b3d-111">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="57b3d-111">"auth-int"</span></span>              | <span data-ttu-id="57b3d-112">Verificação de [*integridade*](../secgloss/i-gly.md) e autenticação usando assinaturas.</span><span class="sxs-lookup"><span data-stu-id="57b3d-112">Authentication and [*integrity*](../secgloss/i-gly.md) checking using signatures.</span></span>                  |
| <span data-ttu-id="57b3d-113">(SASL somente) "auth-conf"</span><span class="sxs-lookup"><span data-stu-id="57b3d-113">(SASL only) "auth-conf"</span></span> | <span data-ttu-id="57b3d-114">Autenticação, integridade e verificação de confidencialidade usando assinaturas e criptografia.</span><span class="sxs-lookup"><span data-stu-id="57b3d-114">Authentication, integrity and confidentiality checking by using signatures and encryption.</span></span> <span data-ttu-id="57b3d-115">Para obter mais informações, consulte [codificações](ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="57b3d-115">For more information, see [Ciphers](ciphers.md).</span></span> |



 

<span data-ttu-id="57b3d-116">A qualidade da proteção é determinada pelos sinalizadores de requisitos de contexto passados para o Microsoft Digest SSP.</span><span class="sxs-lookup"><span data-stu-id="57b3d-116">Quality of protection is determined by context requirement flags passed to the Microsoft Digest SSP.</span></span> <span data-ttu-id="57b3d-117">A tabela a seguir lista os sinalizadores relacionados à qualidade de proteção e o valor resultante da diretiva QoP.</span><span class="sxs-lookup"><span data-stu-id="57b3d-117">The following table lists the flags related to quality of protection, and the resulting value of the qop directive.</span></span>



| <span data-ttu-id="57b3d-118">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="57b3d-118">Flag</span></span>                         | <span data-ttu-id="57b3d-119">valor de QoP</span><span class="sxs-lookup"><span data-stu-id="57b3d-119">qop value</span></span>               |
|------------------------------|-------------------------|
| <span data-ttu-id="57b3d-120">*Xxx* \_ confidencialidade de REQ. \_</span><span class="sxs-lookup"><span data-stu-id="57b3d-120">*XXX*\_REQ\_CONFIDENTIALITY</span></span>  | <span data-ttu-id="57b3d-121">"auth-conf" (SASL somente)</span><span class="sxs-lookup"><span data-stu-id="57b3d-121">"auth-conf" (SASL only)</span></span> |
| <span data-ttu-id="57b3d-122">*Xxx* \_ detecção de repetição do REQ. \_ \_</span><span class="sxs-lookup"><span data-stu-id="57b3d-122">*XXX*\_REQ\_REPLAY\_DETECT</span></span>   | <span data-ttu-id="57b3d-123">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="57b3d-123">"auth-int"</span></span>              |
| <span data-ttu-id="57b3d-124">*Xxx* \_ \_detecção de sequência de req \_</span><span class="sxs-lookup"><span data-stu-id="57b3d-124">*XXX*\_REQ\_SEQUENCE\_DETECT</span></span> | <span data-ttu-id="57b3d-125">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="57b3d-125">"auth-int"</span></span>              |
| <span data-ttu-id="57b3d-126">*Xxx* \_ integridade de REQ. \_</span><span class="sxs-lookup"><span data-stu-id="57b3d-126">*XXX*\_REQ\_INTEGRITY</span></span>        | <span data-ttu-id="57b3d-127">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="57b3d-127">"auth-int"</span></span>              |
| <span data-ttu-id="57b3d-128">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="57b3d-128">(none)</span></span>                       | <span data-ttu-id="57b3d-129">propósito</span><span class="sxs-lookup"><span data-stu-id="57b3d-129">"auth"</span></span>                  |



 

> [!Note]  
> <span data-ttu-id="57b3d-130">Os sinalizadores de requisitos de contexto especificados por aplicativos de servidor têm um prefixo de ASC, e os especificados pelos clientes são prefixados com a ISC.</span><span class="sxs-lookup"><span data-stu-id="57b3d-130">Context requirement flags specified by server applications have a prefix of ASC, and those specified by clients are prefixed with ISC.</span></span> <span data-ttu-id="57b3d-131">Para determinar os valores de sinalizador usados pelo seu aplicativo, substitua um destes prefixos por *xxx*.</span><span class="sxs-lookup"><span data-stu-id="57b3d-131">To determine the flag values used by your application, substitute one of these prefixes for *XXX*.</span></span>

 

<span data-ttu-id="57b3d-132">Para obter informações adicionais relacionadas ao servidor, consulte [gerando o desafio Digest](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="57b3d-132">For additional server-related information, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

<span data-ttu-id="57b3d-133">Para obter informações adicionais relacionadas ao cliente, consulte [gerando a resposta de desafio de resumo](generating-the-digest-challenge-response.md).</span><span class="sxs-lookup"><span data-stu-id="57b3d-133">For additional client-related information, see [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>

 

 
