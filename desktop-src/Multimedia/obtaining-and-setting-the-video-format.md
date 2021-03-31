---
title: Obtendo e definindo o formato de vídeo
description: Obtendo e definindo o formato de vídeo
ms.assetid: 0e6baf24-7a79-45ab-9fc7-69334419956d
keywords:
- macro capGetVideoFormat
- macro capGetVideoFormatSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6890c3a1d653d43d24c5baa0790cc0d26040685b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823750"
---
# <a name="obtaining-and-setting-the-video-format"></a>Obtendo e definindo o formato de vídeo

A estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) é de comprimento variável para acomodar formatos de dados padrão e compactados. Como essa estrutura é de comprimento variável, os aplicativos sempre devem consultar o tamanho da estrutura e alocar memória antes de recuperar o formato de vídeo atual. O exemplo a seguir usa a macro [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) para recuperar o tamanho do buffer e, em seguida, chama a macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) para recuperar o formato de vídeo atual.


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



Os aplicativos podem usar a macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (ou a mensagem do [**VIDEOFORMAT do WM \_ Cap \_ set \_**](wm-cap-set-videoformat.md) ) para enviar uma estrutura de cabeçalho [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) para a janela de captura. Como os formatos de vídeo são específicos do dispositivo, seu aplicativo deve verificar o valor de retorno para determinar se o formato foi aceito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 