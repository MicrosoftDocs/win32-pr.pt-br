---
description: No COM+, o estado transitório compartilhado para objetos é gerenciado usando o SPM (Shared Property Manager). O SPM é um dispensador de recursos que você pode usar para compartilhar o estado entre vários objetos dentro de um processo de servidor.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Conceitos de Gerenciador de Propriedades compartilhados do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771287"
---
# <a name="com-shared-property-manager-concepts"></a><span data-ttu-id="e1676-104">Conceitos de Gerenciador de Propriedades compartilhados do COM+</span><span class="sxs-lookup"><span data-stu-id="e1676-104">COM+ Shared Property Manager Concepts</span></span>

<span data-ttu-id="e1676-105">No COM+, o estado transitório compartilhado para objetos é gerenciado usando o SPM (Shared Property Manager).</span><span class="sxs-lookup"><span data-stu-id="e1676-105">In COM+, shared transient state for objects is managed by using the shared property manager (SPM).</span></span> <span data-ttu-id="e1676-106">O SPM é um dispensador de recursos que você pode usar para compartilhar o estado entre vários objetos dentro de um processo de servidor.</span><span class="sxs-lookup"><span data-stu-id="e1676-106">The SPM is a resource dispenser that you can use to share state among multiple objects within a server process.</span></span>

<span data-ttu-id="e1676-107">Você não pode usar variáveis globais em um ambiente distribuído devido a problemas de simultaneidade e de conflito de nome.</span><span class="sxs-lookup"><span data-stu-id="e1676-107">You cannot use global variables in a distributed environment because of concurrency and name collision issues.</span></span> <span data-ttu-id="e1676-108">O Gerenciador de propriedades compartilhado elimina colisões de nomes fornecendo grupos de propriedades compartilhadas, que estabelecem namespaces exclusivos para as propriedades compartilhadas que eles contêm.</span><span class="sxs-lookup"><span data-stu-id="e1676-108">The shared property manager eliminates name collisions by providing shared property groups, which establish unique namespaces for the shared properties they contain.</span></span> <span data-ttu-id="e1676-109">O SPM também implementa bloqueios e semáforos para ajudar a proteger propriedades compartilhadas de acesso simultâneo, o que pode resultar em atualizações perdidas e deixar Propriedades em um estado imprevisível.</span><span class="sxs-lookup"><span data-stu-id="e1676-109">The SPM also implements locks and semaphores to help protect shared properties from simultaneous access, which could result in lost updates and leave properties in an unpredictable state.</span></span>

> [!Note]  
> <span data-ttu-id="e1676-110">Estado transitório compartilhado são informações de estado mantidas na memória que não sobrevivem a falhas do sistema.</span><span class="sxs-lookup"><span data-stu-id="e1676-110">Shared transient state is state information kept in memory that does not survive system failures.</span></span> <span data-ttu-id="e1676-111">As informações são projetadas para serem compartilhadas por vários objetos entre os limites de transação (mas não entre processos).</span><span class="sxs-lookup"><span data-stu-id="e1676-111">The information is designed to be shared by multiple objects across transaction (but not across process) boundaries.</span></span>

 

<span data-ttu-id="e1676-112">As propriedades compartilhadas armazenadas no SPM estão disponíveis somente para objetos em execução no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="e1676-112">Shared properties stored in the SPM are available only to objects running in the same process.</span></span> <span data-ttu-id="e1676-113">Isso significa que os objetos que usarão o SPM para armazenar valores e que deverão ter acesso a esses valores devem ser instalados como parte do mesmo aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="e1676-113">This means that the objects that will use the SPM for storing values and that will need to have access to these values must be installed as part of the same COM+ application.</span></span> <span data-ttu-id="e1676-114">É possível que os administradores do sistema movam classes COM+ de um pacote para outro depois que seu aplicativo COM+ tiver sido implantado.</span><span class="sxs-lookup"><span data-stu-id="e1676-114">It is possible for system administrators to move COM+ classes from one package to another after your COM+ application has been deployed.</span></span> <span data-ttu-id="e1676-115">Se você depender de vários objetos de compartilhamento de propriedades por meio do SPM, deverá documentar claramente que eles devem ser instalados no mesmo aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="e1676-115">If you rely on several objects sharing properties through the SPM, you should clearly document that they must be installed in the same COM+ application.</span></span>

<span data-ttu-id="e1676-116">Também é importante que os componentes que compartilham propriedades tenham o mesmo atributo de ativação.</span><span class="sxs-lookup"><span data-stu-id="e1676-116">It's also important for components sharing properties to have the same activation attribute.</span></span> <span data-ttu-id="e1676-117">Se dois componentes no mesmo pacote tiverem atributos de ativação diferentes, eles geralmente não poderão compartilhar Propriedades.</span><span class="sxs-lookup"><span data-stu-id="e1676-117">If two components in the same package have different activation attributes, they generally won't be able to share properties.</span></span> <span data-ttu-id="e1676-118">Por exemplo, se um componente estiver configurado para ser executado em um processo de cliente e o outro estiver configurado para ser executado em um processo de servidor, seus objetos normalmente serão executados em processos diferentes, mesmo que estejam no mesmo pacote.</span><span class="sxs-lookup"><span data-stu-id="e1676-118">For example, if one component is configured to run in a client process and the other is configured to run in a server process, their objects will usually run in different processes even though they're in the same package.</span></span>

<span data-ttu-id="e1676-119">Você deve sempre instanciar os objetos [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)e [**SharedProperty**](sharedproperty.md) de componentes com+ em vez de um cliente base.</span><span class="sxs-lookup"><span data-stu-id="e1676-119">You should always instantiate the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md), and [**SharedProperty**](sharedproperty.md) objects from COM+ components rather than from a base client.</span></span> <span data-ttu-id="e1676-120">Se um cliente base criar grupos de propriedades e propriedades compartilhadas, as propriedades compartilhadas estarão dentro do processo de cliente base, não em um processo de servidor.</span><span class="sxs-lookup"><span data-stu-id="e1676-120">If a base client creates shared property groups and properties, the shared properties are inside the base-client process, not in a server process.</span></span> <span data-ttu-id="e1676-121">Isso significa que os objetos COM+ não podem compartilhar as propriedades, a menos que os objetos também estejam em execução no processo do cliente (o que geralmente não é uma boa ideia).</span><span class="sxs-lookup"><span data-stu-id="e1676-121">This means the COM+ objects cannot share the properties unless the objects are also running in the client process (which is generally not a good idea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1676-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1676-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1676-123">Gerenciador de Propriedades COM+ compartilhados</span><span class="sxs-lookup"><span data-stu-id="e1676-123">COM+ Shared Property Manager</span></span>](com--shared-property-manager.md)
</dt> <dt>

[<span data-ttu-id="e1676-124">Grupos de propriedades compartilhadas</span><span class="sxs-lookup"><span data-stu-id="e1676-124">Shared Property Groups</span></span>](shared-property-groups.md)
</dt> </dl>

 

 



