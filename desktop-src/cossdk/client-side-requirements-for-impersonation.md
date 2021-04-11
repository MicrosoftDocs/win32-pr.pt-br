---
description: Requisitos de Client-Side para representação
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Requisitos de Client-Side para representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296131"
---
# <a name="client-side-requirements-for-impersonation"></a><span data-ttu-id="3abe4-103">Requisitos de Client-Side para representação</span><span class="sxs-lookup"><span data-stu-id="3abe4-103">Client-Side Requirements for Impersonation</span></span>

<span data-ttu-id="3abe4-104">As duas configurações a seguir podem ser especificadas em relação à representação no lado do cliente:</span><span class="sxs-lookup"><span data-stu-id="3abe4-104">The following two settings can be specified relative to impersonation on the client side:</span></span>

-   <span data-ttu-id="3abe4-105">Nível de representação, que indica a disposição do cliente para fazer com que o servidor use sua identidade.</span><span class="sxs-lookup"><span data-stu-id="3abe4-105">Impersonation level, which indicates the client's willingness to have the server use its identity.</span></span>
-   <span data-ttu-id="3abe4-106">Uma configuração no serviço de Active Directory por meio do qual a conta do cliente pode ser marcada como "a conta é confidencial e não pode ser delegada", o que desabilitará a delegação.</span><span class="sxs-lookup"><span data-stu-id="3abe4-106">A setting in the Active Directory Service through which the client account can be marked "Account is sensitive and cannot be delegated," which will disable delegation.</span></span>

<span data-ttu-id="3abe4-107">O nível de representação pode ser definido de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="3abe4-107">The impersonation level can be set in a variety of ways.</span></span> <span data-ttu-id="3abe4-108">Se o cliente não indicar um nível de representação, o padrão em todo o computador será usado pelo COM.</span><span class="sxs-lookup"><span data-stu-id="3abe4-108">If the client does not indicate an impersonation level, the machine-wide default will be used by COM.</span></span> <span data-ttu-id="3abe4-109">O padrão em todo o computador pode ser definido usando a ferramenta administrativa serviços de componentes ou Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="3abe4-109">The machine-wide default can be set using either the Component Services administrative tool or Dcomcnfg.exe.</span></span> <span data-ttu-id="3abe4-110">O cliente também pode indicar um nível de representação preferencial administrativamente com Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="3abe4-110">The client can also indicate a preferred impersonation level administratively with Dcomcnfg.exe.</span></span>

<span data-ttu-id="3abe4-111">O cliente pode indicar o nível de representação programaticamente, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)— equivalente a [**IClientSecurity:: setampla**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), que pode ser chamado sempre que necessário — ou [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), que pode ser chamado uma vez por processo.</span><span class="sxs-lookup"><span data-stu-id="3abe4-111">The client can indicate the impersonation level programmatically, using either [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)—equivalent to [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), which can be called as often as necessary—or [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), which can be called once per process.</span></span>

<span data-ttu-id="3abe4-112">Se o cliente indicar representação de nível delegado — a autoridade mais ampla que ele pode conceder ao servidor — o cliente deve estar sendo executado sob uma identidade configurada corretamente no serviço de Active Directory para permitir que sua identidade seja delegada.</span><span class="sxs-lookup"><span data-stu-id="3abe4-112">If the client indicates delegate-level impersonation—the broadest authority it can grant to the server—the client should be running under an identity that is properly configured in the Active Directory Service to enable its identity to be delegated.</span></span>

<span data-ttu-id="3abe4-113">Para obter mais detalhes sobre os níveis de representação e os requisitos para a delegação funcionar, consulte [delegação e representação](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="3abe4-113">For more detail regarding impersonation levels and the requirements for delegation to work, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

<span data-ttu-id="3abe4-114">Os aplicativos COM+ sempre podem atuar como clientes, é claro.</span><span class="sxs-lookup"><span data-stu-id="3abe4-114">COM+ applications can always act as clients, of course.</span></span> <span data-ttu-id="3abe4-115">Quando o aplicativo COM+ faz uma chamada para outro aplicativo ou recurso, ele expressa um nível de representação.</span><span class="sxs-lookup"><span data-stu-id="3abe4-115">When the COM+ application makes a call to another application or resource, it expresses an impersonation level.</span></span> <span data-ttu-id="3abe4-116">Para aplicativos de servidor do COM+, você pode definir um nível de representação administrativamente.</span><span class="sxs-lookup"><span data-stu-id="3abe4-116">For COM+ server applications, you can set an impersonation level administratively.</span></span> <span data-ttu-id="3abe4-117">Os aplicativos de biblioteca COM+ não podem definir seu próprio nível de representação; em vez disso, eles usam o processo de host.</span><span class="sxs-lookup"><span data-stu-id="3abe4-117">COM+ library applications cannot set their own impersonation level; they use that of the host process instead.</span></span> <span data-ttu-id="3abe4-118">Para saber como definir a representação para um aplicativo COM+, consulte [definindo um nível de representação](setting-an-impersonation-level.md).</span><span class="sxs-lookup"><span data-stu-id="3abe4-118">To learn how to set impersonation for a COM+ application, see [Setting an Impersonation Level](setting-an-impersonation-level.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3abe4-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3abe4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3abe4-120">Representação e delegação de cliente</span><span class="sxs-lookup"><span data-stu-id="3abe4-120">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="3abe4-121">Encobrimento</span><span class="sxs-lookup"><span data-stu-id="3abe4-121">Cloaking</span></span>](cloaking.md)
</dt> <dt>

[<span data-ttu-id="3abe4-122">Requisitos do lado do servidor para representação</span><span class="sxs-lookup"><span data-stu-id="3abe4-122">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
