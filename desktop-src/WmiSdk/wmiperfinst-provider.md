---
description: A partir do Windows Vista, o provedor WmiPerfInst fornece dados de contador de desempenho brutos e formatados dinamicamente para classes de contador de desempenho WMI derivadas do desempenho do Win32 \_ .
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Provedor de WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770632"
---
# <a name="wmiperfinst-provider"></a>Provedor de WmiPerfInst

A partir do Windows Vista, o provedor WmiPerfInst fornece dados de contador de desempenho brutos e formatados dinamicamente para [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI derivadas do [**\_ desempenho do Win32**](/windows/desktop/CIMWin32Prov/win32-perf). Esse provedor substitui o [provedor de dados de desempenho formatado](formatted-performance-data-provider.md), também conhecido como "provedor de contador de cooked", e o [provedor de contador de desempenho](performance-counter-provider.md).

O provedor WmiPerfInst fornece dados para as classes WMI que são fornecidas pelo provedor [WMIPerfClass](wmiperfclass-provider.md) . Esse provedor é uma ponte entre instâncias de PDH (auxiliar de dados de desempenho) e as classes de desempenho do WMI fornecidas pelo provedor WmiPerfClass. Quando o WmiPerfInst recebe uma consulta de dados, ele carrega a classe e usa os [qualificadores](qualifiers-specific-to-wmi-performance-classes.md) de classe e propriedade para localizar as instâncias de PDH. Para obter mais informações, consulte [usando as funções de PDH para consumir dados de contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

Não é recomendável que você desenvolva novos objetos de desempenho criando um provedor de alto desempenho WMI e dependa do processo do [*adaptador inverso do adap*](gloss-r.md) para transferir os dados para as bibliotecas de desempenho. A exceção é quando você está desenvolvendo um driver de Windows Driver Model e deseja fornecer dados de desempenho. Embora o processo do adaptador reverso continue a funcionar para compatibilidade com versões anteriores, o método recomendado é usar os [contadores de desempenho versão 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

O nome da instância [**\_ \_ Win32Provider**](--win32provider.md) desse provedor é "WmiPerfInst".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> <dt>

[Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
