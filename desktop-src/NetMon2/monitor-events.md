---
description: Os monitores são projetados para usar Instrumentação de Gerenciamento do Windows (WMI) para acionar eventos em computadores locais ou remotos.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Monitorar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461166"
---
# <a name="monitor-events"></a>Monitorar eventos

Os monitores são projetados para usar [Instrumentação de gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para acionar eventos em computadores locais ou remotos.

> [!Note]  
> Como os monitores usam uma captura em tempo real, eles só podem capturar dados no computador local. Essa é uma limitação da interface **IRTC** do provedor de pacotes de rede. No entanto, usando eventos WMI, os dados capturados podem ser examinados localmente enquanto os eventos podem ser enviados a computadores locais ou remotos.

 

Os monitores não se comunicam diretamente com o WMI. O [*serviço de controle de monitor*](m.md) (MCSVC) fornece uma interface (chamada de [IMonitorEventer](imonitoreventer.md)), que o monitor pode usar para obter uma estrutura de dados de evento e preenchê-la com as informações relevantes. O MCSVC pode então enviar a estrutura de dados de evento para o WMI que, por sua vez, dispara o evento.

 

 
