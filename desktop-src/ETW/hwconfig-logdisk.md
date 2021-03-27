---
description: A \_ classe HWConfig LogDisk é a classe de tipo de evento para eventos de configuração de disco lógico. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: Classe HWConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506138"
---
# <a name="hwconfig_logdisk-class"></a><span data-ttu-id="79d82-104">\_Classe HWConfig LogDisk</span><span class="sxs-lookup"><span data-stu-id="79d82-104">HWConfig\_LogDisk class</span></span>

<span data-ttu-id="79d82-105">A classe **HWConfig \_ LogDisk** é a classe de tipo de evento para eventos de configuração de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="79d82-105">The **HWConfig\_LogDisk** class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="79d82-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="79d82-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d82-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79d82-107">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a><span data-ttu-id="79d82-108">Membros</span><span class="sxs-lookup"><span data-stu-id="79d82-108">Members</span></span>

<span data-ttu-id="79d82-109">A classe **HWConfig \_ LogDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="79d82-109">The **HWConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="79d82-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="79d82-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79d82-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="79d82-111">Properties</span></span>

<span data-ttu-id="79d82-112">A classe **HWConfig \_ LogDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="79d82-112">The **HWConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79d82-113">DiskNumber</span><span class="sxs-lookup"><span data-stu-id="79d82-113">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d82-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79d82-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79d82-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79d82-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79d82-116">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="79d82-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="79d82-117">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="79d82-117">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="79d82-118">Pad</span><span class="sxs-lookup"><span data-stu-id="79d82-118">Pad</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d82-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79d82-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79d82-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79d82-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79d82-121">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="79d82-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="79d82-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="79d82-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="79d82-123">PartitionSize</span><span class="sxs-lookup"><span data-stu-id="79d82-123">PartitionSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d82-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79d82-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79d82-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79d82-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79d82-126">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="79d82-126">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="79d82-127">Tamanho total da partição, em bytes.</span><span class="sxs-lookup"><span data-stu-id="79d82-127">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="79d82-128">StartOffset</span><span class="sxs-lookup"><span data-stu-id="79d82-128">StartOffset</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79d82-129">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79d82-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79d82-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79d82-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79d82-131">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="79d82-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="79d82-132">Deslocamento inicial (em bytes) da partição desde o início do disco.</span><span class="sxs-lookup"><span data-stu-id="79d82-132">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79d82-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79d82-133">Requirements</span></span>



| <span data-ttu-id="79d82-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="79d82-134">Requirement</span></span> | <span data-ttu-id="79d82-135">Valor</span><span class="sxs-lookup"><span data-stu-id="79d82-135">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="79d82-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79d82-136">Minimum supported client</span></span><br/> | <span data-ttu-id="79d82-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="79d82-137">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="79d82-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79d82-138">Minimum supported server</span></span><br/> | <span data-ttu-id="79d82-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="79d82-139">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="79d82-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="79d82-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d82-141">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="79d82-141">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




