---
description: Essa classe é a classe de tipo de evento para eventos de falha de página de hardware. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: Classe PageFault_HardFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 08afd3df20260a8ede63f4d741b3045ce3a39c1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922055"
---
# <a name="pagefault_hardfault-class"></a><span data-ttu-id="5b8a2-104">\_Classe falhadepágina HardFault</span><span class="sxs-lookup"><span data-stu-id="5b8a2-104">PageFault\_HardFault class</span></span>

<span data-ttu-id="5b8a2-105">Essa classe é a classe de tipo de evento para eventos de falha de página de hardware.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-105">This class is the event type class for hard page fault events.</span></span>

<span data-ttu-id="5b8a2-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b8a2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b8a2-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a><span data-ttu-id="5b8a2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5b8a2-108">Members</span></span>

<span data-ttu-id="5b8a2-109">A classe **falhadepágina \_ HardFault** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b8a2-109">The **PageFault\_HardFault** class has these types of members:</span></span>

-   [<span data-ttu-id="5b8a2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b8a2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b8a2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b8a2-111">Properties</span></span>

<span data-ttu-id="5b8a2-112">A classe **falhadepágina \_ HardFault** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-112">The **PageFault\_HardFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b8a2-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b8a2-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b8a2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-116">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="5b8a2-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="5b8a2-117">Quantidade de dados lidos de ReadOffset para satisfazer a falha.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-117">Amount of data read from ReadOffset to satisfy the fault.</span></span>

</dd> <dt>

<span data-ttu-id="5b8a2-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b8a2-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b8a2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-121">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5b8a2-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5b8a2-122">Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**de \_ nome de FileIo**](fileio-name.md) para determinar o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-122">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="5b8a2-123">**Inicialtime**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-123">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b8a2-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b8a2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-126">Qualificadores: WmiDataId (1), extensão ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="5b8a2-126">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="5b8a2-127">Carimbo de data/hora de início em que a falha de página ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-127">Start time stamp at which page fault occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5b8a2-128">**ReadOffset**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-128">**ReadOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b8a2-129">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b8a2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-131">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="5b8a2-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="5b8a2-132">Deslocamento de arquivo do qual os dados foram lidos para atender à falha.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-132">File offset from which data was read to satisfy fault.</span></span>

</dd> <dt>

<span data-ttu-id="5b8a2-133">**TThreadId**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-133">**TThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b8a2-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b8a2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-136">Qualificadores: WmiDataId (5), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="5b8a2-136">Qualifiers: WmiDataId(5), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="5b8a2-137">Identificador de thread do thread que encontrou a falha de página.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-137">Thread identifier of the thread that encountered the page fault.</span></span>

</dd> <dt>

<span data-ttu-id="5b8a2-138">**VirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-138">**VirtualAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b8a2-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b8a2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b8a2-141">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5b8a2-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5b8a2-142">Endereço com falha.</span><span class="sxs-lookup"><span data-stu-id="5b8a2-142">Faulting address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b8a2-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b8a2-143">Requirements</span></span>



| <span data-ttu-id="5b8a2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b8a2-144">Requirement</span></span> | <span data-ttu-id="5b8a2-145">Valor</span><span class="sxs-lookup"><span data-stu-id="5b8a2-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5b8a2-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b8a2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5b8a2-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b8a2-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5b8a2-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b8a2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5b8a2-149">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b8a2-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b8a2-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b8a2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b8a2-151">**Falhadepágina \_ v2**</span><span class="sxs-lookup"><span data-stu-id="5b8a2-151">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




