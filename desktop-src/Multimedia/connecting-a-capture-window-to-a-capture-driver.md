---
title: Conectando uma janela de captura a um driver de captura
description: Conectando uma janela de captura a um driver de captura
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT mensagem
- macro capDriverConnect
- Função capGetDriverDescription
- WM_CAP_DRIVER_GET_NAME mensagem
- Macro capDriverGetName
- WM_CAP_DRIVER_GET_VERSION mensagem
- Macro capDriverGetVersion
- WM_CAP_DRIVER_DISCONNECT mensagem
- macro capDriverDisconnect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf74b5dc7cda0fdb73c8f9bd73f61de5ecefc157c20816c110d71e04bba6c196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144899"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Conectando uma janela de captura a um driver de captura

Você pode se conectar dinamicamente ou desconectar uma janela de captura a um driver de captura. Você pode se conectar ou associar uma janela de captura a um driver de captura usando a mensagem [**WM \_ CAP DRIVER \_ \_ CONNECT**](wm-cap-driver-connect.md) (ou a [**macro capDriverConnect).**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) Depois que uma janela de captura e o driver de captura são conectados, você pode enviar mensagens específicas do dispositivo para o driver de captura associado a uma janela de captura.

Se você tiver mais de um dispositivo de captura instalado em um sistema, poderá conectar uma janela de captura a um driver de dispositivo de captura de vídeo específico especificando um inteiro para o *parâmetro wParam* da mensagem WM \_ CAP DRIVER \_ \_ CONNECT. O inteiro é um índice que identifica um driver de captura de vídeo listado no Registro ou na seção drivers do \[ \] arquivo SYSTEM.INI dados. Use zero para a primeira entrada de índice.

Você pode recuperar o nome e a versão de um driver de captura instalado usando a [**função capGetDriverDescription.**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) Seu aplicativo pode usar essa função para enumerar os drivers e dispositivos de captura instalados, para que o usuário possa selecionar um dispositivo de captura para se conectar a uma janela de captura.

Você pode recuperar o nome do driver de dispositivo de captura conectado a uma janela de captura usando a mensagem [**WM CAP DRIVER GET \_ \_ \_ \_ NAME**](wm-cap-driver-get-name.md) (ou a [**macro capDriverGetName).**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) Para recuperar a versão de um driver de captura instalado, use a mensagem [**WM CAP DRIVER GET \_ \_ \_ \_ VERSION**](wm-cap-driver-get-version.md) (ou a [**macro capDriverGetVersion).**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion)

Você pode desconectar uma janela de captura de um driver de captura usando a mensagem [**WM \_ CAP DRIVER \_ \_ DISCONNECT**](wm-cap-driver-disconnect.md) (ou a [**macro capDriverDisconnect).**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect)

Quando uma janela de captura é destruída, todos os drivers de dispositivo de captura de vídeo conectados são desconectados automaticamente.

 

 




