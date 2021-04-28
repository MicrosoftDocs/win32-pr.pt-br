---
description: Classe SystemConfig_CPU-essa classe é a classe de tipo de evento para eventos de configuração de CPU.
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: Classe SystemConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 07efa01bf58aeadfdfe12cd5db4d010a7f6dbca0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106114"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="b510f-103">\_Classe de CPU SystemConfig</span><span class="sxs-lookup"><span data-stu-id="b510f-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="b510f-104">Essa classe é a classe de tipo de evento para eventos de configuração de CPU.</span><span class="sxs-lookup"><span data-stu-id="b510f-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="b510f-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="b510f-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b510f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b510f-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a><span data-ttu-id="b510f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b510f-107">Members</span></span>

<span data-ttu-id="b510f-108">A classe de **\_ CPU SystemConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b510f-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="b510f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b510f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b510f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b510f-110">Properties</span></span>

<span data-ttu-id="b510f-111">A classe de **\_ CPU SystemConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b510f-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b510f-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="b510f-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b510f-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b510f-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b510f-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b510f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b510f-115">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="b510f-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="b510f-116">Granularidade com a qual a memória virtual é alocada.</span><span class="sxs-lookup"><span data-stu-id="b510f-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="b510f-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="b510f-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b510f-118">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="b510f-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b510f-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b510f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b510f-120">Qualificadores: **WmiDataId** (6), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b510f-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b510f-121">Nome do computador.</span><span class="sxs-lookup"><span data-stu-id="b510f-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b510f-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="b510f-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b510f-123">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="b510f-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b510f-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b510f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b510f-125">Qualificadores: **WmiDataId** (7), **Max** (132), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b510f-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b510f-126">Nome do domínio no qual o computador é membro.</span><span class="sxs-lookup"><span data-stu-id="b510f-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="b510f-127">**HyperThreadingFlag**</span><span class="sxs-lookup"><span data-stu-id="b510f-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b510f-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b510f-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b510f-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b510f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b510f-130">Qualificadores: **WmiDataId** (8), ponteiro</span><span class="sxs-lookup"><span data-stu-id="b510f-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b510f-131">Indica se a opção de hyperthreading está ativada ou desativada para um processador.</span><span class="sxs-lookup"><span data-stu-id="b510f-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="b510f-132">Cada bit reflete o estado do hyperthreading de uma CPU no computador.</span><span class="sxs-lookup"><span data-stu-id="b510f-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b510f-133">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="b510f-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b510f-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b510f-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b510f-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b510f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b510f-136">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="b510f-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="b510f-137">Quantidade total de memória física disponível para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b510f-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="b510f-138">**GHz**</span><span class="sxs-lookup"><span data-stu-id="b510f-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b510f-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b510f-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b510f-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b510f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b510f-141">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="b510f-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="b510f-142">Velocidade máxima do processador, em megahertz.</span><span class="sxs-lookup"><span data-stu-id="b510f-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="b510f-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="b510f-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b510f-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b510f-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b510f-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b510f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b510f-146">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="b510f-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="b510f-147">Número de processadores no computador.</span><span class="sxs-lookup"><span data-stu-id="b510f-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b510f-148">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="b510f-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b510f-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b510f-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b510f-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b510f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b510f-151">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="b510f-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="b510f-152">Tamanho de uma página de permuta, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b510f-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b510f-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b510f-153">Requirements</span></span>



| <span data-ttu-id="b510f-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="b510f-154">Requirement</span></span> | <span data-ttu-id="b510f-155">Valor</span><span class="sxs-lookup"><span data-stu-id="b510f-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b510f-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b510f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b510f-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b510f-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b510f-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b510f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b510f-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b510f-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b510f-160">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b510f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b510f-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="b510f-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




