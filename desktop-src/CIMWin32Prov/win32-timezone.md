---
description: O \_ fuso horário do Win32&\# 8194; A classe WMI representa as informações de fuso horário de um sistema de computador executando o Windows, que inclui as alterações necessárias para fazer a transição para a transição de horário de verão.
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Classe Win32_TimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826338"
---
# <a name="win32_timezone-class"></a><span data-ttu-id="5dc4f-103">\_Classe de fuso horário Win32</span><span class="sxs-lookup"><span data-stu-id="5dc4f-103">Win32\_TimeZone class</span></span>

<span data-ttu-id="5dc4f-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ fuso** horário do Win32 representa as informações de fuso horário de um sistema de computador executando o Windows, que inclui as alterações necessárias para fazer a transição para a transição de horário de verão.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-104">The **Win32\_TimeZone** [WMI class](../wmisdk/retrieving-a-class.md) represents the time zone information for a computer system running Windows, which includes the changes required for transitioning to daylight saving time transition.</span></span>

<span data-ttu-id="5dc4f-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5dc4f-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc4f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5dc4f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a><span data-ttu-id="5dc4f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5dc4f-108">Members</span></span>

<span data-ttu-id="5dc4f-109">A **classe \_ timezone do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5dc4f-109">The **Win32\_TimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="5dc4f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5dc4f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5dc4f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5dc4f-111">Properties</span></span>

<span data-ttu-id="5dc4f-112">A classe de **\_ fuso horário do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-112">The **Win32\_TimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5dc4f-113">**Tendência**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-113">**Bias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-114">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-116">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api diferença de \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-117">Tendência atual de conversão de horário local.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-117">Current bias for local time translation.</span></span> <span data-ttu-id="5dc4f-118">A tendência é a diferença entre o tempo universal coordenado (UTC) e a hora local.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-118">The bias is the difference between Coordinated Universal Time (UTC) and local time.</span></span> <span data-ttu-id="5dc4f-119">Todas as traduções entre o UTC e a hora local são baseadas na seguinte fórmula: UTC = diferença de tempo local.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-119">All translations between UTC and local time are based on the following formula: UTC = local time - bias.</span></span> <span data-ttu-id="5dc4f-120">Esta propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-120">This property is required.</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-124">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-125">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-125">Short textual description of the current object.</span></span>

<span data-ttu-id="5dc4f-126">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="5dc4f-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-127">**Diferençadohoráriodeverão**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-127">**DaylightBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-128">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-130">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| diferençadohoráriodeverão"), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-131">Valor de tendência a ser usado durante as traduções de hora local que ocorrem durante o horário de verão.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-131">Bias value to be used during local time translations that occur during daylight saving time.</span></span> <span data-ttu-id="5dc4f-132">Essa propriedade será ignorada se um valor para a propriedade **DaylightDay** não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-132">This property is ignored if a value for the **DaylightDay** property is not supplied.</span></span> <span data-ttu-id="5dc4f-133">O valor dessa propriedade é adicionado à propriedade **Bias** para formar a tendência usada durante o horário de verão.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-133">The value of this property is added to the **Bias** property to form the bias used during daylight time.</span></span> <span data-ttu-id="5dc4f-134">Na maioria dos fusos horários, o valor dessa propriedade é-60.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-134">In most time zones, the value of this property is -60.</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-135">**DaylightDay**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-135">**DaylightDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-136">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-138">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| WDIA")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-139">**DaylightDayOfWeek** **DaylightMonth** quando a transição do horário padrão para o horário de Verão ocorre neste sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-139">**DaylightDayOfWeek** of the **DaylightMonth** when the transition from standard time to daylight saving time occurs on this operating system.</span></span>

<span data-ttu-id="5dc4f-140">Exemplo: se o dia de transição (**DaylightDayOfWeek**) ocorrer em um domingo, o valor "1" indicará o primeiro domingo do **DaylightMonth**, "2" indica o segundo domingo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-140">Example: If the transition day (**DaylightDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **DaylightMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="5dc4f-141">O valor "5" indica o último **DaylightDayOfWeek** no mês.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-141">The value "5" indicates the last **DaylightDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-142">**DaylightDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-142">**DaylightDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-143">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-145">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wdiadasemana")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-146">Dia da semana em que a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-146">Day of the week when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="5dc4f-147">**Domingo** (0)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-147">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="5dc4f-148">**Segunda** (1)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-148">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="5dc4f-149">**Terça-feira** (2)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-149">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="5dc4f-150">**Quarta-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-150">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="5dc4f-151">**Quinta-feira** (4)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-151">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="5dc4f-152">**Sexta-feira** (5)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-152">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="5dc4f-153">**Sábado** (6)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-153">**Saturday** (6)</span></span>


<span data-ttu-id="5dc4f-154"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5dc4f-154"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="5dc4f-155">Example: 1</span><span class="sxs-lookup"><span data-stu-id="5dc4f-155">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-156">**DaylightHour**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-156">**DaylightHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-159">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| Whora")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-160">Hora do dia em que a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-160">Hour of the day when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="5dc4f-161">Exemplo: 2</span><span class="sxs-lookup"><span data-stu-id="5dc4f-161">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-162">**DaylightMillisecond**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-162">**DaylightMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-165">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wmilissegundos")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-165">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-166">Milissegundo de **DaylightSecond** quando a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-166">Millisecond of the **DaylightSecond** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-167">**DaylightMinute**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-167">**DaylightMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-170">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wminuto")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-171">Minuto do **DaylightHour** quando a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-171">Minute of the **DaylightHour** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="5dc4f-172">Exemplo: 59</span><span class="sxs-lookup"><span data-stu-id="5dc4f-172">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-173">**DaylightMonth**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-173">**DaylightMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-174">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-176">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wmês")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-177">Mês em que a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-177">Month when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="5dc4f-178">**Janeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-178">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="5dc4f-179">**Fevereiro** (2)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-179">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="5dc4f-180">**Março** (3)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-180">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="5dc4f-181">**Abril** (4)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-181">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="5dc4f-182">**Maio** (5)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-182">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="5dc4f-183">**Junho** (6)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-183">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="5dc4f-184">**Julho** (7)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-184">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="5dc4f-185">**Agosto** (8)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-185">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="5dc4f-186">**Setembro** (9)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-186">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="5dc4f-187">**Outubro** (10)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-187">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="5dc4f-188">**Novembro** (11)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-188">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="5dc4f-189">**Dezembro** (12)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-189">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5dc4f-190">**Nomepadrão**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-190">**DaylightName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-193">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| estruturas de tempo \| [**hora \_ \_ informações do fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)do \| horário de verão")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightName")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-194">Fuso horário que está sendo representado quando o horário de verão está em vigor.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-194">Time zone being represented when daylight saving time is in effect.</span></span>

<span data-ttu-id="5dc4f-195">Exemplo: "EDT" (horário de Verão do leste)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-195">Example: "EDT" (Eastern Daylight Time)</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-196">**DaylightSecond**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-196">**DaylightSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-199">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wsegundo")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-199">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-200">Segundo **DaylightMinute** quando a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-200">Second of the **DaylightMinute** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="5dc4f-201">Exemplo: 59</span><span class="sxs-lookup"><span data-stu-id="5dc4f-201">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-202">**DaylightYear**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-202">**DaylightYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-203">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-205">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| Wano")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-206">Ano em que o horário de verão está em vigor.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-206">Year when daylight saving time is in effect.</span></span> <span data-ttu-id="5dc4f-207">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-207">This property is not required.</span></span>

<span data-ttu-id="5dc4f-208">Exemplo: 1997</span><span class="sxs-lookup"><span data-stu-id="5dc4f-208">Example: 1997</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-209">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-209">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-212">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-212">Textual description of the current object.</span></span>

<span data-ttu-id="5dc4f-213">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="5dc4f-213">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-214">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-214">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-217">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-217">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-218">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-218">Identifier by which the current object is known.</span></span>

<span data-ttu-id="5dc4f-219">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="5dc4f-219">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-220">**Diferençapadrão**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-220">**StandardBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-221">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-223">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| diferençapadrão"), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-224">O valor de tendência a ser usado quando o horário de verão não está em vigor.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-224">Bias value to use when daylight saving time is not in effect.</span></span> <span data-ttu-id="5dc4f-225">Essa propriedade será ignorada se um valor de **StandardDay** não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-225">This property is ignored if a value for **StandardDay** is not supplied.</span></span> <span data-ttu-id="5dc4f-226">O valor dessa propriedade é adicionado à propriedade **Bias** para formar a tendência durante o horário padrão.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-226">The value of this property is added to the **Bias** property to form the bias during standard time.</span></span>

<span data-ttu-id="5dc4f-227">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="5dc4f-227">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-228">**StandardDay**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-228">**StandardDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-229">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-231">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datapadrão \| WDIA")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-232">**StandardDayOfWeek** **StandardMonth** quando a transição do horário de verão para o horário padrão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-232">**StandardDayOfWeek** of the **StandardMonth** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="5dc4f-233">Se o dia de transição (**StandardDayOfWeek**) ocorrer em um domingo, o valor "1" indicará o primeiro domingo do **StandardMonth**, "2" indica o segundo domingo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-233">If the transition day (**StandardDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **StandardMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="5dc4f-234">O valor "5" indica o último **StandardDayOfWeek** no mês.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-234">The value "5" indicates the last **StandardDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-235">**StandardDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-235">**StandardDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-236">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-236">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-238">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datapadrão \| wdiadasemana")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-239">Dia da semana em que a transição do horário de verão para o horário padrão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-239">Day of the week when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="5dc4f-240">**Domingo** (0)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-240">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="5dc4f-241">**Segunda** (1)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-241">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="5dc4f-242">**Terça-feira** (2)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-242">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="5dc4f-243">**Quarta-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-243">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="5dc4f-244">**Quinta-feira** (4)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-244">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="5dc4f-245">**Sexta-feira** (5)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-245">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="5dc4f-246">**Sábado** (6)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-246">**Saturday** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5dc4f-247">**StandardHour**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-247">**StandardHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-248">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-248">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-250">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datapadrão \| Whora")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-251">Hora do dia em que a transição do horário de verão para o horário padrão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-251">Hour of the day when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="5dc4f-252">Exemplo: 11</span><span class="sxs-lookup"><span data-stu-id="5dc4f-252">Example: 11</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-253">**StandardMillisecond**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-253">**StandardMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-254">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-256">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datapadrão \| wmilissegundos")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-256">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-257">Milissegundo do **StandardSecond** quando a transição do horário de verão para o horário padrão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-257">Millisecond of the **StandardSecond** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-258">**StandardMinute**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-258">**StandardMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-259">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-261">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datapadrão \| wminuto")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-261">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-262">Minuto do **StandardDay** quando a transição do horário de verão para o horário padrão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-262">Minute of the **StandardDay** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="5dc4f-263">Exemplo: 59</span><span class="sxs-lookup"><span data-stu-id="5dc4f-263">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-264">**StandardMonth**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-264">**StandardMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-265">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-267">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datapadrão \| wmês")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-267">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-268">Mês em que a transição do horário de verão para o horário padrão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-268">Month when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="5dc4f-269">**Janeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-269">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="5dc4f-270">**Fevereiro** (2)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-270">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="5dc4f-271">**Março** (3)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-271">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="5dc4f-272">**Abril** (4)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-272">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="5dc4f-273">**Maio** (5)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-273">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="5dc4f-274">**Junho** (6)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-274">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="5dc4f-275">**Julho** (7)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-275">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="5dc4f-276">**Agosto** (8)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-276">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="5dc4f-277">**Setembro** (9)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-277">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="5dc4f-278">**Outubro** (10)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-278">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="5dc4f-279">**Novembro** (11)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-279">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="5dc4f-280">**Dezembro** (12)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-280">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5dc4f-281">**Nomepadrão**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-281">**StandardName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-284">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| estruturas de tempo \| [**hora do \_ fuso \_ horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-284">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardName")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-285">Nome do fuso horário que está sendo representado quando o horário padrão está em vigor.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-285">Name of the time zone being represented when standard time is in effect.</span></span>

<span data-ttu-id="5dc4f-286">Exemplo: "EST" (hora padrão do leste)</span><span class="sxs-lookup"><span data-stu-id="5dc4f-286">Example: "EST" (Eastern Standard Time)</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-287">**StandardSecond**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-287">**StandardSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-288">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-290">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datapadrão \| wsegundo")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-290">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-291">Segundo **StandardMinute** quando a transição do horário de verão para o horário padrão ocorre em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-291">Second of the **StandardMinute** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="5dc4f-292">Exemplo: 59</span><span class="sxs-lookup"><span data-stu-id="5dc4f-292">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="5dc4f-293">**StandardYear**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-293">**StandardYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc4f-294">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dc4f-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc4f-296">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datapadrão \| Wano")</span><span class="sxs-lookup"><span data-stu-id="5dc4f-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="5dc4f-297">Ano em que a hora padrão está em vigor.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-297">Year when standard time is in effect.</span></span> <span data-ttu-id="5dc4f-298">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-298">This property is not required.</span></span>

<span data-ttu-id="5dc4f-299">Exemplo: 1997</span><span class="sxs-lookup"><span data-stu-id="5dc4f-299">Example: 1997</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dc4f-300">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dc4f-300">Remarks</span></span>

<span data-ttu-id="5dc4f-301">A classe de **\_ fuso horário Win32** é derivada da [**\_ configuração CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="5dc4f-301">The **Win32\_TimeZone** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="5dc4f-302">Você não pode usar formatos de data e hora padrão, como 10/18/2002, ao gravar consultas WMI.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-302">You cannot use standard date-time formats - such as 10/18/2002 - when writing WMI queries.</span></span> <span data-ttu-id="5dc4f-303">Em vez disso, você precisa converter todas as datas usadas em suas consultas para o formato UTC.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-303">Instead, you need to convert any dates used in your queries to UTC format.</span></span> <span data-ttu-id="5dc4f-304">Isso requer duas etapas: 1) você deve determinar o deslocamento (diferença em minutos) entre o fuso horário e o horário de Greenwich e 2) você deve converter 10/18/2002 em um valor UTC.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-304">This requires two steps: 1) You must determine the offset (difference in minutes) between your time zone and Greenwich Mean Time, and 2) you must convert 10/18/2002 to a UTC value.</span></span>

<span data-ttu-id="5dc4f-305">Determinando o deslocamento do tempo médio de Greenwich</span><span class="sxs-lookup"><span data-stu-id="5dc4f-305">Determining the Offset from Greenwich Mean Time</span></span>

<span data-ttu-id="5dc4f-306">Reconhecidamente, o WMI dificulta o trabalho com datas e horários; Felizmente, o WMI, pelo menos, facilita a determinação do deslocamento entre o fuso horário e o horário de Greenwich.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-306">Admittedly, WMI makes it difficult to work with dates and times; fortunately, WMI at least makes it easy to determine the offset between your time zone and Greenwich Mean Time.</span></span> <span data-ttu-id="5dc4f-307">O fuso horário Win32 da classe WMI \_ inclui uma propriedade-Bias-que retorna o deslocamento GMT.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-307">The WMI class Win32\_TimeZone includes a property - Bias - that returns the GMT offset.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



<span data-ttu-id="5dc4f-308">Convertendo uma data em um valor UTC</span><span class="sxs-lookup"><span data-stu-id="5dc4f-308">Converting a Date to a UTC Value</span></span>

<span data-ttu-id="5dc4f-309">Depois de determinar o deslocamento GMT, você deve converter uma data padrão, como 10/18/2002, em uma data UTC.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-309">After you determine the GMT offset, you must then convert a standard date such as 10/18/2002 to a UTC date.</span></span> <span data-ttu-id="5dc4f-310">Para converter uma data padrão em uma data UTC, você pode usar funções de data do VBScript, como ano, mês e dia, para isolar os componentes individuais que compõem uma data UTC.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-310">To convert a standard date to a UTC date, you can use VBScript date functions such as Year, Month, and Day to isolate the individual components that make up a UTC date.</span></span> <span data-ttu-id="5dc4f-311">Depois de ter valores individuais para esses componentes, você pode concatena-los da mesma maneira como faria com qualquer outro valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-311">After you have individual values for these components, you can concatenate them in the same manner as you would any other string value.</span></span> <span data-ttu-id="5dc4f-312">As datas UTC são tratadas como cadeias de caracteres, pois o deslocamento GMT deve ser acrescentado ao final.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-312">UTC dates are treated as strings because the GMT offset must be appended to the end.</span></span> <span data-ttu-id="5dc4f-313">Se a data foi vista como um número, este valor:</span><span class="sxs-lookup"><span data-stu-id="5dc4f-313">If the date were seen as a number, this value:</span></span>

`20011018113047.000000-480`

<span data-ttu-id="5dc4f-314">Seria tratado erroneamente como uma equação matemática (parênteses adicionados para maior clareza):</span><span class="sxs-lookup"><span data-stu-id="5dc4f-314">Would be erroneously treated as a mathematical equation (parentheses added for clarity):</span></span>

`(20011018113047.000000) - (480)`

<span data-ttu-id="5dc4f-315">Por exemplo, na data 10/18/2002, os componentes individuais são:</span><span class="sxs-lookup"><span data-stu-id="5dc4f-315">For example, in the date 10/18/2002, the individual components are:</span></span>

-   <span data-ttu-id="5dc4f-316">Ano: 2002</span><span class="sxs-lookup"><span data-stu-id="5dc4f-316">Year: 2002</span></span>
-   <span data-ttu-id="5dc4f-317">Mês: 10</span><span class="sxs-lookup"><span data-stu-id="5dc4f-317">Month: 10</span></span>
-   <span data-ttu-id="5dc4f-318">Dia: 18</span><span class="sxs-lookup"><span data-stu-id="5dc4f-318">Day: 18</span></span>

<span data-ttu-id="5dc4f-319">O script precisaria combinar esses três valores, a cadeia de caracteres "113047, 0" (representando a hora, incluindo milissegundos) e o deslocamento de GMT para derivar uma data UTC.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-319">The script would need to combine these three values, the string "113047.000000" (representing the time, including milliseconds), and the GMT offset to derive a UTC date.</span></span> <span data-ttu-id="5dc4f-320">Por exemplo, (os parênteses foram adicionados novamente para maior clareza):</span><span class="sxs-lookup"><span data-stu-id="5dc4f-320">For example, (parentheses again added for clarity):</span></span>

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> <span data-ttu-id="5dc4f-321">Você pode usar as funções do VBScript de hora, minuto e segundo para converter a parte de hora de uma data UTC.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-321">You can use the VBScript functions Hour, Minute, and Second to convert the time portion of a UTC date.</span></span> <span data-ttu-id="5dc4f-322">Portanto, uma hora como 11:30:47 A.M.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-322">Thus, a time such as 11:30:47 A.M.</span></span> <span data-ttu-id="5dc4f-323">seria convertido em 113047.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-323">would be converted to 113047.</span></span>

 

<span data-ttu-id="5dc4f-324">Há um fator de complicação.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-324">There is one complicating factor.</span></span> <span data-ttu-id="5dc4f-325">O mês deve ocupar as posições 5 e 6 na cadeia de caracteres; o dia deve ocupar as posições 7 e 8.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-325">The month must take up positions 5 and 6 in the string; the day must take up positions 7 and 8.</span></span> <span data-ttu-id="5dc4f-326">Isso não é problema com o mês 10 e o dia 18.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-326">This is no problem with month 10 and day 18.</span></span> <span data-ttu-id="5dc4f-327">Mas como você obtém 5 de julho (mês 7, dia 5) para preencher as posições de requisito?</span><span class="sxs-lookup"><span data-stu-id="5dc4f-327">But how do you get July 5 (month 7, day 5) to fill up the requisite positions?</span></span> <span data-ttu-id="5dc4f-328">A resposta é adicionar um zero à esquerda a cada valor, alterando assim o 7 para 07 e o 5 a 05.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-328">The answer is to add a leading zero to each value, thus changing the 7 to 07 and the 5 to 05.</span></span>

<span data-ttu-id="5dc4f-329">Para fazer isso, use a função de Len do VBScript para verificar o comprimento (número de caracteres) no mês e no dia.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-329">To do this, use the VBScript Len function to check the length (number of characters) in the month and the day.</span></span> <span data-ttu-id="5dc4f-330">Se o comprimento for 1 (o que significa que há apenas um caractere), adicione um zero à esquerda.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-330">If the length is 1 (meaning that there is just one character), add a leading zero.</span></span> <span data-ttu-id="5dc4f-331">Dessa</span><span class="sxs-lookup"><span data-stu-id="5dc4f-331">Thus:</span></span>


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a><span data-ttu-id="5dc4f-332">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5dc4f-332">Examples</span></span>

<span data-ttu-id="5dc4f-333">O exemplo de VBScript a seguir converte a data atual em uma data UTC.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-333">The following VBScript example converts the current date to a UTC date.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



<span data-ttu-id="5dc4f-334">O VBScript a seguir sampledetermines o deslocamento de GMT e, em seguida, converte uma data atual especificada (neste caso, 10/18/2002) para o formato de data/hora UTC.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-334">The following VBScript sampledetermines the GMT offset, and then converts a specified current date (in this case, 10/18/2002) to UTC date-time format.</span></span> <span data-ttu-id="5dc4f-335">Depois que a data tiver sido convertida, esse valor será usado para pesquisar um computador e retornará uma lista de todas as pastas que foram criadas após 10/18/2002.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-335">After the date has been converted, that value is used to search a computer and returns a list of all the folders that were created after 10/18/2002.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



<span data-ttu-id="5dc4f-336">O exemplo de código VBScript a seguir exibe as configurações para \_ instâncias de fuso horário do Win32.</span><span class="sxs-lookup"><span data-stu-id="5dc4f-336">The following VBScript code example displays the settings for Win32\_TimeZone instances.</span></span>


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a><span data-ttu-id="5dc4f-337">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dc4f-337">Requirements</span></span>



| <span data-ttu-id="5dc4f-338">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dc4f-338">Requirement</span></span> | <span data-ttu-id="5dc4f-339">Valor</span><span class="sxs-lookup"><span data-stu-id="5dc4f-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc4f-340">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dc4f-340">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc4f-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dc4f-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5dc4f-342">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dc4f-342">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc4f-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dc4f-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5dc4f-344">Namespace</span><span class="sxs-lookup"><span data-stu-id="5dc4f-344">Namespace</span></span><br/>                | <span data-ttu-id="5dc4f-345">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5dc4f-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5dc4f-346">MOF</span><span class="sxs-lookup"><span data-stu-id="5dc4f-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5dc4f-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5dc4f-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5dc4f-348">DLL</span><span class="sxs-lookup"><span data-stu-id="5dc4f-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dc4f-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dc4f-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dc4f-350">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dc4f-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc4f-351">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-351">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="5dc4f-352">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="5dc4f-352">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5dc4f-353">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="5dc4f-353">**SWbemDateTime**</span></span>](../wmisdk/swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="5dc4f-354">Formato de data e hora</span><span class="sxs-lookup"><span data-stu-id="5dc4f-354">Date and Time Format</span></span>](../wmisdk/date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="5dc4f-355">Tarefas do WMI: datas e horas</span><span class="sxs-lookup"><span data-stu-id="5dc4f-355">WMI Tasks: Dates and Times</span></span>](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
