---
description: Essa classe é a classe de tipo de evento para eventos de configuração de CPU.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: Classe SystemConfig_V0_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6963201f76afa40e9b1741dc2936fa2ab4433a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922557"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="c33a0-103">\_Classe de \_ CPU SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="c33a0-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="c33a0-104">Essa classe é a classe de tipo de evento para eventos de configuração de CPU.</span><span class="sxs-lookup"><span data-stu-id="c33a0-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="c33a0-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c33a0-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33a0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c33a0-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a><span data-ttu-id="c33a0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c33a0-107">Members</span></span>

<span data-ttu-id="c33a0-108">A classe de **\_ \_ CPU SystemConfig V0** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c33a0-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="c33a0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c33a0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c33a0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c33a0-110">Properties</span></span>

<span data-ttu-id="c33a0-111">A classe de **\_ \_ CPU SystemConfig V0** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c33a0-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c33a0-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="c33a0-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33a0-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33a0-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33a0-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-115">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="c33a0-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c33a0-116">Granularidade com a qual a memória virtual é alocada.</span><span class="sxs-lookup"><span data-stu-id="c33a0-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="c33a0-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="c33a0-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33a0-118">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="c33a0-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33a0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-120">Qualificadores: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c33a0-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c33a0-121">Nome do computador.</span><span class="sxs-lookup"><span data-stu-id="c33a0-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c33a0-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="c33a0-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33a0-123">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="c33a0-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33a0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-125">Qualificadores: **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="c33a0-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="c33a0-126">Nome do domínio no qual o computador é membro.</span><span class="sxs-lookup"><span data-stu-id="c33a0-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="c33a0-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="c33a0-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33a0-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33a0-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33a0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-130">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="c33a0-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c33a0-131">Quantidade total de memória física disponível para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c33a0-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c33a0-132">**GHz**</span><span class="sxs-lookup"><span data-stu-id="c33a0-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33a0-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33a0-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33a0-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-135">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="c33a0-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c33a0-136">Velocidade máxima do processador, em megahertz.</span><span class="sxs-lookup"><span data-stu-id="c33a0-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="c33a0-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="c33a0-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33a0-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33a0-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33a0-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-140">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="c33a0-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c33a0-141">Número de processadores no computador.</span><span class="sxs-lookup"><span data-stu-id="c33a0-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c33a0-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="c33a0-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33a0-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33a0-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33a0-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33a0-145">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="c33a0-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="c33a0-146">Tamanho de uma página de permuta, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c33a0-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c33a0-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c33a0-147">Requirements</span></span>



| <span data-ttu-id="c33a0-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33a0-148">Requirement</span></span> | <span data-ttu-id="c33a0-149">Valor</span><span class="sxs-lookup"><span data-stu-id="c33a0-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c33a0-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c33a0-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c33a0-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c33a0-151">None supported</span></span><br/>                            |
| <span data-ttu-id="c33a0-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c33a0-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c33a0-153">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c33a0-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c33a0-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="c33a0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33a0-155">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c33a0-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




