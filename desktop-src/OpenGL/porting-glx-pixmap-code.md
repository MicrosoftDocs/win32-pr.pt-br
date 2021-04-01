---
title: Portando código de pixmap GLX
description: Portando código de pixmap GLX
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmaps
- OpenGL no Windows, pixmaps
- portando para OpenGL, pixmaps
- Portabilidade do OpenGL, pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008087"
---
# <a name="porting-glx-pixmap-code"></a>Portando código de pixmap GLX

O sistema de janelas X usa *pixmaps*, que são superfícies de desenho virtual fora da tela na forma de uma matriz tridimensional de bits. Você pode considerar uma pixmap como uma pilha de bitmaps: uma matriz bidimensional de pixels com cada pixel com um valor de 0 a 2N1, em que N é a profundidade do pixmap.

Para programas OpenGL, você usa as funções GLX, **glXCreateGLXPixmap** e **glXDestroyGLXPixmap**, para criar e destruir GLX pixmaps usados para renderização fora da tela.

O Windows usa bitmaps independentes de dispositivo que servem a mesma função do sistema de janela X pixmaps. Use as funções padrão de bitmap do Windows para criar e destruir bitmaps.

A tabela a seguir lista as funções GLX pixmap e suas funções equivalentes de bitmap do Windows.



| GLX pixmap e função de fonte                                                          | Bitmap do Windows e função de fonte                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**(display *\* dpy*, XVisualInfo *\* vis*, pixmap *pixmap*) | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const byte *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint * fuUsage ***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finito*, DWORD *IUsage*)<br/> |
| void **glXDestroyGLXPixmap**(display *\* dpy*, GLXPixmap *PIX*)                        | BOOL [ExcluirObjeto](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

