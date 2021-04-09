---
description: A autenticação HTTP usando Microsoft Digest requer três buffers de entrada para gerar uma resposta de desafio. A tabela a seguir resume esses buffers.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Buffers de entrada para a resposta de desafio de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089949"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a><span data-ttu-id="65ef8-104">Buffers de entrada para a resposta de desafio de resumo</span><span class="sxs-lookup"><span data-stu-id="65ef8-104">Input Buffers for the Digest Challenge Response</span></span>

<span data-ttu-id="65ef8-105">A autenticação HTTP usando Microsoft Digest requer três buffers de entrada para gerar uma resposta de desafio.</span><span class="sxs-lookup"><span data-stu-id="65ef8-105">HTTP authentication using Microsoft Digest requires three input buffers to generate a challenge response.</span></span> <span data-ttu-id="65ef8-106">A tabela a seguir resume esses buffers.</span><span class="sxs-lookup"><span data-stu-id="65ef8-106">The following table summarizes these buffers.</span></span>



| <span data-ttu-id="65ef8-107">Número do buffer</span><span class="sxs-lookup"><span data-stu-id="65ef8-107">Buffer number</span></span> | <span data-ttu-id="65ef8-108">Contém</span><span class="sxs-lookup"><span data-stu-id="65ef8-108">Contains</span></span>                                                                                                                                             | <span data-ttu-id="65ef8-109">Tipo de buffer</span><span class="sxs-lookup"><span data-stu-id="65ef8-109">Buffer type</span></span>                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="65ef8-110">0</span><span class="sxs-lookup"><span data-stu-id="65ef8-110">0</span></span>             | <span data-ttu-id="65ef8-111">Desafio recebido do servidor</span><span class="sxs-lookup"><span data-stu-id="65ef8-111">Challenge received from the Server</span></span>                                                                                                                   | <span data-ttu-id="65ef8-112">\_token SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="65ef8-112">SECBUFFER\_TOKEN</span></span>                                            |
| <span data-ttu-id="65ef8-113">1</span><span class="sxs-lookup"><span data-stu-id="65ef8-113">1</span></span>             | <span data-ttu-id="65ef8-114">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="65ef8-114">HTTP Method</span></span>                                                                                                                                          | <span data-ttu-id="65ef8-115">parâmetros de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="65ef8-115">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="65ef8-116">2</span><span class="sxs-lookup"><span data-stu-id="65ef8-116">2</span></span>             | <span data-ttu-id="65ef8-117">H (entidade)</span><span class="sxs-lookup"><span data-stu-id="65ef8-117">H(Entity)</span></span>                                                                                                                                            | <span data-ttu-id="65ef8-118">parâmetros de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="65ef8-118">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="65ef8-119">3</span><span class="sxs-lookup"><span data-stu-id="65ef8-119">3</span></span>             | <span data-ttu-id="65ef8-120">O SPN ( [*nome da entidade de serviço*](../secgloss/s-gly.md) ) do servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="65ef8-120">The [*service principal name*](../secgloss/s-gly.md) (SPN) of the target server.</span></span> | <span data-ttu-id="65ef8-121">**SECBUFFER \_ \_host de destino** \| **SECBUFFER \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="65ef8-121">**SECBUFFER\_TARGET\_HOST** \| **SECBUFFER\_READONLY**</span></span>      |
| <span data-ttu-id="65ef8-122">4</span><span class="sxs-lookup"><span data-stu-id="65ef8-122">4</span></span>             | <span data-ttu-id="65ef8-123">Valores de token de associações de canal</span><span class="sxs-lookup"><span data-stu-id="65ef8-123">Channel bindings token values</span></span>                                                                                                                        | <span data-ttu-id="65ef8-124">**SECBUFFER \_ \_associações de canal** \| **SECBUFFER \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="65ef8-124">**SECBUFFER\_CHANNEL\_BINDINGS** \| **SECBUFFER\_READONLY**</span></span> |



 

<span data-ttu-id="65ef8-125">O buffer zero contém o desafio de resumo recebido do servidor em resposta à solicitação inicial para um recurso protegido por acesso.</span><span class="sxs-lookup"><span data-stu-id="65ef8-125">Buffer zero contains the Digest challenge received from the server in response to the initial request for an access-protected resource.</span></span>

<span data-ttu-id="65ef8-126">O buffer 1 contém a representação de cadeia de caracteres do método, como "GET" ou "POST".</span><span class="sxs-lookup"><span data-stu-id="65ef8-126">Buffer 1 contains the string representation of the method, such as "GET" or "POST".</span></span> <span data-ttu-id="65ef8-127">O método é usado no cálculo de a2, conforme descrito em [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span><span class="sxs-lookup"><span data-stu-id="65ef8-127">The method is used in the calculation of A2, as described in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span></span>

<span data-ttu-id="65ef8-128">Buffer 2 é o hash [*MD5*](../secgloss/m-gly.md) do corpo da entidade da mensagem, conforme descrito em RFC 2617.</span><span class="sxs-lookup"><span data-stu-id="65ef8-128">Buffer 2 is the [*MD5*](../secgloss/m-gly.md) hash of the message's entity-body as described in RFC 2617.</span></span>

<span data-ttu-id="65ef8-129">O buffer 3 contém o SPN do servidor de destino na formatação UTF-8 quando Digest é usado com associações de canal.</span><span class="sxs-lookup"><span data-stu-id="65ef8-129">Buffer 3 contains the SPN of the target server in UTF-8 formatting when Digest is used with channel bindings.</span></span>

<span data-ttu-id="65ef8-130">O buffer 4 contém o valor do token de associação de canal quando Digest é usado com associações de canal.</span><span class="sxs-lookup"><span data-stu-id="65ef8-130">Buffer 4 contains the channel binding token value when Digest is used with channel bindings.</span></span>

## <a name="input-buffers-for-sasl"></a><span data-ttu-id="65ef8-131">Buffers de entrada para SASL</span><span class="sxs-lookup"><span data-stu-id="65ef8-131">Input Buffers for SASL</span></span>

<span data-ttu-id="65ef8-132">Somente buffer de fornecimento zero.</span><span class="sxs-lookup"><span data-stu-id="65ef8-132">Supply buffer zero only.</span></span> <span data-ttu-id="65ef8-133">Para compatibilidade com outros SSPs, você pode chamar [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sem um desafio de servidor válido.</span><span class="sxs-lookup"><span data-stu-id="65ef8-133">For compatibility with other SSPs, you may call [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) without a valid server challenge.</span></span> <span data-ttu-id="65ef8-134">Nesse caso, o parâmetro *pInput* deve ser definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="65ef8-134">In this case the *pInput* parameter should be set to **NULL**.</span></span>

 

 
