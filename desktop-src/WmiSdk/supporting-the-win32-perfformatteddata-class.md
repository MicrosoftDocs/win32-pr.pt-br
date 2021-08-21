---
description: Ao escrever um provedor de alto desempenho que deriva classes de Win32 PerfFormattedData, você deve seguir convenções específicas para que o WMI possa calcular os valores \_ de propriedade.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Dando suporte à Win32_PerfFormattedData classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bbed50bde7ef16f6362d28151744cf22d66e5d0f56df253ad48ab469b397d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050124"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>Suporte à classe Win32 \_ PerfFormattedData

Ao escrever um provedor de alto desempenho que deriva classes de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), você deve seguir convenções específicas para que o WMI possa calcular os valores de propriedade.

> [!Note]  
> Escrever um provedor de alto desempenho WMI para criar contadores de desempenho não é recomendado em nenhuma versão do Windows operacional. Para obter mais informações, consulte [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and Performance [Libraries and WMI](performance-libraries-and-wmi.md).

 

O procedimento a seguir descreve como dar suporte à classe Win32 \_ PerfFormattedData.

**Para dar suporte à classe Win32 \_ PerfFormattedData**

1.  Crie sua classe no mesmo namespace que a classe bruta correspondente. A classe deve ser derivada de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e ter o qualificador **HiPerf** definido como **TRUE.** Para obter mais informações sobre como criar sua própria classe para WMI, consulte [Criando classes Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)
2.  Especifique "HiPerfCooker \_ v1" no [**qualificador**](class-qualifiers-for-performance-counter-classes.md) do provedor.
3.  Especifique os qualificadores de nível de classe a seguir, além dos qualificadores usados para as classes brutas:

    -   [**AutoCook**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Autocook \_ RawClass**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Cozido**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Caro**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dinâmico**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Local**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Provedor**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Singleton**](standard-wmi-qualifiers.md)

    > [!Note]  
    > Não de definido nenhum valor **para GenericPerfCtr,** **PerfIndex ou** **HelpIndex** porque eles serão definidos pelo processo do ADAP. Para obter mais informações, consulte [**Qualificadores de classe para classes de contador de desempenho**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Inclua uma propriedade de chave **chamada Name** em sua classe (essa propriedade não é necessária para classes singleton).

    O valor da **propriedade Name** deve ser o mesmo que a classe bruta correspondente. Você não deve usar nenhuma propriedade de chave diferente **de Nome** em sua classe.

5.  Criar dados de propriedades digitados como **DWORD** (**uint32**) ou **QWORD** (**uint64**).

    As propriedades devem corresponder a uma propriedade na classe bruta ou a uma propriedade na classe que você está criando.

6.  Especifique os qualificadores de nível de propriedade a seguir para todas as propriedades em sua classe, além dos qualificadores **PerfIndex** e **PerfDetail** usados para as propriedades de classe bruta:

    -   [**Base**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Tipo de Cozimento**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Contador**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Para obter mais informações, consulte [**Qualificadores de propriedade para classes de contador de desempenho**](property-qualifiers-for-performance-counter-classes.md). Além disso, o arquivo de título Winperf.h contém valores que você pode especificar para **PerfDetail** e **CounterType**.

7.  Certifique-se de que seu provedor atenda aos [requisitos de desempenho](#performance-requirements).

## <a name="performance-requirements"></a>Requisitos de desempenho

Quando você escreve um provedor de alto desempenho, seu desempenho deve atender aos seguintes requisitos:

-   Abrir o arquivo DLL de alto desempenho não pode levar mais de 100 milissegundos. Em geral, abrir cada provedor de alto desempenho e a biblioteca de desempenho não pode exceder 5 segundos.
-   A atualização de dados não pode levar mais de 10 milissegundos por coleta. Em uma operação geral de atualização e coleta, todos os provedores de alto desempenho juntos não podem levar mais de 800 milissegundos.
-   A carga geral da CPU para todos os provedores de alto desempenho não pode exceder a sobrecarga de CPU de 6 a 7% interativamente ou 5% para registro em log.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformando um provedor de instância em um provedor High-Performance dados](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
