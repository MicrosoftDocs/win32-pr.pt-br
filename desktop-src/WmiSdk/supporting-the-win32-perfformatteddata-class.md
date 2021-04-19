---
description: Ao escrever um provedor de alto desempenho que deriva classes do Win32 \_ PerfFormattedData, você deve seguir convenções específicas para que o WMI possa calcular os valores de propriedade.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Dando suporte à classe Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782508"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>Dando suporte à \_ classe Win32 PerfFormattedData

Ao escrever um provedor de alto desempenho que deriva classes do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), você deve seguir convenções específicas para que o WMI possa calcular os valores de propriedade.

> [!Note]  
> Não é recomendável gravar um provedor WMI de alto desempenho para criar contadores de desempenho em nenhuma versão do sistema operacional Windows. Para obter mais informações, consulte [tornando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)e [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).

 

O procedimento a seguir descreve como dar suporte à \_ classe Win32 PerfFormattedData.

**Para dar suporte à \_ classe Win32 PerfFormattedData**

1.  Crie sua classe no mesmo namespace que a classe RAW correspondente. A classe deve ser derivada do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e ter o qualificador de **Hiperf** definido como **true**. Para obter mais informações sobre como criar sua própria classe para o WMI, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).
2.  Especifique "HiPerfCooker \_ v1" no qualificador do [**provedor**](class-qualifiers-for-performance-counter-classes.md) .
3.  Especifique os seguintes qualificadores de nível de classe, além dos qualificadores usados para as classes brutas:

    -   [**Autocookie**](class-qualifiers-for-performance-counter-classes.md)
    -   [**RawClass de autocookie \_**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Cooked**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dispendiosa**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dinâmico**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Localidade**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Provedor**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Único**](standard-wmi-qualifiers.md)

    > [!Note]  
    > Não defina nenhum valor para **GenericPerfCtr**, **PerfIndex** ou **HelpIndex** porque eles serão definidos pelo processo ADAP. Para obter mais informações, consulte [**qualificadores de classe para classes de contador de desempenho**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Inclua uma propriedade de chave chamada **Name** em sua classe (essa propriedade não é necessária para classes singleton).

    O valor da propriedade **Name** deve ser o mesmo que a classe RAW correspondente. Você não deve usar nenhuma propriedade de chave que não seja **nome** em sua classe.

5.  Crie Propriedades de dados digitadas como **DWORD** (**UInt32**) ou **QWORD** (**UInt64**).

    As propriedades devem corresponder a uma propriedade na classe RAW ou uma propriedade na classe que você está criando.

6.  Especifique os seguintes qualificadores de nível de propriedade para todas as propriedades em sua classe, além dos qualificadores **PerfIndex** e **PerfDetail** usados para as propriedades de classe bruta:

    -   [**Polybase**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Culináriatype**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Contador**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Para obter mais informações, consulte [**qualificadores de propriedade para classes de contador de desempenho**](property-qualifiers-for-performance-counter-classes.md). Além disso, o arquivo de cabeçalho WINPERF. h contém valores que você pode especificar para **PerfDetail** e **MyType**.

7.  Verifique se seu provedor atende aos [requisitos de desempenho](#performance-requirements).

## <a name="performance-requirements"></a>Requisitos de desempenho

Quando você escreve um provedor de alto desempenho, seu desempenho deve atender aos seguintes requisitos:

-   Abrir o arquivo DLL de alto desempenho pode levar até 100 milissegundos. De modo geral, a abertura de cada um dos provedores de alto desempenho e da biblioteca de desempenho não pode exceder 5 segundos.
-   A atualização de dados pode levar até 10 milissegundos por coleta. Em uma operação de atualização e coleta geral, todos os provedores de alto desempenho juntos não podem levar mais de 800 milissegundos.
-   A carga geral de CPU para todos os provedores de alto desempenho não pode exceder 6-7% de sobrecarga de CPU interativamente ou 5% para registro em log.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
