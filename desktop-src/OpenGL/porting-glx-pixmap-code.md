---
title: Portando código de pixmap GLX
description: Portando código de pixmap GLX
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmaps
- OpenGL em Windows, pixmaps
- portando para OpenGL, pixmaps
- Portabilidade do OpenGL, pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e50448c254b8d3e01097f1faec2b4df8aeed56be8ae3abb4f5ce13432582559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012054"
---
# <a name="porting-glx-pixmap-code"></a>Portando código de pixmap GLX

O sistema de janelas X usa *pixmaps*, que são superfícies de desenho virtual fora da tela na forma de uma matriz tridimensional de bits. Você pode considerar uma pixmap como uma pilha de bitmaps: uma matriz bidimensional de pixels com cada pixel com um valor de 0 a 2N1, em que N é a profundidade do pixmap.

Para programas OpenGL, você usa as funções GLX, **glXCreateGLXPixmap** e **glXDestroyGLXPixmap**, para criar e destruir GLX pixmaps usados para renderização fora da tela.

o Windows usa bitmaps independentes de dispositivo que servem a mesma função do sistema de janela X pixmaps. Use as funções de bitmap de Windows padrão para criar e destruir bitmaps.

a tabela a seguir lista as funções GLX pixmap e suas funções de bitmap Windows equivalentes.



| GLX pixmap e função de fonte                                                          | Windows o bitmap e a função de fonte                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**(display *\* dpy*, XVisualInfo *\* vis*, pixmap *pixmap*) | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const byte *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint * fuUsage ***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finito*, DWORD *IUsage*)<br/> |
| void **glXDestroyGLXPixmap**(display *\* dpy*, GLXPixmap *PIX*)                        | BOOL [ExcluirObjeto](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

