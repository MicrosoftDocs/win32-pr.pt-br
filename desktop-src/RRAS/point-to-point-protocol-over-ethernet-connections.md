---
title: protocolo PPP em conexões Ethernet
description: Windows o servidor 2003, Windows XP e sistemas operacionais posteriores oferecem suporte para protocolo PPP via Ethernet (PPPoE). Para uma conexão PPPoE, defina os valores a seguir na estrutura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92703bac13d129ed29cee1c22328825de67325239c1906c1728b96d53398647b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789806"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>protocolo PPP em conexões Ethernet

Windows o servidor 2003, Windows XP e sistemas operacionais posteriores oferecem suporte para protocolo PPP via Ethernet (PPPoE). Para uma conexão PPPoE, defina os valores a seguir na estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .



| Membro                      | Valor             |
|-----------------------------|-------------------|
| RASENTRY.dwType             | \_Banda larga RASET  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | O nome do serviço. |



 

Use a função [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir esses valores.

Você também pode usar [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) e o \_ sinalizador RASEDFLAG NewBroadbandEntry para [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para exibir um assistente para a criação de uma entrada de lista telefônica PPPoE.

 

 