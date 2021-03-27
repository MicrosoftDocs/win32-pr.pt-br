---
description: Essa classe é a classe de tipo de evento para eventos de solicitação de interrupção (IRQ). A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: Classe SystemConfig_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967410"
---
# <a name="systemconfig_irq-class"></a><span data-ttu-id="0b39e-104">\_Classe de IRQ SystemConfig</span><span class="sxs-lookup"><span data-stu-id="0b39e-104">SystemConfig\_IRQ class</span></span>

<span data-ttu-id="0b39e-105">Essa classe é a classe de tipo de evento para eventos de solicitação de interrupção (IRQ).</span><span class="sxs-lookup"><span data-stu-id="0b39e-105">This class is the event type class for interrupt request (IRQ) events.</span></span>

<span data-ttu-id="0b39e-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="0b39e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b39e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b39e-107">Syntax</span></span>

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a><span data-ttu-id="0b39e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0b39e-108">Members</span></span>

<span data-ttu-id="0b39e-109">A **classe \_ IRQ SystemConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b39e-109">The **SystemConfig\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="0b39e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b39e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b39e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b39e-111">Properties</span></span>

<span data-ttu-id="0b39e-112">A **classe \_ IRQ SystemConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b39e-112">The **SystemConfig\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b39e-113">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="0b39e-113">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b39e-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b39e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b39e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b39e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b39e-116">Qualificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="0b39e-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="0b39e-117">Descrição do dispositivo ou software que faz a solicitação.</span><span class="sxs-lookup"><span data-stu-id="0b39e-117">Description of the device or software making the request.</span></span>

</dd> <dt>

<span data-ttu-id="0b39e-118">**DeviceDescriptionLen**</span><span class="sxs-lookup"><span data-stu-id="0b39e-118">**DeviceDescriptionLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b39e-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b39e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b39e-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b39e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b39e-121">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="0b39e-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0b39e-122">Comprimento, em caracteres, da cadeia de caracteres em **DeviceDescription**.</span><span class="sxs-lookup"><span data-stu-id="0b39e-122">Length, in characters, of the string in **DeviceDescription**.</span></span>

</dd> <dt>

<span data-ttu-id="0b39e-123">**IRQAffinity**</span><span class="sxs-lookup"><span data-stu-id="0b39e-123">**IRQAffinity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b39e-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0b39e-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b39e-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b39e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b39e-126">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="0b39e-126">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0b39e-127">Máscara de afinidade de IRQ.</span><span class="sxs-lookup"><span data-stu-id="0b39e-127">IRQ affinity mask.</span></span> <span data-ttu-id="0b39e-128">A máscara de afinidade identifica os processadores específicos (ou grupos de processadores) que podem receber o IRQ.</span><span class="sxs-lookup"><span data-stu-id="0b39e-128">The affinity mask identifies the specific processors (or groups of processors) that can receive the IRQ.</span></span>

</dd> <dt>

<span data-ttu-id="0b39e-129">**IRQNum**</span><span class="sxs-lookup"><span data-stu-id="0b39e-129">**IRQNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b39e-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b39e-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b39e-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b39e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b39e-132">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="0b39e-132">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="0b39e-133">Número da linha da solicitação de interrupção.</span><span class="sxs-lookup"><span data-stu-id="0b39e-133">Interrupt request line number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b39e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b39e-134">Requirements</span></span>



| <span data-ttu-id="0b39e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b39e-135">Requirement</span></span> | <span data-ttu-id="0b39e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="0b39e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0b39e-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b39e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0b39e-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b39e-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0b39e-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b39e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0b39e-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b39e-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b39e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b39e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b39e-142">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="0b39e-142">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




