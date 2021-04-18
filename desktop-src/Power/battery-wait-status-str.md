---
description: Contém informações sobre as condições sob as quais o status da bateria deve ser recuperado.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: Estrutura de BATTERY_WAIT_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756694"
---
# <a name="battery_wait_status-structure"></a><span data-ttu-id="6ca36-103">Estrutura de status de \_ espera da bateria \_</span><span class="sxs-lookup"><span data-stu-id="6ca36-103">BATTERY\_WAIT\_STATUS structure</span></span>

<span data-ttu-id="6ca36-104">Contém informações sobre as condições sob as quais o status da bateria deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6ca36-104">Contains information about the conditions under which the battery status is to be retrieved.</span></span> <span data-ttu-id="6ca36-105">Essa estrutura é usada pelo código de controle do [**\_ \_ \_ status de consulta da bateria do IOCTL**](ioctl-battery-query-status.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca36-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca36-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ca36-106">Syntax</span></span>


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a><span data-ttu-id="6ca36-107">Membros</span><span class="sxs-lookup"><span data-stu-id="6ca36-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6ca36-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="6ca36-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="6ca36-109">A marca de bateria atual para a bateria.</span><span class="sxs-lookup"><span data-stu-id="6ca36-109">The current battery tag for the battery.</span></span> <span data-ttu-id="6ca36-110">Somente informações para uma bateria que correspondem à marca podem ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="6ca36-110">Only information for a battery matching the tag can be returned.</span></span> <span data-ttu-id="6ca36-111">Sempre que esse valor não corresponder à marca atual da bateria, a operação [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) falhará com um código de erro de \_ arquivo de erro \_ não \_ encontrado, que indica ao chamador que a bateria para a qual ela tem uma marca não está mais instalada, o chamador pode optar por usar a operação de [**\_ \_ \_ marca de consulta da bateria do IOCTL**](ioctl-battery-query-tag.md) para determinar a marca da bateria recém-instalada, se houver.</span><span class="sxs-lookup"><span data-stu-id="6ca36-111">Whenever this value does not match the battery's current tag, the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) operation will fail with an error code of ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag is no longer installed The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if any.</span></span> <span data-ttu-id="6ca36-112">Além disso, se a solicitação estiver em andamento quando a bateria for removida ou a marca for alterada, a operação será anulada com o status do \_ arquivo de erro \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="6ca36-112">In addition, if the request is in progress when the battery is removed, or the tag changes, the operation is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="6ca36-113">(Consulte [marcas de bateria](battery-information.md) para obter mais informações.)</span><span class="sxs-lookup"><span data-stu-id="6ca36-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

</dd> <dt>

<span data-ttu-id="6ca36-114">**Tempo Limite**</span><span class="sxs-lookup"><span data-stu-id="6ca36-114">**Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="6ca36-115">O número de milissegundos que a solicitação aguardará pela condição especificada pelos membros **PowerState**, **LowCapacity** e **HighCapacity** antes de concluir.</span><span class="sxs-lookup"><span data-stu-id="6ca36-115">The number of milliseconds the request will wait for the condition specified by the **PowerState**, **LowCapacity**, and **HighCapacity** members before completing.</span></span> <span data-ttu-id="6ca36-116">Um valor de-1 indica que a solicitação aguardará indefinidamente que as condições sejam satisfeitas.</span><span class="sxs-lookup"><span data-stu-id="6ca36-116">A value of -1 indicates that the request will wait indefinitely for the conditions to be satisfied.</span></span> <span data-ttu-id="6ca36-117">Um valor de zero indica que as informações de bateria solicitadas serão retornadas imediatamente, independentemente das outras condições.</span><span class="sxs-lookup"><span data-stu-id="6ca36-117">A value of zero indicates that the requested battery information is to be returned immediately, regardless of the other conditions.</span></span> <span data-ttu-id="6ca36-118">Qualquer outro valor indica que a solicitação deve aguardar esse período de tempo ou até que qualquer uma das outras condições seja satisfeita.</span><span class="sxs-lookup"><span data-stu-id="6ca36-118">Any other value indicates that the request should wait that length of time, or until any one of the other conditions is satisfied.</span></span>

<span data-ttu-id="6ca36-119">Se o computador tiver inserido o modo de suspensão, o relógio continuará a ser executado, mas o esgotamento da contagem não ativará o computador.</span><span class="sxs-lookup"><span data-stu-id="6ca36-119">If the computer has entered sleep mode, the clock will continue to run, but exhausting the count will not wake the computer up.</span></span> <span data-ttu-id="6ca36-120">Se a contagem for esgotada quando o computador for acordado e outras condições forem satisfeitas, a chamada retornará imediatamente na ativação.</span><span class="sxs-lookup"><span data-stu-id="6ca36-120">If the count is exhausted when the computer is awoken, and other conditions are satisfied, the call will return immediately on awakening.</span></span>

</dd> <dt>

<span data-ttu-id="6ca36-121">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="6ca36-121">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="6ca36-122">Zero, um ou mais dos seguintes bits de status, que indicam o estado da bateria.</span><span class="sxs-lookup"><span data-stu-id="6ca36-122">Zero, one, or more of the following status bits, which indicate the state of the battery.</span></span> <span data-ttu-id="6ca36-123">É idêntico ao membro **PowerState** da estrutura de [**\_ status da bateria**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca36-123">It is identical to the **PowerState** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>



| <span data-ttu-id="6ca36-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6ca36-124">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="6ca36-125">Significado</span><span class="sxs-lookup"><span data-stu-id="6ca36-125">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="6ca36-126"><dt>**Bateria \_ CARREGANDO**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="6ca36-126"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="6ca36-127">Indica que a bateria está carregando no momento.</span><span class="sxs-lookup"><span data-stu-id="6ca36-127">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="6ca36-128"><dt>**Bateria \_**</dt> <dt>0x00000008</dt> crítico</span><span class="sxs-lookup"><span data-stu-id="6ca36-128"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="6ca36-129">Indica que a falha da bateria é iminente.</span><span class="sxs-lookup"><span data-stu-id="6ca36-129">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="6ca36-130">Consulte a seção Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6ca36-130">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="6ca36-131"><dt>**Bateria \_ Descarregando**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="6ca36-131"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="6ca36-132">Indica que a bateria está sendo descarregada no momento.</span><span class="sxs-lookup"><span data-stu-id="6ca36-132">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="6ca36-133"><dt>**Bateria \_ LIGAR \_ a \_ linha**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6ca36-133"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6ca36-134">Indica que a bateria tem acesso à energia AC.</span><span class="sxs-lookup"><span data-stu-id="6ca36-134">Indicates that the battery has access to AC power.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="6ca36-135">**LowCapacity**</span><span class="sxs-lookup"><span data-stu-id="6ca36-135">**LowCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="6ca36-136">A capacidade atual da bateria, em mWh (ou relativa).</span><span class="sxs-lookup"><span data-stu-id="6ca36-136">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="6ca36-137">Esse valor é idêntico ao membro de **capacidade** da estrutura [**de \_ status da bateria**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca36-137">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6ca36-138">**HighCapacity**</span><span class="sxs-lookup"><span data-stu-id="6ca36-138">**HighCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="6ca36-139">A capacidade atual da bateria, em mWh (ou relativa).</span><span class="sxs-lookup"><span data-stu-id="6ca36-139">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="6ca36-140">Esse valor é idêntico ao membro de **capacidade** da estrutura [**de \_ status da bateria**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca36-140">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ca36-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ca36-141">Remarks</span></span>

<span data-ttu-id="6ca36-142">As solicitações de informações da bateria são adiadas até que ocorra um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="6ca36-142">Requests for battery information are postponed until one of the following occurs:</span></span>

-   <span data-ttu-id="6ca36-143">O tempo limite expira (supondo que o **tempo limite** não seja-1).</span><span class="sxs-lookup"><span data-stu-id="6ca36-143">The time-out expires (assuming **Timeout** is not -1).</span></span>
-   <span data-ttu-id="6ca36-144">O status atual da bateria não corresponde ao **PowerState**.</span><span class="sxs-lookup"><span data-stu-id="6ca36-144">The battery's current status does not match **PowerState**.</span></span>
-   <span data-ttu-id="6ca36-145">A capacidade da bateria está abaixo de **LowCapacity**.</span><span class="sxs-lookup"><span data-stu-id="6ca36-145">The battery's capacity is below **LowCapacity**.</span></span>
-   <span data-ttu-id="6ca36-146">A capacidade da bateria está acima de **HighCapacity**.</span><span class="sxs-lookup"><span data-stu-id="6ca36-146">The battery's capacity is above **HighCapacity**.</span></span>
-   <span data-ttu-id="6ca36-147">A marca de bateria é alterada.</span><span class="sxs-lookup"><span data-stu-id="6ca36-147">The battery tag changes.</span></span>

<span data-ttu-id="6ca36-148">Quando qualquer uma dessas condições é satisfeita, os dados são coletados e a operação retorna.</span><span class="sxs-lookup"><span data-stu-id="6ca36-148">When any one of these conditions is satisfied, the data is collected and the operation returns.</span></span> <span data-ttu-id="6ca36-149">Isso permite que os aplicativos monitorem informações de baterias dinâmicas típicas sem sondar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ca36-149">This allows applications to monitor typical dynamic battery information without polling the device.</span></span>

<span data-ttu-id="6ca36-150">Antes de usar qualquer uma das duas condições de capacidade, verifique se a bateria dá suporte a elas usando o código de controle de [**\_ \_ \_ status de consulta da bateria do IOCTL**](ioctl-battery-query-status.md) com um tempo limite de zero.</span><span class="sxs-lookup"><span data-stu-id="6ca36-150">Before using either of the two Capacity conditions, make sure the battery supports them by using the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code with a time-out of zero.</span></span> <span data-ttu-id="6ca36-151">Examine os resultados para determinar se o membro de **capacidade** tem suporte (ou seja, sem \_ capacidade de bateria desconhecida \_ ).</span><span class="sxs-lookup"><span data-stu-id="6ca36-151">Examine the results to determine if the **Capacity** member is supported (that is, not BATTERY\_UNKNOWN\_CAPACITY).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca36-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ca36-152">Requirements</span></span>



| <span data-ttu-id="6ca36-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ca36-153">Requirement</span></span> | <span data-ttu-id="6ca36-154">Valor</span><span class="sxs-lookup"><span data-stu-id="6ca36-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca36-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca36-155">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca36-156">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ca36-156">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="6ca36-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca36-157">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca36-158">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ca36-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="6ca36-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ca36-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca36-160"><dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="6ca36-160"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca36-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ca36-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca36-162">**STATUS da bateria \_**</span><span class="sxs-lookup"><span data-stu-id="6ca36-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="6ca36-163">**\_status de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="6ca36-163">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="6ca36-164">**\_marca de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="6ca36-164">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

