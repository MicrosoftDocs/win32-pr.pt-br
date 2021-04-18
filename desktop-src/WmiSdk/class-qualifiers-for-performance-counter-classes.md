---
description: Especifique as informações sobre o objeto de desempenho para o qual a classe do contador de desempenho WMI está mapeada.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Qualificadores de classe para classes de contador de desempenho
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788728"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a>Qualificadores de classe para classes de contador de desempenho

Os qualificadores de classe especificam informações sobre o objeto de desempenho para o qual a [classe do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI é mapeada. Para obter mais informações, consulte [monitorando dados de desempenho](monitoring-performance-data.md).

-   [Qualificadores para PerformanceClasses brutos e formatados](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Qualificadores para classes de desempenho brutos](#)
-   [Qualificadores para classes de desempenho formatadas](#)
-   [Tópicos relacionados](#related-topics)


O contador de desempenho – qualificadores específicos são automaticamente anexados pelo provedor "WbemPerfClass" às classes e propriedades do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) na raiz \\ CIMv2.

Essas informações se aplicam a todas as instâncias da classe. Alguns qualificadores com valores **boolianos** que são sempre **falsos** podem não estar presentes em classes específicas.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Qualificadores para PerformanceClasses brutos e formatados

Os qualificadores a seguir se aplicam a todas as classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**
</dt> <dd>

**booleano**

Indica se a classe contém dados cooked.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**
</dt> <dd>

**cadeia de caracteres**

Nome do objeto de desempenho. Para obter mais informações, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**sint32**

Não fornece dados detalhados. Sempre contém o valor de 100.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dinâmico**
</dt> <dd>

**booleano**

Sempre definido como **true** porque as instâncias são sempre dinâmicas.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**
</dt> <dd>

**booleano**

Indica se a classe é proveniente de uma biblioteca de desempenho herdada. Sempre definido como **true**.

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Os índices não são mais válidos. Esse qualificador é sempre zero.

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**booleano**

Indica que a classe é uma classe de alto desempenho. Sempre definido como **true**.

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Localidade**
</dt> <dd>

**sint32**

Identificador de localidade. O valor é sempre 1033 (inglês americano).

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**int32**

Os índices não são mais válidos. Esse qualificador é sempre zero.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Operador**
</dt> <dd>

**cadeia de caracteres**

Nome do provedor de instância. O valor é "WbemPerfV2".

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**
</dt> <dd>

**cadeia de caracteres**

Nome do driver na chave **HKEY \_ local de \_ \\ \\ Serviços CurrentControlSet** , sob a qual a chave de desempenho pode ser localizada. Esse nome também é o nome do serviço que fornece o contador de desempenho.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Único**
</dt> <dd>

**booleano**

Se **for true**, indicará que existe apenas uma única instância da classe.

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Qualificadores para classes de desempenho brutos

Os qualificadores a seguir se aplicam a todas as classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Dispendiosa**
</dt> <dd>

**booleano**

Indica se a obtenção de instâncias dessa classe é uma operação dispendiosa. Sempre definido como **true** para classes com " \_ dispendioso" acrescentado ao final do nome da classe.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**uint32**

Não fornece dados detalhados. Sempre contém o valor de 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**booleano**

O valor é sempre **false**.

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Qualificadores para classes de desempenho formatadas

Os qualificadores a seguir se aplicam a todas as classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Autocookie**
</dt> <dd>

**int32**

Indica que os valores nas instâncias de classe são calculados automaticamente a partir da classe de dados brutos correspondente. O valor é sempre 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**RawClass de autocookie \_**
</dt> <dd>

**cadeia de caracteres**

Nome da classe bruta a ser usada para cálculo para a classe formatada. Esse qualificador é necessário.

</dd> </dl>

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

 

 
