---
title: Estabelecendo uma conexão dial-up com a Internet
description: As funções a seguir são usadas para lidar com conexões de modem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008030"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Estabelecendo uma conexão dial-up com a Internet

As funções a seguir são usadas para lidar com conexões de modem.

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialHangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> As funções de discagem do WinINet não dão suporte a conexões de discagem dupla, autenticação de cartão inteligente ou conexões que exigem certificação baseada no registro.

 

> [!Note]  
> A partir do Windows Vista e do Windows Server 2008, as funções de dial-up do WinINet usam as [funções de Ras](/windows/desktop/RRAS/remote-access-service-functions) para estabelecer uma conexão discada. O WinINet oferece suporte à funcionalidade documentada na função [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .

 

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 