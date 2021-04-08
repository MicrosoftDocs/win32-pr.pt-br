---
title: Interfaces de gateway Área de Trabalho Remota
description: A API do gateway de Área de Trabalho Remota (Gateway RD) dá suporte às seguintes interfaces. Você pode usar essas interfaces para implementar plug-ins que fornecem autenticação e autorização personalizadas.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916001"
---
# <a name="remote-desktop-gateway-interfaces"></a><span data-ttu-id="66684-104">Interfaces de gateway Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="66684-104">Remote Desktop Gateway Interfaces</span></span>

<span data-ttu-id="66684-105">A API do gateway de Área de Trabalho Remota (Gateway RD) dá suporte às seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="66684-105">The Remote Desktop Gateway (RD Gateway) API supports the following interfaces.</span></span> <span data-ttu-id="66684-106">Você pode usar essas interfaces para implementar plug-ins que fornecem autenticação e autorização personalizadas.</span><span class="sxs-lookup"><span data-stu-id="66684-106">You can use these interfaces to implement plug-ins that provide customized authentication and authorization.</span></span> <span data-ttu-id="66684-107">Não há nenhuma dependência entre o plug-in de autenticação e o plug-in de autorização, e você pode implementar apenas um único plug-in, se escolher.</span><span class="sxs-lookup"><span data-stu-id="66684-107">There is no dependency between the authentication plug-in and the authorization plug-in, and you can implement only a single plug-in if you choose.</span></span>

<span data-ttu-id="66684-108">Os plug-ins de autenticação são [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) e [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span><span class="sxs-lookup"><span data-stu-id="66684-108">The authentication plug-ins are [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) and [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span></span>

<span data-ttu-id="66684-109">Os plug-ins de autorização são [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)e [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span><span class="sxs-lookup"><span data-stu-id="66684-109">The authorization plug-ins are [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink), and [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="66684-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="66684-110">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="66684-111">**ITSGAccountingEngine**</span><span class="sxs-lookup"><span data-stu-id="66684-111">**ITSGAccountingEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

<span data-ttu-id="66684-112">Expõe métodos que fornecem informações sobre a criação ou o fechamento de sessões para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="66684-112">Exposes methods that provide information about the creation or closing of sessions for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="66684-113">**ITSGAuthenticateUserSink**</span><span class="sxs-lookup"><span data-stu-id="66684-113">**ITSGAuthenticateUserSink**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

<span data-ttu-id="66684-114">Expõe métodos que notificam o Gateway RD sobre eventos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="66684-114">Exposes methods that notify RD Gateway about authentication events.</span></span>

</dd> <dt>

[<span data-ttu-id="66684-115">**ITSGAuthenticationEngine**</span><span class="sxs-lookup"><span data-stu-id="66684-115">**ITSGAuthenticationEngine**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

<span data-ttu-id="66684-116">Expõe métodos que autenticam usuários para o gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="66684-116">Exposes methods that authenticate users for RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="66684-117">**ITSGAuthorizeConnectionSink**</span><span class="sxs-lookup"><span data-stu-id="66684-117">**ITSGAuthorizeConnectionSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

<span data-ttu-id="66684-118">Expõe métodos que notificam o Gateway RD sobre o resultado de uma tentativa de autorizar uma conexão.</span><span class="sxs-lookup"><span data-stu-id="66684-118">Exposes methods that notify RD Gateway about the result of an attempt to authorize a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="66684-119">**ITSGAuthorizeResourceSink**</span><span class="sxs-lookup"><span data-stu-id="66684-119">**ITSGAuthorizeResourceSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

<span data-ttu-id="66684-120">Expõe métodos que notificam o Gateway RD sobre o resultado de uma tentativa de autorizar um recurso.</span><span class="sxs-lookup"><span data-stu-id="66684-120">Exposes methods that notify RD Gateway about the result of an attempt to authorize a resource.</span></span>

</dd> <dt>

[<span data-ttu-id="66684-121">**ITSGPolicyEngine**</span><span class="sxs-lookup"><span data-stu-id="66684-121">**ITSGPolicyEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

<span data-ttu-id="66684-122">Expõe métodos que autorizam conexões e recursos.</span><span class="sxs-lookup"><span data-stu-id="66684-122">Exposes methods that authorize connections and resources.</span></span>

</dd> </dl>

 

 




