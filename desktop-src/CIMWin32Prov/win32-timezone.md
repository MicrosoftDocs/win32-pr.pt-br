---
description: O \_ fuso horário do Win32&\# 8194; a classe WMI representa as informações de fuso horário de um sistema de computador executando Windows, que inclui as alterações necessárias para fazer a transição para a transição de horário de verão.
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
ms.openlocfilehash: 02b6d9d5c6100a652cf50096f5ef513fc164cfcfd2d8036e8444adc702459d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827656"
---
# <a name="win32_timezone-class"></a>\_Classe de fuso horário Win32

a  [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ fuso** horário do Win32 representa as informações de fuso horário de um sistema de computador executando Windows, que inclui as alterações necessárias para fazer a transição para a transição de horário de verão.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A **classe \_ timezone do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ fuso horário do Win32** tem essas propriedades.

<dl> <dt>

**Tendência**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api diferença de \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")
</dt> </dl>

Tendência atual de conversão de horário local. A tendência é a diferença entre o tempo universal coordenado (UTC) e a hora local. Todas as traduções entre o UTC e a hora local são baseadas na seguinte fórmula: UTC = diferença de tempo local. Esta propriedade é necessária.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**Diferençadohoráriodeverão**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| diferençadohoráriodeverão"), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")
</dt> </dl>

Valor de tendência a ser usado durante as traduções de hora local que ocorrem durante o horário de verão. Essa propriedade será ignorada se um valor para a propriedade **DaylightDay** não for fornecido. O valor dessa propriedade é adicionado à propriedade **Bias** para formar a tendência usada durante o horário de verão. Na maioria dos fusos horários, o valor dessa propriedade é-60.

</dd> <dt>

**DaylightDay**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| WDIA")
</dt> </dl>

**DaylightDayOfWeek** **DaylightMonth** quando a transição do horário padrão para o horário de Verão ocorre neste sistema operacional.

Exemplo: se o dia de transição (**DaylightDayOfWeek**) ocorrer em um domingo, o valor "1" indicará o primeiro domingo do **DaylightMonth**, "2" indica o segundo domingo e assim por diante. O valor "5" indica o último **DaylightDayOfWeek** no mês.

</dd> <dt>

**DaylightDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wdiadasemana")
</dt> </dl>

Dia da semana em que a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Segunda** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Terça-feira** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Quarta-feira** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Quinta-feira** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Sexta-feira** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (6)


</dt> <dd></dd> </dl>

Example: 1

</dd> <dt>

**DaylightHour**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| Whora")
</dt> </dl>

Hora do dia em que a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.

Exemplo: 2

</dd> <dt>

**DaylightMillisecond**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wmilissegundos")
</dt> </dl>

Milissegundo de **DaylightSecond** quando a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.

</dd> <dt>

**DaylightMinute**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wminuto")
</dt> </dl>

Minuto do **DaylightHour** quando a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.

Exemplo: 59

</dd> <dt>

**DaylightMonth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wmês")
</dt> </dl>

Mês em que a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Janeiro** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Fevereiro** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Março** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Abril** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Maio** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Junho** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Julho** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Setembro** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Outubro** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembro** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dezembro** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nomepadrão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| estruturas de tempo \| [**hora \_ \_ informações do fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)do \| horário de verão")
</dt> </dl>

Fuso horário que está sendo representado quando o horário de verão está em vigor.

Exemplo: "EDT" (horário de Verão do leste)

</dd> <dt>

**DaylightSecond**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de tempo win32api \| [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| datadohoráriodeverão \| wsegundo")
</dt> </dl>

Segundo **DaylightMinute** quando a transição do horário padrão para o horário de Verão ocorre em um sistema operacional.

Exemplo: 59

</dd> <dt>

**DaylightYear**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")
</dt> </dl>

Ano em que o horário de verão está em vigor. Essa propriedade não é necessária.

Exemplo: 1997

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**Settingid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**Standardbias**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Valor de desvio a ser usado quando o horário de verão não está em vigor. Essa propriedade será ignorada se um valor para **StandardDay** não for fornecido. O valor dessa propriedade é adicionado à propriedade **Bias** para formar o desvio durante o tempo padrão.

Exemplo: 0

</dd> <dt>

**StandardDay**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDay")
</dt> </dl>

**StandardDayOfWeek** do **StandardMonth quando** a transição do horário de verão para o horário padrão ocorre em um sistema operacional.

Se o dia de transição (**StandardDayOfWeek**) ocorrer em um domingo, o valor "1" indicará o primeiro domingo do **StandardMonth**, "2" indicará o segundo domingo e assim por diante. O valor "5" indica a última **StandardDayOfWeek** no mês.

</dd> <dt>

**StandardDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")
</dt> </dl>

Dia da semana em que a transição do horário de verão para o horário padrão ocorre em um sistema operacional.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Segunda-feira** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Terça-feira** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Quarta-feira** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Quinta-feira** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Sexta-feira** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardHour**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")
</dt> </dl>

Hora do dia em que a transição do horário de verão para o horário padrão ocorre em um sistema operacional.

Exemplo: 11

</dd> <dt>

**StandardMillisecond**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")
</dt> </dl>

Milissegundos do **StandardSecond quando** a transição do horário de verão para o horário padrão ocorre em um sistema operacional.

</dd> <dt>

**StandardMinute**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")
</dt> </dl>

Minuto do **StandardDay quando** a transição do horário de verão para o horário padrão ocorre em um sistema operacional.

Exemplo: 59

</dd> <dt>

**StandardMonth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")
</dt> </dl>

Mês em que a transição do horário de verão para o horário padrão ocorre em um sistema operacional.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Janeiro** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Fevereiro** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Março** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Abril** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Maio** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Junho** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Julho** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Setembro** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Outubro** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembro** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dezembro** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**Standardname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")
</dt> </dl>

Nome do fuso horário que está sendo representado quando a hora padrão está em vigor.

Exemplo: "EST" (Hora Padrão do Leste)

</dd> <dt>

**StandardSecond**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")
</dt> </dl>

Segundo do **StandardMinute quando** a transição do horário de verão para o horário padrão ocorre em um sistema operacional.

Exemplo: 59

</dd> <dt>

**StandardYear**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")
</dt> </dl>

Ano em que a hora padrão está em vigor. Essa propriedade não é necessária.

Exemplo: 1997

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ TimeZone** é derivada da [**configuração cim \_**](cim-setting.md).

Você não pode usar formatos de data e hora padrão, como 10/18/2002, ao gravar consultas WMI. Em vez disso, você precisa converter todas as datas usadas em suas consultas para o formato UTC. Isso requer duas etapas: 1) você deve determinar o deslocamento (diferença em minutos) entre o fuso horário e o horário de Greenwich e 2) você deve converter 10/18/2002 em um valor UTC.

Determinando o deslocamento do tempo médio de Greenwich

Reconhecidamente, o WMI dificulta o trabalho com datas e horários; Felizmente, o WMI, pelo menos, facilita a determinação do deslocamento entre o fuso horário e o horário de Greenwich. O fuso horário Win32 da classe WMI \_ inclui uma propriedade-Bias-que retorna o deslocamento GMT.


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



Convertendo uma data em um valor UTC

Depois de determinar o deslocamento GMT, você deve converter uma data padrão, como 10/18/2002, em uma data UTC. Para converter uma data padrão em uma data UTC, você pode usar funções de data do VBScript, como ano, mês e dia, para isolar os componentes individuais que compõem uma data UTC. Depois de ter valores individuais para esses componentes, você pode concatena-los da mesma maneira como faria com qualquer outro valor de cadeia de caracteres. As datas UTC são tratadas como cadeias de caracteres, pois o deslocamento GMT deve ser acrescentado ao final. Se a data foi vista como um número, este valor:

`20011018113047.000000-480`

Seria tratado erroneamente como uma equação matemática (parênteses adicionados para maior clareza):

`(20011018113047.000000) - (480)`

Por exemplo, na data 10/18/2002, os componentes individuais são:

-   Ano: 2002
-   Mês: 10
-   Dia: 18

O script precisaria combinar esses três valores, a cadeia de caracteres "113047, 0" (representando a hora, incluindo milissegundos) e o deslocamento de GMT para derivar uma data UTC. Por exemplo, (os parênteses foram adicionados novamente para maior clareza):

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> Você pode usar as funções do VBScript de hora, minuto e segundo para converter a parte de hora de uma data UTC. Portanto, uma hora como 11:30:47 A.M. seria convertido em 113047.

 

Há um fator de complicação. O mês deve ocupar as posições 5 e 6 na cadeia de caracteres; o dia deve ocupar as posições 7 e 8. Isso não é problema com o mês 10 e o dia 18. Mas como você obtém 5 de julho (mês 7, dia 5) para preencher as posições de requisito? A resposta é adicionar um zero à esquerda a cada valor, alterando assim o 7 para 07 e o 5 a 05.

Para fazer isso, use a função de Len do VBScript para verificar o comprimento (número de caracteres) no mês e no dia. Se o comprimento for 1 (o que significa que há apenas um caractere), adicione um zero à esquerda. Dessa


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir converte a data atual em uma data UTC.


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



O VBScript a seguir sampledetermines o deslocamento de GMT e, em seguida, converte uma data atual especificada (neste caso, 10/18/2002) para o formato de data/hora UTC. Depois que a data tiver sido convertida, esse valor será usado para pesquisar um computador e retornará uma lista de todas as pastas que foram criadas após 10/18/2002.


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



O exemplo de código VBScript a seguir exibe as configurações para \_ instâncias de fuso horário do Win32.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração de CIM \_**](cim-setting.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[**SWbemDateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[Formato de data e hora](../wmisdk/date-and-time-format.md)
</dt> <dt>

[Tarefas do WMI: datas e horas](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
