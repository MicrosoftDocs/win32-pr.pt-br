---
description: Classe SystemConfig – essa classe é a classe pai para eventos de configuração de hardware. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: Classe SystemConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 232214aa2c33485d909525d54965f59fdc891a29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105864"
---
# <a name="systemconfig-class"></a><span data-ttu-id="02fdb-104">Classe SystemConfig</span><span class="sxs-lookup"><span data-stu-id="02fdb-104">SystemConfig class</span></span>

<span data-ttu-id="02fdb-105">Essa classe é a classe pai para eventos de configuração de hardware.</span><span class="sxs-lookup"><span data-stu-id="02fdb-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="02fdb-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="02fdb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="02fdb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02fdb-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="02fdb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="02fdb-108">Members</span></span>

<span data-ttu-id="02fdb-109">A classe **SystemConfig** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="02fdb-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="02fdb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="02fdb-110">Remarks</span></span>

<span data-ttu-id="02fdb-111">Esses eventos fornecem a configuração de hardware do computador.</span><span class="sxs-lookup"><span data-stu-id="02fdb-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="02fdb-112">Ao contrário de outros eventos de agente de log do NT, a sessão de kernel gera automaticamente eventos de configuração de hardware; Você não habilita esses eventos ao iniciar a sessão do agente de log do NT kernel.</span><span class="sxs-lookup"><span data-stu-id="02fdb-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="02fdb-113">Para eventos de configuração de hardware no Windows XP, consulte a classe [HWConfig](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="02fdb-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="02fdb-114">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de configuração de hardware chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="02fdb-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="02fdb-115">Use os seguintes tipos de evento para identificar o evento de configuração de hardware real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="02fdb-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="02fdb-116">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="02fdb-116">Event type</span></span>                                                                      | <span data-ttu-id="02fdb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="02fdb-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02fdb-118">**Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ CPU**(o valor do tipo de evento é 10)</span><span class="sxs-lookup"><span data-stu-id="02fdb-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="02fdb-119">Evento de configuração de CPU.</span><span class="sxs-lookup"><span data-stu-id="02fdb-119">CPU configuration event.</span></span> <span data-ttu-id="02fdb-120">As classes MOF de [**\_ CPU do SystemConfig**](systemconfig-cpu.md) definem os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="02fdb-121">**Evento \_ de Tipo de rastreamento \_ \_ config \_ IDECHANNEL**(o valor do tipo de evento é 23)</span><span class="sxs-lookup"><span data-stu-id="02fdb-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="02fdb-122">Evento de configuração de canal IDE primário e secundário.</span><span class="sxs-lookup"><span data-stu-id="02fdb-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="02fdb-123">A classe MOF [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) MOF classes define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="02fdb-124">**Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ IRQ**(o valor do tipo de evento é 21)</span><span class="sxs-lookup"><span data-stu-id="02fdb-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="02fdb-125">Evento de solicitação de interrupção (IRQ).</span><span class="sxs-lookup"><span data-stu-id="02fdb-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="02fdb-126">A classe MOF de [**SystemConfig \_ IRQ**](systemconfig-irq.md) do MOF classes define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="02fdb-127">**Evento \_ de Configuração do tipo de rastreamento \_ \_ \_ LOGICALDISK**(o valor do tipo de evento é 12)</span><span class="sxs-lookup"><span data-stu-id="02fdb-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="02fdb-128">Evento de configuração de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="02fdb-128">Logical disk configuration event.</span></span> <span data-ttu-id="02fdb-129">A classe MOF [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) MOF classes define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="02fdb-130">**Evento \_ de Tipo de rastreamento \_ \_ config \_ NetInfo**(o valor do tipo de evento é 17)</span><span class="sxs-lookup"><span data-stu-id="02fdb-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="02fdb-131">Evento de Iformation de rede.</span><span class="sxs-lookup"><span data-stu-id="02fdb-131">Network iformation event.</span></span> <span data-ttu-id="02fdb-132">A classe MOF de [**\_ rede SystemConfig**](systemconfig-network.md) define os dados de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="02fdb-133">**Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ NIC**(o valor do tipo de evento é 13)</span><span class="sxs-lookup"><span data-stu-id="02fdb-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="02fdb-134">Evento de configuração de NIC.</span><span class="sxs-lookup"><span data-stu-id="02fdb-134">NIC configuration event.</span></span> <span data-ttu-id="02fdb-135">As classes MOF do [**\_ NIC SystemConfig**](systemconfig-nic.md) definem os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="02fdb-136">**Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ PHYSICALDISK**(o valor do tipo de evento é 11)</span><span class="sxs-lookup"><span data-stu-id="02fdb-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="02fdb-137">Evento de configuração de disco físico.</span><span class="sxs-lookup"><span data-stu-id="02fdb-137">Physical disk configuration event.</span></span> <span data-ttu-id="02fdb-138">As classes [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) MOF definem os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="02fdb-139">**Evento \_ de Tipo de rastreamento \_ \_ config \_ PNP**(o valor do tipo de evento é 22)</span><span class="sxs-lookup"><span data-stu-id="02fdb-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="02fdb-140">Evento plug and Play.</span><span class="sxs-lookup"><span data-stu-id="02fdb-140">Plug and play event.</span></span> <span data-ttu-id="02fdb-141">A classe [**SystemConfig \_ PNP**](systemconfig-pnp.md) MOF classes MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="02fdb-142">**Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ Power**(o valor do tipo de evento é 16)</span><span class="sxs-lookup"><span data-stu-id="02fdb-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="02fdb-143">Evento de configuração de energia.</span><span class="sxs-lookup"><span data-stu-id="02fdb-143">Power configuration event.</span></span> <span data-ttu-id="02fdb-144">A classe [**SystemConfig \_ Power**](systemconfig-power.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="02fdb-145">**Evento \_ de \_Serviços de \_ configuração \_ de tipo de rastreamento**(o valor do tipo de evento é 15)</span><span class="sxs-lookup"><span data-stu-id="02fdb-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="02fdb-146">Evento de configuração de serviços.</span><span class="sxs-lookup"><span data-stu-id="02fdb-146">Services configuration event.</span></span> <span data-ttu-id="02fdb-147">A classe MOF [**\_ dos serviços SystemConfigs**](systemconfig-services.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="02fdb-148">**Evento \_ de \_Vídeo de \_ configuração \_ do tipo de rastreamento**(o valor do tipo de evento é 14)</span><span class="sxs-lookup"><span data-stu-id="02fdb-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="02fdb-149">Evento de configuração do adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="02fdb-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="02fdb-150">A classe MOF de [**\_ vídeo SystemConfig**](systemconfig-video.md) define os dados de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="02fdb-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="02fdb-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02fdb-151">Requirements</span></span>



| <span data-ttu-id="02fdb-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="02fdb-152">Requirement</span></span> | <span data-ttu-id="02fdb-153">Valor</span><span class="sxs-lookup"><span data-stu-id="02fdb-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02fdb-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02fdb-154">Minimum supported client</span></span><br/> | <span data-ttu-id="02fdb-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02fdb-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02fdb-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02fdb-156">Minimum supported server</span></span><br/> | <span data-ttu-id="02fdb-157">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02fdb-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02fdb-158">Consulte também</span><span class="sxs-lookup"><span data-stu-id="02fdb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02fdb-159">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="02fdb-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="02fdb-160">**SystemConfig \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="02fdb-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="02fdb-161">**SystemConfig \_ IDEChannel**</span><span class="sxs-lookup"><span data-stu-id="02fdb-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="02fdb-162">**\_IRQ SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="02fdb-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="02fdb-163">**SystemConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="02fdb-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="02fdb-164">**\_Rede SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="02fdb-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="02fdb-165">**\_NIC SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="02fdb-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="02fdb-166">**SystemConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="02fdb-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="02fdb-167">**\_PNP SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="02fdb-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="02fdb-168">**SystemConfig \_ Power**</span><span class="sxs-lookup"><span data-stu-id="02fdb-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="02fdb-169">**Serviços SystemConfigs \_**</span><span class="sxs-lookup"><span data-stu-id="02fdb-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="02fdb-170">**Vídeo do SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="02fdb-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="02fdb-171">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="02fdb-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 
