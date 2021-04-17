---
description: O Windows Server 2008 R2 e o Windows 7 apresentam as seguintes alterações na Serviço de Cópias de Sombra de Volume.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'O que há de novo: VSS no Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811378"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a><span data-ttu-id="fd878-103">O que há de novo: VSS no Windows Server 2008 R2 & Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd878-103">What's New: VSS in Windows Server 2008 R2 & Windows 7</span></span>

<span data-ttu-id="fd878-104">O Windows Server 2008 R2 e o Windows 7 apresentam as seguintes alterações na Serviço de Cópias de Sombra de Volume.</span><span class="sxs-lookup"><span data-stu-id="fd878-104">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Volume Shadow Copy Service.</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="fd878-105">Novas interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="fd878-105">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="fd878-106">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="fd878-106">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[<span data-ttu-id="fd878-107">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="fd878-107">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[<span data-ttu-id="fd878-108">**IVssCreateExpressWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="fd878-108">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[<span data-ttu-id="fd878-109">**IVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="fd878-109">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a><span data-ttu-id="fd878-110">Novas classes VSS</span><span class="sxs-lookup"><span data-stu-id="fd878-110">New VSS Classes</span></span>

<dl>

[<span data-ttu-id="fd878-111">**CVssWriterEx2**</span><span class="sxs-lookup"><span data-stu-id="fd878-111">**CVssWriterEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="fd878-112">Novas enumerações VSS</span><span class="sxs-lookup"><span data-stu-id="fd878-112">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="fd878-113">**\_Opções de recuperação do VSS \_**</span><span class="sxs-lookup"><span data-stu-id="fd878-113">**VSS\_RECOVERY\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a><span data-ttu-id="fd878-114">Novas funções do VSS</span><span class="sxs-lookup"><span data-stu-id="fd878-114">New VSS Functions</span></span>

<dl>

[<span data-ttu-id="fd878-115">**CreateVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="fd878-115">**CreateVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="fd878-116">Modificações de interface VSS existentes</span><span class="sxs-lookup"><span data-stu-id="fd878-116">Existing VSS Interface Modifications</span></span>

<dl>

<span data-ttu-id="fd878-117">Interface [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)</span><span class="sxs-lookup"><span data-stu-id="fd878-117">[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) interface</span></span><dl> <span data-ttu-id="fd878-118">Método adicionado: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span><span class="sxs-lookup"><span data-stu-id="fd878-118">Added method: [**ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span></span>  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="fd878-119">Rastreamento e log de eventos do VSS</span><span class="sxs-lookup"><span data-stu-id="fd878-119">VSS Event Tracing and Logging</span></span>

<span data-ttu-id="fd878-120">A partir do Windows Server 2008 R2 e do Windows 7, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta tracelog para coletar informações de rastreamento para a infraestrutura do VSS.</span><span class="sxs-lookup"><span data-stu-id="fd878-120">Beginning with Windows Server 2008 R2 and Windows 7, you can use the VssTrace tool, the Logman tool, or the Tracelog tool to collect tracing information for the VSS infrastructure.</span></span> <span data-ttu-id="fd878-121">Para obter mais informações, consulte [usando ferramentas de rastreamento com o VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="fd878-121">For more information, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="lun-resynchronization"></a><span data-ttu-id="fd878-122">Ressincronização de LUN</span><span class="sxs-lookup"><span data-stu-id="fd878-122">LUN Resynchronization</span></span>

<span data-ttu-id="fd878-123">No Windows Server 2008 R2 e no Windows 7, os solicitantes do VSS podem usar um recurso de provedor de cópias de sombra de hardware chamado de "LUN Resync" (ressincronização de LUN).</span><span class="sxs-lookup"><span data-stu-id="fd878-123">In Windows Server 2008 R2 and Windows 7, VSS requesters can use a hardware shadow copy provider feature called LUN resynchronization (or "LUN resync").</span></span> <span data-ttu-id="fd878-124">Esse é um esquema de recuperação rápida que permite que um administrador de aplicativos restaure dados de uma cópia de sombra para o número de unidade lógica (LUN) original ou para um novo LUN.</span><span class="sxs-lookup"><span data-stu-id="fd878-124">This is a fast-recovery scheme that allows an application administrator to restore data from a shadow copy to the original logical unit number (LUN) or to a new LUN.</span></span> <span data-ttu-id="fd878-125">A cópia de sombra pode ser um clone completo ou uma cópia de sombra diferencial.</span><span class="sxs-lookup"><span data-stu-id="fd878-125">The shadow copy can be a full clone or a differential shadow copy.</span></span> <span data-ttu-id="fd878-126">Em ambos os casos, no final da operação de ressincronização, o LUN de destino terá o mesmo conteúdo que o LUN de cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="fd878-126">In either case, at the end of the resync operation, the destination LUN will have the same contents as the shadow copy LUN.</span></span> <span data-ttu-id="fd878-127">Durante a operação de ressincronização, a matriz executa uma cópia no nível do bloco da cópia de sombra para o LUN de destino.</span><span class="sxs-lookup"><span data-stu-id="fd878-127">During the resync operation, the array performs a block-level copy from the shadow copy to the destination LUN.</span></span> <span data-ttu-id="fd878-128">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fd878-128">For more information, see the following:</span></span>

-   [<span data-ttu-id="fd878-129">Ressincronização de LUN – um cenário de recuperação rápida no servidor 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fd878-129">LUN Resync - A fast recovery scenario in Server 2008 R2</span></span>](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   <span data-ttu-id="fd878-130">"Como as cópias de sombra são usadas" em [serviço de cópias de sombra de volume](/windows-server/storage/file-server/volume-shadow-copy-service)</span><span class="sxs-lookup"><span data-stu-id="fd878-130">"How Shadow Copies Are Used" in [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service)</span></span>
-   [<span data-ttu-id="fd878-131">Armadilhas comuns de ressincronização de LUN</span><span class="sxs-lookup"><span data-stu-id="fd878-131">Common LUN Resync gotchas</span></span>](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a><span data-ttu-id="fd878-132">Gravadores expressos</span><span class="sxs-lookup"><span data-stu-id="fd878-132">Express Writers</span></span>

<span data-ttu-id="fd878-133">No Windows Server 2008 R2 e no Windows 7, a interface do VSS Express permite que um aplicativo registre o local de seus arquivos de dados sem implementar um gravador VSS.</span><span class="sxs-lookup"><span data-stu-id="fd878-133">In Windows Server 2008 R2 and Windows 7, the VSS express interface allows an application to register the location of its data files without implementing a VSS writer.</span></span> <span data-ttu-id="fd878-134">Para obter mais informações, consulte os [gravadores do serviço de cópias de sombra de volume (VSS) Express](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd878-134">For more information, see [Volume Shadow Copy Service (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span></span>

## <a name="new-vss-writers"></a><span data-ttu-id="fd878-135">Novos gravadores VSS</span><span class="sxs-lookup"><span data-stu-id="fd878-135">New VSS Writers</span></span>

<span data-ttu-id="fd878-136">O Windows Server 2008 R2 e o Windows 7 apresentam os seguintes gravadores VSS:</span><span class="sxs-lookup"><span data-stu-id="fd878-136">Windows Server 2008 R2 and Windows 7 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="fd878-137">Gravador de contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="fd878-137">Performance Counters Writer</span></span>
-   <span data-ttu-id="fd878-138">Gravador de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="fd878-138">Task Scheduler Writer</span></span>
-   <span data-ttu-id="fd878-139">Gravador de repositório de metadados do VSS</span><span class="sxs-lookup"><span data-stu-id="fd878-139">VSS Metadata Store Writer</span></span>

<span data-ttu-id="fd878-140">Esses novos gravadores são documentados em [gravadores VSS](in-box-vss-writers.md)integrados.</span><span class="sxs-lookup"><span data-stu-id="fd878-140">These new writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
