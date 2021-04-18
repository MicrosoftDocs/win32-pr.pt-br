---
description: Contém informações sobre a bateria.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: Estrutura de BATTERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756695"
---
# <a name="battery_information-structure"></a><span data-ttu-id="01b3d-103">Estrutura de informações da bateria \_</span><span class="sxs-lookup"><span data-stu-id="01b3d-103">BATTERY\_INFORMATION structure</span></span>

<span data-ttu-id="01b3d-104">Contém informações sobre a bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-104">Contains battery information.</span></span> <span data-ttu-id="01b3d-105">Essa estrutura é retornada pelo código de controle de [**\_ \_ \_ informações de consulta da bateria do IOCTL**](ioctl-battery-query-information.md) quando o nível de informações BatteryInformation é solicitado.</span><span class="sxs-lookup"><span data-stu-id="01b3d-105">This structure is returned by the [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) control code when the BatteryInformation information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b3d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01b3d-106">Syntax</span></span>


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="01b3d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="01b3d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="01b3d-108">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="01b3d-108">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-109">Os recursos da bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-109">The battery capabilities.</span></span> <span data-ttu-id="01b3d-110">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="01b3d-110">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="01b3d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="01b3d-111">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="01b3d-112">Significado</span><span class="sxs-lookup"><span data-stu-id="01b3d-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <span data-ttu-id="01b3d-113"><dt>**Bateria \_ 0x40000000 \_ relativa à capacidade**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-113"><dt>**BATTERY\_CAPACITY\_RELATIVE**</dt> <dt>0x40000000</dt></span></span> </dl>                    | <span data-ttu-id="01b3d-114">Indica que a capacidade da bateria e as informações de taxa são relativas, e não em unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="01b3d-114">Indicates that the battery capacity and rate information are relative, and not in any specific units.</span></span> <span data-ttu-id="01b3d-115">Se esse bit não for definido, as unidades de relatório serão milliwatt (mWh) para a capacidade e miliwatts (mW) para taxa.</span><span class="sxs-lookup"><span data-stu-id="01b3d-115">If this bit is not set, the reporting units are milliwatt-hours (mWh) for capacity and milliwatts (mW) for rate.</span></span> <span data-ttu-id="01b3d-116">Se esse bit for definido, todas as referências a unidades na outra documentação da bateria poderão ser ignoradas.</span><span class="sxs-lookup"><span data-stu-id="01b3d-116">If this bit is set, all references to units in the other battery documentation can be ignored.</span></span> <span data-ttu-id="01b3d-117">Todas as informações de taxa são relatadas em unidades por hora.</span><span class="sxs-lookup"><span data-stu-id="01b3d-117">All rate information is reported in units per hour.</span></span> <span data-ttu-id="01b3d-118">Por exemplo, se a capacidade totalmente carregada for relatada como 100, uma taxa de 200 indica que a bateria usará toda a sua capacidade em meia hora.</span><span class="sxs-lookup"><span data-stu-id="01b3d-118">For example, if the fully charged capacity is reported as 100, a rate of 200 indicates that the battery will use all of its capacity in half an hour.</span></span><br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <span data-ttu-id="01b3d-119"><dt>**Bateria \_ É 0x20000000 de \_ curto \_ prazo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-119"><dt>**BATTERY\_IS\_SHORT\_TERM**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="01b3d-120">Indica que a operação normal é para uma função com falha.</span><span class="sxs-lookup"><span data-stu-id="01b3d-120">Indicates that the normal operation is for a fail-safe function.</span></span> <span data-ttu-id="01b3d-121">Se esse bit não for definido, espera-se que a bateria seja usada durante o uso normal do sistema.</span><span class="sxs-lookup"><span data-stu-id="01b3d-121">If this bit is not set the battery is expected to be used during normal system usage.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <span data-ttu-id="01b3d-122"><dt>**Bateria \_ DEFINIR \_ cobrança \_ com suporte**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-122"><dt>**BATTERY\_SET\_CHARGE\_SUPPORTED**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="01b3d-123">Indica que as solicitações Set Information do tipo BatteryCharge são suportadas por esse dispositivo de bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-123">Indicates that set information requests of the type BatteryCharge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <span data-ttu-id="01b3d-124"><dt>**Bateria \_ DEFINIR a \_ descarga \_ suportada como**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-124"><dt>**BATTERY\_SET\_DISCHARGE\_SUPPORTED**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="01b3d-125">Indica que as solicitações Set Information do tipo BatteryDischarge são suportadas por esse dispositivo de bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-125">Indicates that set information requests of the type BatteryDischarge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <span data-ttu-id="01b3d-126"><dt>**Bateria \_ \_Bateria do sistema**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-126"><dt>**BATTERY\_SYSTEM\_BATTERY**</dt> <dt>0x80000000</dt></span></span> </dl>                             | <span data-ttu-id="01b3d-127">Indica que a bateria pode fornecer energia geral para executar o sistema.</span><span class="sxs-lookup"><span data-stu-id="01b3d-127">Indicates that the battery can provide general power to run the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="01b3d-128">**Tecnologia**</span><span class="sxs-lookup"><span data-stu-id="01b3d-128">**Technology**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-129">A tecnologia da bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-129">The battery technology.</span></span> <span data-ttu-id="01b3d-130">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="01b3d-130">This member can be one of the following values.</span></span>



| <span data-ttu-id="01b3d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="01b3d-131">Value</span></span>                                                                        | <span data-ttu-id="01b3d-132">Significado</span><span class="sxs-lookup"><span data-stu-id="01b3d-132">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="01b3d-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="01b3d-134">Bateria Nonrechargeable, por exemplo, Alkaline.</span><span class="sxs-lookup"><span data-stu-id="01b3d-134">Nonrechargeable battery, for example, alkaline.</span></span><br/> |
| <dl> <span data-ttu-id="01b3d-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="01b3d-136">Bateria recarregáveis, por exemplo, chumbo em acid.</span><span class="sxs-lookup"><span data-stu-id="01b3d-136">Rechargeable battery, for example, lead acid.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="01b3d-137">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="01b3d-137">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="01b3d-138">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="01b3d-139">**Química**</span><span class="sxs-lookup"><span data-stu-id="01b3d-139">**Chemistry**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-140">Uma cadeia de caracteres abreviada que indica a química da bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-140">An abbreviated character string that indicates the battery's chemistry.</span></span> <span data-ttu-id="01b3d-141">Essa cadeia de caracteres não é necessariamente terminada em zero.</span><span class="sxs-lookup"><span data-stu-id="01b3d-141">This string is not necessarily zero-terminated.</span></span> <span data-ttu-id="01b3d-142">A seguir está uma lista parcial de abreviações que podem ser retornadas e o chemistries associado.</span><span class="sxs-lookup"><span data-stu-id="01b3d-142">The following is a partial list of abbreviations that can be returned and the associated chemistries.</span></span>



| <span data-ttu-id="01b3d-143">Cadeia de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="01b3d-143">Unicode string</span></span>                                                                                                                                           | <span data-ttu-id="01b3d-144">Significado</span><span class="sxs-lookup"><span data-stu-id="01b3d-144">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <span data-ttu-id="01b3d-145"><dt>**PbAc**</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-145"><dt>**PbAc**</dt></span></span> </dl> | <span data-ttu-id="01b3d-146">Acid de chumbo</span><span class="sxs-lookup"><span data-stu-id="01b3d-146">Lead Acid</span></span><br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <span data-ttu-id="01b3d-147"><dt>**LION**</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-147"><dt>**LION**</dt></span></span> </dl>                        | <span data-ttu-id="01b3d-148">Íon de lítio</span><span class="sxs-lookup"><span data-stu-id="01b3d-148">Lithium Ion</span></span><br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <span data-ttu-id="01b3d-149"><dt>**Li-I**</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-149"><dt>**Li-I**</dt></span></span> </dl> | <span data-ttu-id="01b3d-150">Íon de lítio</span><span class="sxs-lookup"><span data-stu-id="01b3d-150">Lithium Ion</span></span><br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <span data-ttu-id="01b3d-151"><dt>**NiCd**</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-151"><dt>**NiCd**</dt></span></span> </dl> | <span data-ttu-id="01b3d-152">Cádmio de níquel</span><span class="sxs-lookup"><span data-stu-id="01b3d-152">Nickel Cadmium</span></span><br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <span data-ttu-id="01b3d-153"><dt>**NiMH**</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-153"><dt>**NiMH**</dt></span></span> </dl> | <span data-ttu-id="01b3d-154">Hydride de metal de níquel</span><span class="sxs-lookup"><span data-stu-id="01b3d-154">Nickel Metal Hydride</span></span><br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <span data-ttu-id="01b3d-155"><dt>**NiZn**</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-155"><dt>**NiZn**</dt></span></span> </dl> | <span data-ttu-id="01b3d-156">Zinc de níquel</span><span class="sxs-lookup"><span data-stu-id="01b3d-156">Nickel Zinc</span></span><br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <span data-ttu-id="01b3d-157"><dt>**RAM**</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-157"><dt>**RAM**</dt></span></span> </dl>                           | <span data-ttu-id="01b3d-158">Alkaline-Manganese recarregáveis</span><span class="sxs-lookup"><span data-stu-id="01b3d-158">Rechargeable Alkaline-Manganese</span></span><br/> |



 

<span data-ttu-id="01b3d-159">Outros chemistries podem aparecer no futuro e seu código deve ser capaz de tratá-los.</span><span class="sxs-lookup"><span data-stu-id="01b3d-159">Other chemistries may appear in the future and your code should be able to handle them.</span></span>

</dd> <dt>

<span data-ttu-id="01b3d-160">**DesignedCapacity**</span><span class="sxs-lookup"><span data-stu-id="01b3d-160">**DesignedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-161">A capacidade teórica da bateria quando nova, em mWh, a menos que a capacidade da bateria \_ \_ relativa esteja definida.</span><span class="sxs-lookup"><span data-stu-id="01b3d-161">The theoretical capacity of the battery when new, in mWh unless BATTERY\_CAPACITY\_RELATIVE is set.</span></span> <span data-ttu-id="01b3d-162">Nesse caso, as unidades são indefinidas.</span><span class="sxs-lookup"><span data-stu-id="01b3d-162">In that case, the units are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="01b3d-163">**FullChargedCapacity**</span><span class="sxs-lookup"><span data-stu-id="01b3d-163">**FullChargedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-164">A capacidade totalmente carregada atual da bateria em mWh (ou relativa).</span><span class="sxs-lookup"><span data-stu-id="01b3d-164">The battery's current fully charged capacity in mWh (or relative).</span></span> <span data-ttu-id="01b3d-165">Compare esse valor com **DesignedCapacity** para estimar o desgaste da bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-165">Compare this value to **DesignedCapacity** to estimate the battery's wear.</span></span>

</dd> <dt>

<span data-ttu-id="01b3d-166">**DefaultAlert1**</span><span class="sxs-lookup"><span data-stu-id="01b3d-166">**DefaultAlert1**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-167">A capacidade sugerida do fabricante, em mWh, em que um alerta de bateria baixa deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="01b3d-167">The manufacturer's suggested capacity, in mWh, at which a low battery alert should occur.</span></span> <span data-ttu-id="01b3d-168">Definições de baixo variam de fabricante para fabricante.</span><span class="sxs-lookup"><span data-stu-id="01b3d-168">Definitions of low vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="01b3d-169">Em geral, um estado de aviso ocorrerá antes de um estado baixo, mas você não deve presumir que ele sempre será.</span><span class="sxs-lookup"><span data-stu-id="01b3d-169">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="01b3d-170">Para reduzir o risco de perda de dados, esse valor geralmente é usado como a configuração padrão para o alarme de bateria crítico.</span><span class="sxs-lookup"><span data-stu-id="01b3d-170">To reduce risk of data loss, this value is usually used as the default setting for the critical battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="01b3d-171">**DefaultAlert2**</span><span class="sxs-lookup"><span data-stu-id="01b3d-171">**DefaultAlert2**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-172">A capacidade sugerida do fabricante, em mWh, na qual um alerta de bateria de aviso deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="01b3d-172">The manufacturer's suggested capacity, in mWh, at which a warning battery alert should occur.</span></span> <span data-ttu-id="01b3d-173">As definições de aviso variam de fabricante para fabricante.</span><span class="sxs-lookup"><span data-stu-id="01b3d-173">Definitions of warning vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="01b3d-174">Em geral, um estado de aviso ocorrerá antes de um estado baixo, mas você não deve presumir que ele sempre será.</span><span class="sxs-lookup"><span data-stu-id="01b3d-174">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="01b3d-175">Para reduzir o risco de perda de dados, esse valor geralmente é usado como a configuração padrão para o alarme de bateria fraca.</span><span class="sxs-lookup"><span data-stu-id="01b3d-175">To reduce risk of data loss, this value is usually used as the default setting for the low battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="01b3d-176">**CriticalBias**</span><span class="sxs-lookup"><span data-stu-id="01b3d-176">**CriticalBias**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-177">Uma tendência de zero, em mWh, que é aplicada ao relatório de bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-177">A bias from zero, in mWh, which is applied to battery reporting.</span></span> <span data-ttu-id="01b3d-178">Algumas baterias reservam um pequeno encargo que se ajusta dos valores de capacidade da bateria para mostrar "0" como o nível de bateria crítico.</span><span class="sxs-lookup"><span data-stu-id="01b3d-178">Some batteries reserve a small charge that is biased out of the battery's capacity values to show "0" as the critical battery level.</span></span> <span data-ttu-id="01b3d-179">A diferença crítica é análoga à definição de um medidor de combustível para mostrar "vazio" quando há vários litros de combustível deixados.</span><span class="sxs-lookup"><span data-stu-id="01b3d-179">Critical bias is analogous to setting a fuel gauge to show "empty" when there are several liters of fuel left.</span></span>

</dd> <dt>

<span data-ttu-id="01b3d-180">**CycleCount**</span><span class="sxs-lookup"><span data-stu-id="01b3d-180">**CycleCount**</span></span>
</dt> <dd>

<span data-ttu-id="01b3d-181">O número de ciclos de cobrança/descarga que a bateria experimentou.</span><span class="sxs-lookup"><span data-stu-id="01b3d-181">The number of charge/discharge cycles the battery has experienced.</span></span> <span data-ttu-id="01b3d-182">Isso fornece um meio para determinar o desgaste da bateria.</span><span class="sxs-lookup"><span data-stu-id="01b3d-182">This provides a means to determine the battery's wear.</span></span> <span data-ttu-id="01b3d-183">Se a bateria não oferecer suporte a um contador de ciclo, esse membro será zero.</span><span class="sxs-lookup"><span data-stu-id="01b3d-183">If the battery does not support a cycle counter, this member is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01b3d-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="01b3d-184">Remarks</span></span>

<span data-ttu-id="01b3d-185">Geralmente, um estado de aviso ocorre antes de um estado baixo, mas você não deve presumir isso.</span><span class="sxs-lookup"><span data-stu-id="01b3d-185">Generally, a warning state occurs before a low state, but you should not assume it will.</span></span> <span data-ttu-id="01b3d-186">É possível sondar uma bateria e descobrir que nenhum nível de alerta ocorreu e sondar a bateria novamente e encontrá-la descarregada na medida em que os dois níveis foram atingidos.</span><span class="sxs-lookup"><span data-stu-id="01b3d-186">It is possible to poll a battery and find that neither alert level has occurred, and poll the battery again and find it discharged to the extent that both levels have been achieved.</span></span> <span data-ttu-id="01b3d-187">Isso pode indicar que você não está sondando com frequência suficiente.</span><span class="sxs-lookup"><span data-stu-id="01b3d-187">This may indicate that you are not polling often enough.</span></span> <span data-ttu-id="01b3d-188">Isso também pode indicar que a bateria não pode manter uma cobrança por muito tempo e está descarregando mais rapidamente do que o esperado.</span><span class="sxs-lookup"><span data-stu-id="01b3d-188">It may also indicate that the battery is unable to hold a charge for very long and is discharging more rapidly than you expected.</span></span> <span data-ttu-id="01b3d-189">Essa bateria pode estar se aproximando do fim de sua vida útil ou pode estar danificada.</span><span class="sxs-lookup"><span data-stu-id="01b3d-189">Such a battery may be nearing the end of its useful life, or it may be damaged.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b3d-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01b3d-190">Requirements</span></span>



| <span data-ttu-id="01b3d-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b3d-191">Requirement</span></span> | <span data-ttu-id="01b3d-192">Valor</span><span class="sxs-lookup"><span data-stu-id="01b3d-192">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b3d-193">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01b3d-193">Minimum supported client</span></span><br/> | <span data-ttu-id="01b3d-194">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01b3d-194">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="01b3d-195">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01b3d-195">Minimum supported server</span></span><br/> | <span data-ttu-id="01b3d-196">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01b3d-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="01b3d-197">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01b3d-197">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b3d-198"><dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="01b3d-198"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b3d-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="01b3d-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b3d-200">**\_informações de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="01b3d-200">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




