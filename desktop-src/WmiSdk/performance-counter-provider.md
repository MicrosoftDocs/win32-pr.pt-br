---
description: O provedor contador de desempenho é um provedor de alto desempenho que fornece dados brutos do contador de desempenho para as Classes do Contador de Desempenho WMI derivadas de Win32 \_ PerfRawData. O \_ \_ nome da instância win32Provider é &\# 0034; NT5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Provedor de Contadores de Desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c846d66cd183e866623004cacfbcb630ac68480fab8dd58eca2b5a4dc6d2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050524"
---
# <a name="performance-counter-provider"></a>Provedor de Contadores de Desempenho

\[O Provedor do Contador de Desempenho não está mais disponível para uso. Em vez disso, use [o provedor WMIPerfInst.](wmiperfinst-provider.md)\]

O provedor do Contador de Desempenho é um provedor de alto desempenho que fornece dados brutos do contador de desempenho para as Classes do Contador de Desempenho [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes) derivadas de [**Win32 \_ PerfRawData.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) O [**\_ \_ nome da instância win32Provider**](--win32provider.md) é "NT5 \_ GenericPerfProvider \_ V1".

As [**classes Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) estão localizadas no \\ namespace "CIMv2 raiz" do WMI. Cada classe de desempenho WMI corresponde a um objeto de desempenho em uma biblioteca de desempenho. As propriedades dessas classes representam os contadores do objeto . O nome da classe WMI para um objeto de contador bruto é do formato * Nome do objeto do nome do serviço *Win32 \_ \_ \_ PerfRawData***.* \_ *\_* \_ Por exemplo, o nome da classe WMI que contém os contadores de disco lógico é [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).

Você pode usar a classe [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondente para obter os dados de desempenho pré-calculados mostrados no [*Monitor do Sistema.*](gloss-s.md) Por exemplo, use a [**classe \_ \_ \_ LogicalDisk PerfDisk Do Win32 PerfFormattedData para**](./retrieving-raw-and-formatted-performance-data.md) obter dados de disco pré-calculados.

Para obter mais informações sobre como escrever um cliente que pode acessar dados brutos de desempenho, consulte Acessando dados [de desempenho no C++.](accessing-performance-data-in-c--.md)

Como um provedor de alto desempenho, o provedor do Contador de Desempenho implementa a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como o método [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e os seguintes métodos [**IWbemHiPerfProvider:**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)

-   [**CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**Getobjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> </dl>

 

 
