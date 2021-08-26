---
description: Para consumir dados do contador, consulte consumindo dados do contador.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Utilizando contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 18bb017a34fb23188c20e81bce28c171c50dcb4d43cd52d458e92be99b7d03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033206"
---
# <a name="using-performance-counters"></a>Utilizando contadores de desempenho

Os **consumidores** do contador de desempenho são componentes de software que coletam e fazem uso de dados do contador de desempenho. Os consumidores de exemplo fornecidos pela Microsoft incluem monitor de desempenho (perfmon.exe), Monitor de Recursos (resmon.exe), Gerenciador de logs (logman.exe) e typeperf.exe. Componentes de software de terceiros também podem coletar dados de desempenho por meio de APIs de coleta de desempenho ou por meio de classes de contador de desempenho WMI.

Os **provedores** de contador de desempenho são componentes de software que publicam dados do contador de desempenho. Os contadores de desempenho podem ser fornecidos por componentes do sistema operacional, drivers de dispositivo e serviços. muitos contadores de desempenho são fornecidos como parte do sistema operacional Windows. Contadores adicionais podem ser fornecidos por componentes de software de terceiros por meio das APIs do provedor de contador de desempenho.

- Use as [Ferramentas do contador de desempenho](performance-counters-tools.md) quando desejar coletar ou exibir os dados do contador de um sistema.
- Use as [APIs de consumidor do contador de desempenho](consuming-counter-data.md) quando desejar escrever um programa que coleta dados do contador do sistema local.
- Use as [classes do contador de desempenho do WMI](/windows/desktop/WmiSdk/monitoring-performance-data) quando desejar coletar dados do contador de um sistema local ou remoto usando o WMI.
- Use as [APIs do provedor de contador de desempenho](providing-counter-data.md) quando desejar publicar dados do contador de desempenho do seu componente de software.

## <a name="see-also"></a>Confira também

[Sobre contadores de desempenho](about-performance-counters.md)

[Referência de contadores de desempenho](performance-counters-reference.md)
