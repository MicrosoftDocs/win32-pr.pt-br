---
description: O provedor de contador de desempenho é um provedor de alto desempenho que fornece dados brutos do contador de desempenho para as classes do contador de desempenho WMI derivadas do Win32 \_ PerfRawData. O \_ \_ nome da instância win32provider é &\# 0034; OS nt5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Provedor de Contadores de Desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011709"
---
# <a name="performance-counter-provider"></a>Provedor de Contadores de Desempenho

\[O provedor do contador de desempenho não está mais disponível para uso. Em vez disso, use o provedor [WMIPerfInst](wmiperfinst-provider.md) .\]

O provedor de contador de desempenho é um provedor de alto desempenho que fornece dados brutos do contador de desempenho para as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). O nome da instância [**\_ \_ Win32Provider**](--win32provider.md) é "os nt5 \_ GenericPerfProvider \_ v1".

As [**classes \_ PerfRawData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) estão localizadas no namespace "raiz \\ CIMv2" do WMI. Cada classe de desempenho WMI corresponde a um objeto de desempenho em uma biblioteca de desempenho. As propriedades dessas classes representam os contadores para o objeto. O nome da classe WMI para um objeto de contador bruto é do formato ** \_ Win32 \_ \_ PerfRawData* Service \_ name *\_* Object \_ Name * * *. Por exemplo, o nome da classe WMI que contém os contadores de disco lógico é o [**\_ PerfRawData de \_ perfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md).

Você pode usar a classe [**\_ PerfFormattedData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondente para obter os dados de desempenho previamente calculados mostrados no [*Monitor do sistema*](gloss-s.md). Por exemplo, use a [**classe \_ PerfFormattedData \_ \_ de perfdisk do Win32**](./retrieving-raw-and-formatted-performance-data.md) para obter dados de disco previamente calculados.

Para obter mais informações sobre como escrever um cliente que pode acessar dados de desempenho brutos, consulte [acessando dados de desempenho em C++](accessing-performance-data-in-c--.md).

Como um provedor de alto desempenho, o provedor de contador de desempenho implementa a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como o método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e os seguintes métodos de [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :

-   [**CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**Createrefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> </dl>

 

 
