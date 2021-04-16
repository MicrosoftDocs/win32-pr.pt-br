---
description: Essa classe é a classe de tipo de evento para eventos de ISR (rotina de serviço de interrupção). A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: Classe ISR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967981"
---
# <a name="isr-class"></a><span data-ttu-id="a5d57-104">Classe ISR</span><span class="sxs-lookup"><span data-stu-id="a5d57-104">ISR class</span></span>

<span data-ttu-id="a5d57-105">Essa classe é a classe de tipo de evento para eventos de ISR (rotina de serviço de interrupção).</span><span class="sxs-lookup"><span data-stu-id="a5d57-105">This class is the event type class for interrupt service routine (ISR) events.</span></span>

<span data-ttu-id="a5d57-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="a5d57-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d57-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5d57-107">Syntax</span></span>

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="a5d57-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a5d57-108">Members</span></span>

<span data-ttu-id="a5d57-109">A classe **ISR** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a5d57-109">The **ISR** class has these types of members:</span></span>

-   [<span data-ttu-id="a5d57-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a5d57-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5d57-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a5d57-111">Properties</span></span>

<span data-ttu-id="a5d57-112">A classe **ISR** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a5d57-112">The **ISR** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5d57-113">**Inicialtime**</span><span class="sxs-lookup"><span data-stu-id="a5d57-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5d57-114">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="a5d57-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5d57-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-116">Qualificadores: WmiDataId (1), extensão ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="a5d57-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="a5d57-117">Tempo de entrada de ISR.</span><span class="sxs-lookup"><span data-stu-id="a5d57-117">ISR entry time.</span></span>

</dd> <dt>

<span data-ttu-id="a5d57-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a5d57-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5d57-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5d57-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5d57-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-121">Qualificadores: WmiDataId (5), ponteiro</span><span class="sxs-lookup"><span data-stu-id="a5d57-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a5d57-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a5d57-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a5d57-123">**ReturnValue**</span><span class="sxs-lookup"><span data-stu-id="a5d57-123">**ReturnValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5d57-124">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="a5d57-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5d57-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-126">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="a5d57-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="a5d57-127">Booliano que indica se a interrupção foi reivindicada (é true se a interrupção foi reivindicada).</span><span class="sxs-lookup"><span data-stu-id="a5d57-127">Boolean indicating if the interrupt was claimed (is True if the interrupt was claimed).</span></span>

</dd> <dt>

<span data-ttu-id="a5d57-128">**Rotina**</span><span class="sxs-lookup"><span data-stu-id="a5d57-128">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5d57-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5d57-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5d57-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-131">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="a5d57-131">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a5d57-132">Endereço da rotina de ISR.</span><span class="sxs-lookup"><span data-stu-id="a5d57-132">Address of ISR routine.</span></span> <span data-ttu-id="a5d57-133">Use o endereço com os eventos de imagem para descobrir qual imagem foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="a5d57-133">Use the address with the Image events to find which image started.</span></span>

</dd> <dt>

<span data-ttu-id="a5d57-134">**Vetor**</span><span class="sxs-lookup"><span data-stu-id="a5d57-134">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5d57-135">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="a5d57-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5d57-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5d57-137">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="a5d57-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a5d57-138">Vetor da tabela de descritor de interrupção à qual a rotina de ISR é atribuída.</span><span class="sxs-lookup"><span data-stu-id="a5d57-138">Vector from interrupt descriptor table to which ISR routine is assigned.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5d57-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5d57-139">Requirements</span></span>



| <span data-ttu-id="a5d57-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d57-140">Requirement</span></span> | <span data-ttu-id="a5d57-141">Valor</span><span class="sxs-lookup"><span data-stu-id="a5d57-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a5d57-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5d57-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d57-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5d57-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a5d57-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5d57-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d57-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a5d57-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




