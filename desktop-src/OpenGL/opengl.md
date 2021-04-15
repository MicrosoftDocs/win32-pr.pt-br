---
title: OpenGL
description: Como uma interface de software para hardware de gráficos, o OpenGL renderiza objetos multidimensionais em um framebuffer.
ms.assetid: ddd7c8d0-f1d1-4d16-bd0c-99cee3d733c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bec69473f937d4dfff9c496d291e8070ffadef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454297"
---
# <a name="opengl"></a><span data-ttu-id="c5e41-103">OpenGL</span><span class="sxs-lookup"><span data-stu-id="c5e41-103">OpenGL</span></span>

## <a name="purpose"></a><span data-ttu-id="c5e41-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="c5e41-104">Purpose</span></span>

<span data-ttu-id="c5e41-105">Como uma interface de software para hardware de gráficos, o OpenGL renderiza objetos multidimensionais em um framebuffer.</span><span class="sxs-lookup"><span data-stu-id="c5e41-105">As a software interface for graphics hardware, OpenGL renders multidimensional objects into a framebuffer.</span></span> <span data-ttu-id="c5e41-106">A implementação da Microsoft do OpenGL para o sistema operacional Windows é um software gráfico padrão da indústria com o qual os programadores podem criar imagens de cores tridimensionais e de alta qualidade ainda e animadas.</span><span class="sxs-lookup"><span data-stu-id="c5e41-106">The Microsoft implementation of OpenGL for the Windows operating system is industry-standard graphics software with which programmers can create high-quality still and animated three-dimensional color images.</span></span> <span data-ttu-id="c5e41-107">A versão do OpenGL descrita nesta seção é 1,1.</span><span class="sxs-lookup"><span data-stu-id="c5e41-107">The version of OpenGL described in this section is 1.1.</span></span>

<span data-ttu-id="c5e41-108">Para obter informações sobre OpenGL ES em execução no Windows, consulte [Angle for Windows Store](https://github.com/microsoft/angle/wiki).</span><span class="sxs-lookup"><span data-stu-id="c5e41-108">For information about OpenGL ES running on Windows, see [ANGLE for Windows Store](https://github.com/microsoft/angle/wiki).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c5e41-109">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="c5e41-109">Where applicable</span></span>

<span data-ttu-id="c5e41-110">O OpenGL foi criado para compatibilidade entre hardware e sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="c5e41-110">OpenGL is built for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="c5e41-111">Essa arquitetura facilita a porta de programas OpenGL de um sistema para outro.</span><span class="sxs-lookup"><span data-stu-id="c5e41-111">This architecture makes it easy to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="c5e41-112">Embora cada sistema operacional tenha requisitos exclusivos, o código OpenGL em muitos programas pode ser usado como está.</span><span class="sxs-lookup"><span data-stu-id="c5e41-112">While each operating system has unique requirements, the OpenGL code in many programs can be used as is.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c5e41-113">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="c5e41-113">Developer audience</span></span>

<span data-ttu-id="c5e41-114">Projetado para ser usado por programadores C/C++, o OpenGL requer familiaridade com a interface gráfica do usuário do Windows, bem como a arquitetura controlada por mensagem.</span><span class="sxs-lookup"><span data-stu-id="c5e41-114">Designed for use by C/C++ programmers, OpenGL requires familiarity with the Windows graphical user interface as well as message-driven architecture.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c5e41-115">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="c5e41-115">Run-time requirements</span></span>

<span data-ttu-id="c5e41-116">Para obter mais informações sobre quais sistemas operacionais são necessários para uma função específica, consulte a seção requisitos da documentação da função.</span><span class="sxs-lookup"><span data-stu-id="c5e41-116">For more information on which operating systems are required for a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5e41-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c5e41-117">In this section</span></span>



| <span data-ttu-id="c5e41-118">Tópico</span><span class="sxs-lookup"><span data-stu-id="c5e41-118">Topic</span></span>                                             | <span data-ttu-id="c5e41-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5e41-119">Description</span></span>                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5e41-120">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c5e41-120">Overview</span></span>](basic-opengl-operation.md)<br/> | <span data-ttu-id="c5e41-121">Informações gerais sobre como o OpenGL funciona.</span><span class="sxs-lookup"><span data-stu-id="c5e41-121">General information about how OpenGL works.</span></span><br/>                             |
| [<span data-ttu-id="c5e41-122">Referência</span><span class="sxs-lookup"><span data-stu-id="c5e41-122">Reference</span></span>](opengl-reference.md)<br/>      | <span data-ttu-id="c5e41-123">Documentação de funções, estruturas e outros elementos de programação.</span><span class="sxs-lookup"><span data-stu-id="c5e41-123">Documentation of functions, structures, and other programming elements.</span></span><br/> |
| [<span data-ttu-id="c5e41-124">Amostras</span><span class="sxs-lookup"><span data-stu-id="c5e41-124">Samples</span></span>](a-porting-sample.md)<br/>        | <span data-ttu-id="c5e41-125">Exemplos de código OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c5e41-125">Examples of OpenGL code.</span></span><br/>                                                |



 

## <a name="related-topics"></a><span data-ttu-id="c5e41-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5e41-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5e41-127">Elementos gráficos e jogos do DirectX</span><span class="sxs-lookup"><span data-stu-id="c5e41-127">DirectX Graphics and Gaming</span></span>](/windows/desktop/directx)
</dt> <dt>

<span data-ttu-id="c5e41-128">[Imagem ainda](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5e41-128">[Still Image](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c5e41-129">[WCS (sistema de cores do Windows)](/previous-versions//dd372446(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5e41-129">[Windows Color System (WCS)](/previous-versions//dd372446(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c5e41-130">GDI do Windows</span><span class="sxs-lookup"><span data-stu-id="c5e41-130">Windows GDI</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> <dt>

[<span data-ttu-id="c5e41-131">Aquisição de imagem do Windows</span><span class="sxs-lookup"><span data-stu-id="c5e41-131">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="c5e41-132">Multimídia do Windows</span><span class="sxs-lookup"><span data-stu-id="c5e41-132">Windows Multimedia</span></span>](/windows/desktop/Multimedia/windows-multimedia-start-page)
</dt> <dt>

<span data-ttu-id="c5e41-133">[API do Windows](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5e41-133">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>
</dt> </dl>

 

