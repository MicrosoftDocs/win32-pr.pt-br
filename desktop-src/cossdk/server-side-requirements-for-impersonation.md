---
description: Requisitos de Server-Side para representação
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Requisitos de Server-Side para representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765145"
---
# <a name="server-side-requirements-for-impersonation"></a><span data-ttu-id="904a6-103">Requisitos de Server-Side para representação</span><span class="sxs-lookup"><span data-stu-id="904a6-103">Server-Side Requirements for Impersonation</span></span>

<span data-ttu-id="904a6-104">O servidor executa a representação programaticamente.</span><span class="sxs-lookup"><span data-stu-id="904a6-104">The server performs impersonation programmatically.</span></span> <span data-ttu-id="904a6-105">Ele assume explicitamente as credenciais de segurança do cliente usando [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span><span class="sxs-lookup"><span data-stu-id="904a6-105">It explicitly assumes the client's security credentials by using [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span> <span data-ttu-id="904a6-106">Quando o cliente tiver concedido a autoridade suficiente do servidor, isso terá o efeito de substituir as credenciais de segurança do cliente pelo token de thread do servidor, no lugar do token do processo.</span><span class="sxs-lookup"><span data-stu-id="904a6-106">When the client has granted the server sufficient authority, this has the effect of substituting the client's security credentials with the server thread token, in place of the process token.</span></span>

<span data-ttu-id="904a6-107">Quando isso tiver sido feito, o servidor poderá, por exemplo, usar o token do cliente para acessar recursos protegidos com um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="904a6-107">When this has been done, the server can, for example, use the client token to access resources guarded with a security descriptor.</span></span> <span data-ttu-id="904a6-108">Ou pode fazer chamadas sob a identidade do cliente, se o encobrimento estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="904a6-108">Or it can make calls under the client identity, if cloaking is enabled.</span></span>

<span data-ttu-id="904a6-109">O servidor pode definir explicitamente o encobrimento programaticamente ou pode contar com uma configuração administrativa.</span><span class="sxs-lookup"><span data-stu-id="904a6-109">The server can explicitly set cloaking programmatically, or it can rely on an administrative setting.</span></span> <span data-ttu-id="904a6-110">Por padrão, os aplicativos COM+ são configurados para usar o encobrimento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="904a6-110">By default, COM+ applications are configured to use dynamic cloaking.</span></span> <span data-ttu-id="904a6-111">Para obter mais detalhes, consulte [encobrindo](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="904a6-111">For more detail, see [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="904a6-112">Se o servidor estiver implementando a delegação em nome do cliente — usando a identidade do cliente pela rede — a identidade do processo do servidor deverá ser marcada como "confiável para delegação" no serviço de Active Directory; caso contrário, haverá falha na delegação.</span><span class="sxs-lookup"><span data-stu-id="904a6-112">If the server is implementing delegation on behalf of the client—using the client identity over network—the server process identity must be marked as "Trusted for delegation" in the Active Directory Service; otherwise, delegation will fail.</span></span>

<span data-ttu-id="904a6-113">Quando terminar de usar a identidade do cliente, o servidor poderá reverter para seu próprio token de processo usando o [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="904a6-113">When it has finished using the client's identity, the server can revert to its own process token using [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="904a6-114">Para obter detalhes sobre como implementar a representação e a delegação, consulte [delegação e representação](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="904a6-114">For details on implementing impersonation and delegation, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="904a6-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="904a6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="904a6-116">Representação e delegação de cliente</span><span class="sxs-lookup"><span data-stu-id="904a6-116">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="904a6-117">Requisitos do lado do cliente para representação</span><span class="sxs-lookup"><span data-stu-id="904a6-117">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="904a6-118">Encobrimento</span><span class="sxs-lookup"><span data-stu-id="904a6-118">Cloaking</span></span>](cloaking.md)
</dt> </dl>

 

 
