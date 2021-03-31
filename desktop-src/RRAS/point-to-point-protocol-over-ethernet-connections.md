---
title: protocolo PPP em conexões Ethernet
description: Os sistemas operacionais Windows Server 2003, Windows XP e posterior fornecem suporte para protocolo PPP over Ethernet (PPPoE). Para uma conexão PPPoE, defina os valores a seguir na estrutura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917604"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>protocolo PPP em conexões Ethernet

Os sistemas operacionais Windows Server 2003, Windows XP e posterior fornecem suporte para protocolo PPP over Ethernet (PPPoE). Para uma conexão PPPoE, defina os valores a seguir na estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .



| Membro                      | Valor             |
|-----------------------------|-------------------|
| RASENTRY.dwType             | \_Banda larga RASET  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | O nome do serviço. |



 

Use a função [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir esses valores.

Você também pode usar [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) e o \_ sinalizador RASEDFLAG NewBroadbandEntry para [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para exibir um assistente para a criação de uma entrada de lista telefônica PPPoE.

 

 