---
description: Informações de contexto de chamada de segurança
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informações de contexto de chamada de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164158"
---
# <a name="security-call-context-information"></a><span data-ttu-id="1aff8-103">Informações de contexto de chamada de segurança</span><span class="sxs-lookup"><span data-stu-id="1aff8-103">Security Call Context Information</span></span>

<span data-ttu-id="1aff8-104">A segurança baseada em funções é criada em um mecanismo geral que permite que você recupere informações de segurança sobre todos os chamadores upstream na cadeia de chamadas para seu componente.</span><span class="sxs-lookup"><span data-stu-id="1aff8-104">Role-based security is built on a general mechanism that enables you to retrieve security information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="1aff8-105">Essas informações estão disponíveis somente quando você tem a verificação de função no nível de componente habilitada.</span><span class="sxs-lookup"><span data-stu-id="1aff8-105">This information is available only when you have component-level role checking enabled.</span></span> <span data-ttu-id="1aff8-106">Para obter detalhes sobre como definir a segurança em nível de componente, consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="1aff8-106">For details about how to set component-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="1aff8-107">Você pode usar a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) para acessar informações de contexto de chamada de segurança programaticamente.</span><span class="sxs-lookup"><span data-stu-id="1aff8-107">You can use the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface to access security call context information programmatically.</span></span> <span data-ttu-id="1aff8-108">Para obter uma descrição, consulte [segurança de componente programática](programmatic-component-security.md).</span><span class="sxs-lookup"><span data-stu-id="1aff8-108">For a description, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

<span data-ttu-id="1aff8-109">O contexto de chamada de segurança é passado sempre que um limite de segurança é ultrapassado.</span><span class="sxs-lookup"><span data-stu-id="1aff8-109">Security call context is passed along every time a security boundary is crossed.</span></span> <span data-ttu-id="1aff8-110">Para chamadas entre componentes dentro de um aplicativo, que residem no mesmo limite de segurança, nenhuma informação de contexto de chamada é passada.</span><span class="sxs-lookup"><span data-stu-id="1aff8-110">For calls between components within an application, which reside within the same security boundary, no call context information is passed.</span></span> <span data-ttu-id="1aff8-111">Para chamadas entre processos ou entre aplicativos em um processo, os fluxos de informações de contexto de chamada.</span><span class="sxs-lookup"><span data-stu-id="1aff8-111">For calls between processes or between applications within a process, call context information flows along.</span></span>

<span data-ttu-id="1aff8-112">Esse recurso será particularmente útil se você quiser fazer auditoria e log detalhados.</span><span class="sxs-lookup"><span data-stu-id="1aff8-112">This facility is particularly useful if you wish to do detailed auditing and logging.</span></span> <span data-ttu-id="1aff8-113">Você pode recuperar e registrar informações de segurança para cada chamador upstream.</span><span class="sxs-lookup"><span data-stu-id="1aff8-113">You can retrieve and record security information for every upstream caller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1aff8-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1aff8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aff8-115">Criando funções com eficiência</span><span class="sxs-lookup"><span data-stu-id="1aff8-115">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="1aff8-116">Limites de segurança</span><span class="sxs-lookup"><span data-stu-id="1aff8-116">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="1aff8-117">Propriedade de contexto de segurança</span><span class="sxs-lookup"><span data-stu-id="1aff8-117">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="1aff8-118">Usando funções para autorização de cliente</span><span class="sxs-lookup"><span data-stu-id="1aff8-118">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



