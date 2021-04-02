---
description: Provedores de associação permitem que clientes Instrumentação de Gerenciamento do Windows (WMI) percorram e recuperem perfis e instâncias de classe associadas de namespaces diferentes.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Acessando dados no namespace Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922599"
---
# <a name="accessing-data-in-the-interop-namespace"></a><span data-ttu-id="09aee-103">Acessando dados no namespace Interop</span><span class="sxs-lookup"><span data-stu-id="09aee-103">Accessing Data in the Interop Namespace</span></span>

<span data-ttu-id="09aee-104">Provedores de associação permitem que clientes Instrumentação de Gerenciamento do Windows (WMI) percorram e recuperem perfis e instâncias de classe associadas de namespaces diferentes.</span><span class="sxs-lookup"><span data-stu-id="09aee-104">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>

<span data-ttu-id="09aee-105">Provedores de associação e classes residem no \\ \\ \\ namespace de interoperabilidade raiz.</span><span class="sxs-lookup"><span data-stu-id="09aee-105">Association providers and classes reside in the \\\\root\\interop namespace.</span></span> <span data-ttu-id="09aee-106">Para obter mais informações, consulte [passagem de associação de namespace cruzado](cross-namespace-association-traversal.md) e [gravando um provedor de associação](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="09aee-106">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) and [Writing an Association Provider](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="09aee-107">Provedores de associação expõem perfis padrão, como um perfil de energia.</span><span class="sxs-lookup"><span data-stu-id="09aee-107">Association providers expose standard profiles, like a power profile.</span></span> <span data-ttu-id="09aee-108">Os exemplos a seguir usam o perfil de energia para ilustrar como descobrir e acessar dados por meio do namespace Interop.</span><span class="sxs-lookup"><span data-stu-id="09aee-108">The following examples use the power profile to illustrate how to discover and access data through the interop namespace.</span></span>

<span data-ttu-id="09aee-109">O Windows PowerShell fornece um mecanismo simples para percorrer a associação apropriada, recuperar um perfil de dispositivo e chamar um método.</span><span class="sxs-lookup"><span data-stu-id="09aee-109">Windows PowerShell provides a simple mechanism to traverse through the appropriate association, retrieve a device profile, and call a method.</span></span>

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a><span data-ttu-id="09aee-110">Enumerando perfis no namespace root/Interop</span><span class="sxs-lookup"><span data-stu-id="09aee-110">Enumerating profiles in the root/interop namespace</span></span>

<span data-ttu-id="09aee-111">O seguinte comando do Windows PowerShell enumera os perfis com suporte da[DMTF](https://www.dmtf.org/standards/wsman)(Distributed Management Task Force) em um computador com o Windows 7:</span><span class="sxs-lookup"><span data-stu-id="09aee-111">The following Windows PowerShell command enumerates the Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman))-supported profiles on a Windows 7 computer:</span></span>


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a><span data-ttu-id="09aee-112">Recuperando instâncias de um perfil de dispositivo específico</span><span class="sxs-lookup"><span data-stu-id="09aee-112">Retrieving instances of a specific device profile</span></span>

<span data-ttu-id="09aee-113">O comando do Windows PowerShell a seguir retorna todas as instâncias de um perfil especificado por meio do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="09aee-113">The following Windows PowerShell command returns all instances of a specified profile through [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span></span>


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a><span data-ttu-id="09aee-114">Atribuindo o perfil de energia a uma variável</span><span class="sxs-lookup"><span data-stu-id="09aee-114">Assigning the power profile to a variable</span></span>

<span data-ttu-id="09aee-115">O seguinte comando do Windows PowerShell atribui a instância do perfil de energia a uma variável:</span><span class="sxs-lookup"><span data-stu-id="09aee-115">The following Windows PowerShell command assigns the power profile instance to a variable:</span></span>


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a><span data-ttu-id="09aee-116">Enumerando os planos de energia em um computador</span><span class="sxs-lookup"><span data-stu-id="09aee-116">Enumerating the power plans on a computer</span></span>

<span data-ttu-id="09aee-117">O seguinte comando do Windows PowerShell enumera os planos de perfil de energia disponíveis:</span><span class="sxs-lookup"><span data-stu-id="09aee-117">The following Windows PowerShell command enumerates the available power profile plans:</span></span>


```PowerShell
$pplan
```



## <a name="calling-a-method"></a><span data-ttu-id="09aee-118">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="09aee-118">Calling a method</span></span>

<span data-ttu-id="09aee-119">O comando do Windows PowerShell a seguir chama o método [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) para o plano de energia:</span><span class="sxs-lookup"><span data-stu-id="09aee-119">The following Windows PowerShell command calls the [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) method for the power plan:</span></span>


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a><span data-ttu-id="09aee-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09aee-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09aee-121">Passagem de associação entre namespaces</span><span class="sxs-lookup"><span data-stu-id="09aee-121">Cross Namespace Association Traversal</span></span>](cross-namespace-association-traversal.md)
</dt> <dt>

[<span data-ttu-id="09aee-122">Escrevendo um provedor de associação</span><span class="sxs-lookup"><span data-stu-id="09aee-122">Writing an Association Provider</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

<span data-ttu-id="09aee-123">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09aee-123">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="09aee-124">[**\_PowerPlan Win32**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09aee-124">[**Win32\_PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span></span>
</dt> </dl>

 

 
