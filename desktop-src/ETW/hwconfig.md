---
description: A classe HWConfig é a classe pai para eventos de configuração de hardware no Windows XP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Classe HWConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837339"
---
# <a name="hwconfig-class"></a><span data-ttu-id="53e29-104">Classe HWConfig</span><span class="sxs-lookup"><span data-stu-id="53e29-104">HWConfig class</span></span>

<span data-ttu-id="53e29-105">A classe **HWConfig** é a classe pai para eventos de configuração de hardware no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="53e29-105">The **HWConfig** class is the parent class for hardware configuration events on Windows XP.</span></span>

<span data-ttu-id="53e29-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="53e29-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e29-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53e29-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="53e29-108">Membros</span><span class="sxs-lookup"><span data-stu-id="53e29-108">Members</span></span>

<span data-ttu-id="53e29-109">A classe **HWConfig** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="53e29-109">The **HWConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e29-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="53e29-110">Remarks</span></span>

<span data-ttu-id="53e29-111">Esses eventos fornecem a configuração de hardware do computador.</span><span class="sxs-lookup"><span data-stu-id="53e29-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="53e29-112">Ao contrário de outros eventos de agente de log do NT, a sessão de kernel gera automaticamente eventos de configuração de hardware; Você não habilita esses eventos ao iniciar a sessão do agente de log do NT kernel.</span><span class="sxs-lookup"><span data-stu-id="53e29-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="53e29-113">**Windows 2000:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="53e29-113">**Windows 2000:** Not supported.</span></span>

<span data-ttu-id="53e29-114">Para eventos de configuração de hardware no Windows Vista e no Windows Server 2003, consulte a classe [SystemConfig](systemconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="53e29-114">For hardware configuration events on Windows Vista and Windows Server 2003, see the [SystemConfig](systemconfig.md) class.</span></span>

<span data-ttu-id="53e29-115">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de configuração de hardware chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="53e29-115">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="53e29-116">Use os seguintes tipos de evento para identificar o evento de configuração de hardware real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="53e29-116">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="53e29-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="53e29-117">Event type</span></span>                                                                      | <span data-ttu-id="53e29-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="53e29-118">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53e29-119">**Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ CPU**(o valor do tipo de evento é 10)</span><span class="sxs-lookup"><span data-stu-id="53e29-119">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="53e29-120">Evento de configuração de CPU.</span><span class="sxs-lookup"><span data-stu-id="53e29-120">CPU configuration event.</span></span> <span data-ttu-id="53e29-121">As classes MOF de [**\_ CPU do HWConfig**](hwconfig-cpu.md) definem os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="53e29-121">The [**HWConfig\_CPU**](hwconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="53e29-122">**Evento \_ de Configuração do tipo de rastreamento \_ \_ \_ LOGICALDISK**(o valor do tipo de evento é 12)</span><span class="sxs-lookup"><span data-stu-id="53e29-122">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="53e29-123">Evento de configuração de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="53e29-123">Logical disk configuration event.</span></span> <span data-ttu-id="53e29-124">A classe MOF [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) MOF classes define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="53e29-124">The [**HWConfig\_LogDisk**](hwconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="53e29-125">**Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ NIC**(o valor do tipo de evento é 13)</span><span class="sxs-lookup"><span data-stu-id="53e29-125">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="53e29-126">Evento de configuração de NIC.</span><span class="sxs-lookup"><span data-stu-id="53e29-126">NIC configuration event.</span></span> <span data-ttu-id="53e29-127">As classes MOF do [**\_ NIC HWConfig**](hwconfig-nic.md) definem os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="53e29-127">The [**HWConfig\_NIC**](hwconfig-nic.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="53e29-128">**Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ PHYSICALDISK**(o valor do tipo de evento é 11)</span><span class="sxs-lookup"><span data-stu-id="53e29-128">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="53e29-129">Evento de configuração de disco físico.</span><span class="sxs-lookup"><span data-stu-id="53e29-129">Physical disk configuration event.</span></span> <span data-ttu-id="53e29-130">As classes [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) MOF definem os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="53e29-130">The [**HWConfig\_PhyDisk**](hwconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="53e29-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53e29-131">Requirements</span></span>



| <span data-ttu-id="53e29-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="53e29-132">Requirement</span></span> | <span data-ttu-id="53e29-133">Valor</span><span class="sxs-lookup"><span data-stu-id="53e29-133">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="53e29-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53e29-134">Minimum supported client</span></span><br/> | <span data-ttu-id="53e29-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="53e29-135">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="53e29-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53e29-136">Minimum supported server</span></span><br/> | <span data-ttu-id="53e29-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="53e29-137">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="53e29-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="53e29-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e29-139">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="53e29-139">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="53e29-140">**HWConfig \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="53e29-140">**HWConfig\_CPU**</span></span>](hwconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="53e29-141">**HWConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="53e29-141">**HWConfig\_LogDisk**</span></span>](hwconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="53e29-142">**\_NIC HWConfig**</span><span class="sxs-lookup"><span data-stu-id="53e29-142">**HWConfig\_NIC**</span></span>](hwconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="53e29-143">**HWConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="53e29-143">**HWConfig\_PhyDisk**</span></span>](hwconfig-phydisk.md)
</dt> </dl>

 

 
