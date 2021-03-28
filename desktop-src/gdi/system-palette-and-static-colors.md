---
description: Normalmente, as entradas da paleta do sistema que o sistema reserva para cores estáticas não podem ser alteradas.
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: Paleta do sistema e cores estáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537bdc87fecdd055334b83a56b0a53f9999be94c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967868"
---
# <a name="system-palette-and-static-colors"></a>Paleta do sistema e cores estáticas

Normalmente, as entradas da paleta do sistema que o sistema reserva para cores estáticas não podem ser alteradas. Um aplicativo pode substituir esse comportamento padrão usando a função [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) para reduzir o número de entradas de cores estáticas e, assim, aumentar o número de entradas de paleta do sistema não utilizadas. No entanto, como alterar as cores estáticas pode ter um efeito imediato e significativo em todas as janelas na exibição, um aplicativo não deve chamar **SetSystemPaletteUse**, a menos que tenha uma janela maximizada e o foco de entrada.

Quando um aplicativo chama [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) com o \_ valor noestático SYSPAL, o sistema libera Todas, exceto duas, das entradas reservadas, permitindo que essas entradas recebam novos valores de cor quando o aplicativo, em seguida, percebe sua paleta lógica. As duas entradas de cor estática restantes permanecem reservadas e são definidas como branco e preto. Um aplicativo pode restaurar as entradas reservadas chamando **SetSystemPaletteUse** com o \_ valor estático SYSPAL. Ele pode descobrir o uso atual da paleta do sistema usando a função [**GetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse) .

Além disso, depois de definir o uso da paleta do sistema como SYSPAL \_ noestático, o aplicativo deve reconhecer imediatamente sua paleta lógica, chamar a função [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) para salvar as configurações de cor do sistema atual, chamar a função [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) para definir as cores do sistema para valores razoáveis usando preto e branco e, finalmente, enviar a mensagem do [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) para outras janelas de nível superior para permitir que elas sejam Ao definir cores do sistema usando preto e branco, o aplicativo deve garantir que itens adjacentes ou sobrepostos, como quadros de janelas e bordas, sejam definidos como preto e branco, respectivamente.

Antes de o aplicativo perder o foco de entrada, fecha sua janela ou termina, ele deve chamar imediatamente [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) com o \_ valor estático SYSPAL, perceber sua paleta lógica, restaurar as cores do sistema para seus valores anteriores e enviar a [**mensagem \_ SYSCOLORCHANGE do WM**](wm-syscolorchange.md) . O sistema envia uma mensagem de [**\_ pintura do WM**](wm-paint.md) para qualquer janela afetada por uma alteração de cor do sistema. Os aplicativos que têm pincéis usando as cores do sistema existentes devem excluir esses pincéis e recriá-los usando as novas cores do sistema.

 

 
