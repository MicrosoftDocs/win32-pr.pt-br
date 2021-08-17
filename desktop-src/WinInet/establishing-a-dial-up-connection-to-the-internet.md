---
title: Estabelecer uma conexão discar com a Internet
description: As funções a seguir são usadas para lidar com conexões de modem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ac81096d657453d1ebaa0182f39d31af0fe96c01e73122a2de6e0ba9a765e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955586"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Estabelecer uma conexão discar com a Internet

As funções a seguir são usadas para lidar com conexões de modem.

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialAutup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> As funções discadas do WinINet não são suportadas por conexões discadas duplas, autenticação de Cartão Inteligente ou conexões que exigem certificação baseada no Registro.

 

> [!Note]  
> A partir do Windows Vista e Windows Server 2008, as funções de discagem WinINet usam as funções [RAS](/windows/desktop/RRAS/remote-access-service-functions) para estabelecer uma conexão discável. O WinINet dá suporte à funcionalidade documentada na [**função RasDialDlg.**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga)

 

> [!Note]  
> O WinINet não dá suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o WinHTTP (Microsoft Windows HTTP Services).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 