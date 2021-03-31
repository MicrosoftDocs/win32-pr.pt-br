---
title: Usando Transport-Level segurança no cliente
description: O cliente especifica como o servidor representa o cliente quando o cliente estabelece a associação de cadeia de caracteres.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando segurança em nível de transporte no cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917600"
---
# <a name="using-transport-level-security-on-the-client"></a><span data-ttu-id="4d1f8-104">Usando Transport-Level segurança no cliente</span><span class="sxs-lookup"><span data-stu-id="4d1f8-104">Using Transport-Level Security on the Client</span></span>

<span data-ttu-id="4d1f8-105">O cliente especifica como o servidor representa o cliente quando o cliente estabelece a associação de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-105">The client specifies how the server impersonates the client when the client establishes the string binding.</span></span> <span data-ttu-id="4d1f8-106">Essas informações de QOS são fornecidas como uma opção de ponto de extremidade na associação de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-106">This QOS information is provided as an endpoint option in the string binding.</span></span> <span data-ttu-id="4d1f8-107">O cliente pode especificar o nível de representação, controle dinâmico ou estático e o sinalizador somente efetiva.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-107">The client can specify the level of impersonation, dynamic or static tracking, and the effective-only flag.</span></span>

<span data-ttu-id="4d1f8-108">**Para fornecer informações de qualidade de serviço para o servidor**</span><span class="sxs-lookup"><span data-stu-id="4d1f8-108">**To supply quality-of-service information for the server**</span></span>

1.  <span data-ttu-id="4d1f8-109">O cliente chama [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) para criar as cadeias de componentes, incluindo as opções de ponto de extremidade, no contexto de ligação de cadeia de caracteres correto.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-109">The client calls [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) to create the component strings, including endpoint options, in the correct string-binding context.</span></span>
2.  <span data-ttu-id="4d1f8-110">O cliente chama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obter um novo identificador de ligação e aplicar as informações de qualidade de serviço para o cliente.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-110">The client calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain a new binding handle and to apply the quality-of-service information for the client.</span></span>
3.  <span data-ttu-id="4d1f8-111">O cliente faz chamadas de procedimento remoto usando a alça.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-111">The client makes remote procedure calls using the handle.</span></span>

<span data-ttu-id="4d1f8-112">O Microsoft RPC dá suporte a recursos de segurança do Windows somente em [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) e [**Ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="4d1f8-112">Microsoft RPC supports Windows security features only on [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) and [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="4d1f8-113">As opções de segurança para outros transportes são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-113">Security options for other transports are ignored.</span></span>

<span data-ttu-id="4d1f8-114">O cliente pode associar os seguintes parâmetros de segurança à associação para o transporte nomeado pipe [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) ou [**Ncalrpc**](/windows/desktop/Midl/ncalrpc):</span><span class="sxs-lookup"><span data-stu-id="4d1f8-114">The client can associate the following security parameters to the binding for the named-pipe transport [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) or [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span></span>

-   <span data-ttu-id="4d1f8-115">Identificação, representação ou anônima.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-115">Identification, Impersonation, or Anonymous.</span></span> <span data-ttu-id="4d1f8-116">Especifica o tipo de segurança usado.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-116">Specifies the type of security used.</span></span> <span data-ttu-id="4d1f8-117">O padrão é representação.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-117">The default is Impersonation.</span></span>
-   <span data-ttu-id="4d1f8-118">Dinâmico ou estático.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-118">Dynamic or Static.</span></span> <span data-ttu-id="4d1f8-119">Determina se as informações de segurança associadas a um thread são uma cópia das informações de segurança criadas no momento em que a chamada de procedimento remoto é feita (estática) ou um ponteiro para as informações de segurança (dinâmico).</span><span class="sxs-lookup"><span data-stu-id="4d1f8-119">Determines whether security information associated with a thread is a copy of the security information created at the time the remote procedure call is made (static) or a pointer to the security information (dynamic).</span></span>

    <span data-ttu-id="4d1f8-120">As informações de segurança estática não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-120">Static security information does not change.</span></span> <span data-ttu-id="4d1f8-121">A configuração dinâmica reflete as configurações de segurança atuais, incluindo as alterações feitas depois que a chamada de procedimento remoto é feita.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-121">The dynamic setting reflects the current security settings, including changes made after the remote procedure call is made.</span></span> <span data-ttu-id="4d1f8-122">Para [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), o padrão para conexões de pipe nomeado remoto é estático, para conexões de pipe nomeado local, o padrão é dinâmico.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-122">For [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), the default for remote named pipe connections is static, for local named pipe connections the default is dynamic.</span></span>

-   <span data-ttu-id="4d1f8-123">**True** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-123">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="4d1f8-124">Especifica o valor do sinalizador somente efetivo.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-124">Specifies the value of the effective-only flag.</span></span> <span data-ttu-id="4d1f8-125">Um valor **true** indica que somente os privilégios de token definidos como on no momento da chamada entram em vigor.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-125">A value of **TRUE** indicates that only token privileges set to on at the time of the call are effective.</span></span> <span data-ttu-id="4d1f8-126">Um valor **false** indica que todos os privilégios estão disponíveis e que o aplicativo pode modificá-los.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-126">A value of **FALSE** indicates that all privileges are available and that the application can modify them.</span></span>

<span data-ttu-id="4d1f8-127">Qualquer combinação dessas configurações pode ser atribuída à associação, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="4d1f8-127">Any combination of these settings can be assigned to the binding, as shown in the following example:</span></span>

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

<span data-ttu-id="4d1f8-128">As configurações de parâmetro de segurança padrão variam de acordo com o protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="4d1f8-128">Default security-parameter settings vary according to the transport protocol.</span></span>

<span data-ttu-id="4d1f8-129">Para obter informações adicionais sobre a sintaxe das opções de ponto de extremidade, consulte [ponto de extremidade](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="4d1f8-129">For additional information about the syntax of the endpoint options, see [endpoint](/windows/desktop/Midl/endpoint).</span></span>

 

 