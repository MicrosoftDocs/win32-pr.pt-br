---
description: Essas classes WMI são declaradas em CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Provedor WMI CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500814"
---
# <a name="cim-wmi-provider"></a><span data-ttu-id="84916-103">Provedor WMI CIM</span><span class="sxs-lookup"><span data-stu-id="84916-103">CIM WMI Provider</span></span>

<span data-ttu-id="84916-104">Essas classes WMI são declaradas em CimWin32. mof.</span><span class="sxs-lookup"><span data-stu-id="84916-104">These WMI classes are declared in CimWin32.mof.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84916-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="84916-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="84916-106">**Ação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-106">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dd>

<span data-ttu-id="84916-107">Uma classe de [**\_ ação CIM**](cim-action.md) é uma operação que faz parte de um processo para criar um elemento de software em seu estado seguinte ou para eliminar o elemento de software no estado atual.</span><span class="sxs-lookup"><span data-stu-id="84916-107">A [**CIM\_Action**](cim-action.md) class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-108">**\_ACTIONSEQUENCE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-108">**CIM\_ActionSequence**</span></span>](cim-actionsequence.md)
</dt> <dd>

<span data-ttu-id="84916-109">A associação [**CIM \_ ActionSequence**](cim-actionsequence.md) define uma série de operações que fazem a transição do elemento software (referenciado pela Associação [**\_ SoftwareElementActions do CIM**](cim-softwareelementactions.md) ) para seu próximo estado ou remove o elemento software de seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="84916-109">The [**CIM\_ActionSequence**](cim-actionsequence.md) association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-110">**\_ACTSASSPARE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-110">**CIM\_ActsAsSpare**</span></span>](cim-actsasspare.md)
</dt> <dd>

<span data-ttu-id="84916-111">A associação [**CIM \_ ActsAsSpare**](cim-actsasspare.md) indica quais elementos podem ser sobressalentes ou substituir outros elementos agregados.</span><span class="sxs-lookup"><span data-stu-id="84916-111">The [**CIM\_ActsAsSpare**](cim-actsasspare.md) association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="84916-112">Um sobressalente pode operar no modo "hot-standby", conforme especificado de acordo com o elemento.</span><span class="sxs-lookup"><span data-stu-id="84916-112">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-113">**\_ADJACENTSLOTS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-113">**CIM\_AdjacentSlots**</span></span>](cim-adjacentslots.md)
</dt> <dd>

<span data-ttu-id="84916-114">A associação [**CIM \_ AdjacentSlots**](cim-adjacentslots.md) descreve o layout dos slots em uma placa de adaptador ou placa de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="84916-114">The [**CIM\_AdjacentSlots**](cim-adjacentslots.md) association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="84916-115">Informações, como a distância entre os slots e se elas são "compartilhadas" (se uma for populada, o outro slot não poderá ser usado), será transmitido como propriedades de associação.</span><span class="sxs-lookup"><span data-stu-id="84916-115">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-116">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-116">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> <dd>

<span data-ttu-id="84916-117">A classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) fornece informações resumidas sobre blocos lógicos endereçáveis, que estão no mesmo grupo de redundância de armazenamento e localizados na mesma mídia física.</span><span class="sxs-lookup"><span data-stu-id="84916-117">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-118">**\_AGGREGATEPSEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-118">**CIM\_AggregatePSExtent**</span></span>](cim-aggregatepsextent.md)
</dt> <dd>

<span data-ttu-id="84916-119">A classe [**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) define o número de blocos lógicos endereçáveis em um único dispositivo de armazenamento, excluindo blocos lógicos mapeados como dados de verificação.</span><span class="sxs-lookup"><span data-stu-id="84916-119">The [**CIM\_AggregatePSExtent**](cim-aggregatepsextent.md) class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="84916-120">Se os conjuntos de volumes forem definidos, os blocos lógicos estarão contidos em um único conjunto de volumes.</span><span class="sxs-lookup"><span data-stu-id="84916-120">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="84916-121">Esse é um agrupamento alternativo para [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md), quando apenas informações resumidas são necessárias ou quando a configuração automática é usada.</span><span class="sxs-lookup"><span data-stu-id="84916-121">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-122">**\_AGGREGATEREDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-122">**CIM\_AggregateRedundancyComponent**</span></span>](cim-aggregateredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="84916-123">A classe [**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) descreve a extensão física agregada em um grupo de redundância de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84916-123">The [**CIM\_AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) class describes the aggregate physical extent in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-124">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-124">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> <dd>

<span data-ttu-id="84916-125">A classe [**CIM \_ AlarmDevice**](cim-alarmdevice.md) é um dispositivo de alarme que emite indicações audíveis ou visíveis relacionadas a uma situação de problema.</span><span class="sxs-lookup"><span data-stu-id="84916-125">The [**CIM\_AlarmDevice**](cim-alarmdevice.md) class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-126">**\_ALLOCATEDRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-126">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dd>

<span data-ttu-id="84916-127">A classe [**CIM \_ AllocatedResource**](cim-allocatedresource.md) representa uma associação entre dispositivos lógicos e recursos do sistema e indica que o recurso está atribuído ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84916-127">The [**CIM\_AllocatedResource**](cim-allocatedresource.md) class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-128">**\_APPLICATIONSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-128">**CIM\_ApplicationSystem**</span></span>](cim-applicationsystem.md)
</dt> <dd>

<span data-ttu-id="84916-129">A classe [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) representa um sistema de aplicativo ou de software que dá suporte a uma função comercial específica que pode ser gerenciada como uma unidade independente.</span><span class="sxs-lookup"><span data-stu-id="84916-129">The [**CIM\_ApplicationSystem**](cim-applicationsystem.md) class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="84916-130">Esse sistema pode ser decomposto em seus componentes funcionais usando a classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-130">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="84916-131">Os recursos de software para um determinado aplicativo ou sistema de software estão localizados usando a associação [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-131">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-132">**\_APPLICATIONSYSTEMSOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-132">**CIM\_ApplicationSystemSoftwareFeature**</span></span>](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="84916-133">A classe [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) representa uma associação que identifica os recursos de software que compõem um sistema de aplicativos específico.</span><span class="sxs-lookup"><span data-stu-id="84916-133">The [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="84916-134">Os recursos de software podem ser incluídos em produtos diferentes.</span><span class="sxs-lookup"><span data-stu-id="84916-134">The software features can be included in different products.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-135">**\_ASSOCIATEDALARM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-135">**CIM\_AssociatedAlarm**</span></span>](cim-associatedalarm.md)
</dt> <dd>

<span data-ttu-id="84916-136">A dependência do [**CIM \_ AssociatedAlarm**](cim-associatedalarm.md) associa um alarme a um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84916-136">The [**CIM\_AssociatedAlarm**](cim-associatedalarm.md) dependency associates an alarm with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-137">**\_ASSOCIATEDBATTERY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-137">**CIM\_AssociatedBattery**</span></span>](cim-associatedbattery.md)
</dt> <dd>

<span data-ttu-id="84916-138">A dependência do [**CIM \_ AssociatedBattery**](cim-associatedbattery.md) associa uma bateria a um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84916-138">The [**CIM\_AssociatedBattery**](cim-associatedbattery.md) dependency associates a battery with a logical device.</span></span> <span data-ttu-id="84916-139">Use essa associação para modelar baterias individuais que compõem uma fonte de alimentação ininterrupta (UPS).</span><span class="sxs-lookup"><span data-stu-id="84916-139">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-140">**\_ASSOCIATEDCOOLING CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-140">**CIM\_AssociatedCooling**</span></span>](cim-associatedcooling.md)
</dt> <dd>

<span data-ttu-id="84916-141">A associação [**CIM \_ AssociatedCooling**](cim-associatedcooling.md) indica quando ventiladores ou outros dispositivos de resfriamento são específicos para um dispositivo (em vez de fornecer resfriamento de compartimento ou de gabinete).</span><span class="sxs-lookup"><span data-stu-id="84916-141">The [**CIM\_AssociatedCooling**](cim-associatedcooling.md) association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-142">**\_ASSOCIATEDMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-142">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> <dd>

<span data-ttu-id="84916-143">A classe [**CIM \_ AssociateMemory**](cim-associatedmemory.md) associa a memória instalada ou associada, como memória de cache com um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84916-143">The [**CIM\_AssociateMemory**](cim-associatedmemory.md) class associates installed or associated memory, such as cache memory with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-144">**\_ASSOCIATEDPROCESSORMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-144">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dd>

<span data-ttu-id="84916-145">A classe [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md) associa o processador e a memória do sistema ou o cache de um processador.</span><span class="sxs-lookup"><span data-stu-id="84916-145">The [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md) class associates the processor and system memory, or a processor's cache.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-146">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-146">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> <dd>

<span data-ttu-id="84916-147">A classe [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) associa um sensor instalado a um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84916-147">The [**CIM\_AssociatedSensor**](cim-associatedsensor.md) class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="84916-148">O sensor mede as propriedades de entrada e saída críticas e pode ser incluído no dispositivo ou instalado no próximo.</span><span class="sxs-lookup"><span data-stu-id="84916-148">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-149">**\_ASSOCIATEDSUPPLYCURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-149">**CIM\_AssociatedSupplyCurrentSensor**</span></span>](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

<span data-ttu-id="84916-150">A classe [**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) associa uma fonte de energia a um sensor atual (amperagem) que monitora sua frequência de entrada.</span><span class="sxs-lookup"><span data-stu-id="84916-150">The [**CIM\_AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-151">**\_ASSOCIATEDSUPPLYVOLTAGESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-151">**CIM\_AssociatedSupplyVoltageSensor**</span></span>](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

<span data-ttu-id="84916-152">Associa uma fonte de energia a um sensor de tensão que monitora sua tensão de entrada.</span><span class="sxs-lookup"><span data-stu-id="84916-152">Associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-153">**\_Baseado em CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-153">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> <dd>

<span data-ttu-id="84916-154">A [**classe \_ com base em CIM**](cim-basedon.md) representa uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="84916-154">The [**CIM\_BasedOn**](cim-basedon.md) class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="84916-155">Por exemplo, as extensões físicas incluem extensões de espaço protegido.</span><span class="sxs-lookup"><span data-stu-id="84916-155">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="84916-156">Portanto, os conjuntos de volumes são montados de uma ou mais extensões de espaço físico ou protegido.</span><span class="sxs-lookup"><span data-stu-id="84916-156">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="84916-157">A memória de cache pode ser definida de forma independente e realizada em um elemento físico, ou pode ser baseada em extensões de armazenamento voláteis ou não voláteis.</span><span class="sxs-lookup"><span data-stu-id="84916-157">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-158">**\_Bateria CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-158">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dd>

<span data-ttu-id="84916-159">A classe de [**\_ bateria CIM**](cim-battery.md) representa os recursos e o gerenciamento do dispositivo lógico da bateria.</span><span class="sxs-lookup"><span data-stu-id="84916-159">The [**CIM\_Battery**](cim-battery.md) class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="84916-160">Essa classe se aplica a baterias em sistemas de laptop e outras baterias internas e externas.</span><span class="sxs-lookup"><span data-stu-id="84916-160">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-161">**\_BINARYSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-161">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> <dd>

<span data-ttu-id="84916-162">A classe [**CIM \_ BinarySensor**](cim-binarysensor.md) fornece uma saída booliana.</span><span class="sxs-lookup"><span data-stu-id="84916-162">The [**CIM\_BinarySensor**](cim-binarysensor.md) class provides a Boolean output.</span></span> <span data-ttu-id="84916-163">As propriedades **CurrentState** e **PossibleStates** foram adicionadas para o sensor, tornando a **subclasse \_ BinarySensor CIM** não mais necessária, embora seja mantida para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="84916-163">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="84916-164">Um sensor binário pode ser criado instanciando-se um sensor com dois Estados possíveis.</span><span class="sxs-lookup"><span data-stu-id="84916-164">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-165">**CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="84916-165">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dd>

<span data-ttu-id="84916-166">A classe [**CIM \_ bioselement**](cim-bioselement.md) representa o software de nível baixo que é carregado no armazenamento não volátil e usado para iniciar e configurar um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="84916-166">The [**CIM\_BIOSElement**](cim-bioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-167">**\_BIOSFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-167">**CIM\_BIOSFeature**</span></span>](cim-biosfeature.md)
</dt> <dd>

<span data-ttu-id="84916-168">representa os recursos do software de nível baixo que é usado para iniciar e configurar um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="84916-168">represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-169">**\_BIOSFEATUREBIOSELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-169">**CIM\_BIOSFeatureBIOSElements**</span></span>](cim-biosfeaturebioselements.md)
</dt> <dd>

<span data-ttu-id="84916-170">A classe [**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) associa um recurso do BIOS e seus elementos do BIOS agregados.</span><span class="sxs-lookup"><span data-stu-id="84916-170">The [**CIM\_BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) class associates a BIOS feature and its aggregated BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-171">**\_BIOSLOADEDINNV CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-171">**CIM\_BIOSLoadedInNV**</span></span>](cim-biosloadedinnv.md)
</dt> <dd>

<span data-ttu-id="84916-172">A classe [**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) associa um elemento BIOS e o armazenamento não volátil no qual ele é carregado.</span><span class="sxs-lookup"><span data-stu-id="84916-172">The [**CIM\_BIOSLoadedInNV**](cim-biosloadedinnv.md) class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-173">**\_BOOTOSFROMFS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-173">**CIM\_BootOSFromFS**</span></span>](cim-bootosfromfs.md)
</dt> <dd>

<span data-ttu-id="84916-174">A classe [**CIM \_ BootOSFromFS**](cim-bootosfromfs.md) associa o sistema operacional e os sistemas de arquivos dos quais o sistema operacional é carregado.</span><span class="sxs-lookup"><span data-stu-id="84916-174">The [**CIM\_BootOSFromFS**](cim-bootosfromfs.md) class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="84916-175">A associação é muitos-para-muitos; um sistema operacional distribuído pode depender de vários sistemas de arquivos para serem carregados de forma correta e completa.</span><span class="sxs-lookup"><span data-stu-id="84916-175">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-176">**\_BOOTSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-176">**CIM\_BootSAP**</span></span>](cim-bootsap.md)
</dt> <dd>

<span data-ttu-id="84916-177">A classe [**CIM \_ BootSAP**](cim-bootsap.md) representa os pontos de acesso de um serviço de inicialização.</span><span class="sxs-lookup"><span data-stu-id="84916-177">The [**CIM\_BootSAP**](cim-bootsap.md) class represents the access points of a boot service.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-178">**\_DS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-178">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> <dd>

<span data-ttu-id="84916-179">A classe [**CIM \_ DS**](cim-bootservice.md) representa a funcionalidade fornecida por um dispositivo ou software, ou por uma rede, para carregar um sistema operacional em um sistema de computador unitário.</span><span class="sxs-lookup"><span data-stu-id="84916-179">The [**CIM\_BootService**](cim-bootservice.md) class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-180">**\_BOOTSERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-180">**CIM\_BootServiceAccessBySAP**</span></span>](cim-bootserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="84916-181">A classe [**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) associa um serviço de inicialização e seus pontos de acesso.</span><span class="sxs-lookup"><span data-stu-id="84916-181">The [**CIM\_BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) class associates a boot service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-182">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-182">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dd>

<span data-ttu-id="84916-183">A classe [**CIM \_ CacheMemory**](cim-cachememory.md) define os recursos e o gerenciamento da memória cache.</span><span class="sxs-lookup"><span data-stu-id="84916-183">The [**CIM\_CacheMemory**](cim-cachememory.md) class defines the capabilities and management of cache memory.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-184">**\_Placa CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-184">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dd>

<span data-ttu-id="84916-185">A classe de [**\_ placa CIM**](cim-card.md) representa um tipo de contêiner físico que pode ser conectado a outro cartão ou placa de hospedagem, ou é uma placa de hospedagem/placa-mãe em um chassi.</span><span class="sxs-lookup"><span data-stu-id="84916-185">The [**CIM\_Card**](cim-card.md) class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="84916-186">Essa classe inclui qualquer pacote que seja capaz de carregar sinais e fornecer um ponto de montagem para componentes físicos, como chips ou outros pacotes físicos, como outros cartões.</span><span class="sxs-lookup"><span data-stu-id="84916-186">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-187">**\_CARDINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-187">**CIM\_CardInSlot**</span></span>](cim-cardinslot.md)
</dt> <dd>

<span data-ttu-id="84916-188">A classe [**CIM \_ CardInSlot**](cim-cardinslot.md) associa uma placa de adaptador ao contêiner no qual ela é inserida.</span><span class="sxs-lookup"><span data-stu-id="84916-188">The [**CIM\_CardInSlot**](cim-cardinslot.md) class associates an adapter card with the container into which it is inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-189">**\_CARDONCARD CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-189">**CIM\_CardOnCard**</span></span>](cim-cardoncard.md)
</dt> <dd>

<span data-ttu-id="84916-190">A associação [**CIM \_ CardOnCard**](cim-cardoncard.md) descreve as relações sobre os cartões que podem ser conectados a placas-mãe/placas, daughtercards de um adaptador ou cartões que dão suporte a módulos especiais semelhantes a cartões.</span><span class="sxs-lookup"><span data-stu-id="84916-190">The [**CIM\_CardOnCard**](cim-cardoncard.md) association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-191">**\_CDROMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-191">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dd>

<span data-ttu-id="84916-192">A classe [**CIM \_ CDROMDrive**](cim-cdromdrive.md) representa uma unidade de CD-ROM no computador.</span><span class="sxs-lookup"><span data-stu-id="84916-192">The [**CIM\_CDROMDrive**](cim-cdromdrive.md) class represents a CD-ROM drive on the computer.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-193">**\_Chassi CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-193">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dd>

<span data-ttu-id="84916-194">A classe de [**\_ chassi CIM**](cim-chassis.md) representa os elementos físicos que incluem outros elementos e fornece funcionalidade definíveis, como um desktop, nó de processamento, UPS, armazenamento em disco ou fita ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="84916-194">The [**CIM\_Chassis**](cim-chassis.md) class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-195">**\_CHASSISINRACK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-195">**CIM\_ChassisInRack**</span></span>](cim-chassisinrack.md)
</dt> <dd>

<span data-ttu-id="84916-196">A associação de [**\_ ChassisInRack do CIM**](cim-chassisinrack.md) representa a relação de "contenção" entre um rack e um chassi que ele contém.</span><span class="sxs-lookup"><span data-stu-id="84916-196">The [**CIM\_ChassisInRack**](cim-chassisinrack.md) association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-197">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-197">**CIM\_Check**</span></span>](cim-check.md)
</dt> <dd>

<span data-ttu-id="84916-198">A classe de [**\_ verificação CIM**](cim-check.md) representa uma condição ou característica que deve ser verdadeira em um ambiente definido ou com escopo por uma instância de uma classe [**de \_ sistema CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-198">The [**CIM\_Check**](cim-check.md) class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="84916-199">As verificações associadas a um determinado elemento de software são organizadas em um dos dois grupos usando a propriedade **Phase** da Associação [**\_ SoftwareElementChecks do CIM**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-199">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-200">**\_Chip CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-200">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> <dd>

<span data-ttu-id="84916-201">A classe de [**\_ chip CIM**](cim-chip.md) representa o tipo de hardware de circuito integrado, incluindo ASICs, processadores, chips de memória e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="84916-201">The [**CIM\_Chip**](cim-chip.md) class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-202">**\_CLUSTERINGSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-202">**CIM\_ClusteringSAP**</span></span>](cim-clusteringsap.md)
</dt> <dd>

<span data-ttu-id="84916-203">A classe [**CIM \_ ClusteringSAP**](cim-clusteringsap.md) representa os pontos de acesso de um serviço de clustering.</span><span class="sxs-lookup"><span data-stu-id="84916-203">The [**CIM\_ClusteringSAP**](cim-clusteringsap.md) class represents the access points of a clustering service.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-204">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-204">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> <dd>

<span data-ttu-id="84916-205">A classe [**CIM \_ ClusteringService**](cim-clusteringservice.md) representa a funcionalidade fornecida por um cluster.</span><span class="sxs-lookup"><span data-stu-id="84916-205">The [**CIM\_ClusteringService**](cim-clusteringservice.md) class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="84916-206">Por exemplo, a funcionalidade de failover pode ser modelada como um serviço de um cluster de failover.</span><span class="sxs-lookup"><span data-stu-id="84916-206">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-207">**\_CLUSTERSERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-207">**CIM\_ClusterServiceAccessBySAP**</span></span>](cim-clusterserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="84916-208">A classe [**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) representa a relação entre um serviço de clustering e seus pontos de acesso.</span><span class="sxs-lookup"><span data-stu-id="84916-208">The [**CIM\_ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) class represents the relationship between a clustering service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-209">**\_COLLECTEDCOLLECTIONS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-209">**CIM\_CollectedCollections**</span></span>](cim-collectedcollections.md)
</dt> <dd>

<span data-ttu-id="84916-210">A classe [**CIM \_ CollectedCollections**](cim-collectedcollections.md) é uma associação de agregação que representa uma coleção de elementos do sistema gerenciados (MSE) contidas em uma coleção de MSEs.</span><span class="sxs-lookup"><span data-stu-id="84916-210">The [**CIM\_CollectedCollections**](cim-collectedcollections.md) class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-211">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-211">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> <dd>

<span data-ttu-id="84916-212">A classe de associação [**CIM \_ CollectedMSEs**](cim-collectedmses.md) representa os membros do objeto GROUPING, uma classe [**CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-212">The [**CIM\_CollectedMSEs**](cim-collectedmses.md) association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-213">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="84916-213">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> <dd>

<span data-ttu-id="84916-214">O objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) permite o agrupamento de objetos [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) com a finalidade de associar definições e configurações.</span><span class="sxs-lookup"><span data-stu-id="84916-214">The [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="84916-215">É abstrato exigir mais definição e refinamento semântico em subclasses.</span><span class="sxs-lookup"><span data-stu-id="84916-215">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-216">**\_COLLECTIONOFSENSORS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-216">**CIM\_CollectionOfSensors**</span></span>](cim-collectionofsensors.md)
</dt> <dd>

<span data-ttu-id="84916-217">A associação [**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md) representa os sensores binários que compõem o sensor de multiestado.</span><span class="sxs-lookup"><span data-stu-id="84916-217">The [**CIM\_CollectionOfSensors**](cim-collectionofsensors.md) association represents the binary sensors that make up the multistate sensor.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-218">**\_COLLECTIONSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-218">**CIM\_CollectionSetting**</span></span>](cim-collectionsetting.md)
</dt> <dd>

<span data-ttu-id="84916-219">A classe [**CIM \_ CollectionSetting**](cim-collectionsetting.md) representa a associação entre um [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) e a classe de configuração definida para eles.</span><span class="sxs-lookup"><span data-stu-id="84916-219">The [**CIM\_CollectionSetting**](cim-collectionsetting.md) class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-220">**\_COMPATIBLEPRODUCT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-220">**CIM\_CompatibleProduct**</span></span>](cim-compatibleproduct.md)
</dt> <dd>

<span data-ttu-id="84916-221">A classe [**CIM \_ CompatibleProduct**](cim-compatibleproduct.md) representa uma associação entre produtos que indica se dois produtos referenciados são interoperáveis, como se eles podem ser instalados juntos ou se um pode ser o contêiner físico para o outro, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="84916-221">The [**CIM\_CompatibleProduct**](cim-compatibleproduct.md) class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-222">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-222">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dd>

<span data-ttu-id="84916-223">A associação de [**\_ componente CIM**](cim-component.md) representa as partes de uma relação entre MSEs.</span><span class="sxs-lookup"><span data-stu-id="84916-223">The [**CIM\_Component**](cim-component.md) association represents the parts of a relationship between MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-224">**\_Sistema de COMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-224">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dd>

<span data-ttu-id="84916-225">Uma classe de [**\_ sistema CIM**](cim-computersystem.md) representa uma coleção especial de instâncias do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-225">A [**CIM\_ComputerSystem**](cim-computersystem.md) class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="84916-226">Esta coleção fornece recursos do computador e serve como um ponto de agregação para associar um ou mais dos seguintes elementos: sistema de arquivos, sistema operacional, processador e memória (armazenamento volátil e não volátil).</span><span class="sxs-lookup"><span data-stu-id="84916-226">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="84916-227">Essa classe é derivada do [**\_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="84916-227">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-228">**\_COMPUTERSYSTEMDMA CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-228">**CIM\_ComputerSystemDMA**</span></span>](cim-computersystemdma.md)
</dt> <dd>

<span data-ttu-id="84916-229">A classe [**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) representa uma associação entre um sistema de computador e seus canais de DMA (acesso direto à memória) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="84916-229">The [**CIM\_ComputerSystemDMA**](cim-computersystemdma.md) class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-230">**\_COMPUTERSYSTEMIRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-230">**CIM\_ComputerSystemIRQ**</span></span>](cim-computersystemirq.md)
</dt> <dd>

<span data-ttu-id="84916-231">A classe [**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) representa uma associação entre um sistema de computador e suas IRQs (linhas de solicitação de interrupção) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="84916-231">The [**CIM\_ComputerSystemIRQ**](cim-computersystemirq.md) class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-232">**\_COMPUTERSYSTEMMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-232">**CIM\_ComputerSystemMappedIO**</span></span>](cim-computersystemmappedio.md)
</dt> <dd>

<span data-ttu-id="84916-233">A classe [**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) representa uma associação entre um sistema de computador e suas portas de e/s mapeadas de memória disponíveis.</span><span class="sxs-lookup"><span data-stu-id="84916-233">The [**CIM\_ComputerSystemMappedIO**](cim-computersystemmappedio.md) class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-234">**\_COMPUTERSYSTEMPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-234">**CIM\_ComputerSystemPackage**</span></span>](cim-computersystempackage.md)
</dt> <dd>

<span data-ttu-id="84916-235">A classe [**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) representa uma associação que define explicitamente a relação entre os sistemas de computador unitários e um ou mais pacotes físicos.</span><span class="sxs-lookup"><span data-stu-id="84916-235">The [**CIM\_ComputerSystemPackage**](cim-computersystempackage.md) class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="84916-236">A associação é semelhante à forma como os dispositivos lógicos são concretizados por elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="84916-236">The association is similar to the way that logical devices are realized by physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-237">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-237">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dd>

<span data-ttu-id="84916-238">A classe [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md) representa uma associação entre um sistema de computador e seus recursos de sistema disponíveis.</span><span class="sxs-lookup"><span data-stu-id="84916-238">The [**CIM\_ComputerSystemResource**](cim-computersystemresource.md) class represents an association between a computer system and its available system resources.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-239">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-239">**CIM\_Configuration**</span></span>](cim-configuration.md)
</dt> <dd>

<span data-ttu-id="84916-240">O objeto de [**\_ configuração CIM**](cim-configuration.md) permite o agrupamento de conjuntos de parâmetros (definidos em objetos de [**\_ configuração CIM**](cim-setting.md) ) e dependências para um ou mais elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="84916-240">The [**CIM\_Configuration**](cim-configuration.md) object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-241">**CIM \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="84916-241">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> <dd>

<span data-ttu-id="84916-242">A classe [**CIM \_ conectadoto**](cim-connectedto.md) representa uma associação que indica que dois ou mais conectores físicos estão conectados.</span><span class="sxs-lookup"><span data-stu-id="84916-242">The [**CIM\_ConnectedTo**](cim-connectedto.md) class represents an association that indicates that two or more physical connectors are connected.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-243">**\_CONNECTORONPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-243">**CIM\_ConnectorOnPackage**</span></span>](cim-connectoronpackage.md)
</dt> <dd>

<span data-ttu-id="84916-244">A classe [**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) representa uma associação que torna explícita a relação de confinamento entre conectores e pacotes.</span><span class="sxs-lookup"><span data-stu-id="84916-244">The [**CIM\_ConnectorOnPackage**](cim-connectoronpackage.md) class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="84916-245">Os pacotes físicos contêm conectores e outros elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="84916-245">Physical packages contain connectors as well as other physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-246">**\_Contêiner CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-246">**CIM\_Container**</span></span>](cim-container.md)
</dt> <dd>

<span data-ttu-id="84916-247">A classe de [**\_ contêiner CIM**](cim-container.md) representa uma associação entre um elemento físico contido e um que o contém.</span><span class="sxs-lookup"><span data-stu-id="84916-247">The [**CIM\_Container**](cim-container.md) class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="84916-248">Um objeto recipiente deve ser um pacote físico.</span><span class="sxs-lookup"><span data-stu-id="84916-248">A containing object must be a physical package.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-249">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-249">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dd>

<span data-ttu-id="84916-250">O relacionamento [**CIM \_ ControlledBy**](cim-controlledby.md) indica quais dispositivos são incluídos no comando ou acessados por meio do dispositivo lógico do controlador.</span><span class="sxs-lookup"><span data-stu-id="84916-250">The [**CIM\_ControlledBy**](cim-controlledby.md) relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-251">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-251">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dd>

<span data-ttu-id="84916-252">A classe do [**\_ controlador CIM**](cim-controller.md) é uma classe pai para agrupar dispositivos diversos relacionados ao controle.</span><span class="sxs-lookup"><span data-stu-id="84916-252">The [**CIM\_Controller**](cim-controller.md) class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="84916-253">Os exemplos de controladores são controladores SCSI, controladores USB e controladores seriais.</span><span class="sxs-lookup"><span data-stu-id="84916-253">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-254">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-254">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> <dd>

<span data-ttu-id="84916-255">A classe [**CIM \_ CoolingDevice**](cim-coolingdevice.md) representa os recursos e o gerenciamento de dispositivos de resfriamento.</span><span class="sxs-lookup"><span data-stu-id="84916-255">The [**CIM\_CoolingDevice**](cim-coolingdevice.md) class represents the capabilities and management of cooling devices.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-256">**CIM \_ CopyAction**</span><span class="sxs-lookup"><span data-stu-id="84916-256">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> <dd>

<span data-ttu-id="84916-257">A classe [**CIM \_ CopyValue**](cim-copyfileaction.md) representa a movimentação ou a cópia de arquivos de um sistema de computador para um novo local.</span><span class="sxs-lookup"><span data-stu-id="84916-257">The [**CIM\_CopyFileAction**](cim-copyfileaction.md) class represents moving or copying files from a computer system to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-258">**CIM \_ Createdirectoryaction**</span><span class="sxs-lookup"><span data-stu-id="84916-258">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="84916-259">A classe [**CIM \_ createdirectoryaction**](cim-createdirectoryaction.md) cria diretórios vazios para que os elementos de software sejam instalados localmente.</span><span class="sxs-lookup"><span data-stu-id="84916-259">The [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class creates empty directories for software elements to be installed locally.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-260">**\_CURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-260">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dd>

<span data-ttu-id="84916-261">A classe [**CIM \_ CurrentSensor**](cim-currentsensor.md) existe para compatibilidade com versões anteriores de definições de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="84916-261">The [**CIM\_CurrentSensor**](cim-currentsensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-262">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-262">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dd>

<span data-ttu-id="84916-263">A classe de [**\_ DataFile do CIM**](cim-datafile.md) representa uma coleção nomeada de dados ou código executável.</span><span class="sxs-lookup"><span data-stu-id="84916-263">The [**CIM\_DataFile**](cim-datafile.md) class represents a named collection of data or executable code.</span></span> <span data-ttu-id="84916-264">Somente as instâncias de arquivos em discos fixos locais serão retornadas</span><span class="sxs-lookup"><span data-stu-id="84916-264">Only instances of files on local fixed disks will be returned</span></span>

</dd> <dt>

[<span data-ttu-id="84916-265">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-265">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dd>

<span data-ttu-id="84916-266">A classe de [**\_ dependência CIM**](cim-dependency.md) representa uma associação que estabelece relações de dependência entre objetos.</span><span class="sxs-lookup"><span data-stu-id="84916-266">The [**CIM\_Dependency**](cim-dependency.md) class represents an association that establishes dependency relationships between objects.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-267">**\_DEPENDENCYCONTEXT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-267">**CIM\_DependencyContext**</span></span>](cim-dependencycontext.md)
</dt> <dd>

<span data-ttu-id="84916-268">O relacionamento [**CIM \_ DependencyContext**](cim-dependencycontext.md) associa uma classe de [**\_ dependência CIM**](cim-dependency.md) a um ou mais objetos de [**\_ configuração CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-268">The [**CIM\_DependencyContext**](cim-dependencycontext.md) relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="84916-269">Por exemplo, as dependências de um sistema de computador podem ser alteradas com base na rede à qual o sistema está anexado.</span><span class="sxs-lookup"><span data-stu-id="84916-269">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-270">**\_DESKTOPMONITOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-270">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dd>

<span data-ttu-id="84916-271">A classe [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) representa os recursos e o gerenciamento do dispositivo lógico do monitor de área de trabalho (CRT).</span><span class="sxs-lookup"><span data-stu-id="84916-271">The [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-272">**\_DEVICEACCESSEDBYFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-272">**CIM\_DeviceAccessedByFile**</span></span>](cim-deviceaccessedbyfile.md)
</dt> <dd>

<span data-ttu-id="84916-273">A classe de associação [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) especifica o dispositivo lógico acessado usando a classe de [**\_ dispositivo CIM**](cim-devicefile.md) referenciada.</span><span class="sxs-lookup"><span data-stu-id="84916-273">The [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-274">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-274">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> <dd>

<span data-ttu-id="84916-275">A classe de associação [**CIM \_ DeviceConnection**](cim-deviceconnection.md) representa dois ou mais dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="84916-275">The [**CIM\_DeviceConnection**](cim-deviceconnection.md) association class represents two or more connected devices.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-276">**\_DEVICEERRORCOUNTS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-276">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> <dd>

<span data-ttu-id="84916-277">A classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) é uma classe estatística que contém contadores relacionados a erros para um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84916-277">The [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="84916-278">Os tipos de erros são definidos por CCITT (REC X. 733) e ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="84916-278">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-279">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-279">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> <dd>

<span data-ttu-id="84916-280">A classe [**CIM \_ devicefile**](cim-devicefile.md) representa um tipo de arquivo lógico, que representa um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84916-280">The [**CIM\_DeviceFile**](cim-devicefile.md) class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="84916-281">Essa convenção é útil para sistemas operacionais que gerenciam dispositivos usando um modelo de e/s de fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="84916-281">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="84916-282">O dispositivo lógico associado a esse arquivo é especificado usando a relação de [**\_ DeviceAccessedByFile do CIM**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-282">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-283">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-283">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dd>

<span data-ttu-id="84916-284">A classe [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado.</span><span class="sxs-lookup"><span data-stu-id="84916-284">The [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="84916-285">Quando muitos dispositivos lógicos são associados a um SAP, os elementos operam em conjunto para fornecer o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="84916-285">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="84916-286">Se houver implementações diferentes de um SAP, cada implementação resultará em instanciações individuais do objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="84916-286">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-287">**\_DEVICESERVICEIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-287">**CIM\_DeviceServiceImplementation**</span></span>](cim-deviceserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="84916-288">A classe [**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) representa uma associação entre um serviço e como ele é implementado.</span><span class="sxs-lookup"><span data-stu-id="84916-288">The [**CIM\_DeviceServiceImplementation**](cim-deviceserviceimplementation.md) class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="84916-289">Quando vários dispositivos são associados a um serviço, os elementos operam em conjunto para fornecer o serviço.</span><span class="sxs-lookup"><span data-stu-id="84916-289">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="84916-290">Se houver implementações diferentes de um serviço, cada implementação resultará em instanciações individuais do objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="84916-290">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-291">**\_DEVICESOFTWARE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-291">**CIM\_DeviceSoftware**</span></span>](cim-devicesoftware.md)
</dt> <dd>

<span data-ttu-id="84916-292">O relacionamento [**CIM \_ DeviceSoftware**](cim-devicesoftware.md) identifica o software associado a um dispositivo, como drivers, configuração ou software de aplicativo ou firmware.</span><span class="sxs-lookup"><span data-stu-id="84916-292">The [**CIM\_DeviceSoftware**](cim-devicesoftware.md) relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-293">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-293">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dd>

<span data-ttu-id="84916-294">A classe de [**\_ diretório CIM**](cim-directory.md) representa um tipo de arquivo que agrupa logicamente os arquivos de dados que ele contém e fornece informações de caminho para os arquivos agrupados.</span><span class="sxs-lookup"><span data-stu-id="84916-294">The [**CIM\_Directory**](cim-directory.md) class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-295">**\_Directoryaction do CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> <dd>

<span data-ttu-id="84916-296">A classe abstrata do [**CIM \_ directoryaction**](cim-directoryaction.md) gerencia diretórios.</span><span class="sxs-lookup"><span data-stu-id="84916-296">The [**CIM\_DirectoryAction**](cim-directoryaction.md) abstract class manages directories.</span></span> <span data-ttu-id="84916-297">A criação de diretório é tratada pela classe [**CIM \_ createdirectoryaction**](cim-createdirectoryaction.md) e a remoção de diretório é tratada pela classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-297">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-298">**\_DIRECTORYCONTAINSFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-298">**CIM\_DirectoryContainsFile**</span></span>](cim-directorycontainsfile.md)
</dt> <dd>

<span data-ttu-id="84916-299">A classe [**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) representa uma associação entre um diretório e os arquivos contidos nesse diretório.</span><span class="sxs-lookup"><span data-stu-id="84916-299">The [**CIM\_DirectoryContainsFile**](cim-directorycontainsfile.md) class represents an association between a directory and files contained within that directory.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-300">**\_DIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-300">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> <dd>

<span data-ttu-id="84916-301">A classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) captura a estrutura de diretório principal de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="84916-301">The [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class captures the major directory structure of a software element.</span></span> <span data-ttu-id="84916-302">Essa classe é usada para organizar os arquivos de um elemento de software em unidades gerenciáveis que podem ser realocadas em um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="84916-302">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-303">**\_DIRECTORYSPECIFICATIONFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-303">**CIM\_DirectorySpecificationFile**</span></span>](cim-directoryspecificationfile.md)
</dt> <dd>

<span data-ttu-id="84916-304">A associação [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) representa o diretório que contém o arquivo especificado referenciando a classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-304">The [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-305">**\_DISCRETESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-305">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> <dd>

<span data-ttu-id="84916-306">A classe [**CIM \_ DiscreteSensor**](cim-discretesensor.md) tem um conjunto de valores de cadeia de caracteres legais que ele pode relatar.</span><span class="sxs-lookup"><span data-stu-id="84916-306">The [**CIM\_DiscreteSensor**](cim-discretesensor.md) class has a set of legal string values that it can report.</span></span> <span data-ttu-id="84916-307">Os valores são enumerados na propriedade **PossibleValues** do sensor.</span><span class="sxs-lookup"><span data-stu-id="84916-307">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="84916-308">Um sensor discreto sempre tem uma leitura atual que corresponde a um dos valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="84916-308">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-309">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-309">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dd>

<span data-ttu-id="84916-310">A classe [**CIM \_ DiskDrive**](cim-diskdrive.md) representa uma unidade de disco físico, como visto pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="84916-310">The [**CIM\_DiskDrive**](cim-diskdrive.md) class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="84916-311">Os recursos da unidade de disco correspondem às características lógica e de gerenciamento da unidade e, em alguns casos, podem não refletir as características físicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84916-311">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="84916-312">Uma interface para uma unidade física é um membro dessa classe.</span><span class="sxs-lookup"><span data-stu-id="84916-312">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="84916-313">No entanto, um objeto baseado em outro dispositivo lógico não é membro dessa classe.</span><span class="sxs-lookup"><span data-stu-id="84916-313">However, an object based on another logical device is not a member of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-314">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-314">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dd>

<span data-ttu-id="84916-315">A classe [**CIM \_ DisketteDrive**](cim-diskettedrive.md) representa os recursos e o gerenciamento de uma unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="84916-315">The [**CIM\_DisketteDrive**](cim-diskettedrive.md) class represents the capabilities and management of a diskette drive.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-316">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-316">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dd>

<span data-ttu-id="84916-317">A classe [**CIM \_ DiskPartition**](cim-diskpartition.md) representa um intervalo contíguo de blocos lógicos que é identificável pelo sistema operacional por meio dos campos tipo e subtipo da partição.</span><span class="sxs-lookup"><span data-stu-id="84916-317">The [**CIM\_DiskPartition**](cim-diskpartition.md) class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="84916-318">As partições de disco devem ser realizadas diretamente pela mídia física (indicada pela Associação de [**\_ RealizesDiskPartition do CIM**](cim-realizesdiskpartition.md) ) ou criados em volumes de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84916-318">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-319">**\_DISKSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-319">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> <dd>

<span data-ttu-id="84916-320">A classe [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) verifica a quantidade de espaço em disco disponível do sistema e especifica-o na propriedade **AvailableDiskSpace** .</span><span class="sxs-lookup"><span data-stu-id="84916-320">The [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="84916-321">Os detalhes são comparados com o valor na propriedade **AvailableSpace** do objeto de [**sistema de \_ arquivos CIM**](cim-filesystem.md) que está associado ao objeto [**CIM \_ ComputerSystem**](cim-computersystem.md) , que descreve o ambiente do sistema.</span><span class="sxs-lookup"><span data-stu-id="84916-321">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="84916-322">Quando o valor da propriedade **AvailableSpace** for maior ou igual ao valor especificado na propriedade **AvailableDiskSpace** , a condição será satisfeita.</span><span class="sxs-lookup"><span data-stu-id="84916-322">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-323">**Exibição de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-323">**CIM\_Display**</span></span>](cim-display.md)
</dt> <dd>

<span data-ttu-id="84916-324">A classe de [**\_ vídeo CIM**](cim-display.md) é uma classe pai para agrupar dispositivos de vídeo diversos.</span><span class="sxs-lookup"><span data-stu-id="84916-324">The [**CIM\_Display**](cim-display.md) class is a parent class for grouping miscellaneous display devices.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-325">**DMA de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-325">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dd>

<span data-ttu-id="84916-326">A classe [**CIM \_ DMA**](cim-dma.md) representa o DMA (acesso direto à memória) da arquitetura do computador.</span><span class="sxs-lookup"><span data-stu-id="84916-326">The [**CIM\_DMA**](cim-dma.md) class represents computer architecture direct memory access (DMA).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-327">**CIM \_ encaixado**</span><span class="sxs-lookup"><span data-stu-id="84916-327">**CIM\_Docked**</span></span>](cim-docked.md)
</dt> <dd>

<span data-ttu-id="84916-328">A associação de [**\_ encaixe CIM**](cim-docked.md) representa a relação entre dois chassis.</span><span class="sxs-lookup"><span data-stu-id="84916-328">The [**CIM\_Docked**](cim-docked.md) association represents the relationship between two chassis.</span></span> <span data-ttu-id="84916-329">Por exemplo, um laptop (um tipo de chassi) pode ser encaixado em uma estação de encaixe (outro tipo de chassi).</span><span class="sxs-lookup"><span data-stu-id="84916-329">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="84916-330">Essa relação típica é descrita explicitamente.</span><span class="sxs-lookup"><span data-stu-id="84916-330">This typical relationship is explicitly described.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-331">**\_ELEMENTCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-331">**CIM\_ElementCapacity**</span></span>](cim-elementcapacity.md)
</dt> <dd>

<span data-ttu-id="84916-332">A classe [**CIM \_ ElementCapacity**](cim-elementcapacity.md) associa um objeto [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a um ou mais elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="84916-332">The [**CIM\_ElementCapacity**](cim-elementcapacity.md) class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="84916-333">Ele associa uma descrição dos requisitos mínimos e máximos de hardware (ou recursos) aos elementos físicos descritos.</span><span class="sxs-lookup"><span data-stu-id="84916-333">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-334">**\_ELEMENTCONFIGURATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-334">**CIM\_ElementConfiguration**</span></span>](cim-elementconfiguration.md)
</dt> <dd>

<span data-ttu-id="84916-335">A associação [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) relaciona um objeto de [**\_ configuração CIM**](cim-configuration.md) a um ou mais elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="84916-335">The [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="84916-336">O objeto de **\_ configuração CIM** representa um determinado comportamento ou um estado funcional desejado para o [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associado.</span><span class="sxs-lookup"><span data-stu-id="84916-336">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-337">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-337">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="84916-338">A classe [**CIM \_ ElementSetting**](cim-elementsetting.md) representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.</span><span class="sxs-lookup"><span data-stu-id="84916-338">The [**CIM\_ElementSetting**](cim-elementsetting.md) class represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-339">**\_ELEMENTSLINKED CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-339">**CIM\_ElementsLinked**</span></span>](cim-elementslinked.md)
</dt> <dd>

<span data-ttu-id="84916-340">A associação [**CIM \_ ElementsLinked**](cim-elementslinked.md) representa os elementos físicos que são cabeados juntos por um link físico.</span><span class="sxs-lookup"><span data-stu-id="84916-340">The [**CIM\_ElementsLinked**](cim-elementslinked.md) association represents physical elements that are cabled together by a physical link.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-341">**\_ERRORCOUNTERSFORDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-341">**CIM\_ErrorCountersForDevice**</span></span>](cim-errorcountersfordevice.md)
</dt> <dd>

<span data-ttu-id="84916-342">A classe [**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) associa a classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) ao dispositivo lógico ao qual se aplica.</span><span class="sxs-lookup"><span data-stu-id="84916-342">The [**CIM\_ErrorCountersForDevice**](cim-errorcountersfordevice.md) class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-343">**\_EXECUTEPROGRAM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-343">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> <dd>

<span data-ttu-id="84916-344">A classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) representa os arquivos que podem ser executados no sistema onde o elemento de software está instalado.</span><span class="sxs-lookup"><span data-stu-id="84916-344">The [**CIM\_ExecuteProgram**](cim-executeprogram.md) class represents files that can be executed on the system where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-345">**Exportação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-345">**CIM\_Export**</span></span>](cim-export.md)
</dt> <dd>

<span data-ttu-id="84916-346">A classe de [**\_ exportação CIM**](cim-export.md) representa uma associação entre um sistema de arquivos local e seus diretórios, o que indica que os diretórios especificados estão disponíveis para montagem.</span><span class="sxs-lookup"><span data-stu-id="84916-346">The [**CIM\_Export**](cim-export.md) class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="84916-347">Ao exportar um sistema de arquivos inteiro, o diretório deve fazer referência ao diretório de nível superior do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="84916-347">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-348">**\_EXTRACAPACITYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-348">**CIM\_ExtraCapacityGroup**</span></span>](cim-extracapacitygroup.md)
</dt> <dd>

<span data-ttu-id="84916-349">A classe [**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) é derivada de um grupo de redundância que indica que os elementos agregados têm mais capacidade ou capacidade do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="84916-349">The [**CIM\_ExtraCapacityGroup**](cim-extracapacitygroup.md) class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="84916-350">Um exemplo desse tipo de redundância é a instalação de N + 1 fontes de alimentação ou ventiladores em um sistema.</span><span class="sxs-lookup"><span data-stu-id="84916-350">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-351">**\_Ventilador CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-351">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dd>

<span data-ttu-id="84916-352">A classe de [**\_ ventilador CIM**](cim-fan.md) representa os recursos e o gerenciamento de um dispositivo de resfriamento de ventilador.</span><span class="sxs-lookup"><span data-stu-id="84916-352">The [**CIM\_Fan**](cim-fan.md) class represents the capabilities and management of a fan cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-353">**\_Arquivo de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-353">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> <dd>

<span data-ttu-id="84916-354">A [**classe \_ fileaction do CIM**](cim-fileaction.md) permite que o autor Localize arquivos que já existem no computador de um usuário e, em seguida, mova ou copie esses arquivos para um novo local.</span><span class="sxs-lookup"><span data-stu-id="84916-354">The [**CIM\_FileAction**](cim-fileaction.md) class allows the author to locate files that already exist on a user's computer, and then move or copy those files to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-355">**Inespecificações de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-355">**CIM\_FileSpecification**</span></span>](cim-filespecification.md)
</dt> <dd>

<span data-ttu-id="84916-356">A classe [**CIM \_ fileespecífication**](cim-filespecification.md) representa um arquivo que está ligado ou desligado do sistema.</span><span class="sxs-lookup"><span data-stu-id="84916-356">The [**CIM\_FileSpecification**](cim-filespecification.md) class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="84916-357">O arquivo está localizado no diretório identificado pela Associação de [**\_ DirectorySpecificationFile do CIM**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-357">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="84916-358">O método [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa as informações para verificar a existência do arquivo.</span><span class="sxs-lookup"><span data-stu-id="84916-358">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="84916-359">Observe que as propriedades com um valor **nulo** não são verificadas.</span><span class="sxs-lookup"><span data-stu-id="84916-359">Note that properties with a **Null** value are not checked.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-360">**Armazenamento de filecim \_**</span><span class="sxs-lookup"><span data-stu-id="84916-360">**CIM\_FileStorage**</span></span>](cim-filestorage.md)
</dt> <dd>

<span data-ttu-id="84916-361">A associação de [**\_ armazenamento**](cim-filestorage.md) de arquivo CIM vincula o sistema de arquivos e os arquivos lógicos endereçados por meio do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="84916-361">The [**CIM\_FileStorage**](cim-filestorage.md) association links the file system and the logical files addressed through the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-362">**\_Sistema de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-362">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> <dd>

<span data-ttu-id="84916-363">A [**classe \_ FileSystem do CIM**](cim-filesystem.md) representa um arquivo ou conjunto de dados local para um sistema de computador ou montado remotamente de um servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="84916-363">The [**CIM\_FileSystem**](cim-filesystem.md) class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-364">**\_FLATPANEL CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-364">**CIM\_FlatPanel**</span></span>](cim-flatpanel.md)
</dt> <dd>

<span data-ttu-id="84916-365">A classe [**CIM \_ FlatPanel**](cim-flatpanel.md) representa os recursos e o gerenciamento do dispositivo lógico do painel plano.</span><span class="sxs-lookup"><span data-stu-id="84916-365">The [**CIM\_FlatPanel**](cim-flatpanel.md) class represents the capabilities and management of the flat panel logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-366">**\_FROMDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-366">**CIM\_FromDirectoryAction**</span></span>](cim-fromdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="84916-367">A associação [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) identifica o diretório de origem para a ação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="84916-367">The [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="84916-368">Quando essa associação é usada, a suposição é que o diretório de origem foi criado por uma ação anterior.</span><span class="sxs-lookup"><span data-stu-id="84916-368">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="84916-369">Essa associação não pode existir com uma associação de [**\_ FromDirectorySpecification CIM**](cim-fromdirectoryspecification.md) ; uma ação de arquivo só pode envolver um único diretório de origem.</span><span class="sxs-lookup"><span data-stu-id="84916-369">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-370">**\_FROMDIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-370">**CIM\_FromDirectorySpecification**</span></span>](cim-fromdirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="84916-371">A associação [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) identifica o diretório de origem para a ação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="84916-371">The [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="84916-372">Quando essa associação é usada, a suposição é que o diretório de origem já existe.</span><span class="sxs-lookup"><span data-stu-id="84916-372">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="84916-373">Essa associação não pode existir com uma associação de [**\_ FromDirectoryAction CIM**](cim-fromdirectoryaction.md) ; uma ação de arquivo só pode envolver um único diretório de origem.</span><span class="sxs-lookup"><span data-stu-id="84916-373">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-374">**\_FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-374">**CIM\_FRU**</span></span>](cim-fru.md)
</dt> <dd>

<span data-ttu-id="84916-375">A classe de [**\_ FRU do CIM**](cim-fru.md) representa uma coleção de produtos e elementos físicos definidos pelo fornecedor que estão associados a uma FRU (unidade de substituição de campo) para oferecer suporte, manutenção ou atualização de um produto no local do cliente.</span><span class="sxs-lookup"><span data-stu-id="84916-375">The [**CIM\_FRU**](cim-fru.md) class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-376">**\_FRUINCLUDESPRODUCT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-376">**CIM\_FRUIncludesProduct**</span></span>](cim-fruincludesproduct.md)
</dt> <dd>

<span data-ttu-id="84916-377">A classe [**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md) indica que uma FRU (unidade substituível de campo) pode ser composta por outros produtos.</span><span class="sxs-lookup"><span data-stu-id="84916-377">The [**CIM\_FRUIncludesProduct**](cim-fruincludesproduct.md) class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-378">**\_FRUPHYSICALELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-378">**CIM\_FRUPhysicalElements**</span></span>](cim-fruphysicalelements.md)
</dt> <dd>

<span data-ttu-id="84916-379">A classe [**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) representa os elementos físicos que compõem uma unidade de substituição de campo (FRU).</span><span class="sxs-lookup"><span data-stu-id="84916-379">The [**CIM\_FRUPhysicalElements**](cim-fruphysicalelements.md) class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-380">**\_HEATPIPE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-380">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dd>

<span data-ttu-id="84916-381">A classe [**CIM \_ HeatPipe**](cim-heatpipe.md) representa os recursos e o gerenciamento de um dispositivo de resfriamento de tubo de calor.</span><span class="sxs-lookup"><span data-stu-id="84916-381">The [**CIM\_HeatPipe**](cim-heatpipe.md) class represents the capabilities and management of a heat pipe cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-382">**\_HOSTEDACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-382">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> <dd>

<span data-ttu-id="84916-383">A classe [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) representa uma associação entre um SAP (ponto de acesso a serviços) e o sistema no qual ele é fornecido.</span><span class="sxs-lookup"><span data-stu-id="84916-383">The [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md) class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="84916-384">Cada sistema pode hospedar muitos SAPs.</span><span class="sxs-lookup"><span data-stu-id="84916-384">Each system may host many SAPs.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-385">**\_HOSTEDBOOTSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-385">**CIM\_HostedBootSAP**</span></span>](cim-hostedbootsap.md)
</dt> <dd>

<span data-ttu-id="84916-386">A classe [**CIM \_ HostedBootSAP**](cim-hostedbootsap.md) define o sistema de computador unitário de hospedagem para uma classe [**\_ BootSAP CIM**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-386">The [**CIM\_HostedBootSAP**](cim-hostedbootsap.md) class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="84916-387">Como essa relação é subclasse do [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), ela herda o esquema de escopo/nomenclatura definido para o [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md), em que um ponto de acesso é adiado para seu sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="84916-387">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="84916-388">Nesse caso, o **CIM \_ BootSAP** deve adiar para sua classe de [**\_ UnitaryComputerSystem do CIM**](cim-unitarycomputersystem.md) de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="84916-388">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-389">**\_HOSTEDBOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-389">**CIM\_HostedBootService**</span></span>](cim-hostedbootservice.md)
</dt> <dd>

<span data-ttu-id="84916-390">A classe [**CIM \_ HostedBootService**](cim-hostedbootservice.md) associa um sistema de hospedagem e um serviço de inicialização.</span><span class="sxs-lookup"><span data-stu-id="84916-390">The [**CIM\_HostedBootService**](cim-hostedbootservice.md) class associates a hosting system and a boot service.</span></span> <span data-ttu-id="84916-391">Como essa relação é subclasse de [**CIM \_ HostedService**](cim-hostedservice.md), ela herda o esquema de escopo/nomenclatura definido para o serviço, em que um serviço é adiado para seu sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="84916-391">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-392">**\_HOSTEDFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-392">**CIM\_HostedFileSystem**</span></span>](cim-hostedfilesystem.md)
</dt> <dd>

<span data-ttu-id="84916-393">A associação [**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md) representa um link entre o sistema de computador e o sistema de arquivos hospedado no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="84916-393">The [**CIM\_HostedFileSystem**](cim-hostedfilesystem.md) association represents a link between the computer system and the file system hosted on the computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-394">**\_HOSTEDJOBDESTINATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-394">**CIM\_HostedJobDestination**</span></span>](cim-hostedjobdestination.md)
</dt> <dd>

<span data-ttu-id="84916-395">A classe [**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) representa uma associação entre um destino de trabalho e o sistema no qual ele reside.</span><span class="sxs-lookup"><span data-stu-id="84916-395">The [**CIM\_HostedJobDestination**](cim-hostedjobdestination.md) class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="84916-396">Um sistema pode hospedar muitas filas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84916-396">A system may host many job queues.</span></span> <span data-ttu-id="84916-397">Destinos de trabalho adiados para o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="84916-397">Job destinations defer to the hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-398">**HostedService do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-398">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dd>

<span data-ttu-id="84916-399">A classe [**CIM \_ HostedService**](cim-hostedservice.md) representa uma associação entre um serviço e o sistema no qual a funcionalidade reside.</span><span class="sxs-lookup"><span data-stu-id="84916-399">The [**CIM\_HostedService**](cim-hostedservice.md) class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="84916-400">Um sistema pode hospedar muitos serviços, o que adia para o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="84916-400">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="84916-401">O modelo não representa serviços hospedados em vários sistemas.</span><span class="sxs-lookup"><span data-stu-id="84916-401">The model does not represent services hosted across multiple systems.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-402">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-402">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dd>

<span data-ttu-id="84916-403">A classe [**CIM \_ InfraredController**](cim-infraredcontroller.md) representa os recursos e o gerenciamento de um controlador de infravermelho.</span><span class="sxs-lookup"><span data-stu-id="84916-403">The [**CIM\_InfraredController**](cim-infraredcontroller.md) class represents the capabilities and management of an infrared controller.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-404">**\_INSTALLEDOS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-404">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dd>

<span data-ttu-id="84916-405">A classe de associação [**CIM \_ InstalledOS**](cim-installedos.md) representa um link entre o sistema de computador e o sistema operacional instalado.</span><span class="sxs-lookup"><span data-stu-id="84916-405">The [**CIM\_InstalledOS**](cim-installedos.md) association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="84916-406">Um sistema operacional é instalado quando está na extensão de armazenamento de um sistema de computador (por exemplo, copiado para uma unidade de disco ou baixado para memória).</span><span class="sxs-lookup"><span data-stu-id="84916-406">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-407">**\_INSTALLEDSOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-407">**CIM\_InstalledSoftwareElement**</span></span>](cim-installedsoftwareelement.md)
</dt> <dd>

<span data-ttu-id="84916-408">A classe [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) associa um sistema de computador a um elemento de software instalado.</span><span class="sxs-lookup"><span data-stu-id="84916-408">The [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) class associates a computer system with an installed software element.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-409">**IRQ de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-409">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dd>

<span data-ttu-id="84916-410">A classe de [**\_ IRQ de CIM**](cim-irq.md) representa uma IRQ (linha de solicitação de interrupção) de arquitetura da Intel.</span><span class="sxs-lookup"><span data-stu-id="84916-410">The [**CIM\_IRQ**](cim-irq.md) class represents an Intel architecture interrupt request line (IRQ).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-411">**Trabalho do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-411">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dd>

<span data-ttu-id="84916-412">A classe de [**\_ trabalho CIM**](cim-job.md) representa uma unidade de trabalho para um sistema, como um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="84916-412">The [**CIM\_Job**](cim-job.md) class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="84916-413">Um trabalho é diferente de um processo porque um trabalho pode ser agendado.</span><span class="sxs-lookup"><span data-stu-id="84916-413">A job is distinct from a process because a job can be scheduled.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-414">**\_JOBDESTINATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-414">**CIM\_JobDestination**</span></span>](cim-jobdestination.md)
</dt> <dd>

<span data-ttu-id="84916-415">A classe [**CIM \_ JobDestination**](cim-jobdestination.md) representa onde um trabalho é enviado para processamento.</span><span class="sxs-lookup"><span data-stu-id="84916-415">The [**CIM\_JobDestination**](cim-jobdestination.md) class represents where a job is submitted for processing.</span></span> <span data-ttu-id="84916-416">Ele pode se referir a uma fila que contém zero ou mais trabalhos, como uma fila de impressão que contém trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="84916-416">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="84916-417">Os destinos de trabalho são hospedados em sistemas, de forma semelhante ao modo como os serviços são hospedados em sistemas.</span><span class="sxs-lookup"><span data-stu-id="84916-417">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-418">**\_JOBDESTINATIONJOBS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-418">**CIM\_JobDestinationJobs**</span></span>](cim-jobdestinationjobs.md)
</dt> <dd>

<span data-ttu-id="84916-419">A associação [**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md) descreve onde um trabalho é enviado para processamento (ou seja, para qual destino de trabalho).</span><span class="sxs-lookup"><span data-stu-id="84916-419">The [**CIM\_JobDestinationJobs**](cim-jobdestinationjobs.md) association describes where a job is submitted for processing (that is, to which job destination).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-420">**\_Teclado CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-420">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dd>

<span data-ttu-id="84916-421">A classe de [**\_ teclado CIM**](cim-keyboard.md) representa os recursos e o gerenciamento do dispositivo lógico do teclado.</span><span class="sxs-lookup"><span data-stu-id="84916-421">The [**CIM\_Keyboard**](cim-keyboard.md) class represents the capabilities and management of the keyboard logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-422">**\_LINKHASCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-422">**CIM\_LinkHasConnector**</span></span>](cim-linkhasconnector.md)
</dt> <dd>

<span data-ttu-id="84916-423">A classe [**CIM \_ LinkHasConnector**](cim-linkhasconnector.md) associa cabos e links usados como conectores físicos, que conectam os elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="84916-423">The [**CIM\_LinkHasConnector**](cim-linkhasconnector.md) class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="84916-424">Essa associação define explicitamente a relação de conectores [**para \_ PhysicalLink CIM**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="84916-424">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-425">**\_LOCALFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-425">**CIM\_LocalFileSystem**</span></span>](cim-localfilesystem.md)
</dt> <dd>

<span data-ttu-id="84916-426">A classe [**CIM \_ LocalFileSystem**](cim-localfilesystem.md) representa o repositório de arquivos controlado por um sistema de computador por meio de meios locais (por exemplo, acesso direto ao driver de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="84916-426">The [**CIM\_LocalFileSystem**](cim-localfilesystem.md) class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="84916-427">O armazenamento de arquivos pode ser gerenciado diretamente pelo sistema de computador, sem a necessidade de outro computador agir como um servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="84916-427">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="84916-428">No entanto, para um sistema de arquivos clusterizado, o sistema de arquivos é local e, portanto, é adiado para o cluster.</span><span class="sxs-lookup"><span data-stu-id="84916-428">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-429">**Local do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-429">**CIM\_Location**</span></span>](cim-location.md)
</dt> <dd>

<span data-ttu-id="84916-430">A classe de [**\_ local do CIM**](cim-location.md) representa a posição e o endereço de um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="84916-430">The [**CIM\_Location**](cim-location.md) class represents the position and address of a physical element.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-431">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-431">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dd>

<span data-ttu-id="84916-432">A classe [**CIM \_ LogicalDevice**](cim-logicaldevice.md) representa uma entidade de hardware que pode ou não ser realizada em hardware físico.</span><span class="sxs-lookup"><span data-stu-id="84916-432">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-433">**\_LOGICALDISK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-433">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dd>

<span data-ttu-id="84916-434">A classe de [**\_ LogicalDisk CIM**](cim-logicaldisk.md) representa um intervalo contíguo de blocos lógicos que é identificável por um sistema de arquivos por meio do campo **DeviceID** (chave) do disco.</span><span class="sxs-lookup"><span data-stu-id="84916-434">The [**CIM\_LogicalDisk**](cim-logicaldisk.md) class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="84916-435">Por exemplo, em um ambiente do Windows, o campo **DeviceID** contém uma letra da unidade; em um ambiente UNIX, ele contém o caminho de acesso; e em um ambiente do NetWare, ele contém o nome do volume.</span><span class="sxs-lookup"><span data-stu-id="84916-435">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-436">**\_LOGICALDISKBASEDONPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-436">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

<span data-ttu-id="84916-437">A classe [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) associa um disco lógico à partição de disco na qual ele reside.</span><span class="sxs-lookup"><span data-stu-id="84916-437">The [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) class associates a logical disk with the disk partition on which it resides.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-438">**\_LOGICALDISKBASEDONVOLUMESET CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-438">**CIM\_LogicalDiskBasedOnVolumeSet**</span></span>](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

<span data-ttu-id="84916-439">A associação de [**\_ LogicalDiskBasedOnVolumeSet do CIM**](cim-logicaldiskbasedonvolumeset.md) relaciona discos lógicos com o volume no qual eles são encontrados.</span><span class="sxs-lookup"><span data-stu-id="84916-439">The [**CIM\_LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="84916-440">Discos lógicos podem ser baseados em um único volume (por exemplo, exposto por um Gerenciador de volume de software) ou uma partição de disco.</span><span class="sxs-lookup"><span data-stu-id="84916-440">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-441">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="84916-441">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="84916-442">A classe [**CIM \_ LogicalElement**](cim-logicalelement.md) é a classe base para todos os componentes do sistema que representam componentes do sistema abstratos, como perfis, processos ou recursos do sistema, na forma de dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="84916-442">The [**CIM\_LogicalElement**](cim-logicalelement.md) class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-443">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="84916-443">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dd>

<span data-ttu-id="84916-444">A classe [**CIM \_ LogicalFile**](cim-logicalfile.md) representa uma coleção nomeada de dados, que pode ser código executável, que está localizada em um sistema de arquivos em uma extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84916-444">The [**CIM\_LogicalFile**](cim-logicalfile.md) class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-445">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-445">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dd>

<span data-ttu-id="84916-446">A classe [**CIM \_ LogicalIdentity**](cim-logicalidentity.md) é uma associação abstrata e genérica que indica que dois elementos lógicos representam diferentes aspectos da mesma entidade subjacente.</span><span class="sxs-lookup"><span data-stu-id="84916-446">The [**CIM\_LogicalIdentity**](cim-logicalidentity.md) class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-447">**\_MAGNETOOPTICALDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-447">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> <dd>

<span data-ttu-id="84916-448">A classe [**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) representa os recursos e o gerenciamento de uma unidade magneto-óptica, um subtipo do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="84916-448">The [**CIM\_MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-449">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-449">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="84916-450">A classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) é a classe base para a hierarquia de elementos do sistema.</span><span class="sxs-lookup"><span data-stu-id="84916-450">The [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="84916-451">Qualquer componente de sistema diferencial é um candidato para inclusão nessa classe.</span><span class="sxs-lookup"><span data-stu-id="84916-451">Any distinguishable system component is a candidate for inclusion in this class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-452">**\_MANAGEMENTCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-452">**CIM\_ManagementController**</span></span>](cim-managementcontroller.md)
</dt> <dd>

<span data-ttu-id="84916-453">A classe [**CIM \_ ManagementController**](cim-managementcontroller.md) está relacionada aos recursos e ao gerenciamento de um controlador de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="84916-453">The [**CIM\_ManagementController**](cim-managementcontroller.md) class relates to the capabilities and management of a management controller.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-454">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-454">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> <dd>

<span data-ttu-id="84916-455">A classe [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) representa a capacidade de acessar uma ou mais mídias e, em seguida, usar a mídia para armazenar e recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="84916-455">The [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-456">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-456">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dd>

<span data-ttu-id="84916-457">A associação [**CIM \_ MediaPresent**](cim-mediapresent.md) descreve uma relação em que uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="84916-457">The [**CIM\_MediaPresent**](cim-mediapresent.md) association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-458">**\_Memória CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-458">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dd>

<span data-ttu-id="84916-459">A classe de [**\_ memória CIM**](cim-memory.md) representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.</span><span class="sxs-lookup"><span data-stu-id="84916-459">The [**CIM\_Memory**](cim-memory.md) class represents the capabilities and management of memory-related logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-460">**\_MEMORYCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-460">**CIM\_MemoryCapacity**</span></span>](cim-memorycapacity.md)
</dt> <dd>

<span data-ttu-id="84916-461">A classe [**CIM \_ MemoryCapacity**](cim-memorycapacity.md) representa a memória que pode ser instalada em um elemento físico e suas configurações mínimas e máximas.</span><span class="sxs-lookup"><span data-stu-id="84916-461">The [**CIM\_MemoryCapacity**](cim-memorycapacity.md) class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="84916-462">Informações sobre a memória que está atualmente instalada e os requisitos mínimos e máximos de um elemento estão localizados em instâncias da classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-462">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-463">**\_MEMORYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-463">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> <dd>

<span data-ttu-id="84916-464">A classe [**CIM \_ MemoryCheck**](cim-memorycheck.md) especifica uma condição para a quantidade mínima de memória que deve estar disponível em um sistema.</span><span class="sxs-lookup"><span data-stu-id="84916-464">The [**CIM\_MemoryCheck**](cim-memorycheck.md) class specifies a condition for the minimum amount of memory that must be available on a system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-465">**\_MEMORYMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-465">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dd>

<span data-ttu-id="84916-466">A classe [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) representa e/s mapeada pela memória da arquitetura do computador.</span><span class="sxs-lookup"><span data-stu-id="84916-466">The [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="84916-467">Essa classe trata da memória e dos recursos de e/s de porta.</span><span class="sxs-lookup"><span data-stu-id="84916-467">This class addresses memory and port I/O resources.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-468">**\_MEMORYONCARD CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-468">**CIM\_MemoryOnCard**</span></span>](cim-memoryoncard.md)
</dt> <dd>

<span data-ttu-id="84916-469">A classe [**CIM \_ MemoryOnCard**](cim-memoryoncard.md) associa a memória física localizada em placas de hospedagem, placas de adaptador e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="84916-469">The [**CIM\_MemoryOnCard**](cim-memoryoncard.md) class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="84916-470">Essa associação define explicitamente a relação de memória para os cartões.</span><span class="sxs-lookup"><span data-stu-id="84916-470">This association explicitly defines the relationship of memory to cards.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-471">**\_MEMORYWITHMEDIA CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-471">**CIM\_MemoryWithMedia**</span></span>](cim-memorywithmedia.md)
</dt> <dd>

<span data-ttu-id="84916-472">A classe [**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md) associa a memória física a uma mídia física e a seu cartucho.</span><span class="sxs-lookup"><span data-stu-id="84916-472">The [**CIM\_MemoryWithMedia**](cim-memorywithmedia.md) class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="84916-473">A memória fornece a identificação de mídia e armazena dados específicos do usuário.</span><span class="sxs-lookup"><span data-stu-id="84916-473">The memory provides media identification and stores user-specific data.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-474">**\_MODIFYSETTINGACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-474">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> <dd>

<span data-ttu-id="84916-475">A classe [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) representa as informações para modificar um arquivo de configuração específico, para uma entrada específica, com um valor específico.</span><span class="sxs-lookup"><span data-stu-id="84916-475">The [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-476">**\_MONITORRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-476">**CIM\_MonitorResolution**</span></span>](cim-monitorresolution.md)
</dt> <dd>

<span data-ttu-id="84916-477">A classe [**CIM \_ MonitorResolution**](cim-monitorresolution.md) representa a relação entre as resoluções horizontal e vertical e a taxa de atualização e o modo de verificação para um monitor de desktop.</span><span class="sxs-lookup"><span data-stu-id="84916-477">The [**CIM\_MonitorResolution**](cim-monitorresolution.md) class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="84916-478">Os valores são especificados no objeto do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="84916-478">Values are specified in the video controller object.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-479">**\_MONITORSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-479">**CIM\_MonitorSetting**</span></span>](cim-monitorsetting.md)
</dt> <dd>

<span data-ttu-id="84916-480">A classe [**CIM \_ MonitorSetting**](cim-monitorsetting.md) associa a resolução do monitor ao monitor de área de trabalho ao qual se aplica.</span><span class="sxs-lookup"><span data-stu-id="84916-480">The [**CIM\_MonitorSetting**](cim-monitorsetting.md) class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-481">**Montagem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-481">**CIM\_Mount**</span></span>](cim-mount.md)
</dt> <dd>

<span data-ttu-id="84916-482">A classe de [**\_ montagem CIM**](cim-mount.md) representa uma associação entre um sistema de arquivos e um diretório ao qual ele está anexado.</span><span class="sxs-lookup"><span data-stu-id="84916-482">The [**CIM\_Mount**](cim-mount.md) class represents an association between a file system and a directory to which it is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-483">**\_MULTISTATESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-483">**CIM\_MultiStateSensor**</span></span>](cim-multistatesensor.md)
</dt> <dd>

<span data-ttu-id="84916-484">A classe [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) representa um conjunto de vários membros de sensores binários em que cada sensor binário relata um resultado booliano.</span><span class="sxs-lookup"><span data-stu-id="84916-484">The [**CIM\_MultiStateSensor**](cim-multistatesensor.md) class represents a multi-member set of binary sensors where each binary sensor reports a Boolean result.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-485">**\_Adaptador CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-485">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dd>

<span data-ttu-id="84916-486">A classe [**CIM \_ adaptador**](cim-networkadapter.md) é uma classe abstrata que define os conceitos gerais de hardware de rede (por exemplo, endereço permanente ou velocidade de operação).</span><span class="sxs-lookup"><span data-stu-id="84916-486">The [**CIM\_NetworkAdapter**](cim-networkadapter.md) class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="84916-487">As informações são transmitidas usando a associação [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-487">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-488">**\_NFS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-488">**CIM\_NFS**</span></span>](cim-nfs.md)
</dt> <dd>

<span data-ttu-id="84916-489">A classe [**CIM \_ NFS**](cim-nfs.md) representa um sistema de arquivos remoto que é montado, usando o protocolo NFS (sistema de arquivos de rede), de um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="84916-489">The [**CIM\_NFS**](cim-nfs.md) class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-490">**\_NONVOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-490">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> <dd>

<span data-ttu-id="84916-491">A classe [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) representa os recursos e o gerenciamento do armazenamento não volátil.</span><span class="sxs-lookup"><span data-stu-id="84916-491">The [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="84916-492">A memória não volátil inclui, nativamente, o armazenamento flash e ROM.</span><span class="sxs-lookup"><span data-stu-id="84916-492">Nonvolatile memory natively includes flash and ROM storage.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-493">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-493">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> <dd>

<span data-ttu-id="84916-494">A classe [**CIM \_ NumericSensor**](cim-numericsensor.md) representa um sensor numérico que retorna leituras numéricas e, opcionalmente, dá suporte a configurações de limites.</span><span class="sxs-lookup"><span data-stu-id="84916-494">The [**CIM\_NumericSensor**](cim-numericsensor.md) class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-495">**Sistema \_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-495">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dd>

<span data-ttu-id="84916-496">A classe [**CIM \_ OperatingSystem**](cim-operatingsystem.md) representa um sistema operacional de computador, que é composto por software e firmware que tornam o hardware de um sistema de computador utilizável.</span><span class="sxs-lookup"><span data-stu-id="84916-496">The [**CIM\_OperatingSystem**](cim-operatingsystem.md) class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-497">**\_OPERATINGSYSTEMSOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-497">**CIM\_OperatingSystemSoftwareFeature**</span></span>](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="84916-498">A classe [**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) representa os recursos de software que compõem o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="84916-498">The [**CIM\_OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) class represents the software features that make up the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-499">**\_OSPROCESS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-499">**CIM\_OSProcess**</span></span>](cim-osprocess.md)
</dt> <dd>

<span data-ttu-id="84916-500">A classe [**CIM \_ OSProcess**](cim-osprocess.md) associa o sistema operacional e um ou mais processos em execução no contexto do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="84916-500">The [**CIM\_OSProcess**](cim-osprocess.md) class associates the operating system and one or more processes running in the context of the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-501">**\_OSVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-501">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> <dd>

<span data-ttu-id="84916-502">A classe [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) especifica as versões do sistema operacional que podem dar suporte a um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="84916-502">The [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class specifies the versions of the operating system that can support a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-503">**\_PACKAGEALARM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-503">**CIM\_PackageAlarm**</span></span>](cim-packagealarm.md)
</dt> <dd>

<span data-ttu-id="84916-504">A associação [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa a relação na qual um dispositivo de alarme é instalado como parte de um pacote.</span><span class="sxs-lookup"><span data-stu-id="84916-504">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="84916-505">A instalação indica problemas com o ambiente do pacote — seu estado de segurança ou sua integridade geral.</span><span class="sxs-lookup"><span data-stu-id="84916-505">The installation indicates issues with the package's environment—its security state or its overall health.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-506">**\_PACKAGECOOLING CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-506">**CIM\_PackageCooling**</span></span>](cim-packagecooling.md)
</dt> <dd>

<span data-ttu-id="84916-507">A associação [**CIM \_ PackageCooling**](cim-packagecooling.md) representa a relação na qual um dispositivo de resfriamento é instalado em um pacote, como um chassi ou rack, para auxiliar na resfriamento do pacote.</span><span class="sxs-lookup"><span data-stu-id="84916-507">The [**CIM\_PackageCooling**](cim-packagecooling.md) association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-508">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-508">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dd>

<span data-ttu-id="84916-509">A associação [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) representa uma relação explícita na qual um componente é normalmente contido por um pacote físico, como um chassi ou cartão.</span><span class="sxs-lookup"><span data-stu-id="84916-509">The [**CIM\_PackagedComponent**](cim-packagedcomponent.md) association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-510">**\_PACKAGEINCHASSIS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-510">**CIM\_PackageInChassis**</span></span>](cim-packageinchassis.md)
</dt> <dd>

<span data-ttu-id="84916-511">A associação [**CIM \_ PackageInChassis**](cim-packageinchassis.md) representa a relação na qual um chassi pode conter outros pacotes, como outros chassis e cartões.</span><span class="sxs-lookup"><span data-stu-id="84916-511">The [**CIM\_PackageInChassis**](cim-packageinchassis.md) association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-512">**\_PACKAGEINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-512">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> <dd>

<span data-ttu-id="84916-513">A associação [**CIM \_ PackageInSlot**](cim-packageinslot.md) representa a relação entre os cartões de dispositivo e o chassi no qual eles são montados.</span><span class="sxs-lookup"><span data-stu-id="84916-513">The [**CIM\_PackageInSlot**](cim-packageinslot.md) association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-514">**\_PACKAGETEMPSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-514">**CIM\_PackageTempSensor**</span></span>](cim-packagetempsensor.md)
</dt> <dd>

<span data-ttu-id="84916-515">A associação [**CIM \_ PackageTempSensor**](cim-packagetempsensor.md) representa a relação na qual um sensor de temperatura é frequentemente instalado em um pacote, como um chassi ou um rack, para monitorar o ambiente do pacote.</span><span class="sxs-lookup"><span data-stu-id="84916-515">The [**CIM\_PackageTempSensor**](cim-packagetempsensor.md) association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-516">**\_PARALLELCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-516">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dd>

<span data-ttu-id="84916-517">A associação de [**\_ ParallelController CIM**](cim-parallelcontroller.md) está relacionada aos recursos e ao gerenciamento do dispositivo lógico de porta paralela.</span><span class="sxs-lookup"><span data-stu-id="84916-517">The [**CIM\_ParallelController**](cim-parallelcontroller.md) association relates to the capabilities and management of the parallel port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-518">**\_PARTICIPATESINSET CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-518">**CIM\_ParticipatesInSet**</span></span>](cim-participatesinset.md)
</dt> <dd>

<span data-ttu-id="84916-519">A classe [**CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica os elementos físicos que devem ser substituídos juntos.</span><span class="sxs-lookup"><span data-stu-id="84916-519">The [**CIM\_ParticipatesInSet**](cim-participatesinset.md) class identifies physical elements that should be replaced together.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-520">**\_PCICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-520">**CIM\_PCIController**</span></span>](cim-pcicontroller.md)
</dt> <dd>

<span data-ttu-id="84916-521">A classe [**CIM \_ PCIController**](cim-pcicontroller.md) representa as propriedades e o gerenciamento de um controlador PCI.</span><span class="sxs-lookup"><span data-stu-id="84916-521">The [**CIM\_PCIController**](cim-pcicontroller.md) class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="84916-522">As propriedades nessa classe e suas subclasses são definidas nas várias especificações de PCI publicadas pelo SIG de PCI.</span><span class="sxs-lookup"><span data-stu-id="84916-522">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-523">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-523">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dd>

<span data-ttu-id="84916-524">A classe [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) representa os recursos e o gerenciamento de um controlador de PCMCIA (Associação Internacional de cartão de memória) do computador pessoal.</span><span class="sxs-lookup"><span data-stu-id="84916-524">The [**CIM\_PCMCIAController**](cim-pcmciacontroller.md) class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-525">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-525">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dd>

<span data-ttu-id="84916-526">O [**\_ PCVideoController CIM**](cim-pcvideocontroller.md) representa os recursos e o gerenciamento de um controlador de vídeo de computador pessoal, um subtipo de um controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="84916-526">The [**CIM\_PCVideoController**](cim-pcvideocontroller.md) represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-527">**\_PEXTENTREDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-527">**CIM\_PExtentRedundancyComponent**</span></span>](cim-pextentredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="84916-528">A classe [**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) representa as extensões físicas que participam de um grupo de redundância de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84916-528">The [**CIM\_PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) class represents the physical extents that participate in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-529">**\_PHYSICALCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-529">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> <dd>

<span data-ttu-id="84916-530">A classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) é uma classe abstrata que representa os requisitos mínimos e máximos de um elemento físico e sua capacidade de dar suporte a diferentes tipos de hardware.</span><span class="sxs-lookup"><span data-stu-id="84916-530">The [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="84916-531">Por exemplo, os requisitos mínimos e máximos de memória podem ser modelados como uma subclasse de **\_ PhysicalCapacity CIM**.</span><span class="sxs-lookup"><span data-stu-id="84916-531">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-532">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-532">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dd>

<span data-ttu-id="84916-533">A classe [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) representa um componente básico ou de baixo nível em um pacote.</span><span class="sxs-lookup"><span data-stu-id="84916-533">The [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="84916-534">Um elemento físico que não é um link, um conector ou um pacote é um descendente (ou membro) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="84916-534">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-535">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-535">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dd>

<span data-ttu-id="84916-536">A classe [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) representa qualquer elemento físico que é usado para se conectar a outros elementos.</span><span class="sxs-lookup"><span data-stu-id="84916-536">The [**CIM\_PhysicalConnector**](cim-physicalconnector.md) class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="84916-537">Qualquer objeto que possa se conectar e transmitir sinais ou potência entre dois ou mais elementos físicos é um descendente (ou membro) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="84916-537">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-538">**Físico do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-538">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> <dd>

<span data-ttu-id="84916-539">As subclasses do [**CIM \_ PhysicalElement**](cim-physicalelement.md) definem qualquer componente de um sistema que tenha uma identidade física distinta.</span><span class="sxs-lookup"><span data-stu-id="84916-539">The [**CIM\_PhysicalElement**](cim-physicalelement.md) subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="84916-540">As instâncias dessa classe podem ser definidas em termos de rótulos que podem ser fisicamente anexados ao objeto.</span><span class="sxs-lookup"><span data-stu-id="84916-540">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-541">**\_PHYSICALELEMENTLOCATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-541">**CIM\_PhysicalElementLocation**</span></span>](cim-physicalelementlocation.md)
</dt> <dd>

<span data-ttu-id="84916-542">A classe [**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md) associa um elemento físico a um objeto de [**\_ local CIM**](cim-location.md) para fins de inventário ou substituição.</span><span class="sxs-lookup"><span data-stu-id="84916-542">The [**CIM\_PhysicalElementLocation**](cim-physicalelementlocation.md) class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-543">**\_PHYSICALEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-543">**CIM\_PhysicalExtent**</span></span>](cim-physicalextent.md)
</dt> <dd>

<span data-ttu-id="84916-544">A classe [**CIM \_ PhysicalExtent**](cim-physicalextent.md) representa uma implementação de RAID SCC.</span><span class="sxs-lookup"><span data-stu-id="84916-544">The [**CIM\_PhysicalExtent**](cim-physicalextent.md) class represents an SCC RAID implementation.</span></span> <span data-ttu-id="84916-545">Ele define os endereços de bloco endereçáveis consecutivos em um único dispositivo de armazenamento que são tratados como uma única extensão de armazenamento na mesma classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-545">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="84916-546">Uma alternativa, quando a configuração automática é usada, é instanciar ou estender a classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-546">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-547">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-547">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> <dd>

<span data-ttu-id="84916-548">A classe [**CIM \_ PhysicalFrame**](cim-physicalframe.md) é uma classe pai de rack, chassi e outros compartimentos de quadro, pois são definidos em classes de extensão.</span><span class="sxs-lookup"><span data-stu-id="84916-548">The [**CIM\_PhysicalFrame**](cim-physicalframe.md) class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="84916-549">Propriedades como **VisibleAlarm** e **AudibleAlarm** e dados relacionados a violações de segurança são incluídos nessa classe pai.</span><span class="sxs-lookup"><span data-stu-id="84916-549">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-550">**\_PHYSICALLINK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-550">**CIM\_PhysicalLink**</span></span>](cim-physicallink.md)
</dt> <dd>

<span data-ttu-id="84916-551">A classe [**CIM \_ PhysicalLink**](cim-physicallink.md) representa o cabeamento dos elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="84916-551">The [**CIM\_PhysicalLink**](cim-physicallink.md) class represents the cabling of physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-552">**\_PHYSICALMEDIA CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-552">**CIM\_PhysicalMedia**</span></span>](cim-physicalmedia.md)
</dt> <dd>

<span data-ttu-id="84916-553">A classe [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) representa tipos de mídia de documentação e armazenamento, como fitas, CD ROMs e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="84916-553">The [**CIM\_PhysicalMedia**](cim-physicalmedia.md) class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-554">**\_PHYSICALMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-554">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dd>

<span data-ttu-id="84916-555">A classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) representa dispositivos de memória de nível baixo, como Simms, DIMMs, chips de memória bruta e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="84916-555">The [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-556">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-556">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dd>

<span data-ttu-id="84916-557">A classe [**CIM \_ PhysicalPackage**](cim-physicalpackage.md) representa os elementos físicos que contêm ou hospedam outros componentes.</span><span class="sxs-lookup"><span data-stu-id="84916-557">The [**CIM\_PhysicalPackage**](cim-physicalpackage.md) class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="84916-558">Os exemplos são um compartimento de rack ou uma placa de adaptador.</span><span class="sxs-lookup"><span data-stu-id="84916-558">Examples are a rack enclosure or an adapter card.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-559">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-559">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dd>

<span data-ttu-id="84916-560">A classe [**CIM \_ PointingDevice**](cim-pointingdevice.md) representa um dispositivo que aponta para regiões na exibição.</span><span class="sxs-lookup"><span data-stu-id="84916-560">The [**CIM\_PointingDevice**](cim-pointingdevice.md) class represents a device that points to regions on the display.</span></span> <span data-ttu-id="84916-561">Qualquer dispositivo que manipule um ponteiro ou aponta para regiões em uma exibição Visual é membro dessa classe.</span><span class="sxs-lookup"><span data-stu-id="84916-561">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="84916-562">Por exemplo, um mouse, uma caneta, um touch pad ou um Tablet.</span><span class="sxs-lookup"><span data-stu-id="84916-562">For example, a mouse, stylus, touch pad, or tablet.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-563">**\_POTSMODEM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-563">**CIM\_POTSModem**</span></span>](cim-potsmodem.md)
</dt> <dd>

<span data-ttu-id="84916-564">A classe [**CIM \_ POTSModem**](cim-potsmodem.md) representa um dispositivo que traduz dados binários em modulações de onda para transmissão baseada em som conectando-se à rede do sistema de telefonia antigo (POTS).</span><span class="sxs-lookup"><span data-stu-id="84916-564">The [**CIM\_POTSModem**](cim-potsmodem.md) class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-565">**Fonte de \_ alimentação CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-565">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> <dd>

<span data-ttu-id="84916-566">A classe [**CIM \_ powersupply**](cim-powersupply.md) representa os recursos e o gerenciamento do dispositivo lógico da fonte de energia.</span><span class="sxs-lookup"><span data-stu-id="84916-566">The [**CIM\_PowerSupply**](cim-powersupply.md) class represents the capabilities and management of the power supply logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-567">**\_Impressora CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-567">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dd>

<span data-ttu-id="84916-568">A classe de [**\_ impressora CIM**](cim-printer.md) representa os recursos e o gerenciamento do dispositivo lógico da impressora.</span><span class="sxs-lookup"><span data-stu-id="84916-568">The [**CIM\_Printer**](cim-printer.md) class represents the capabilities and management of the printer logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-569">**\_Processo CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-569">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dd>

<span data-ttu-id="84916-570">A classe de [**\_ processo CIM**](cim-process.md) representa uma única instância de um programa em execução.</span><span class="sxs-lookup"><span data-stu-id="84916-570">The [**CIM\_Process**](cim-process.md) class represents a single instance of a running program.</span></span> <span data-ttu-id="84916-571">Um usuário normalmente vê um processo como um aplicativo ou uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="84916-571">A user typically sees a process as an application or task.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-572">**\_PROCESSEXECUTABLE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-572">**CIM\_ProcessExecutable**</span></span>](cim-processexecutable.md)
</dt> <dd>

<span data-ttu-id="84916-573">A classe [**CIM \_ ProcessExecutable**](cim-processexecutable.md) representa um vínculo entre um processo e um arquivo de dados e indica que o arquivo participa da execução do processo.</span><span class="sxs-lookup"><span data-stu-id="84916-573">The [**CIM\_ProcessExecutable**](cim-processexecutable.md) class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-574">**\_Processador CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-574">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dd>

<span data-ttu-id="84916-575">A classe de [**\_ processador CIM**](cim-processor.md) representa os recursos e o gerenciamento do dispositivo lógico do processador.</span><span class="sxs-lookup"><span data-stu-id="84916-575">The [**CIM\_Processor**](cim-processor.md) class represents the capabilities and management of the processor logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-576">**\_PROCESSTHREAD CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-576">**CIM\_ProcessThread**</span></span>](cim-processthread.md)
</dt> <dd>

<span data-ttu-id="84916-577">A classe [**CIM \_ ProcessThread**](cim-processthread.md) representa um link entre um processo e os threads em execução no contexto do processo.</span><span class="sxs-lookup"><span data-stu-id="84916-577">The [**CIM\_ProcessThread**](cim-processthread.md) class represents a link between a process and the threads running in the context of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-578">**\_Produto CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-578">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dd>

<span data-ttu-id="84916-579">A classe de [**\_ produto CIM**](cim-product.md) é uma classe concreta que representa uma coleção de elementos físicos, recursos de software e outros produtos, adquiridos como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="84916-579">The [**CIM\_Product**](cim-product.md) class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="84916-580">A aquisição implica um contrato entre o fornecedor e o consumidor, o que pode ter implicações no licenciamento, suporte e garantia do produto.</span><span class="sxs-lookup"><span data-stu-id="84916-580">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-581">**\_PRODUCTFRU CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-581">**CIM\_ProductFRU**</span></span>](cim-productfru.md)
</dt> <dd>

<span data-ttu-id="84916-582">A classe [**CIM \_ ProductFRU**](cim-productfru.md) representa uma associação entre o produto e uma unidade de substituição de campo (FRU), que fornece informações sobre os componentes do produto que foram ou estão sendo substituídos.</span><span class="sxs-lookup"><span data-stu-id="84916-582">The [**CIM\_ProductFRU**](cim-productfru.md) class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-583">**\_PRODUCTPARENTCHILD CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-583">**CIM\_ProductParentChild**</span></span>](cim-productparentchild.md)
</dt> <dd>

<span data-ttu-id="84916-584">A associação [**CIM \_ ProductParentChild**](cim-productparentchild.md) define uma hierarquia pai-filho entre os produtos.</span><span class="sxs-lookup"><span data-stu-id="84916-584">The [**CIM\_ProductParentChild**](cim-productparentchild.md) association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="84916-585">Por exemplo, um produto pode ser agrupado com outros produtos.</span><span class="sxs-lookup"><span data-stu-id="84916-585">For example, a product can come bundled with other products.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-586">**\_PRODUCTPHYSICALELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-586">**CIM\_ProductPhysicalElements**</span></span>](cim-productphysicalelements.md)
</dt> <dd>

<span data-ttu-id="84916-587">A classe [**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) representa os elementos físicos que compõem um produto.</span><span class="sxs-lookup"><span data-stu-id="84916-587">The [**CIM\_ProductPhysicalElements**](cim-productphysicalelements.md) class represents the physical elements that make up a product.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-588">**\_PRODUCTPRODUCTDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-588">**CIM\_ProductProductDependency**</span></span>](cim-productproductdependency.md)
</dt> <dd>

<span data-ttu-id="84916-589">A classe [**CIM \_ ProductProductDependency**](cim-productproductdependency.md) representa uma associação entre dois produtos, que indica que um deve ser instalado ou ausente para que o outro funcione.</span><span class="sxs-lookup"><span data-stu-id="84916-589">The [**CIM\_ProductProductDependency**](cim-productproductdependency.md) class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="84916-590">Isso é conceitualmente equivalente à associação [**de \_ ServiceServiceDependency do CIM**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="84916-590">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-591">**\_PRODUCTSOFTWAREFEATURES CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-591">**CIM\_ProductSoftwareFeatures**</span></span>](cim-productsoftwarefeatures.md)
</dt> <dd>

<span data-ttu-id="84916-592">A associação [**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifica os recursos de software para um produto específico.</span><span class="sxs-lookup"><span data-stu-id="84916-592">The [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association identifies the software features for a particular product.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-593">**\_PRODUCTSUPPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-593">**CIM\_ProductSupport**</span></span>](cim-productsupport.md)
</dt> <dd>

<span data-ttu-id="84916-594">A classe [**CIM \_ ProductSupport**](cim-productsupport.md) representa uma associação entre produto e acesso de suporte que transmite como o suporte é obtido para o produto.</span><span class="sxs-lookup"><span data-stu-id="84916-594">The [**CIM\_ProductSupport**](cim-productsupport.md) class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="84916-595">Vários tipos de suporte estão disponíveis para um produto; o mesmo objeto de suporte pode fornecer assistência para vários produtos.</span><span class="sxs-lookup"><span data-stu-id="84916-595">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-596">**\_PROTECTEDSPACEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-596">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> <dd>

<span data-ttu-id="84916-597">A classe [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) representa endereços de bloco lógico endereçáveis, que são tratados como uma única extensão de armazenamento, mas estão localizados em uma única extensão física.</span><span class="sxs-lookup"><span data-stu-id="84916-597">The [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) class represents addressable logical-block addresses, which are treated as a single storage extent, but are located on a single physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-598">**\_PSEXTENTBASEDONPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-598">**CIM\_PSExtentBasedOnPExtent**</span></span>](cim-psextentbasedonpextent.md)
</dt> <dd>

<span data-ttu-id="84916-599">A classe [**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) associa extensões de espaço protegidas que se baseiam em uma extensão física.</span><span class="sxs-lookup"><span data-stu-id="84916-599">The [**CIM\_PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) class associates protected space extents that are based on a physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-600">**\_Rack CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-600">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> <dd>

<span data-ttu-id="84916-601">A classe de [**\_ rack CIM**](cim-rack.md) representa um rack (um quadro físico ou compartimento) no qual os chassis são armazenados.</span><span class="sxs-lookup"><span data-stu-id="84916-601">The [**CIM\_Rack**](cim-rack.md) class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="84916-602">Normalmente, um rack representa o compartimento; todos os componentes em funcionamento são empacotados no chassi.</span><span class="sxs-lookup"><span data-stu-id="84916-602">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-603">**O CIM \_ percebe**</span><span class="sxs-lookup"><span data-stu-id="84916-603">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dd>

<span data-ttu-id="84916-604">O [**CIM \_ percebe**](cim-realizes.md) que a classe representa a associação que define o mapeamento entre um dispositivo lógico e o componente físico que implementa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84916-604">The [**CIM\_Realizes**](cim-realizes.md) class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-605">**\_REALIZESAGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-605">**CIM\_RealizesAggregatePExtent**</span></span>](cim-realizesaggregatepextent.md)
</dt> <dd>

<span data-ttu-id="84916-606">A associação [**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) representa a relação na qual a classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) é realizada em uma mídia física.</span><span class="sxs-lookup"><span data-stu-id="84916-606">The [**CIM\_RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-607">**\_REALIZESDISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-607">**CIM\_RealizesDiskPartition**</span></span>](cim-realizesdiskpartition.md)
</dt> <dd>

<span data-ttu-id="84916-608">A classe [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) representa uma partição de disco em uma mídia física que modela a criação de partições em uma unidade SCSI ou IDE bruto.</span><span class="sxs-lookup"><span data-stu-id="84916-608">The [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-609">**\_REALIZESPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-609">**CIM\_RealizesPExtent**</span></span>](cim-realizespextent.md)
</dt> <dd>

<span data-ttu-id="84916-610">A associação [**CIM \_ RealizesPExtent**](cim-realizespextent.md) representa a relação na qual as extensões físicas são realizadas em uma mídia física.</span><span class="sxs-lookup"><span data-stu-id="84916-610">The [**CIM\_RealizesPExtent**](cim-realizespextent.md) association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="84916-611">Além disso, o endereço inicial da extensão física na mídia física é especificado.</span><span class="sxs-lookup"><span data-stu-id="84916-611">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-612">**Reinicialização de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-612">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> <dd>

<span data-ttu-id="84916-613">A classe [**CIM \_ rebootaction**](cim-rebootaction.md) causa uma reinicialização do sistema onde o elemento de software é instalado.</span><span class="sxs-lookup"><span data-stu-id="84916-613">The [**CIM\_RebootAction**](cim-rebootaction.md) class causes a system reboot where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-614">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-614">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> <dd>

<span data-ttu-id="84916-615">A classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) associa um grupo de redundância composto por elementos do sistema gerenciado e indica que, juntos, os elementos fornecem redundância.</span><span class="sxs-lookup"><span data-stu-id="84916-615">The [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="84916-616">Todos os elementos agregados em um grupo de redundância devem ser instanciações da mesma classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="84916-616">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-617">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-617">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> <dd>

<span data-ttu-id="84916-618">A classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) representa uma coleção de elementos de sistema gerenciados, que indica que os componentes agregados, juntos, fornecem redundância.</span><span class="sxs-lookup"><span data-stu-id="84916-618">The [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="84916-619">Todos os elementos agregados em um grupo de redundância devem ser instanciações da mesma classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="84916-619">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-620">**\_Refrigeração CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-620">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dd>

<span data-ttu-id="84916-621">A classe de [**\_ refrigeração CIM**](cim-refrigeration.md) representa os recursos e o gerenciamento de um dispositivo de resfriamento de refrigeração.</span><span class="sxs-lookup"><span data-stu-id="84916-621">The [**CIM\_Refrigeration**](cim-refrigeration.md) class represents the capabilities and management of a refrigeration cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-622">**\_RELATEDSTATISTICS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-622">**CIM\_RelatedStatistics**</span></span>](cim-relatedstatistics.md)
</dt> <dd>

<span data-ttu-id="84916-623">A associação [**CIM \_ RelatedStatistics**](cim-relatedstatistics.md) representa hierarquias e dependências de classes [**\_ StatisticalInformation do CIM**](cim-statisticalinformation.md) relacionadas.</span><span class="sxs-lookup"><span data-stu-id="84916-623">The [**CIM\_RelatedStatistics**](cim-relatedstatistics.md) association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-624">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-624">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> <dd>

<span data-ttu-id="84916-625">A classe [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) representa um sistema de arquivos remoto que é acessado por meio de um serviço relacionado à rede.</span><span class="sxs-lookup"><span data-stu-id="84916-625">The [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md) class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="84916-626">Nesse caso, o armazenamento de arquivos é hospedado por um computador, que atua como um servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="84916-626">In this case, the file store is hosted by a computer, which acts as a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-627">**\_REMOVEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-627">**CIM\_RemoveDirectoryAction**</span></span>](cim-removedirectoryaction.md)
</dt> <dd>

<span data-ttu-id="84916-628">A classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) remove diretórios de elementos de software.</span><span class="sxs-lookup"><span data-stu-id="84916-628">The [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class removes directories for software elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-629">**\_RemoveFile CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-629">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> <dd>

<span data-ttu-id="84916-630">A classe [**CIM \_ removeaction**](cim-removefileaction.md) desinstala arquivos.</span><span class="sxs-lookup"><span data-stu-id="84916-630">The [**CIM\_RemoveFileAction**](cim-removefileaction.md) class uninstalls files.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-631">**Replacement do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-631">**CIM\_ReplacementSet**</span></span>](cim-replacementset.md)
</dt> <dd>

<span data-ttu-id="84916-632">A classe de conjunto de [**\_ substituição CIM**](cim-replacementset.md) agrega elementos físicos que devem ser substituídos juntos.</span><span class="sxs-lookup"><span data-stu-id="84916-632">The [**CIM\_ReplacementSet**](cim-replacementset.md) class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="84916-633">Por exemplo, ao substituir um cartão de memória, os chips de memória do componente também podem ser removidos e substituídos.</span><span class="sxs-lookup"><span data-stu-id="84916-633">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="84916-634">Ou, essa associação pode ser usada para substituir ou atualizar um conjunto de chips de memória.</span><span class="sxs-lookup"><span data-stu-id="84916-634">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-635">**\_RESIDESONEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-635">**CIM\_ResidesOnExtent**</span></span>](cim-residesonextent.md)
</dt> <dd>

<span data-ttu-id="84916-636">A classe [**CIM \_ ResidesOnExtent**](cim-residesonextent.md) representa uma associação entre um sistema de arquivos e a extensão de armazenamento onde ele está localizado.</span><span class="sxs-lookup"><span data-stu-id="84916-636">The [**CIM\_ResidesOnExtent**](cim-residesonextent.md) class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="84916-637">Normalmente, um sistema de arquivos reside em um disco lógico.</span><span class="sxs-lookup"><span data-stu-id="84916-637">Typically, a file system resides on a logical disk.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-638">**\_RUNNINGOS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-638">**CIM\_RunningOS**</span></span>](cim-runningos.md)
</dt> <dd>

<span data-ttu-id="84916-639">A classe [**CIM \_ RunningOS**](cim-runningos.md) representa o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="84916-639">The [**CIM\_RunningOS**](cim-runningos.md) class represents the currently executing operating system.</span></span> <span data-ttu-id="84916-640">No máximo, um sistema operacional pode ser executado a qualquer momento em um sistema de computador; o sistema de computador pode não estar inicializado no momento ou seu sistema operacional pode ser desconhecido.</span><span class="sxs-lookup"><span data-stu-id="84916-640">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-641">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-641">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> <dd>

<span data-ttu-id="84916-642">A classe [**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md) é uma associação entre dois SAPs (pontos de acesso ao serviço), o que indica que o segundo SAP é necessário para que o primeiro SAP se conecte ao seu serviço.</span><span class="sxs-lookup"><span data-stu-id="84916-642">The [**CIM\_SAPSAPDependency**](cim-sapsapdependency.md) class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-643">**\_Scanner CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-643">**CIM\_Scanner**</span></span>](cim-scanner.md)
</dt> <dd>

<span data-ttu-id="84916-644">O [**\_ scanner CIM**](cim-scanner.md) representa os recursos e o gerenciamento do dispositivo lógico do scanner.</span><span class="sxs-lookup"><span data-stu-id="84916-644">The [**CIM\_Scanner**](cim-scanner.md) represents the capabilities and management of the scanner logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-645">**\_SCSICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-645">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dd>

<span data-ttu-id="84916-646">A classe [**CIM \_ SCSIController**](cim-scsicontroller.md) representa os recursos e o gerenciamento do dispositivo lógico do controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="84916-646">The [**CIM\_SCSIController**](cim-scsicontroller.md) class represents the capabilities and management of the SCSI controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-647">**\_SCSIINTERFACE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-647">**CIM\_SCSIInterface**</span></span>](cim-scsiinterface.md)
</dt> <dd>

<span data-ttu-id="84916-648">representa uma relação de [**\_ ControlledBy CIM**](cim-controlledby.md) que indica quais dispositivos são acessados por meio de um controlador SCSI e as características de acesso.</span><span class="sxs-lookup"><span data-stu-id="84916-648">represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-649">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-649">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> <dd>

<span data-ttu-id="84916-650">A classe de [**\_ sensor CIM**](cim-sensor.md) representa um dispositivo de hardware capaz de medir as características de uma propriedade física (por exemplo, as características de temperatura ou voltagem de um sistema de computador unitário).</span><span class="sxs-lookup"><span data-stu-id="84916-650">The [**CIM\_Sensor**](cim-sensor.md) class represents a hardware device that is capable of measuring the characteristics of a physical property (for example, the temperature or voltage characteristics of a unitary computer system).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-651">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-651">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dd>

<span data-ttu-id="84916-652">A classe [**CIM \_ SerialController**](cim-serialcontroller.md) representa os recursos e o gerenciamento do dispositivo lógico da porta serial.</span><span class="sxs-lookup"><span data-stu-id="84916-652">The [**CIM\_SerialController**](cim-serialcontroller.md) class represents the capabilities and management of the serial port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-653">**\_SERIALINTERFACE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-653">**CIM\_SerialInterface**</span></span>](cim-serialinterface.md)
</dt> <dd>

<span data-ttu-id="84916-654">A classe [**CIM \_ SerialInterface**](cim-serialinterface.md) representa um relacionamento [**CIM \_ ControlledBy**](cim-controlledby.md) que indica quais dispositivos são acessados por meio do controlador serial e as características do acesso.</span><span class="sxs-lookup"><span data-stu-id="84916-654">The [**CIM\_SerialInterface**](cim-serialinterface.md) class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-655">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-655">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dd>

<span data-ttu-id="84916-656">A classe de [**\_ serviço CIM**](cim-service.md) representa um elemento lógico que contém informações para representar e gerenciar a funcionalidade fornecida por um dispositivo ou recurso de software.</span><span class="sxs-lookup"><span data-stu-id="84916-656">The [**CIM\_Service**](cim-service.md) class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="84916-657">Um serviço é um objeto de finalidade geral para configurar e gerenciar a implementação da funcionalidade; Ela não é a funcionalidade propriamente dita.</span><span class="sxs-lookup"><span data-stu-id="84916-657">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-658">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-658">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="84916-659">A classe de associação [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) representa os pontos de acesso de um serviço.</span><span class="sxs-lookup"><span data-stu-id="84916-659">The [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md) association class represents the access points for a service.</span></span> <span data-ttu-id="84916-660">Por exemplo, uma impressora pode ser acessada pelos SAPs (pontos de acesso de serviço) do NetWare, do Macintosh ou do Windows, que são potencialmente hospedados em sistemas diferentes.</span><span class="sxs-lookup"><span data-stu-id="84916-660">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-661">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-661">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dd>

<span data-ttu-id="84916-662">A classe [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) representa a capacidade de usar ou invocar um serviço.</span><span class="sxs-lookup"><span data-stu-id="84916-662">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="84916-663">Os pontos de acesso representam serviços que estão disponíveis para uso por outras entidades.</span><span class="sxs-lookup"><span data-stu-id="84916-663">Access points represent services that are available for use by other entities.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-664">**\_SERVICESAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-664">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> <dd>

<span data-ttu-id="84916-665">A classe [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) representa uma associação entre um serviço e um ponto de acesso de serviço (SAP), que indica que o SAP referenciado é usado pelo serviço para fornecer sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="84916-665">The [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-666">**\_SERVICESERVICEDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-666">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dd>

<span data-ttu-id="84916-667">A classe [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) representa uma associação entre dois serviços.</span><span class="sxs-lookup"><span data-stu-id="84916-667">The [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) class represents an association between two services.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-668">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-668">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="84916-669">A classe de [**\_ configuração CIM**](cim-setting.md) representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="84916-669">The [**CIM\_Setting**](cim-setting.md) class represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-670">**\_SETTINGCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-670">**CIM\_SettingCheck**</span></span>](cim-settingcheck.md)
</dt> <dd>

<span data-ttu-id="84916-671">A classe [**CIM \_ SettingCheck**](cim-settingcheck.md) especifica as informações necessárias para verificar um arquivo de configuração específico em busca de uma entrada específica que contenha um valor igual ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="84916-671">The [**CIM\_SettingCheck**](cim-settingcheck.md) class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="84916-672">Todas as comparações são consideradas não diferenciando maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84916-672">All comparisons are assumed to be case insensitive.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-673">**\_SETTINGCONTEXT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-673">**CIM\_SettingContext**</span></span>](cim-settingcontext.md)
</dt> <dd>

<span data-ttu-id="84916-674">A classe [**CIM \_ SettingContext**](cim-settingcontext.md) associa objetos de configuração a objetos de configuração.</span><span class="sxs-lookup"><span data-stu-id="84916-674">The [**CIM\_SettingContext**](cim-settingcontext.md) class associates configuration objects with setting objects.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-675">**\_Slot CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-675">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dd>

<span data-ttu-id="84916-676">A classe de [**\_ slot CIM**](cim-slot.md) representa conectores nos quais os pacotes são inseridos.</span><span class="sxs-lookup"><span data-stu-id="84916-676">The [**CIM\_Slot**](cim-slot.md) class represents connectors into which packages are inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-677">**\_SLOTINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-677">**CIM\_SlotInSlot**</span></span>](cim-slotinslot.md)
</dt> <dd>

<span data-ttu-id="84916-678">A relação de [**\_ SlotInSlot do CIM**](cim-slotinslot.md) representa a capacidade de um adaptador especial estender a estrutura de slot existente para permitir que cartões incompatíveis sejam conectados a um quadro ou placa de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="84916-678">The [**CIM\_SlotInSlot**](cim-slotinslot.md) relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-679">**\_Software CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-679">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> <dd>

<span data-ttu-id="84916-680">A classe [**CIM \_ softwareelement**](cim-softwareelement.md) decompõe um objeto [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) em um conjunto de partes individuais gerenciáveis ou implantáveis para uma plataforma específica.</span><span class="sxs-lookup"><span data-stu-id="84916-680">The [**CIM\_SoftwareElement**](cim-softwareelement.md) class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="84916-681">A plataforma de um elemento de software é identificada exclusivamente por sua arquitetura de hardware e sistema operacional subjacentes.</span><span class="sxs-lookup"><span data-stu-id="84916-681">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-682">**\_SOFTWAREELEMENTACTIONS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-682">**CIM\_SoftwareElementActions**</span></span>](cim-softwareelementactions.md)
</dt> <dd>

<span data-ttu-id="84916-683">A associação [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) identifica as ações para um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="84916-683">The [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association identifies the actions for a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-684">**\_SOFTWAREELEMENTCHECKS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-684">**CIM\_SoftwareElementChecks**</span></span>](cim-softwareelementchecks.md)
</dt> <dd>

<span data-ttu-id="84916-685">A classe de associação [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) relaciona um elemento de software com informações de condição ou local que um recurso pode exigir.</span><span class="sxs-lookup"><span data-stu-id="84916-685">The [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association class relates a software element with condition or location information that a feature may require.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-686">**\_SOFTWAREELEMENTVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-686">**CIM\_SoftwareElementVersionCheck**</span></span>](cim-softwareelementversioncheck.md)
</dt> <dd>

<span data-ttu-id="84916-687">A classe [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) representa um tipo de elemento de software que deve existir no ambiente.</span><span class="sxs-lookup"><span data-stu-id="84916-687">The [**CIM\_SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) class represents a type of software element that must exist in the environment.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-688">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-688">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> <dd>

<span data-ttu-id="84916-689">A classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) representa uma função ou um recurso específico de um produto ou sistema de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="84916-689">The [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class represents a particular function or capability of a product or application system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-690">**\_SOFTWAREFEATURESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-690">**CIM\_SoftwareFeatureSAPImplementation**</span></span>](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

<span data-ttu-id="84916-691">A classe [**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado no software.</span><span class="sxs-lookup"><span data-stu-id="84916-691">The [**CIM\_SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-692">**\_SOFTWAREFEATURESERVICEIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-692">**CIM\_SoftwareFeatureServiceImplementation**</span></span>](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="84916-693">A classe [**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) representa uma associação entre um serviço e como ele é implementado no software.</span><span class="sxs-lookup"><span data-stu-id="84916-693">The [**CIM\_SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) class represents an association between a service and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-694">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-694">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

<span data-ttu-id="84916-695">A associação [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) identifica os elementos de software que compõem um recurso de software específico.</span><span class="sxs-lookup"><span data-stu-id="84916-695">The [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) association identifies the software elements that make up a specific software feature.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-696">**Telespare CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-696">**CIM\_SpareGroup**</span></span>](cim-sparegroup.md)
</dt> <dd>

<span data-ttu-id="84916-697">A classe de [**\_ Spar sobressalente CIM**](cim-sparegroup.md) é derivada da classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) e indica que um ou mais dos elementos agregados podem ser resobrados.</span><span class="sxs-lookup"><span data-stu-id="84916-697">The [**CIM\_SpareGroup**](cim-sparegroup.md) class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-698">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-698">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dd>

<span data-ttu-id="84916-699">A classe [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) é uma classe raiz para a coleção arbitrária de dados estatísticos ou métricas aplicáveis a um ou mais elementos do sistema gerenciados.</span><span class="sxs-lookup"><span data-stu-id="84916-699">The [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-700">**Estatísticas de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-700">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> <dd>

<span data-ttu-id="84916-701">A classe [**CIM \_ Statistics**](cim-statistics.md) representa uma associação que relaciona os elementos do sistema gerenciado aos grupos estatísticos que se aplicam a eles.</span><span class="sxs-lookup"><span data-stu-id="84916-701">The [**CIM\_Statistics**](cim-statistics.md) class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-702">**\_STORAGEDEFECT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-702">**CIM\_StorageDefect**</span></span>](cim-storagedefect.md)
</dt> <dd>

<span data-ttu-id="84916-703">A agregação [**CIM \_ StorageDefect**](cim-storagedefect.md) coleta os erros de armazenamento para uma extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84916-703">The [**CIM\_StorageDefect**](cim-storagedefect.md) aggregation collects the storage errors for a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-704">**\_STORAGEERROR CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-704">**CIM\_StorageError**</span></span>](cim-storageerror.md)
</dt> <dd>

<span data-ttu-id="84916-705">A classe [**CIM \_ StorageError**](cim-storageerror.md) representa blocos de mídia ou espaço de memória que são mapeados fora de uso devido a erros.</span><span class="sxs-lookup"><span data-stu-id="84916-705">The [**CIM\_StorageError**](cim-storageerror.md) class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="84916-706">A chave da classe é a propriedade **StartingAddress** dos bytes em erro.</span><span class="sxs-lookup"><span data-stu-id="84916-706">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-707">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-707">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dd>

<span data-ttu-id="84916-708">A classe [**CIM \_ StorageExtent**](cim-storageextent.md) representa os recursos e o gerenciamento de várias mídias que existem para armazenar dados e permitir a recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="84916-708">The [**CIM\_StorageExtent**](cim-storageextent.md) class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="84916-709">Essa classe pai pode representar os vários componentes de RAID (hardware ou software) ou uma extensão lógica bruta na parte superior da mídia física.</span><span class="sxs-lookup"><span data-stu-id="84916-709">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-710">**\_STORAGEREDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-710">**CIM\_StorageRedundancyGroup**</span></span>](cim-storageredundancygroup.md)
</dt> <dd>

<span data-ttu-id="84916-711">A classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) representa informações de redundância relacionadas ao armazenamento em massa.</span><span class="sxs-lookup"><span data-stu-id="84916-711">The [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class represents mass storage-related redundancy information.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-712">**\_SUPPORTACCESS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-712">**CIM\_SupportAccess**</span></span>](cim-supportaccess.md)
</dt> <dd>

<span data-ttu-id="84916-713">A classe [**CIM \_ SupportAccess**](cim-supportaccess.md) define como obter assistência para um produto.</span><span class="sxs-lookup"><span data-stu-id="84916-713">The [**CIM\_SupportAccess**](cim-supportaccess.md) class defines how to obtain assistance for a product.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-714">**\_SWAPSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-714">**CIM\_SwapSpaceCheck**</span></span>](cim-swapspacecheck.md)
</dt> <dd>

<span data-ttu-id="84916-715">A classe [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) especifica a quantidade de espaço de permuta que deve estar disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="84916-715">The [**CIM\_SwapSpaceCheck**](cim-swapspacecheck.md) class specifies the amount of swap space that must be available on the system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-716">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-716">**CIM\_System**</span></span>](cim-system.md)
</dt> <dd>

<span data-ttu-id="84916-717">A classe de [**\_ sistema CIM**](cim-system.md) agrega um conjunto enumerável de elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="84916-717">The [**CIM\_System**](cim-system.md) class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="84916-718">A agregação funciona como um todo funcional.</span><span class="sxs-lookup"><span data-stu-id="84916-718">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="84916-719">Em qualquer subclasse específica do sistema, há uma lista bem definida de classes de elementos do sistema gerenciado cujas instâncias devem ser agregadas.</span><span class="sxs-lookup"><span data-stu-id="84916-719">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-720">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-720">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dd>

<span data-ttu-id="84916-721">uma classe de associação de modelo CIM (CIM) que estabelece relações entre um sistema e os elementos do sistema gerenciado dos quais ele é composto.</span><span class="sxs-lookup"><span data-stu-id="84916-721">a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-722">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-722">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dd>

<span data-ttu-id="84916-723">A associação [**CIM \_ SystemDevice**](cim-systemdevice.md) representa uma relação explícita na qual os dispositivos lógicos podem ser agregados por um sistema.</span><span class="sxs-lookup"><span data-stu-id="84916-723">The [**CIM\_SystemDevice**](cim-systemdevice.md) association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-724">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-724">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dd>

<span data-ttu-id="84916-725">A classe [**CIM \_ SystemResource**](cim-systemresource.md) representa uma entidade gerenciada pelo BIOS ou um sistema operacional que está disponível para uso por software e dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="84916-725">The [**CIM\_SystemResource**](cim-systemresource.md) class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-726">**\_Tacômetro CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-726">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> <dd>

<span data-ttu-id="84916-727">A classe do [**\_ tacômetro CIM**](cim-tachometer.md) existe para compatibilidade com versões anteriores de definições de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="84916-727">The [**CIM\_Tachometer**](cim-tachometer.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-728">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-728">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dd>

<span data-ttu-id="84916-729">A classe [**CIM \_ TapeDrive**](cim-tapedrive.md) representa uma unidade de fita no sistema.</span><span class="sxs-lookup"><span data-stu-id="84916-729">The [**CIM\_TapeDrive**](cim-tapedrive.md) class represents a tape drive on the system.</span></span> <span data-ttu-id="84916-730">As unidades de fita são basicamente diferenciadas, pois só podem ser acessadas sequencialmente.</span><span class="sxs-lookup"><span data-stu-id="84916-730">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-731">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-731">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dd>

<span data-ttu-id="84916-732">A classe [**CIM \_ sensor**](cim-temperaturesensor.md) existe para compatibilidade com versões anteriores de definições de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="84916-732">The [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-733">**\_Thread CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-733">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dd>

<span data-ttu-id="84916-734">A classe de [**\_ thread CIM**](cim-thread.md) representa a capacidade de executar unidades de um processo ou tarefa, em paralelo.</span><span class="sxs-lookup"><span data-stu-id="84916-734">The [**CIM\_Thread**](cim-thread.md) class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="84916-735">Um processo pode ter muitos threads, cada um dos quais é fraco para o processo.</span><span class="sxs-lookup"><span data-stu-id="84916-735">A process can have many threads, each of which is weak to the process.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-736">**CIM \_ Todirectoryaction**</span><span class="sxs-lookup"><span data-stu-id="84916-736">**CIM\_ToDirectoryAction**</span></span>](cim-todirectoryaction.md)
</dt> <dd>

<span data-ttu-id="84916-737">A associação [**CIM \_ todirectoryaction**](cim-todirectoryaction.md) identifica o diretório de destino para a ação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="84916-737">The [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-738">**\_TODIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-738">**CIM\_ToDirectorySpecification**</span></span>](cim-todirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="84916-739">A associação [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) identifica o diretório de destino para a ação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="84916-739">The [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-740">**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-740">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> <dd>

<span data-ttu-id="84916-741">A classe [**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) representa os recursos e o gerenciamento de uma fonte de energia ininterrupta (UPS).</span><span class="sxs-lookup"><span data-stu-id="84916-741">The [**CIM\_UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="84916-742">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-742">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dd>

<span data-ttu-id="84916-743">A classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) representa um computador desktop, móvel, de rede, servidor ou outro tipo de sistema de computador de nó único.</span><span class="sxs-lookup"><span data-stu-id="84916-743">The [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-744">**\_USBCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-744">**CIM\_USBController**</span></span>](cim-usbcontroller.md)
</dt> <dd>

<span data-ttu-id="84916-745">A classe [**CIM \_ USBController**](cim-usbcontroller.md) representa os recursos e o gerenciamento de um controlador USB.</span><span class="sxs-lookup"><span data-stu-id="84916-745">The [**CIM\_USBController**](cim-usbcontroller.md) class represents the capabilities and management of a USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-746">**\_USBCONTROLLERHASHUB CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-746">**CIM\_USBControllerHasHub**</span></span>](cim-usbcontrollerhashub.md)
</dt> <dd>

<span data-ttu-id="84916-747">A classe [**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) define os hubs que são DOWNSTREAM do controlador USB.</span><span class="sxs-lookup"><span data-stu-id="84916-747">The [**CIM\_USBControllerHasHub**](cim-usbcontrollerhashub.md) class defines the hubs that are downstream of the USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-748">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-748">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> <dd>

<span data-ttu-id="84916-749">A classe [**CIM \_ UsbDevice**](cim-usbdevice.md) representa as características de gerenciamento de um dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="84916-749">The [**CIM\_USBDevice**](cim-usbdevice.md) class represents the management characteristics of a USB device.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-750">**CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="84916-750">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> <dd>

<span data-ttu-id="84916-751">A classe [**CIM \_ USBHub**](cim-usbhub.md) representa os recursos e o gerenciamento de um hub USB.</span><span class="sxs-lookup"><span data-stu-id="84916-751">The [**CIM\_USBHub**](cim-usbhub.md) class represents the capabilities and management of a USB hub.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-752">**Userdevice do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84916-752">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dd>

<span data-ttu-id="84916-753">A classe [**CIM \_ userdevice**](cim-userdevice.md) é uma classe pai da qual outras classes, como o [**CIM \_ Keyboard**](cim-keyboard.md) ou [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md), descendem.</span><span class="sxs-lookup"><span data-stu-id="84916-753">The [**CIM\_UserDevice**](cim-userdevice.md) class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="84916-754">Os dispositivos de usuário são dispositivos lógicos que permitem que o usuário de um sistema de computador insira, exiba ou Ouça dados.</span><span class="sxs-lookup"><span data-stu-id="84916-754">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-755">**\_VERSIONCOMPATIBILITYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-755">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> <dd>

<span data-ttu-id="84916-756">A classe [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) especifica se é permitido criar o próximo estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="84916-756">The [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class specifies whether it is permissible to create the next state of a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-757">**\_VIDEOBIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-757">**CIM\_VideoBIOSElement**</span></span>](cim-videobioselement.md)
</dt> <dd>

<span data-ttu-id="84916-758">A classe [**CIM \_ VideoBIOSElement**](cim-videobioselement.md) representa o software de nível baixo que é carregado no armazenamento não volátil e usado para configurar e acessar o controlador de vídeo de um sistema de computador e exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="84916-758">The [**CIM\_VideoBIOSElement**](cim-videobioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-759">**\_VIDEOBIOSFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-759">**CIM\_VideoBIOSFeature**</span></span>](cim-videobiosfeature.md)
</dt> <dd>

<span data-ttu-id="84916-760">A classe [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) representa os recursos do software de baixo nível usado para configurar e acessar o controlador de vídeo de um sistema de computador e exibir o.</span><span class="sxs-lookup"><span data-stu-id="84916-760">The [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-761">**\_VIDEOBIOSFEATUREVIDEOBIOSELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-761">**CIM\_VideoBIOSFeatureVideoBIOSElements**</span></span>](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

<span data-ttu-id="84916-762">A classe [**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) associa um recurso de BIOS de vídeo e seus elementos de BIOS de vídeo agregados.</span><span class="sxs-lookup"><span data-stu-id="84916-762">The [**CIM\_VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-763">**\_VIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-763">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> <dd>

<span data-ttu-id="84916-764">A classe [**CIM \_ VideoController**](cim-videocontroller.md) representa os recursos e o gerenciamento do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="84916-764">The [**CIM\_VideoController**](cim-videocontroller.md) class represents the capabilities and management of the video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-765">**\_VIDEOCONTROLLERRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-765">**CIM\_VideoControllerResolution**</span></span>](cim-videocontrollerresolution.md)
</dt> <dd>

<span data-ttu-id="84916-766">A classe [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) representa os vários modos de vídeo aos quais um controlador de vídeo pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="84916-766">The [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class represents the various video modes that a video controller can support.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-767">**\_VIDEOSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-767">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dd>

<span data-ttu-id="84916-768">A classe [**CIM \_ VideoSetting**](cim-videosetting.md) associa o objeto de configuração [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) ao controlador ao qual ele se aplica.</span><span class="sxs-lookup"><span data-stu-id="84916-768">The [**CIM\_VideoSetting**](cim-videosetting.md) class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-769">**\_VOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-769">**CIM\_VolatileStorage**</span></span>](cim-volatilestorage.md)
</dt> <dd>

<span data-ttu-id="84916-770">A classe [**CIM \_ VolatileStorage**](cim-volatilestorage.md) representa os recursos e o gerenciamento do armazenamento volátil.</span><span class="sxs-lookup"><span data-stu-id="84916-770">The [**CIM\_VolatileStorage**](cim-volatilestorage.md) class represents the capabilities and management of volatile storage.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-771">**\_Voltagem CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-771">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dd>

<span data-ttu-id="84916-772">A classe [**CIM \_ voltagem**](cim-voltagesensor.md) existe para compatibilidade com versões anteriores de definições de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="84916-772">The [**CIM\_VoltageSensor**](cim-voltagesensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="84916-773">Com adições às classes [**do \_ sensor CIM**](cim-sensor.md) e do [**cim \_ NumericSensor**](cim-numericsensor.md) na versão 2,2, ela não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="84916-773">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-774">**\_Volumeset CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-774">**CIM\_VolumeSet**</span></span>](cim-volumeset.md)
</dt> <dd>

<span data-ttu-id="84916-775">A classe [**CIM \_ volumeset**](cim-volumeset.md) representa um intervalo contíguo de blocos lógicos apresentados ao ambiente operacional para leitura e gravação de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="84916-775">The [**CIM\_VolumeSet**](cim-volumeset.md) class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span>

</dd> <dt>

[<span data-ttu-id="84916-776">**\_WORMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="84916-776">**CIM\_WORMDrive**</span></span>](cim-wormdrive.md)
</dt> <dd>

<span data-ttu-id="84916-777">A classe [**CIM \_ WORMDrive**](cim-wormdrive.md) representa os recursos e o gerenciamento de uma unidade de worm, um subtipo do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="84916-777">The [**CIM\_WORMDrive**](cim-wormdrive.md) class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

</dd> </dl>

 

 
