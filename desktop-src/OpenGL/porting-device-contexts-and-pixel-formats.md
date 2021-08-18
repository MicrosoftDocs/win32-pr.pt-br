---
title: Portando contextos de dispositivo e formatos de pixel
description: Portando contextos de dispositivo e formatos de pixel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- portando para OpenGL, pixels
- Portabilidade do OpenGL, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b292fb3f27eb2ed888a4db94198944f41a8571114b38c5c90b994cdd1cb6367f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144079"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>Portando contextos de dispositivo e formatos de pixel

cada janela na implementação da Microsoft do OpenGL para Windows tem seu próprio formato de pixel atual. Um formato de pixel é definido por uma estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) . Como cada janela tem seu próprio formato de pixel, você obtém um contexto de dispositivo, define o formato de pixel do contexto do dispositivo e, em seguida, cria um contexto de renderização OpenGL para o contexto do dispositivo. O contexto de renderização usa automaticamente o formato de pixel de seu contexto de dispositivo.

O sistema de janelas X também usa uma estrutura de dados, **XVisualInfo**, para especificar as propriedades de pixels em uma janela. Estruturas **XVisualInfo** contêm uma estrutura de dados **visuais** que descreve como os recursos de cores são usados em uma tela específica.

No sistema X Window, **XVisualInfo** é usado para criar uma janela definindo a janela como o formato de pixel desejado. A estrutura retornada é usada para criar a janela e um contexto de renderização. em Windows, primeiro você cria uma janela e obtém um identificador para um contexto de dispositivo (HDC) da janela. Em seguida, o HDC é usado para definir o formato de pixel para a janela. O contexto de renderização usa o formato de pixel da janela.

a tabela a seguir compara o sistema de janelas X e as funções visuais GLX com suas funções de formato de pixel equivalentes Windows.



| Função X Window/GLX Visual                                                                                     | Windows função de formato de pixel                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| XVisualInfo \* **glXChooseVisual**(exibição *\* dpy*, *tela* int, *\* atributo* intlist)                               | int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, PIXELFORMATDESCRIPTOR *\* PPFD*)                                      |
| int **glXGetConfig**(exibição *\* dpy*, XVisualInfo *\* vis*, int *\* atriblist*, *\* valor* int)                      | int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *iPixelFormat*, uint *nbytes*, LPPIXELFORMATDESCRIPTOR *PPFD*) |
| XVisualInfo \* **XGetVisualInfo**( *\* dpy* de exibição, *\_ máscara de vinfo* longa, XVisualInfo *\* vinfo \_ Templ*, int *\* nItems*) | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)                                                                           |
| O *Visual* retornado por **glxChooseVisual** é usado quando uma janela é criada.                                   | BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *iPixelFormat*, PIXELFORMATDESCRIPTOR *\* PPFD*)                        |



 

As seções a seguir fornecem exemplos de fragmentos de código de formato de pixel para um programa do sistema de janelas X e o mesmo código após ele ter sido transportado para Windows.

-   [Exemplo de código de formato de pixel GLX](glx-pixel-format-code-sample.md)
-   [Windows Exemplo de código de formato de pixel](win32-pixel-format-code-sample.md)

Para obter mais informações sobre formatos de pixel, consulte [formatos de pixel](pixel-formats.md).

 

 




