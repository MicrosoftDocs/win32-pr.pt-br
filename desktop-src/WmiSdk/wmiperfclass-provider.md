---
description: Começando com Windows Vista, esse provedor cria as Classes de Contador de Desempenho WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Provedor WmiPerfClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7d8fa26597da9bc273055d4fd08b161358e6f57e599552d533a72f2e6ba094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920886"
---
# <a name="wmiperfclass-provider"></a>Provedor WmiPerfClass

Começando com Windows Vista, esse provedor cria as Classes de Contador de Desempenho [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes). Os dados são fornecidos dinamicamente para essas classes de desempenho WMI pelo [provedor WMIPerfInst.](wmiperfinst-provider.md) O processo de Descoberta Automática/ADAP não transfere mais objetos de contador de desempenho para classes de desempenho WMI no repositório WMI. Para obter mais informações, consulte [Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).

Para obter mais informações, consulte [Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).

Embora não seja recomendável que você desenvolva novos objetos de desempenho criando um provedor de alto desempenho WMI e dependa do processo de adaptador reverso do [*ADAP*](gloss-r.md) para transferir os dados para as bibliotecas de desempenho, a exceção é o desenvolvimento de um driver de modelo de driver do Windows que fornece dados de desempenho. Embora o processo de adaptador reverso continue a funcionar para compatibilidade com versões regressivas, o método recomendado é usar contadores de [desempenho versão 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).

O [**\_ \_ nome da instância win32Provider**](--win32provider.md) desse provedor é "WmiPerfClass".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> <dt>

[Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
