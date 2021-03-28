---
description: Essa classe é a classe de tipo de evento para eventos DPC (chamada de procedimento deferida) do dispositivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: Classe DPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826874"
---
# <a name="dpc-class"></a><span data-ttu-id="8b936-104">Classe DPC</span><span class="sxs-lookup"><span data-stu-id="8b936-104">DPC class</span></span>

<span data-ttu-id="8b936-105">Essa classe é a classe de tipo de evento para eventos DPC (chamada de procedimento deferida) do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b936-105">This class is the event type class for device deferred procedure call (DPC) events.</span></span>

<span data-ttu-id="8b936-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="8b936-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b936-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b936-107">Syntax</span></span>

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a><span data-ttu-id="8b936-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8b936-108">Members</span></span>

<span data-ttu-id="8b936-109">A classe **DPC** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8b936-109">The **DPC** class has these types of members:</span></span>

-   [<span data-ttu-id="8b936-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b936-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b936-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b936-111">Properties</span></span>

<span data-ttu-id="8b936-112">A classe **DPC** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b936-112">The **DPC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b936-113">**Inicialtime**</span><span class="sxs-lookup"><span data-stu-id="8b936-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b936-114">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="8b936-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8b936-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b936-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b936-116">Qualificadores: WmiDataId (1), extensão ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="8b936-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="8b936-117">Tempo de entrada de DPC.</span><span class="sxs-lookup"><span data-stu-id="8b936-117">DPC entry time.</span></span>

</dd> <dt>

<span data-ttu-id="8b936-118">**Rotina**</span><span class="sxs-lookup"><span data-stu-id="8b936-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b936-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b936-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b936-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b936-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b936-121">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="8b936-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8b936-122">Endereço da rotina de DPC.</span><span class="sxs-lookup"><span data-stu-id="8b936-122">Address of DPC routine.</span></span> <span data-ttu-id="8b936-123">Use o endereço com os eventos de imagem para descobrir qual imagem foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="8b936-123">Use the address with the Image events to find which image started.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b936-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b936-124">Remarks</span></span>

<span data-ttu-id="8b936-125">Esses eventos são registrados quando um DPC é inserido.</span><span class="sxs-lookup"><span data-stu-id="8b936-125">These events are logged when a DPC is entered.</span></span> <span data-ttu-id="8b936-126">Você usa esses eventos para monitorar e verificar o comportamento de drivers e componentes do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="8b936-126">You use these events to monitor and verify the behavior of drivers and kernel-mode components.</span></span> <span data-ttu-id="8b936-127">Por exemplo, você pode usar eventos DPC, ISR e Image para determinar os componentes que gastam muito tempo em níveis altos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="8b936-127">For example, you can use DPC, ISR, and Image events to determine those components that spend too much time at high interrupt levels.</span></span> <span data-ttu-id="8b936-128">Os eventos DPC e ISR têm um carimbo de data/hora de entrada que é usado para calcular a duração das rotinas.</span><span class="sxs-lookup"><span data-stu-id="8b936-128">DPC and ISR events have an entry time stamp which is used to compute the duration of the routines.</span></span> <span data-ttu-id="8b936-129">Os eventos de imagem são lidos para construir as regiões de memória que são mapeadas para determinados módulos.</span><span class="sxs-lookup"><span data-stu-id="8b936-129">The image events are read to construct the memory regions that map to certain modules.</span></span> <span data-ttu-id="8b936-130">Você pode usar o mapeamento para localizar o módulo que contém a rotina de interrupção.</span><span class="sxs-lookup"><span data-stu-id="8b936-130">You can use the mapping to locate the module that contains the interrupt routine.</span></span>

<span data-ttu-id="8b936-131">O evento TimerDPC registra quando um DPC é acionado como resultado de uma expiração do temporizador e dos registros de evento ThreadDPC quando um DPC thread é executado.</span><span class="sxs-lookup"><span data-stu-id="8b936-131">The TimerDPC event records when a DPC fires as a result of a timer expiration and the ThreadDPC event records when a threaded DPC executes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b936-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b936-132">Requirements</span></span>



| <span data-ttu-id="8b936-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b936-133">Requirement</span></span> | <span data-ttu-id="8b936-134">Valor</span><span class="sxs-lookup"><span data-stu-id="8b936-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8b936-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b936-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8b936-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b936-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8b936-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b936-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8b936-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b936-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




