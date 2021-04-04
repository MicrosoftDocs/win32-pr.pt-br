---
title: Proxy de aplicativo Web
description: Proxy de aplicativo Web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104084956"
---
# <a name="web-application-proxy"></a><span data-ttu-id="5affc-103">Proxy de aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="5affc-103">Web Application Proxy</span></span>

## <a name="platform"></a><span data-ttu-id="5affc-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="5affc-104">Platform</span></span>

<span data-ttu-id="5affc-105">**Servidores-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5affc-105">**Servers -** Windows Server 2012 R2</span></span>  






## <a name="description"></a><span data-ttu-id="5affc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5affc-106">Description</span></span>

<span data-ttu-id="5affc-107">No Windows Server 2012 R2, adicionamos um novo serviço chamado proxy de aplicativo Web na função de acesso remoto que permite aos administradores publicar aplicativos para acesso externo.</span><span class="sxs-lookup"><span data-stu-id="5affc-107">In Windows Server 2012 R2, we added a new service called the Web Application Proxy under the Remote Access role that allows administrators to publish applications for external access.</span></span> <span data-ttu-id="5affc-108">Esse serviço atua como um proxy reverso e como um proxy de Serviços de Federação do Active Directory (AD FS) (AD FS).</span><span class="sxs-lookup"><span data-stu-id="5affc-108">This service acts as a reverse proxy and as an Active Directory Federation Services (AD FS) proxy.</span></span> <span data-ttu-id="5affc-109">Na verdade, esse serviço substitui o serviço de proxy AD FS como era conhecido no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5affc-109">In fact, this service replaces the AD FS proxy service as it was known in Windows Server 2012.</span></span>

<span data-ttu-id="5affc-110">Com o proxy de aplicativo Web, uma organização pode tornar os recursos da Web locais disponíveis para acesso externo, ao mesmo tempo em que gerencia o risco desse acesso controlando as políticas de autenticação e autorização no AD FS.</span><span class="sxs-lookup"><span data-stu-id="5affc-110">With the Web Application Proxy, an organization can make on-premises web resources available for external access while at the same time managing the risk of this access by controlling authentication and authorization policies on the AD FS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="5affc-111">Manifestação</span><span class="sxs-lookup"><span data-stu-id="5affc-111">Manifestation</span></span>

<span data-ttu-id="5affc-112">O serviço proxy de AD FS não está mais na função Serviços de Federação do Active Directory (AD FS) (AD FS), mas foi substituído pelo proxy de aplicativo Web na função de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="5affc-112">The AD FS proxy service is no longer under the Active Directory Federation Services role (AD FS), but has been replaced by the Web Application Proxy under the Remote Access role.</span></span> <span data-ttu-id="5affc-113">Isso representa uma expansão do serviço de proxy de AD FS, incluindo a funcionalidade de proxy reverso para publicação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5affc-113">This represents an expansion of the AD FS proxy service by including reverse proxy functionality for application publishing.</span></span>

## <a name="solution"></a><span data-ttu-id="5affc-114">Solução</span><span class="sxs-lookup"><span data-stu-id="5affc-114">Solution</span></span>

<span data-ttu-id="5affc-115">Para acessar o proxy de aplicativo Web, os administradores podem ir para Gerenciador do Servidor e adicionar um novo serviço de função/função.</span><span class="sxs-lookup"><span data-stu-id="5affc-115">To access the Web Application Proxy, administrators can go to Server Manager and add a new role/role service.</span></span> <span data-ttu-id="5affc-116">O administrador encontrará o proxy de aplicativo Web na função de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="5affc-116">The administrator will find the Web Application Proxy under the Remote Access role.</span></span>

## <a name="resources"></a><span data-ttu-id="5affc-117">Recursos</span><span class="sxs-lookup"><span data-stu-id="5affc-117">Resources</span></span>

-   <span data-ttu-id="5affc-118">[Guia da solução](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="5affc-118">[Solution guide](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span></span>

 

 