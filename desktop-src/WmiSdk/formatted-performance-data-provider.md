---
description: Suprimentos calculados (&\# 0034; cooked&\# 0034;) dados do contador de desempenho. Fornece dados dinâmicos para as classes WMI derivadas do Win32 \_ PerfFormattedData. Também conhecido como o provedor de contador de cooked.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Provedor de Dados de desempenho formatado
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab8e931c3d03c619af5b1e37cadd8dacdccd21534513ed3a1aa1d7b9076acfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556609"
---
# <a name="formatted-performance-data-provider"></a>Provedor de Dados de desempenho formatado

\[o Provedor de Dados de desempenho formatado, também conhecido como "provedor de contador de Cooked", não está mais disponível para uso. Em vez disso, use o provedor [WMIPerfInst](wmiperfinst-provider.md) .\]

O provedor de dados de desempenho formatado de alto desempenho fornece dados de contador de desempenho calculados ("cooked"), como a porcentagem de tempo que um disco gasta gravando dados. Esse provedor fornece dados dinâmicos para as classes WMI derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). A diferença entre esse provedor e o [provedor](performance-counter-provider.md) de contador de desempenho é que o provedor de contador de desempenho fornece dados brutos e o provedor de contador de cooked fornece dados de desempenho que aparecem exatamente como no [*Monitor do sistema*](gloss-s.md). O nome da instância [**\_ \_ Win32Provider**](--win32provider.md) é "HiPerfCooker \_ v1".

O nome da classe formatada pelo WMI para um objeto de contador é do formato " \_ nome do objeto do nome do serviço Win32 PerfFormattedData \_ *\_* \_ ".*\_* Por exemplo, o nome da classe WMI que contém os contadores de disco lógico é o **\_ PerfFormattedData de \_ perfdisk \_ do Win32**. Essas classes estão localizadas no namespace "raiz \\ CIMv2".

Como as classes de dados de desempenho são adicionadas e modificadas dinamicamente em um determinado sistema, não é possível documentar formalmente as propriedades de todos os objetos de desempenho conhecidos. Para determinar quais classes estão disponíveis para você e identificar quais membros essas classes têm, consulte [recuperando a documentação para objetos de dados de desempenho brutos e formatados](retrieving-raw-and-formatted-performance-data.md).

As classes [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) usam o qualificador de **culináriatype** nos [tipos de contador de desempenho WMI](wmi-performance-counter-types.md) para especificar a fórmula para calcular dados de desempenho. Esse qualificador é o mesmo que o qualificador de **tipo** em classes [**\_ PerfRawData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .

Como um provedor de alto desempenho, o provedor de contador cooked implementa a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como o método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e os seguintes métodos [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :

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

 

 
