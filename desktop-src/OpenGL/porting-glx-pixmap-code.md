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
# <a name="porting-glx-pixmap-code"></a><span data-ttu-id="d96a4-107">Portando código de pixmap GLX</span><span class="sxs-lookup"><span data-stu-id="d96a4-107">Porting GLX Pixmap Code</span></span>

<span data-ttu-id="d96a4-108">O sistema de janelas X usa *pixmaps*, que são superfícies de desenho virtual fora da tela na forma de uma matriz tridimensional de bits.</span><span class="sxs-lookup"><span data-stu-id="d96a4-108">The X Window System uses *pixmaps*, which are off-screen virtual drawing surfaces in the form of a three-dimensional array of bits.</span></span> <span data-ttu-id="d96a4-109">Você pode considerar uma pixmap como uma pilha de bitmaps: uma matriz bidimensional de pixels com cada pixel com um valor de 0 a 2N1, em que N é a profundidade do pixmap.</span><span class="sxs-lookup"><span data-stu-id="d96a4-109">You can think of a pixmap as a stack of bitmaps: a two-dimensional array of pixels with each pixel having a value from 0 to 2N1 where N is the depth of the pixmap.</span></span>

<span data-ttu-id="d96a4-110">Para programas OpenGL, você usa as funções GLX, **glXCreateGLXPixmap** e **glXDestroyGLXPixmap**, para criar e destruir GLX pixmaps usados para renderização fora da tela.</span><span class="sxs-lookup"><span data-stu-id="d96a4-110">For OpenGL programs you use the GLX functions, **glXCreateGLXPixmap** and **glXDestroyGLXPixmap**, to create and destroy GLX pixmaps used for off-screen rendering.</span></span>

<span data-ttu-id="d96a4-111">O Windows usa bitmaps independentes de dispositivo que servem a mesma função do sistema de janela X pixmaps.</span><span class="sxs-lookup"><span data-stu-id="d96a4-111">Windows uses device-independent bitmaps that serve the same function as X Window System pixmaps.</span></span> <span data-ttu-id="d96a4-112">Use as funções padrão de bitmap do Windows para criar e destruir bitmaps.</span><span class="sxs-lookup"><span data-stu-id="d96a4-112">Use the standard Windows bitmap functions to create and destroy bitmaps.</span></span>

<span data-ttu-id="d96a4-113">A tabela a seguir lista as funções GLX pixmap e suas funções equivalentes de bitmap do Windows.</span><span class="sxs-lookup"><span data-stu-id="d96a4-113">The following table lists the GLX pixmap functions and their equivalent Windows bitmap functions.</span></span>



| <span data-ttu-id="d96a4-114">GLX pixmap e função de fonte</span><span class="sxs-lookup"><span data-stu-id="d96a4-114">GLX pixmap and font function</span></span>                                                          | <span data-ttu-id="d96a4-115">Bitmap do Windows e função de fonte</span><span class="sxs-lookup"><span data-stu-id="d96a4-115">Windows bitmap and font function</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d96a4-116">GLXPixmap **glXCreateGLXPixmap**(display *\* dpy*, XVisualInfo *\* vis*, pixmap *pixmap*)</span><span class="sxs-lookup"><span data-stu-id="d96a4-116">GLXPixmap **glXCreateGLXPixmap**( Display *\*dpy*,XVisualInfo *\*vis*,Pixmap *pixmap*)</span></span> | <span data-ttu-id="d96a4-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const byte *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint \* fuUsage \***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finito*, DWORD *IUsage*)</span><span class="sxs-lookup"><span data-stu-id="d96a4-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\*lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage\*\*\*)*\* HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)</span></span><br/> |
| <span data-ttu-id="d96a4-118">void **glXDestroyGLXPixmap**(display *\* dpy*, GLXPixmap *PIX*)</span><span class="sxs-lookup"><span data-stu-id="d96a4-118">void **glXDestroyGLXPixmap**( Display *\*dpy*,GLXPixmap *pix*)</span></span>                        | <span data-ttu-id="d96a4-119">BOOL [ExcluirObjeto](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)</span><span class="sxs-lookup"><span data-stu-id="d96a4-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)</span></span>                                                                                                                                                                                                                                  |



 

 

