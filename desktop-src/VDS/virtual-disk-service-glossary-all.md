---
description: Esta seção fornece um glossário de termos técnicos usados na documentação do VDS (serviço de disco virtual).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossário do serviço de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc8804f1aea832f59fcbcab65423e92e134939f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921826"
---
# <a name="virtual-disk-service-glossary"></a><span data-ttu-id="4423c-103">Glossário do serviço de disco virtual</span><span class="sxs-lookup"><span data-stu-id="4423c-103">Virtual Disk Service Glossary</span></span>

<span data-ttu-id="4423c-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4423c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="4423c-105">Esta seção fornece um glossário de termos técnicos usados na documentação do VDS (serviço de disco virtual).</span><span class="sxs-lookup"><span data-stu-id="4423c-105">This section provides a glossary of technical terms used in the Virtual Disk Service (VDS) documentation.</span></span>

<dl> <dt>

<span data-ttu-id="4423c-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configuração do automagic**</span><span class="sxs-lookup"><span data-stu-id="4423c-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic configuration**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-107">Provedor de RAID de hardware que fornece um conjunto de regras para escolher o remapeamento de bloco lógico LUN com base em atributos simples.</span><span class="sxs-lookup"><span data-stu-id="4423c-107">Hardware RAID provider that supplies a set of rules for choosing LUN logical block remapping based on simple attributes.</span></span> <span data-ttu-id="4423c-108">Os provedores automagic também podem alterar dinamicamente o mapeamento para desempenho ou gerenciamento de falhas.</span><span class="sxs-lookup"><span data-stu-id="4423c-108">Automagic providers can also dynamically alter the mapping for performance or fault management.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**Dicas do automagic**</span><span class="sxs-lookup"><span data-stu-id="4423c-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic hints**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-110">Informações fornecidas a um provedor automagic para orientar a configuração de bloco lógico de LUN.</span><span class="sxs-lookup"><span data-stu-id="4423c-110">Information supplied to an automagic provider to guide the LUN logical block configuration.</span></span> <span data-ttu-id="4423c-111">As dicas incluem informações sobre a tolerância a falhas, a atomicidade física e o padrão de acesso de e/s desejado.</span><span class="sxs-lookup"><span data-stu-id="4423c-111">Hints include information as to the desired fault tolerance, physical atomicity, and intended I/O access pattern.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco básico**</span><span class="sxs-lookup"><span data-stu-id="4423c-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**basic disk**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-113">Um disco gerenciado pelo provedor de software mais simples possível.</span><span class="sxs-lookup"><span data-stu-id="4423c-113">A disk managed by the simplest possible software provider.</span></span> <span data-ttu-id="4423c-114">O provedor de disco básico dá suporte apenas a volumes que são mapeados diretamente para as estruturas de dados de configuração de partição.</span><span class="sxs-lookup"><span data-stu-id="4423c-114">The basic disk provider supports only volumes that directly map to partition configuration data structures.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**vinculação**</span><span class="sxs-lookup"><span data-stu-id="4423c-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-116">Selecionando um conjunto de mapeamentos para recursos físicos.</span><span class="sxs-lookup"><span data-stu-id="4423c-116">Selecting for a set of mappings to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**vertê**</span><span class="sxs-lookup"><span data-stu-id="4423c-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**convert**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-118">O processo de converter um disco básico em um disco dinâmico.</span><span class="sxs-lookup"><span data-stu-id="4423c-118">The process of converting a basic disk to a dynamic disk.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuração**</span><span class="sxs-lookup"><span data-stu-id="4423c-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuration**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-120">Uma coleção de parâmetros operacionais que fornecem o mapeamento de um volume, ou LUN, para recursos físicos.</span><span class="sxs-lookup"><span data-stu-id="4423c-120">A collection of the operating parameters that supply the mapping from a volume, or LUN, to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controle**</span><span class="sxs-lookup"><span data-stu-id="4423c-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-122">Um programa de software que contém a inteligência de tempo de execução para um provedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="4423c-122">A software program that contains the runtime intelligence for a hardware provider.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disco**</span><span class="sxs-lookup"><span data-stu-id="4423c-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disk**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-124">Um disco físico ou LUN RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="4423c-124">A physical disk or hardware RAID LUN.</span></span> <span data-ttu-id="4423c-125">Os discos são destinos para carga de e/s de armazenamento em tempo de execução; A Plug and Play (PNP) não faz distinção entre JBOD e LUNs.</span><span class="sxs-lookup"><span data-stu-id="4423c-125">Disks are targets for runtime storage I/O load; Plug and Play (PNP) does not distinguish between JBOD and LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**platter de disco**</span><span class="sxs-lookup"><span data-stu-id="4423c-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disk platter**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-127">Um subconjunto de um pacote usado para exportar ou importar volumes de um pacote.</span><span class="sxs-lookup"><span data-stu-id="4423c-127">A subset of a pack used for exporting or importing volumes from a pack.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**pacote de disco**</span><span class="sxs-lookup"><span data-stu-id="4423c-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**disk pack**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-129">Consulte o *pacote*.</span><span class="sxs-lookup"><span data-stu-id="4423c-129">See *pack*.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**Dirigir**</span><span class="sxs-lookup"><span data-stu-id="4423c-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**drive**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-131">Um eixo de disco físico em um subsistema RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="4423c-131">A physical disk spindle within a hardware RAID subsystem.</span></span> <span data-ttu-id="4423c-132">As unidades são associadas a LUNs pelo subsistema.</span><span class="sxs-lookup"><span data-stu-id="4423c-132">Drives are bound into LUNs by the subsystem.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinâmico**</span><span class="sxs-lookup"><span data-stu-id="4423c-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamic disk**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-134">Um disco gerenciado por um provedor de RAID de software com suporte para reconfiguração de volume flexível.</span><span class="sxs-lookup"><span data-stu-id="4423c-134">A disk managed by a software RAID provider with support for flexible volume reconfiguration.</span></span> <span data-ttu-id="4423c-135">Um disco dinâmico usa uma partição como um contêiner para volumes; Não há nenhum mapeamento garantido.</span><span class="sxs-lookup"><span data-stu-id="4423c-135">A dynamic disk uses a partition as a container for volumes; there is no guaranteed mapping.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configuração explícita**</span><span class="sxs-lookup"><span data-stu-id="4423c-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explicit configuration**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-137">Uma configuração com os parâmetros, incluindo o tipo de volume e o layout exato, para uma coleção de volumes de destino.</span><span class="sxs-lookup"><span data-stu-id="4423c-137">A configuration with the parameters, including the volume type and the exact layout, for a collection of target volumes.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**Export**</span><span class="sxs-lookup"><span data-stu-id="4423c-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**export**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-139">O ato de mover um platter de disco e todos os volumes contidos nesse platter para fora de um pacote.</span><span class="sxs-lookup"><span data-stu-id="4423c-139">The act of moving a disk platter and all volumes contained on that platter out of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**tention**</span><span class="sxs-lookup"><span data-stu-id="4423c-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-141">Um intervalo contíguo de setores lógicos que contribuem para um único volume ou disco.</span><span class="sxs-lookup"><span data-stu-id="4423c-141">A contiguous range of logical sectors contributing to a single volume or disk.</span></span> <span data-ttu-id="4423c-142">Uma extensão também pode ser um intervalo de setores não alocados.</span><span class="sxs-lookup"><span data-stu-id="4423c-142">An extent can also be range of unallocated sectors.</span></span> <span data-ttu-id="4423c-143">Normalmente, um sistema de arquivos exibe os detalhes de extensão para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="4423c-143">Commonly, a file system displays the extent details to an end-user.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabela de partição GUID (GPT)**</span><span class="sxs-lookup"><span data-stu-id="4423c-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID Partition Table (GPT)**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-145">Estruturas usadas pelo firmware EFI.</span><span class="sxs-lookup"><span data-stu-id="4423c-145">Structures used by EFI firmware.</span></span> <span data-ttu-id="4423c-146">O GPT é um dos dois formatos de dados de configuração de software de nível mais baixo usados pelo firmware de plataforma para localizar um sistema operacional inicializável ou outra imagem executável.</span><span class="sxs-lookup"><span data-stu-id="4423c-146">GPT is one of two lowest level software configuration data formats used by platform firmware to locate a bootable operating system or other executable image.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**provedor de hardware**</span><span class="sxs-lookup"><span data-stu-id="4423c-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**hardware provider**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-148">Uma coleção de software que é executada no host, um adaptador de barramento e, possivelmente, um subsistema de armazenamento externo que funciona em conjunto para a superfície e o gerenciamento de LUNs RAID.</span><span class="sxs-lookup"><span data-stu-id="4423c-148">A collection of software that executes on the host, a bus adapter, and possibly an external storage subsystem that works together to surface and manage RAID LUNs.</span></span> <span data-ttu-id="4423c-149">Os provedores de hardware para a maioria dos subsistemas de armazenamento externos contêm apenas o software de modo de usuário, baseado em host.</span><span class="sxs-lookup"><span data-stu-id="4423c-149">Hardware providers for most external storage subsystems contain only user-mode, host-based software.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**monitoramento**</span><span class="sxs-lookup"><span data-stu-id="4423c-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**health**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-151">O status atual de gerenciamento de falhas de um volume ou LUN.</span><span class="sxs-lookup"><span data-stu-id="4423c-151">The current fault-management status of a volume or a LUN.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**Hot Sparing**</span><span class="sxs-lookup"><span data-stu-id="4423c-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-153">Adicionando temporariamente um plex de volume a um volume.</span><span class="sxs-lookup"><span data-stu-id="4423c-153">Temporarily adding a volume plex to a volume.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**importe**</span><span class="sxs-lookup"><span data-stu-id="4423c-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**import**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-155">O ato de mover um platter de disco e todos os seus volumes para um pacote existente.</span><span class="sxs-lookup"><span data-stu-id="4423c-155">The act of moving a disk platter and all its volumes into an existing pack.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**apenas um monte de discos (JBOD)**</span><span class="sxs-lookup"><span data-stu-id="4423c-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**just a bunch of disks (JBOD)**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-157">Uma coleção de eixos físicos sem o controle coordenado fornecido por um dispositivo RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="4423c-157">A collection of physical spindles without the coordinated control provided by a hardware RAID device.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**número de bloco lógico (LBN)**</span><span class="sxs-lookup"><span data-stu-id="4423c-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logical block number (LBN)**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-159">A menor unidade endereçável de dados de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4423c-159">The smallest addressable unit of storage data.</span></span> <span data-ttu-id="4423c-160">LBN é usado com protocolos de comando de e/s.</span><span class="sxs-lookup"><span data-stu-id="4423c-160">LBN is used with I/O command protocols.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**mapeamento de bloco lógico**</span><span class="sxs-lookup"><span data-stu-id="4423c-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logical block mapping**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-162">A transformação dos blocos lógicos apresentados a um provedor para aqueles expostos pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="4423c-162">The transformation of the logical blocks presented to a provider to those exposed by the provider.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**LUN (número de unidade lógica)**</span><span class="sxs-lookup"><span data-stu-id="4423c-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logical unit number (LUN)**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-164">Uma unidade de armazenamento fisicamente endereçável, como na superfície de um subsistema RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="4423c-164">A physically addressable storage unit as surfaced by a hardware RAID subsystem.</span></span> <span data-ttu-id="4423c-165">Esse termo também pode se referir ao identificador SCSI para a unidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4423c-165">This term can also refer to the SCSI identifier for the storage unit.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Número de LUN**</span><span class="sxs-lookup"><span data-stu-id="4423c-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN number**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-167">Um número que um provedor de hardware VDS atribui a um LUN em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="4423c-167">A number that a VDS hardware provider assigns to a LUN in an array.</span></span> <span data-ttu-id="4423c-168">Isso não é o mesmo que o "número de unidade lógica" no endereço SCSI do disco.</span><span class="sxs-lookup"><span data-stu-id="4423c-168">This is not the same as the "logical unit number" in the disk's SCSI address.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**serviço de gerenciamento**</span><span class="sxs-lookup"><span data-stu-id="4423c-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**management service**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-170">Um programa de software que é executado conforme necessário para executar a configuração, o monitoramento ou o tratamento de falhas do volume.</span><span class="sxs-lookup"><span data-stu-id="4423c-170">A software program that executes as needed to perform volume configuration, monitoring, or fault handling.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**correlação**</span><span class="sxs-lookup"><span data-stu-id="4423c-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-172">Um volume que é exposto ao sistema operacional e tem um nome de volume associado (uma letra de unidade).</span><span class="sxs-lookup"><span data-stu-id="4423c-172">A volume that is exposed to the operating system and has an associated volume name (a drive letter).</span></span> <span data-ttu-id="4423c-173">Um volume pode ser acessado por um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4423c-173">A volume is accessible by a file system.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**mascaramento**</span><span class="sxs-lookup"><span data-stu-id="4423c-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**masking**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-175">Um disco não reconhecido pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4423c-175">A disk not recognized by the operating system.</span></span> <span data-ttu-id="4423c-176">Um disco pode ser mascarado pelo subsistema RAID de hardware, comutador, reserva SCSI por outro host de computador ou software na pilha de discos.</span><span class="sxs-lookup"><span data-stu-id="4423c-176">A disk can be masked by the hardware RAID subsystem, switch, SCSI RESERVE by another computer host, or software in the disk stack.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**particionamento mestre de registro de inicialização (MBR)**</span><span class="sxs-lookup"><span data-stu-id="4423c-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**master boot record partitioning (MBR)**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-178">MBR é um dos dois formatos de dados de configuração de software de nível mais baixo e é usado pelo firmware do BIOS para localizar uma imagem do sistema operacional inicializável.</span><span class="sxs-lookup"><span data-stu-id="4423c-178">MBR is one of two lowest level software configuration data formats, and is used by BIOS firmware to locate a bootable operating system image.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**associado**</span><span class="sxs-lookup"><span data-stu-id="4423c-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**member**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-180">Uma coleção de extensões de disco concatenadas contidas em um ou mais discos.</span><span class="sxs-lookup"><span data-stu-id="4423c-180">A collection of concatenated disk extents contained on one more disks.</span></span> <span data-ttu-id="4423c-181">Um disco pode contribuir para apenas um membro de um volume.</span><span class="sxs-lookup"><span data-stu-id="4423c-181">A disk can contribute to only one member of a volume.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**espelho**</span><span class="sxs-lookup"><span data-stu-id="4423c-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mirror**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-183">Um volume ou mapeamento de disco que mantém duas ou mais cópias de dados idênticas.</span><span class="sxs-lookup"><span data-stu-id="4423c-183">A volume or disk mapping that maintains two or more identical data copies.</span></span> <span data-ttu-id="4423c-184">O tipo de mapeamento também é chamado de nível de RAID 1.</span><span class="sxs-lookup"><span data-stu-id="4423c-184">The type of mapping is also called RAID Level 1.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**pacotes**</span><span class="sxs-lookup"><span data-stu-id="4423c-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**pack**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-186">Uma coleção de volumes lógicos e discos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="4423c-186">A collection of logical volumes and underlying disks.</span></span> <span data-ttu-id="4423c-187">Um pacote é a unidade de fechamento transitório de um volume.</span><span class="sxs-lookup"><span data-stu-id="4423c-187">A pack is the unit of transitive closure for a volume.</span></span> <span data-ttu-id="4423c-188">Os pacotes de disco dinâmico e os grupos de discos são os termos do mesmo item.</span><span class="sxs-lookup"><span data-stu-id="4423c-188">Dynamic disk packs and disk groups are terms for the same item.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**faixa de paridade**</span><span class="sxs-lookup"><span data-stu-id="4423c-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**parity stripe**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-190">Um volume ou mapeamento de disco que mantém informações de verificação de paridade, bem como dados.</span><span class="sxs-lookup"><span data-stu-id="4423c-190">A volume or disk mapping that maintains parity check information as well as data.</span></span> <span data-ttu-id="4423c-191">Cada fornecedor fornece o mapeamento exato e o esquema de proteção.</span><span class="sxs-lookup"><span data-stu-id="4423c-191">Each vendor supplies the exact mapping and protection scheme.</span></span> <span data-ttu-id="4423c-192">Inclui RAID 3, 4, 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="4423c-192">Includes RAID 3, 4, 5, and 6.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configuração parcialmente direcionada**</span><span class="sxs-lookup"><span data-stu-id="4423c-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**partially directed configuration**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-194">Uma configuração de volume ou disco que não é totalmente explícita.</span><span class="sxs-lookup"><span data-stu-id="4423c-194">A volume or disk configuration that is not fully explicit.</span></span> <span data-ttu-id="4423c-195">O tipo de associação e uma coleção de recursos de destino são especificados; o layout real não é.</span><span class="sxs-lookup"><span data-stu-id="4423c-195">The binding type and a collection of target resources are specified; the actual layout is not.</span></span> <span data-ttu-id="4423c-196">A configuração parcialmente direcionada é a configuração de volume mais comum.</span><span class="sxs-lookup"><span data-stu-id="4423c-196">Partially directed configuration is the most common volume configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**particion**</span><span class="sxs-lookup"><span data-stu-id="4423c-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**partition**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-198">Um intervalo contíguo de setores lógicos descrito por uma única entrada na estrutura MBR ou GPT.</span><span class="sxs-lookup"><span data-stu-id="4423c-198">A contiguous range of logical sectors described by a single entry in the MBR or GPT structure.</span></span> <span data-ttu-id="4423c-199">Em discos básicos, as partições correspondem diretamente aos volumes simples.</span><span class="sxs-lookup"><span data-stu-id="4423c-199">On basic disks, partitions directly correspond to simple volumes.</span></span> <span data-ttu-id="4423c-200">As estruturas de partição são compartilhadas entre o firmware da plataforma BIOS ou EFI e um sistema operacional ou outra imagem inicializável.</span><span class="sxs-lookup"><span data-stu-id="4423c-200">Partition structures are shared between the BIOS or EFI platform firmware and an operating system or other bootable image.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-201"><span id="base.path"></span><span id="BASE.PATH"></span>**Multi-Path**</span><span class="sxs-lookup"><span data-stu-id="4423c-201"><span id="base.path"></span><span id="BASE.PATH"></span>**path**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-202">O caminho de acesso de um computador para um disco ou LUN de hardware externo.</span><span class="sxs-lookup"><span data-stu-id="4423c-202">The access path from a computer to a disk or external hardware LUN.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plexos**</span><span class="sxs-lookup"><span data-stu-id="4423c-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plex**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-204">Um membro de um volume espelhado ou LUN.</span><span class="sxs-lookup"><span data-stu-id="4423c-204">One member of a mirrored volume or LUN.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-205"><span id="base.port"></span><span id="BASE.PORT"></span>**Porto**</span><span class="sxs-lookup"><span data-stu-id="4423c-205"><span id="base.port"></span><span id="BASE.PORT"></span>**port**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-206">O ponto de extremidade de um caminho em um disco.</span><span class="sxs-lookup"><span data-stu-id="4423c-206">The endpoint of a path at a disk.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**matriz redundante de discos independentes (RAID)**</span><span class="sxs-lookup"><span data-stu-id="4423c-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundant array of independent disks (RAID)**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-208">Uma coleção de técnicas para gerenciar vários discos.</span><span class="sxs-lookup"><span data-stu-id="4423c-208">A collection of techniques for managing multiple disks.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**serviço de tempo de execução**</span><span class="sxs-lookup"><span data-stu-id="4423c-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**runtime service**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-210">Um programa de software que é executado em uma base de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="4423c-210">A software program that executes on an I/O-request basis.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco simples**</span><span class="sxs-lookup"><span data-stu-id="4423c-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**simple disk**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-212">Um eixo que não está conectado a um controlador RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="4423c-212">A spindle that is not connected to a hardware RAID controller.</span></span> <span data-ttu-id="4423c-213">Consulte também apenas um monte de discos (JBOD).</span><span class="sxs-lookup"><span data-stu-id="4423c-213">See also Just a Bunch Of Disks (JBOD).</span></span>

</dd> <dt>

<span data-ttu-id="4423c-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**provedor de software**</span><span class="sxs-lookup"><span data-stu-id="4423c-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-215">Software baseado em host que expõe volumes lógicos e opera em discos.</span><span class="sxs-lookup"><span data-stu-id="4423c-215">Host-based software that exposes logical volumes and operates on disks.</span></span> <span data-ttu-id="4423c-216">Um provedor de software inclui serviços de tempo de execução de modo kernel, dados de configuração e serviços de gerenciamento de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="4423c-216">A software provider includes kernel-mode runtime services, configuration data, and user-mode management services.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**compreende**</span><span class="sxs-lookup"><span data-stu-id="4423c-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**span**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-218">Um mapeamento linear de volume ou disco de várias extensões de disco ou unidade descontínuas.</span><span class="sxs-lookup"><span data-stu-id="4423c-218">A volume or disk linear mapping of multiple discontinuous disk or drive extents.</span></span> <span data-ttu-id="4423c-219">As extensões podem estar em um ou mais eixos ou LUNs.</span><span class="sxs-lookup"><span data-stu-id="4423c-219">The extents can be on one or more spindles or LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**eixo**</span><span class="sxs-lookup"><span data-stu-id="4423c-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**spindle**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-221">Uma unidade física de armazenamento em disco.</span><span class="sxs-lookup"><span data-stu-id="4423c-221">A physical unit of disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**empilhamento**</span><span class="sxs-lookup"><span data-stu-id="4423c-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**stacking**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-223">O ato de construir um volume ou LUN executando mais de uma operação de mapeamento de bloco lógico.</span><span class="sxs-lookup"><span data-stu-id="4423c-223">The act of constructing a volume or LUN by performing more than one logical block mapping operation.</span></span> <span data-ttu-id="4423c-224">Um exemplo é um volume distribuído espelhado.</span><span class="sxs-lookup"><span data-stu-id="4423c-224">An example is a mirrored striped volume.</span></span> <span data-ttu-id="4423c-225">A pilha mais comum ocorre quando o RAID de software é usado em LUNs construídos pelo RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="4423c-225">The most common stacking occurs when software RAID is used across LUNs constructed by hardware RAID.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Stripe**</span><span class="sxs-lookup"><span data-stu-id="4423c-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-227">Um volume ou mapeamento de disco que intercala extensões contíguas em vários volumes, discos ou unidades.</span><span class="sxs-lookup"><span data-stu-id="4423c-227">A volume or disk mapping that interleaves contiguous extents across multiple volumes, disks, or drives.</span></span> <span data-ttu-id="4423c-228">Esse mapeamento também é chamado de RAID 0.</span><span class="sxs-lookup"><span data-stu-id="4423c-228">This mapping is also called RAID 0.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**Estado**</span><span class="sxs-lookup"><span data-stu-id="4423c-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**status**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-230">A disponibilidade atual de um volume, disco ou unidade.</span><span class="sxs-lookup"><span data-stu-id="4423c-230">The current availability of a volume, disk, or drive.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsistema**</span><span class="sxs-lookup"><span data-stu-id="4423c-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsystem**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-232">A instanciação do software do provedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="4423c-232">The instantiation of hardware-provider software.</span></span> <span data-ttu-id="4423c-233">Um subsistema contém pelo menos um controlador e uma unidade.</span><span class="sxs-lookup"><span data-stu-id="4423c-233">A subsystem contains at least one controller and one drive.</span></span> <span data-ttu-id="4423c-234">Se o subsistema for externo ao computador, um ou mais caminhos de rede conectarão o subsistema ao computador.</span><span class="sxs-lookup"><span data-stu-id="4423c-234">If the subsystem is external to the computer, one or more network paths connect the subsystem to the computer.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**Estado de transição**</span><span class="sxs-lookup"><span data-stu-id="4423c-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**transition state**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-236">Status do mapeamento lógico para físico que está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="4423c-236">Status of the logical to physical mapping that is undergoing change.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco não inicializado**</span><span class="sxs-lookup"><span data-stu-id="4423c-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**uninitialized disk**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-238">Um disco que não é um membro de um pacote.</span><span class="sxs-lookup"><span data-stu-id="4423c-238">A disk that is not a member of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco não mascarado**</span><span class="sxs-lookup"><span data-stu-id="4423c-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmasked disk**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-240">Um disco que é visível para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4423c-240">A disk that is visible to the operating system.</span></span> <span data-ttu-id="4423c-241">O conteúdo de um disco não mascarado é visível para gerenciadores de volume de software, sistemas de arquivos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4423c-241">The contents of an unmasked disk are visible to software volume managers, file systems, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="4423c-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span><span class="sxs-lookup"><span data-stu-id="4423c-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="4423c-243">Várias extensões de disco associadas a um intervalo praticamente contíguo de blocos lógicos.</span><span class="sxs-lookup"><span data-stu-id="4423c-243">A number of disk extents bound into a virtually contiguous range of logical blocks.</span></span> <span data-ttu-id="4423c-244">Um volume pode ser acessado por meio de uma letra de unidade, uma pasta montada ou um caminho de GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="4423c-244">A volume can be accessed through a drive letter, a mounted folder, or a volume GUID path.</span></span>

</dd> </dl>

 

 
