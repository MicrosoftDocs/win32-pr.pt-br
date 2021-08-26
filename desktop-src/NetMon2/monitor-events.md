---
description: Os monitores são projetados para usar Windows WMI (Instrumentação de Gerenciamento) para disparar eventos em computadores locais ou remotos.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Monitorar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe76ddd8df02694f871899e0b172dda3529fc29c0e16b6b4a65e2ad15bd2ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995476"
---
# <a name="monitor-events"></a>Monitorar eventos

Os monitores são projetados [para usar Windows WMI (Instrumentação](/windows/desktop/WmiSdk/wmi-start-page) de Gerenciamento) para disparar eventos em computadores locais ou remotos.

> [!Note]  
> Como os monitores usam uma captura em tempo real, eles só podem capturar dados no computador local. Essa é uma limitação da interface **IRTC** do provedor de pacotes de rede. No entanto, usando eventos WMI, os dados capturados podem ser examinados localmente, enquanto os eventos podem ser enviados para computadores locais ou remotos.

 

Os monitores não se comunicam diretamente com o WMI. O MCSVC (Monitor [*Control Service)*](m.md) fornece uma interface (chamada [IMonitorEventer),](imonitoreventer.md)que o monitor pode usar para obter uma estrutura de dados de evento e preenchê-la com as informações relevantes. O MCSVC pode enviar a estrutura de dados do evento para o WMI, que, por sua vez, a dispara o evento.

 

 
