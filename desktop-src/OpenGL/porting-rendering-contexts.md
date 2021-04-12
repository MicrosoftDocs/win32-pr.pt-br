---
title: Portando contextos de renderização
description: Portando contextos de renderização
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- contextos de renderização OpenGL, portabilidade
- OpenGL no Windows, contextos de renderização
- portando para OpenGL, contextos de renderização
- Portabilidade do OpenGL, contextos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364172"
---
# <a name="porting-rendering-contexts"></a><span data-ttu-id="a416f-107">Portando contextos de renderização</span><span class="sxs-lookup"><span data-stu-id="a416f-107">Porting Rendering Contexts</span></span>

<span data-ttu-id="a416f-108">O sistema de janelas X e o Windows renderizam os contextos de renderização.</span><span class="sxs-lookup"><span data-stu-id="a416f-108">The X Window System and Windows render through rendering contexts.</span></span> <span data-ttu-id="a416f-109">Seis funções GLX gerenciam contextos de renderização e cinco deles têm uma função equivalente do Windows.</span><span class="sxs-lookup"><span data-stu-id="a416f-109">Six GLX functions manage rendering contexts and five of them have an equivalent Windows function.</span></span>

<span data-ttu-id="a416f-110">A tabela a seguir lista as funções de renderização GLX e suas funções equivalentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="a416f-110">The following table lists the GLX rendering functions and their equivalent Windows functions.</span></span>



| <span data-ttu-id="a416f-111">Função de contexto de renderização GLX</span><span class="sxs-lookup"><span data-stu-id="a416f-111">GLX rendering context function</span></span>                                                                            | <span data-ttu-id="a416f-112">Função de contexto de renderização do Windows</span><span class="sxs-lookup"><span data-stu-id="a416f-112">Windows rendering context function</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a416f-113">GLXContext **glXCopyContext**(display *\* dpy*, GLXContext *src*, GLXContext *DST*, GLuint *Mask*)</span><span class="sxs-lookup"><span data-stu-id="a416f-113">GLXContext **glXCopyContext**( Display *\*dpy*,GLXContext *src*,GLXContext *dst*,GLuint *mask*)</span></span>            | <span data-ttu-id="a416f-114">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="a416f-114">Not applicable.</span></span>                                                         |
| <span data-ttu-id="a416f-115">GLXContext **glXCreateContext**(display *\* dpy*, XVisualInfo *\* vis*, GLXContext *sharelist*, bool *Direct*)</span><span class="sxs-lookup"><span data-stu-id="a416f-115">GLXContext **glXCreateContext**( Display *\*dpy*,XVisualInfo *\*vis*,GLXContext *shareList*,Bool *direct*)</span></span> | <span data-ttu-id="a416f-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="a416f-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)</span></span>          |
| <span data-ttu-id="a416f-117">void **glXDeleteContext**(display *\* dpy*, GLXContext *CTX*)</span><span class="sxs-lookup"><span data-stu-id="a416f-117">void **glXDeleteContext**( Display *\*dpy*,GLXContext *ctx*)</span></span>                                              | <span data-ttu-id="a416f-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(HGLRC *HGLRC*)</span><span class="sxs-lookup"><span data-stu-id="a416f-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)</span></span>       |
| <span data-ttu-id="a416f-119">GLXContext **glXGetCurrentContext**(*void*)</span><span class="sxs-lookup"><span data-stu-id="a416f-119">GLXContext **glXGetCurrentContext**(*void*)</span></span>                                                               | <span data-ttu-id="a416f-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)</span><span class="sxs-lookup"><span data-stu-id="a416f-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)</span></span>      |
| <span data-ttu-id="a416f-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span><span class="sxs-lookup"><span data-stu-id="a416f-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span></span>                                                             | <span data-ttu-id="a416f-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)</span><span class="sxs-lookup"><span data-stu-id="a416f-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)</span></span>                  |
| <span data-ttu-id="a416f-123">Bool **glXMakeCurrent**(display *\* dpy*, GLXDrawable *draw*, GLXContext *CTX*)</span><span class="sxs-lookup"><span data-stu-id="a416f-123">Bool **glXMakeCurrent**( Display *\*dpy*,GLXDrawable *draw*,GLXContext *ctx*)</span></span>                              | <span data-ttu-id="a416f-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, HGLRC *HGLRC*)</span><span class="sxs-lookup"><span data-stu-id="a416f-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*,HGLRC *hglrc*)</span></span> |



 

<span data-ttu-id="a416f-125">Tipos de retorno e outros tipos têm nomes diferentes no sistema de janelas X do que no Windows.</span><span class="sxs-lookup"><span data-stu-id="a416f-125">Return types and other types have different names in the X Window System than in Windows.</span></span> <span data-ttu-id="a416f-126">Você pode pesquisar por ocorrências de GLXContext para ajudar a localizar partes do seu código que precisam ser portadas.</span><span class="sxs-lookup"><span data-stu-id="a416f-126">You can search for occurrences of GLXContext to help find parts of your code that need to be ported.</span></span>

<span data-ttu-id="a416f-127">As seções a seguir comparam os exemplos de código de contexto de renderização em um programa do sistema de janelas X e o mesmo código após ele ter sido transportado para o Windows.</span><span class="sxs-lookup"><span data-stu-id="a416f-127">The following sections compare rendering context code samples in an X Window System program and the same code after it has been ported to Windows.</span></span>

<span data-ttu-id="a416f-128">Para obter mais informações sobre contextos de renderização, consulte [contextos de renderização](rendering-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="a416f-128">For more information on rendering contexts, see [Rendering Contexts](rendering-contexts.md).</span></span>

 

 




