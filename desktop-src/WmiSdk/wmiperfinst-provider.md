---
description: A partir do Windows Vista, o provedor WmiPerfInst fornece dados brutos e formatados do contador de desempenho dinamicamente para classes de contador de desempenho WMI derivadas de Win32 \_ Perf.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Provedor WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a781fc1dc48f0e16d1c25e03eff1b2ab3c80fcd7058d1b49f95912b392d241
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049744"
---
# <a name="wmiperfinst-provider"></a>Provedor WmiPerfInst

A partir do Windows Vista, o provedor WmiPerfInst fornece dados brutos e formatados do contador de desempenho dinamicamente para classes de contador de desempenho [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes) derivadas de [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf). Esse provedor substitui o provedor de desempenho [formatado Provedor de Dados](formatted-performance-data-provider.md), também conhecido como "Provedor de Contadores Preparados" e o Provedor [do Contador de Desempenho](performance-counter-provider.md).

O provedor WmiPerfInst fornece dados para as classes WMI fornecidas pelo provedor [WMIPerfClass.](wmiperfclass-provider.md) Esse provedor é uma ponte entre as instâncias do PDH (Performance Data Helper) e as classes de desempenho WMI fornecidas pelo Provedor WmiPerfClass. Quando WmiPerfInst recebe uma consulta para dados, ele carrega a [](qualifiers-specific-to-wmi-performance-classes.md) classe e usa os qualificadores de classe e propriedade para localizar as instâncias pdh. Para obter mais informações, [consulte Usando as funções PDH para consumir dados do contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

Não é recomendável que você desenvolva novos objetos de desempenho criando um provedor de alto desempenho WMI e dependa do processo de adaptador reverso do [*ADAP*](gloss-r.md) para transferir os dados para as bibliotecas de desempenho. A exceção é quando você está desenvolvendo um driver Windows Driver Model e deseja fornecer dados de desempenho. Embora o processo de adaptador reverso continue a funcionar para compatibilidade com versões regressivas, o método recomendado é usar contadores de [desempenho versão 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).

O [**\_ \_ nome da instância win32Provider**](--win32provider.md) desse provedor é "WmiPerfInst".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> <dt>

[Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
