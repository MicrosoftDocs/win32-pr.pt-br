---
description: Contém o estado atual da bateria.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: Estrutura de BATTERY_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778700"
---
# <a name="battery_status-structure"></a><span data-ttu-id="7a3de-103">Estrutura de status da bateria \_</span><span class="sxs-lookup"><span data-stu-id="7a3de-103">BATTERY\_STATUS structure</span></span>

<span data-ttu-id="7a3de-104">Contém o estado atual da bateria.</span><span class="sxs-lookup"><span data-stu-id="7a3de-104">Contains the current state of the battery.</span></span> <span data-ttu-id="7a3de-105">Essa estrutura é usada pelo código de controle do [**\_ \_ \_ status de consulta da bateria do IOCTL**](ioctl-battery-query-status.md) .</span><span class="sxs-lookup"><span data-stu-id="7a3de-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a3de-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a3de-106">Syntax</span></span>


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a><span data-ttu-id="7a3de-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7a3de-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a3de-108">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="7a3de-108">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="7a3de-109">O estado da bateria.</span><span class="sxs-lookup"><span data-stu-id="7a3de-109">The battery state.</span></span> <span data-ttu-id="7a3de-110">Esse membro pode ser zero, um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7a3de-110">This member can be zero, one, or more of the following values.</span></span>



| <span data-ttu-id="7a3de-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7a3de-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="7a3de-112">Significado</span><span class="sxs-lookup"><span data-stu-id="7a3de-112">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="7a3de-113"><dt>**Bateria \_ CARREGANDO**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7a3de-113"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="7a3de-114">Indica que a bateria está carregando no momento.</span><span class="sxs-lookup"><span data-stu-id="7a3de-114">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="7a3de-115"><dt>**Bateria \_**</dt> <dt>0x00000008</dt> crítico</span><span class="sxs-lookup"><span data-stu-id="7a3de-115"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="7a3de-116">Indica que a falha da bateria é iminente.</span><span class="sxs-lookup"><span data-stu-id="7a3de-116">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="7a3de-117">Consulte a seção Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="7a3de-117">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="7a3de-118"><dt>**Bateria \_ Descarregando**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7a3de-118"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="7a3de-119">Indica que a bateria está sendo descarregada no momento.</span><span class="sxs-lookup"><span data-stu-id="7a3de-119">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="7a3de-120"><dt>**Bateria \_ LIGAR \_ a \_ linha**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7a3de-120"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="7a3de-121">Indica que o sistema tem acesso à energia AC, portanto, nenhuma bateria está sendo descarregada.</span><span class="sxs-lookup"><span data-stu-id="7a3de-121">Indicates that the system has access to AC power, so no batteries are being discharged.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="7a3de-122">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="7a3de-122">**Capacity**</span></span>
</dt> <dd>

<span data-ttu-id="7a3de-123">A capacidade atual da bateria, em mWh (ou relativa).</span><span class="sxs-lookup"><span data-stu-id="7a3de-123">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="7a3de-124">Esse valor pode ser usado para gerar uma exibição de "medidor de gás" dividindo-a pelo membro **FullChargedCapacity** da estrutura de [**\_ informações da bateria**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="7a3de-124">This value can be used to generate a "gas gauge" display by dividing it by **FullChargedCapacity** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="7a3de-125">Se a capacidade não estiver disponível, esse membro será de \_ capacidade desconhecida da bateria \_ .</span><span class="sxs-lookup"><span data-stu-id="7a3de-125">If the capacity is unavailable, this member is BATTERY\_UNKNOWN\_CAPACITY.</span></span>

</dd> <dt>

<span data-ttu-id="7a3de-126">**Voltagem**</span><span class="sxs-lookup"><span data-stu-id="7a3de-126">**Voltage**</span></span>
</dt> <dd>

<span data-ttu-id="7a3de-127">A voltagem da bateria atual entre os terminais da bateria, em milivolts (MV).</span><span class="sxs-lookup"><span data-stu-id="7a3de-127">The current battery voltage across the battery terminals, in millivolts (mv).</span></span> <span data-ttu-id="7a3de-128">Se a tensão não estiver disponível, esse membro será a \_ tensão desconhecida da bateria \_ .</span><span class="sxs-lookup"><span data-stu-id="7a3de-128">If the voltage is unavailable, this member is BATTERY\_UNKNOWN\_VOLTAGE.</span></span>

</dd> <dt>

<span data-ttu-id="7a3de-129">**Tarifa**</span><span class="sxs-lookup"><span data-stu-id="7a3de-129">**Rate**</span></span>
</dt> <dd>

<span data-ttu-id="7a3de-130">A taxa atual de carga ou descarga da bateria.</span><span class="sxs-lookup"><span data-stu-id="7a3de-130">The current rate of battery charge or discharge.</span></span> <span data-ttu-id="7a3de-131">Esse valor estará em miliwatts, a menos que as informações de taxa de bateria sejam relativas, caso em que elas estarão em unidades arbitrárias por hora.</span><span class="sxs-lookup"><span data-stu-id="7a3de-131">This value will be in milliwatts unless the battery rate information is relative, in which case it will be in arbitrary units per hour.</span></span> <span data-ttu-id="7a3de-132">Para determinar se as informações da bateria são relativas, examine o \_ sinalizador relativo da capacidade da bateria \_ no membro de **recursos** da estrutura de [**\_ informações da bateria**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="7a3de-132">To determine if battery information is relative, examine the BATTERY\_CAPACITY\_RELATIVE flag in the **Capabilities** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="7a3de-133">Uma taxa positiva diferente de zero indica cobrança; uma taxa negativa indica o descarregamento.</span><span class="sxs-lookup"><span data-stu-id="7a3de-133">A nonzero, positive rate indicates charging; a negative rate indicates discharging.</span></span> <span data-ttu-id="7a3de-134">Algumas baterias relatam apenas taxas de descarregamento.</span><span class="sxs-lookup"><span data-stu-id="7a3de-134">Some batteries report only discharging rates.</span></span> <span data-ttu-id="7a3de-135">Se a taxa não estiver disponível, esse membro será uma \_ taxa de bateria desconhecida \_ .</span><span class="sxs-lookup"><span data-stu-id="7a3de-135">If the rate is unavailable, this member is BATTERY\_UNKNOWN\_RATE.</span></span> <span data-ttu-id="7a3de-136">Se o estado da bateria ou fonte de energia for alterado, a taxa poderá ficar disponível.</span><span class="sxs-lookup"><span data-stu-id="7a3de-136">If the state of the battery or power source changes, the rate may become available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a3de-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a3de-137">Remarks</span></span>

<span data-ttu-id="7a3de-138">O \_ sinalizador de bateria crítica no membro do **PowerState** dessa estrutura indica uma condição de "bateria crítica" de hardware.</span><span class="sxs-lookup"><span data-stu-id="7a3de-138">The BATTERY\_CRITICAL flag in the **PowerState** member of this structure indicates a hardware "battery critical" condition.</span></span> <span data-ttu-id="7a3de-139">Esse nível crítico é definido pelo fabricante da bateria, não pelo usuário no "alarme de bateria crítica".</span><span class="sxs-lookup"><span data-stu-id="7a3de-139">This critical level is set by the battery manufacturer, not by the user in the "critical battery alarm."</span></span> <span data-ttu-id="7a3de-140">Geralmente, isso significa que o sistema de bateria calculou que a bateria está totalmente descarregada, e qualquer energia que esteja sendo desenhada está além do esperado.</span><span class="sxs-lookup"><span data-stu-id="7a3de-140">It generally means that the battery system has calculated that the battery is totally drained, and any power being drawn is beyond what is expected.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a3de-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a3de-141">Requirements</span></span>



| <span data-ttu-id="7a3de-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a3de-142">Requirement</span></span> | <span data-ttu-id="7a3de-143">Valor</span><span class="sxs-lookup"><span data-stu-id="7a3de-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3de-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a3de-144">Minimum supported client</span></span><br/> | <span data-ttu-id="7a3de-145">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7a3de-145">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="7a3de-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a3de-146">Minimum supported server</span></span><br/> | <span data-ttu-id="7a3de-147">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a3de-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="7a3de-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a3de-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a3de-149"><dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="7a3de-149"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a3de-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a3de-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a3de-151">**informações da bateria \_**</span><span class="sxs-lookup"><span data-stu-id="7a3de-151">**BATTERY\_INFORMATION**</span></span>](battery-information-str.md)
</dt> <dt>

[<span data-ttu-id="7a3de-152">**\_status de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="7a3de-152">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> </dl>

 

 




