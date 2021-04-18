---
description: Ao escrever um provedor de alto desempenho que deriva classes do Win32 \_ PerfRawData, você deve seguir convenções específicas para que o WMI possa fornecer dados aos valores de propriedade.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Dando suporte à classe Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752002"
---
# <a name="supporting-the-win32_perfrawdata-class"></a>Dando suporte à \_ classe Win32 PerfRawData

Ao escrever um provedor de alto desempenho que deriva classes do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), você deve seguir convenções específicas para que o WMI possa fornecer dados aos valores de propriedade.

> [!Note]  
> Não é recomendável gravar um provedor WMI de alto desempenho para criar contadores de desempenho em nenhuma versão do sistema operacional Windows. Para obter mais informações, consulte [tornando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)e [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).

 

O procedimento a seguir descreve como dar suporte à classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) com seu provedor de alto desempenho.

**Para dar suporte à \_ classe Win32 PerfRawData**

1.  Crie sua classe no namespace raiz \\ CIMv2.

    A classe deve ser derivada do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e ter o qualificador de **Hiperf** definido como **true**. Você também pode adicionar classes de dados de desempenho WDM (driver) ao \\ namespace WMI raiz. Para obter mais informações sobre como criar sua própria classe para o WMI, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).

2.  Especifique o provedor como "os nt5 \_ GenericPerfProvider \_ v1" no qualificador do **provedor** .
3.  Especifique os seguintes qualificadores de nível de classe:

    -   **HiPerf**
    -   **Localidade**
    -   **PerfDetail**
    -   **Provedor**

    Para obter mais informações, consulte [**qualificadores de classe para classes de contador de desempenho**](class-qualifiers-for-performance-counter-classes.md). Não defina o qualificador **GenericPerfCtr** porque ele está reservado para o processo ADAP que transfere dados da biblioteca de desempenho para classes WMI.

4.  Preencha as propriedades apropriadas de carimbo de data/hora e frequência usadas para computar fórmulas de tipo de contador.

    Essas propriedades são herdadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e, se você estiver escrevendo um provedor de alto desempenho, deverá preenchê-las para a classe a ser exibida no monitor do sistema.

5.  Inclua uma propriedade de chave chamada **Name** em sua classe (essa propriedade não é necessária para classes singleton).

    Você não deve usar nenhuma propriedade de chave que não seja **nome** em sua classe.

6.  Crie Propriedades dados-tipados como **DWORD** (**UInt32**) ou **QWORD** (**UInt64**). Essas propriedades se tornam contadores de desempenho quando transferidas para as bibliotecas de desempenho.
7.  Especifique os seguintes qualificadores de nível de propriedade para todas as propriedades em sua classe:

    -   **DisplayName**
    -   **CounterType**
    -   **DefaultScale**
    -   **Descrição**
    -   **PerfDefault**
    -   **PerfDetail**

    Para obter mais informações, consulte [**qualificadores de propriedade para classes de contador de desempenho**](property-qualifiers-for-performance-counter-classes.md). Além disso, o arquivo de cabeçalho WINPERF. h contém valores que você pode especificar para **PerfDetail** e **MyType**.

    O WMI usa os qualificadores **DisplayName**, **locale** e **Description** para localização. Você deve adicionar qualificadores corrigidos ao \_ namespace MS 409 (inglês) para que o monitor do sistema possa exibir corretamente os dados da classe. Isso significa que você altera a definição de propriedade adicionando um qualificador de **Descrição** com texto explicativo e preenchendo o valor **DisplayName** . Você também deve adicionar qualificadores corrigidos a qualquer outro namespace de localidade ao qual sua classe dá suporte. Se um usuário solicitar dados de uma localidade para a qual você não fornece qualificadores corrigidos, o WMI usa as definições especificadas no namespace do MS \_ 409.

8.  Crie uma propriedade base para qualquer propriedade que tenha um tipo de contador esperando um valor base.

    Essa propriedade segue imediatamente a propriedade e é nomeada * PropertyName ***\_ base**. Por exemplo, a propriedade média **AvgDiskBytesPerRead** na classe [**do \_ PerfRawData de \_ Perfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md) de AvgDiskBytesPerRead de entrada requer uma propriedade de base denominada base de **\_ dados** para o número de amostras, a contagem de um e- Para determinar se o tipo de contador que você deseja usar requer uma propriedade base, localize o tipo de contador por nome ou valor decimal nos [tipos de contador de desempenho WMI](wmi-performance-counter-types.md).

9.  Verifique se seu provedor atende aos [requisitos de desempenho](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
