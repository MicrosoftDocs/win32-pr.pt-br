---
description: A \_ classe de CPU HWConfig é a classe de tipo de evento para eventos de configuração de CPU. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: Classe HWConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 493952e25080d4a64e018477ca1b45033c8747af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967581"
---
# <a name="hwconfig_cpu-class"></a><span data-ttu-id="19752-104">\_Classe de CPU HWConfig</span><span class="sxs-lookup"><span data-stu-id="19752-104">HWConfig\_CPU class</span></span>

<span data-ttu-id="19752-105">A classe de **\_ CPU HWConfig** é a classe de tipo de evento para eventos de configuração de CPU.</span><span class="sxs-lookup"><span data-stu-id="19752-105">The **HWConfig\_CPU** class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="19752-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="19752-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="19752-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19752-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a><span data-ttu-id="19752-108">Membros</span><span class="sxs-lookup"><span data-stu-id="19752-108">Members</span></span>

<span data-ttu-id="19752-109">A classe de **\_ CPU HWConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="19752-109">The **HWConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="19752-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="19752-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19752-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="19752-111">Properties</span></span>

<span data-ttu-id="19752-112">A classe de **\_ CPU HWConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="19752-112">The **HWConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19752-113">AllocationGranularity</span><span class="sxs-lookup"><span data-stu-id="19752-113">AllocationGranularity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19752-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19752-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19752-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19752-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19752-116">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="19752-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="19752-117">Granularidade com a qual a memória virtual é alocada.</span><span class="sxs-lookup"><span data-stu-id="19752-117">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="19752-118">ComputerName</span><span class="sxs-lookup"><span data-stu-id="19752-118">ComputerName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19752-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19752-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19752-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19752-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19752-121">Qualificadores: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="19752-121">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="19752-122">Nome do computador.</span><span class="sxs-lookup"><span data-stu-id="19752-122">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="19752-123">MemSize</span><span class="sxs-lookup"><span data-stu-id="19752-123">MemSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19752-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19752-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19752-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19752-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19752-126">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="19752-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="19752-127">Quantidade total de memória física disponível para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="19752-127">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="19752-128">GHz</span><span class="sxs-lookup"><span data-stu-id="19752-128">MHz</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19752-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19752-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19752-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19752-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19752-131">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="19752-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="19752-132">Velocidade máxima do processador, em megahertz.</span><span class="sxs-lookup"><span data-stu-id="19752-132">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="19752-133">NumberOfProcessors</span><span class="sxs-lookup"><span data-stu-id="19752-133">NumberOfProcessors</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19752-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19752-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19752-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19752-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19752-136">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="19752-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="19752-137">Número de processadores no computador.</span><span class="sxs-lookup"><span data-stu-id="19752-137">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="19752-138">PageSize</span><span class="sxs-lookup"><span data-stu-id="19752-138">PageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19752-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19752-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19752-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19752-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19752-141">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="19752-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="19752-142">Tamanho de uma página de permuta, em bytes.</span><span class="sxs-lookup"><span data-stu-id="19752-142">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19752-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19752-143">Requirements</span></span>



| <span data-ttu-id="19752-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="19752-144">Requirement</span></span> | <span data-ttu-id="19752-145">Valor</span><span class="sxs-lookup"><span data-stu-id="19752-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="19752-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19752-146">Minimum supported client</span></span><br/> | <span data-ttu-id="19752-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="19752-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="19752-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19752-148">Minimum supported server</span></span><br/> | <span data-ttu-id="19752-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="19752-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="19752-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="19752-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19752-151">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="19752-151">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




