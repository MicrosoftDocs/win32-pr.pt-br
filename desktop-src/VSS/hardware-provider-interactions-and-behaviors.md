---
description: Interações e comportamentos do provedor de hardware
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interações e comportamentos do provedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165424"
---
# <a name="hardware-provider-interactions-and-behaviors"></a><span data-ttu-id="cb15d-103">Interações e comportamentos do provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="cb15d-103">Hardware Provider Interactions and Behaviors</span></span>

<span data-ttu-id="cb15d-104">Os provedores de hardware podem dar suporte a cópias de sombra de espelho de cópia completa e/ou de espelhamento completo (diferencial e/ou Plex).</span><span class="sxs-lookup"><span data-stu-id="cb15d-104">Hardware providers may support copy-on-write and/or full copy mirror (differential and/or plex) shadow copies.</span></span> <span data-ttu-id="cb15d-105">A alocação de recursos para cópias de sombra deve seguir o contexto especificado pelo solicitante em [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerado pelo [**\_ \_ \_ contexto de instantâneo VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)para o conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="cb15d-105">Resource allocation for shadow copies should follow the context specified by the requester in [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerated by [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), for the shadow copy set.</span></span>

-   <span data-ttu-id="cb15d-106">Se o solicitante especificar um contexto de cópia de sombra com suporte do provedor, o provedor deverá criar uma cópia de sombra usando esse método.</span><span class="sxs-lookup"><span data-stu-id="cb15d-106">If the requester specifies a shadow copy context that is supported by the provider, the provider should create a shadow copy using that method.</span></span>
-   <span data-ttu-id="cb15d-107">Se o solicitante especificar um contexto de cópia de sombra que não tenha suporte do provedor, o provedor não deverá tentar criar a cópia de sombra e retornar **false** por meio do parâmetro *pbIsSupported* em [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span><span class="sxs-lookup"><span data-stu-id="cb15d-107">If the requester specifies a shadow copy context that is not supported by the provider, then the provider should not attempt to create the shadow copy and return **FALSE** through the *pbIsSupported* parameter in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span></span>
-   <span data-ttu-id="cb15d-108">Se o solicitante não especificar explicitamente um contexto de cópia de sombra, o provedor deverá usar um comportamento padrão razoável para a criação da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="cb15d-108">If the requester does not explicitly specify a shadow copy context, then the provider should use reasonable default behavior for shadow copy creation.</span></span>

<span data-ttu-id="cb15d-109">Os provedores de hardware associados aos subsistemas de RAID SAN devem dar suporte a cópias de sombra transportáveis para permitir a movimentação entre hosts em uma SAN.</span><span class="sxs-lookup"><span data-stu-id="cb15d-109">Hardware providers associated with SAN RAID subsystems should support transportable shadow copies to allow movement between hosts on a SAN.</span></span>

<span data-ttu-id="cb15d-110">Os provedores de hardware em execução em vários computadores em uma SAN que ainda gerenciam o mesmo subsistema RAID não precisam coordenar entre os provedores em uma SAN.</span><span class="sxs-lookup"><span data-stu-id="cb15d-110">Hardware providers running on multiple machines on a SAN yet managing the same RAID subsystem do not need to coordinate between providers on a SAN.</span></span> <span data-ttu-id="cb15d-111">O coordenador mantém qualquer Estado necessário.</span><span class="sxs-lookup"><span data-stu-id="cb15d-111">The coordinator maintains any necessary state.</span></span> <span data-ttu-id="cb15d-112">Dois tipos de estado são reconhecidos:</span><span class="sxs-lookup"><span data-stu-id="cb15d-112">Two kinds of state are recognized:</span></span>

-   <span data-ttu-id="cb15d-113">Estado necessário para dar suporte ao acesso a dados para os volumes contidos em uma cópia de sombra de hardware.</span><span class="sxs-lookup"><span data-stu-id="cb15d-113">State necessary to support data access to the volumes contained on a hardware shadow copy.</span></span> <span data-ttu-id="cb15d-114">Isso inclui qualquer marcação de um volume como somente leitura ou oculto.</span><span class="sxs-lookup"><span data-stu-id="cb15d-114">This includes any tagging of a volume as read-only or hidden.</span></span> <span data-ttu-id="cb15d-115">Esse Estado deve estar no LUN de hardware e viajar com o LUN.</span><span class="sxs-lookup"><span data-stu-id="cb15d-115">This state must be on the hardware LUN and travel with the LUN.</span></span> <span data-ttu-id="cb15d-116">Esse estado é preservado entre as épocas de inicialização e/ou a descoberta do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cb15d-116">This state is preserved across boot epochs and/or device discovery.</span></span> <span data-ttu-id="cb15d-117">O VSS gerencia esse estado durante o tempo de vida da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="cb15d-117">VSS manages this state for the lifetime of the shadow copy.</span></span>
-   <span data-ttu-id="cb15d-118">Estado necessário para reconhecer um volume específico como parte de um conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="cb15d-118">State necessary to recognize a specific volume as part of a shadow copy set.</span></span> <span data-ttu-id="cb15d-119">Esse estado é persistido pelo VSS em conjunto com o solicitante que criou originalmente o conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="cb15d-119">This state is persisted by VSS in conjunction with the requester that originally created the shadow copy set.</span></span>

<span data-ttu-id="cb15d-120">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="cb15d-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="cb15d-121">O processo de criação de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cb15d-121">The Shadow Copy Creation Process</span></span>](the-shadow-copy-creation-process.md)
-   [<span data-ttu-id="cb15d-122">Comportamentos necessários para provedores de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cb15d-122">Required Behaviors for Shadow Copy Providers</span></span>](required-behaviors-for-shadow-copy-providers.md)
-   [<span data-ttu-id="cb15d-123">Transições de estado em provedores de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cb15d-123">State Transitions in shadow copy providers</span></span>](state-transitions-in-shadow-copy-providers.md)
-   [<span data-ttu-id="cb15d-124">Tratamento de erro em provedores de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cb15d-124">Error Handling in shadow copy providers</span></span>](error-handling-in-shadow-copy-providers.md)

 

 



