---
description: Classe SystemConfig_V0_CPU-essa classe é a classe de tipo de evento para eventos de configuração de CPU.
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
ms.openlocfilehash: de3b63def40cb6ead40f6f4c95625603cfc581ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105984"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="16014-103">\_Classe de \_ CPU SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="16014-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="16014-104">Essa classe é a classe de tipo de evento para eventos de configuração de CPU.</span><span class="sxs-lookup"><span data-stu-id="16014-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="16014-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="16014-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="16014-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16014-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="16014-107">Membros</span><span class="sxs-lookup"><span data-stu-id="16014-107">Members</span></span>

<span data-ttu-id="16014-108">A classe de **\_ \_ CPU SystemConfig V0** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="16014-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="16014-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16014-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16014-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16014-110">Properties</span></span>

<span data-ttu-id="16014-111">A classe de **\_ \_ CPU SystemConfig V0** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="16014-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16014-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="16014-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16014-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16014-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16014-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16014-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16014-115">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="16014-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="16014-116">Granularidade com a qual a memória virtual é alocada.</span><span class="sxs-lookup"><span data-stu-id="16014-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="16014-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="16014-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16014-118">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="16014-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="16014-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16014-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16014-120">Qualificadores: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="16014-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="16014-121">Nome do computador.</span><span class="sxs-lookup"><span data-stu-id="16014-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="16014-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="16014-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16014-123">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="16014-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="16014-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16014-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16014-125">Qualificadores: **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="16014-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="16014-126">Nome do domínio no qual o computador é membro.</span><span class="sxs-lookup"><span data-stu-id="16014-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="16014-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="16014-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16014-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16014-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16014-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16014-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16014-130">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="16014-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="16014-131">Quantidade total de memória física disponível para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="16014-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="16014-132">**GHz**</span><span class="sxs-lookup"><span data-stu-id="16014-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16014-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16014-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16014-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16014-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16014-135">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="16014-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="16014-136">Velocidade máxima do processador, em megahertz.</span><span class="sxs-lookup"><span data-stu-id="16014-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="16014-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="16014-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16014-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16014-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16014-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16014-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16014-140">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="16014-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="16014-141">Número de processadores no computador.</span><span class="sxs-lookup"><span data-stu-id="16014-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="16014-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="16014-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16014-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16014-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16014-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16014-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16014-145">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="16014-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="16014-146">Tamanho de uma página de permuta, em bytes.</span><span class="sxs-lookup"><span data-stu-id="16014-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16014-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16014-147">Requirements</span></span>



| <span data-ttu-id="16014-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="16014-148">Requirement</span></span> | <span data-ttu-id="16014-149">Valor</span><span class="sxs-lookup"><span data-stu-id="16014-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16014-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16014-150">Minimum supported client</span></span><br/> | <span data-ttu-id="16014-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="16014-151">None supported</span></span><br/>                            |
| <span data-ttu-id="16014-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16014-152">Minimum supported server</span></span><br/> | <span data-ttu-id="16014-153">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="16014-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16014-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="16014-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16014-155">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="16014-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




