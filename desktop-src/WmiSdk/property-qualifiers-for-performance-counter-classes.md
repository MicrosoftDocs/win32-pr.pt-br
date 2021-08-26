---
description: Os qualificadores de propriedade especificam informações sobre o contador de desempenho para o qual a propriedade é mapeada.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Qualificadores de propriedade para classes de contador de desempenho
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 105bd010704364dc3865b2e704b3daeaafdb29a772d4f3b3fe036b88da2d43cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996176"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a>Qualificadores de propriedade para classes de contador de desempenho

Os qualificadores de propriedade especificam informações sobre o contador de desempenho para o qual a propriedade é mapeada.

-   [Qualificadores de propriedade para classes de desempenho RAW e formatadas](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Qualificadores de propriedade para classes de desempenho brutos](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Qualificadores de propriedade para classes de desempenho formatadas](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Como interpretar qualificadores de propriedade](#how-to-interpret-property-qualifiers)
-   [Tópicos relacionados](#related-topics)

O contador de desempenho faz parte de um objeto de desempenho representado por um contador de desempenho de [classe de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI – qualificadores específicos são automaticamente anexados pelo provedor WbemPerfClass às classes e propriedades do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) na raiz \\ CIMv2.

Essas informações se aplicam a todas as instâncias da classe de desempenho. Alguns qualificadores com valores **boolianos** que são sempre falsos podem não estar presentes em classes específicas.

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a>Qualificadores de propriedade para classes de desempenho RAW e formatadas

A lista a seguir lista os qualificadores que se aplicam a propriedades em classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) ou [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)
</dt> <dd>

**sint32**

Valor inteiro na enumeração de tipo de contador, conforme definido em WINPERF. h ou Perflib. h. O qualificador de [**tipo**](countertype-qualifier.md)de referenda indica a fórmula ou o algoritmo usado para calcular o valor mostrado no monitor do sistema para o contador que a propriedade representa.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**
</dt> <dd>

**cadeia de caracteres**

O nome do contador de desempenho, conforme especificado pelo PDH (auxiliar de dados de desempenho).

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Não usado. Sempre contém 0.

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**sint32**

Não usado. Sempre contém 0.

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a>Qualificadores de propriedade para classes de desempenho brutos

A lista a seguir lista os qualificadores que se aplicam a todas as propriedades de classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**booleano**

Indica se essa propriedade é o contador padrão a ser usado em caixas de listagem. Esse qualificador assume como padrão o **falso** para os contadores de desempenho versão 6,0 porque eles não fornecem dados para ele. Para obter mais informações, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**
</dt> <dd>

**sint32**

A potência de 10 a ser usada para exibição do contador. Para zero, o máximo estimado é 10 ^ 0 ou 1.

</dd> <dt>

<span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)
</dt> <dd>

**sint32**

Nível de conhecimento do público. Não usado. O valor é sempre 100.

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a>Qualificadores de propriedade para classes de desempenho formatadas

A lista a seguir lista os qualificadores que se aplicam a todas as propriedades de classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**Culináriatype**
</dt> <dd>

**cadeia de caracteres**

Tipo de fórmula usado para produzir o resultado. Cada tipo de contador usa os outros qualificadores de propriedade para calcular o resultado mostrado como o valor da propriedade atual. Os qualificadores **Counter**, **PerfTimeStamp** e **PerfTimeFreq** são mapeados para propriedades em uma classe RAW que fornece os dados.

Para obter mais informações, consulte [qualificador de tipo](countertype-qualifier.md).

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Neutraliza**
</dt> <dd>

**cadeia de caracteres**

Nome de uma propriedade necessária na classe bruta correspondente a ser usada como o valor do contador na fórmula de culinária. O valor deve ser o nome da propriedade da propriedade da fonte de dados na classe bruta correspondente.

</dd> <dt>

<span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**
</dt> <dd>

**cadeia de caracteres**

Nome de uma propriedade em uma classe bruta a ser usada como uma frequência na fórmula de culinária. O valor padrão apropriado no nível de classe será usado se esse qualificador não estiver presente para a propriedade. A frequência representa as tiques por segundo do carimbo de data/hora.

</dd> <dt>

<span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**
</dt> <dd>

**cadeia de caracteres**

Nome de uma propriedade em uma classe bruta a ser usada como um carimbo de data/hora na fórmula de culinária. O valor padrão apropriado no nível de classe será usado se esse qualificador não estiver presente para a propriedade. Um carimbo de data/hora gerado automaticamente pode introduzir um erro em um cálculo porque o carimbo de data/hora é uma aproximação e não conta a sobrecarga incorrida pelo marshaling e pela coleta de dados real.

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a>Como interpretar qualificadores de propriedade

as propriedades nas [**classes \_ PerfFormattedData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contêm os dados calculados fornecidos pelo [Provedor de Dados de desempenho formatado](formatted-performance-data-provider.md). O valor da propriedade é o resultado calculado final. Os qualificadores fornecem uma receita.

O **contador** e os qualificadores de **base** apontam para as fontes de dados e o **culináriatype** especifica a fórmula usada para produzir o resultado. O carimbo de data e hora e a frequência de exemplo também vêm da classe bruta correspondente e são nomeados em **PerfTimeStamp** e **PerfTimeFreq**.

Por exemplo, uma das classes formatadas fornecida pelo WMI, [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contém uma propriedade chamada **AvgDiskBytesPerRead**. O nome da propriedade na classe formatada deve ser igual à propriedade na classe RAW. A propriedade **AvgDiskBytesPerRead** tem os qualificadores a seguir.

A lista a seguir lista os qualificadores de propriedade disponíveis para propriedades de todas as classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).



| Qualificador         | Valor                     |
|-------------------|---------------------------|
| **Culináriatype**   | \_massa média de desempenho \_       |
| **Contador**       | AvgDiskBytesPerRead       |
| **PerfTimeStamp** | Carimbo de data/hora \_ PerfTime       |
| **PerfTimeFreq**  | Frequência \_ PerfTime       |
| **PerfIndex**     | 408                       |
| **HelpIndex**     | 409                       |
| **Base**          | \_Base AvgDiskBytesPerRead |



 

A propriedade **AvgDiskBytesPerRead** relata o número médio de bytes transferidos do disco durante operações de leitura. A fórmula para a \_ quantidade média de desempenho \_ é:

(Sample2-Sample1)/(base Sample2-base Sample1)

A operação de leitura é amostrada na frequência especificada por **PerfTimeFreq** com o valor **PerfTimeStamp** indicando o exemplo mais recente. Os dados brutos do contador em bytes são extraídos da propriedade **AvgDiskBytesPerRead** na classe do [**\_ PerfRawData de \_ perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md) do uso do Win32. O número base de dados de operações é obtido da **propriedade \_ base AvgDiskBytesPerRead** na mesma classe.

Para obter mais informações, consulte [obtendo dados de desempenho estatísticos](obtaining-statistical-performance-data.md) e [monitorando dados de desempenho](monitoring-performance-data.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> <dt>

[Qualificadores específicos para classes de desempenho WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Acessando classes de desempenho de WMI pré-instalado](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tarefas do WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
