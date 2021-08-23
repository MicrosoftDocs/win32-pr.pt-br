---
description: Uma classe base abstrata para as classes de dados preinstaladas e calculadas.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Classe Win32_PerfFormattedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 55a765102d5fcc40caff41a7fa68184afea114838152dd84157d506a62c15da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020134"
---
# <a name="win32_perfformatteddata-class"></a>\_Classe Win32 PerfFormattedData

Uma classe base abstrata para as classes de dados preinstaladas e calculadas. Um exemplo dessa classe é o [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md). essas classes contêm valores calculados fornecidos pelo [Provedor de Dados de desempenho formatado](../wmisdk/formatted-performance-data-provider.md)de alto desempenho.

A sintaxe a seguir é simplificada do código MOF e mostra todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ PerfFormattedData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PerfFormattedData** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrição textual para a estatística ou métrica.

Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual da estatística ou métrica.

Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

</dd> <dt>

**\_Objeto Frequency**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Frequência em tiques por segundo da propriedade **do \_ objeto timestamp** . Quando em subclasse, o provedor define essa propriedade.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).

</dd> <dt>

**Frequência \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Frequência em tiques por segundo da propriedade **de \_ PerfTime de frequência** . um valor pode ser obtido chamando a função Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).

</dd> <dt>

**Frequência \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Frequência em tiques por segundo da propriedade **timestamp \_ Sys100NS** (10 milhões).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Rótulo pelo qual a estatística ou métrica é conhecida. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

</dd> <dt>

**\_Objeto timestamp**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Carimbo de data/hora definido pelo objeto. O provedor define sua propriedade.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).

</dd> <dt>

**Carimbo de data/hora \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Carimbo de data/hora do contador de alto desempenho. um valor pode ser obtido chamando a função Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).

</dd> <dt>

**\_Sys100NS timestamp**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor de carimbo de data/hora em unidades de 100 nanossegundos.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ PerfFormattedData** é derivada do [**\_ desempenho do Win32**](win32-perf.md), que é derivado de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md). A classe é encontrada no namespace **raiz \\ cimv2** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                             |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Desempenho do Win32 \_**](win32-perf.md)
</dt> <dt>

[Classes de contador de desempenho](performance-counter-classes.md)
</dt> <dt>

[Acessando classes de desempenho de WMI pré-instalado](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tarefas do WMI: monitoramento de desempenho](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Acessando dados de desempenho no script](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
