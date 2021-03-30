---
title: Conectando uma janela de captura a um driver de captura
description: Conectando uma janela de captura a um driver de captura
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT mensagem
- macro capDriverConnect
- função capGetDriverDescription
- WM_CAP_DRIVER_GET_NAME mensagem
- macro capDriverGetName
- WM_CAP_DRIVER_GET_VERSION mensagem
- macro capDriverGetVersion
- WM_CAP_DRIVER_DISCONNECT mensagem
- macro capDriverDisconnect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635787"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Conectando uma janela de captura a um driver de captura

Você pode conectar ou desconectar dinamicamente uma janela de captura a um driver de captura. Você pode conectar ou associar uma janela de captura a um driver de captura usando a mensagem de [**conexão do driver do WM \_ \_ \_ Cap**](wm-cap-driver-connect.md) (ou a macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ). Depois que uma janela de captura e o driver de captura estiverem conectados, você poderá enviar mensagens específicas do dispositivo para o driver de captura associado a uma janela de captura.

Se você tiver mais de um dispositivo de captura instalado em um sistema, poderá conectar uma janela de captura a um driver de dispositivo de captura de vídeo específico especificando um inteiro para o parâmetro *wParam* da mensagem de conexão do driver do WM \_ Cap \_ \_ . O inteiro é um índice que identifica um driver de captura de vídeo listado no registro ou na \[ \] seção de drivers do arquivo de SYSTEM.INI. Use zero para a primeira entrada de índice.

Você pode recuperar o nome e a versão de um driver de captura instalado usando a função [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) . Seu aplicativo pode usar essa função para enumerar os dispositivos e drivers de captura instalados, para que o usuário possa selecionar um dispositivo de captura para se conectar a uma janela de captura.

Você pode recuperar o nome do driver de dispositivo de captura conectado a uma janela de captura usando a mensagem de [**\_ \_ \_ \_ nome Get do driver do WM Cap**](wm-cap-driver-get-name.md) (ou a macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ). Para recuperar a versão de um driver de captura instalado, use a mensagem [**\_ \_ \_ obter \_ versão do driver do WM Cap**](wm-cap-driver-get-version.md) (ou a macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).

Você pode desconectar uma janela de captura de um driver de captura usando a mensagem de [**\_ \_ \_ desconexão do driver do WM Cap**](wm-cap-driver-disconnect.md) (ou a macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).

Quando uma janela de captura é destruída, todos os drivers de dispositivo de captura de vídeo conectados são desconectados automaticamente.

 

 




