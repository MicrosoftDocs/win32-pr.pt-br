---
title: Automatizando a reprodução
description: Automatizando a reprodução
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- Macro MCIWndCreate
- Macro MCIWndPlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1c05041bade08f47505a2cf1207739777c5af825ea9f5f300b343b87efe3c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691966"
---
# <a name="automating-playback"></a>Automatizando a reprodução

Você pode automatizar a reprodução em seu aplicativo usando [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e a macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , juntamente com a macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) ou [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) . Para automatizar a reprodução, especifique os \_ estilos MCIWNDF NOPLAYBAR e MCIWNDF \_ notifymode no parâmetro **MCIWndCreate**_dwStyle_ . Especifique o \_ estilo MCIWNDF NOPLAYBAR para ocultar a barra de ferramentas e o \_ estilo notifymode MCIWNDF para emitir uma mensagem de notificação apropriada quando o dispositivo parar de ser executado.

Você pode reproduzir o dispositivo ou o arquivo especificado em **MCIWndCreate** usando **MCIWndPlay**. A macro MCIWndPlay começa a reproduzir o conteúdo de sua posição de reprodução atual e continua até seu fim.

Você pode destruir ou fechar uma janela do MCIWnd usando a macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) ou [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) . A macro **MCIWndDestroy** fecha o dispositivo ou arquivo e destrói a janela MCIWnd invalidando seu identificador. Se seu aplicativo puder reutilizar a janela MCIWnd, use **MCIWndClose** para fechar o dispositivo sem destruir a janela.

Seu aplicativo pode detectar quando o dispositivo para de reproduzir e fechar automaticamente a janela. Para fazer isso, especifique o \_ estilo notifymode MCIWNDF para o parâmetro *DwStyle* de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea). Isso faz com que o dispositivo envie uma mensagem [**MCIWNDM \_ notifymode**](mciwndm-notifymode.md) sempre que ele altera os modos. Seu aplicativo pode interceptar esta mensagem para determinar se o dispositivo parou de ser reproduzido. Quando o dispositivo para de ser executado, o aplicativo fecha a janela.

 

 




