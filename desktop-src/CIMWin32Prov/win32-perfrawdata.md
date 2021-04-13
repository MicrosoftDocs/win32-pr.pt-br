---
description: A classe base abstrata para todas as classes de contador de desempenho brutos concretos.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Classe Win32_PerfRawData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501105"
---
# <a name="win32_perfrawdata-class"></a>\_Classe Win32 PerfRawData

A classe base abstrata para todas as classes de contador de desempenho brutos concretos.

Para aparecer no monitor do sistema, as classes do contador de desempenho devem ser adicionadas ao \\ namespace raiz cimv2 e derivadas do **Win32 \_ PerfRawData**. Os dados nessas classes são fornecidos pelo [provedor de contador de desempenho](../wmisdk/performance-counter-provider.md)de alto desempenho.

As propriedades a seguir são herdadas quando uma classe é derivada do **Win32 \_ PerfRawData**:

-   **Carimbo de data/hora \_ PerfTime**
-   **\_Sys100NS timestamp**
-   **\_Objeto timestamp**
-   **Frequência \_ PerfTime**
-   **Frequência \_ Sys100NS**
-   **\_Objeto Frequency**

Em cada caso, as propriedades devem ser preenchidas pelo provedor ou a classe não pode ser exibida no monitor do sistema. Essas propriedades são usadas para computar fórmulas de tipo de contador por consumidores de dados de desempenho.

A sintaxe a seguir é simplificada do código MOF e mostra todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

A classe **Win32 \_ PerfRawData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PerfRawData** tem essas propriedades.

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

Frequência em tiques por segundo da propriedade **de \_ PerfTime de frequência** . Um valor pode ser obtido chamando a função do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

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

Carimbo de data/hora do contador de alto desempenho. Um valor pode ser obtido chamando a função do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

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

A classe **Win32 \_ PerfRawData** é derivada do [**\_ desempenho do Win32**](win32-perf.md), que é derivado de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

Todas as classes derivadas do [**Win32 \_ perf**](win32-perf.md) são projetadas para serem usadas com um objeto de [*atualização*](../wmisdk/gloss-r.md) . Para obter mais informações sobre como criar e usar um objeto atualizador na linguagem de programação C++, consulte [acessando dados de desempenho em C++](../wmisdk/accessing-performance-data-in-c--.md). Para obter mais informações sobre como criar e usar um objeto de atualização em uma linguagem de programação de script, consulte [atualizando dados do WMI em scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).

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

 

 
