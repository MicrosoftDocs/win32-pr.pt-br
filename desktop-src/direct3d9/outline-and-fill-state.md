---
description: Os primitivos que não têm texturas são renderizados com a cor especificada por seu material ou com as cores especificadas para os vértices, se houver.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Estrutura de tópicos e estado de preenchimento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105790322"
---
# <a name="outline-and-fill-state-direct3d-9"></a><span data-ttu-id="790e1-103">Estrutura de tópicos e estado de preenchimento (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="790e1-103">Outline and Fill State (Direct3D 9)</span></span>

<span data-ttu-id="790e1-104">Os primitivos que não têm texturas são renderizados com a cor especificada por seu material ou com as cores especificadas para os vértices, se houver.</span><span class="sxs-lookup"><span data-stu-id="790e1-104">Primitives that have no textures are rendered with the color specified by their material, or with the colors specified for the vertices, if any.</span></span> <span data-ttu-id="790e1-105">Você pode selecionar o método para preenchê-los especificando um valor definido pelo tipo enumerado [**D3DFILLMODE**](./d3dfillmode.md) para o \_ estado de renderização FillMode D3DRS.</span><span class="sxs-lookup"><span data-stu-id="790e1-105">You can select the method to fill them by specifying a value defined by the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type for the D3DRS\_FILLMODE render state.</span></span>

<span data-ttu-id="790e1-106">Para habilitar o pontilhamento, seu aplicativo deve passar o \_ valor enumerado D3DRS DITHERENABLE como o primeiro parâmetro para [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="790e1-106">To enable dithering, your application must pass the D3DRS\_DITHERENABLE enumerated value as the first parameter to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span> <span data-ttu-id="790e1-107">Ele deve definir o segundo parâmetro como **true** para habilitar o pontilhamento e **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="790e1-107">It must set the second parameter to **TRUE** to enable dithering, and **FALSE** to disable it.</span></span>

<span data-ttu-id="790e1-108">Às vezes, desenhar o último pixel em uma linha pode causar uma sobreposição insightável com primitivas ao redor.</span><span class="sxs-lookup"><span data-stu-id="790e1-108">At times, drawing the last pixel in a line can cause unsightly overlap with surrounding primitives.</span></span> <span data-ttu-id="790e1-109">Você pode controlar isso usando o \_ valor enumerado D3DRS LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="790e1-109">You can control this using the D3DRS\_LASTPIXEL enumerated value.</span></span> <span data-ttu-id="790e1-110">No entanto, não altere essa configuração sem alguma reflexões.</span><span class="sxs-lookup"><span data-stu-id="790e1-110">However, do not alter this setting without some forethought.</span></span> <span data-ttu-id="790e1-111">Em algumas condições, suprimir a renderização do último pixel pode causar falhas insightáveis entre primitivos.</span><span class="sxs-lookup"><span data-stu-id="790e1-111">Under some conditions, suppressing the rendering of the last pixel can cause unsightly gaps between primitives.</span></span>

<span data-ttu-id="790e1-112">Contornos de objeto podem ser desenhados definindo o padrão de desenho de linha apropriado.</span><span class="sxs-lookup"><span data-stu-id="790e1-112">Object outlines can be drawn by setting the appropriate line drawing pattern.</span></span> <span data-ttu-id="790e1-113">O estado de desenho de linha padrão é desenhar linhas sólidas.</span><span class="sxs-lookup"><span data-stu-id="790e1-113">The default line drawing state is to draw solid lines.</span></span> <span data-ttu-id="790e1-114">Para obter mais informações, consulte [suporte de desenho de linha no estado de RENDERIZAÇÃO D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) .</span><span class="sxs-lookup"><span data-stu-id="790e1-114">For more information, see [Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) render state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="790e1-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="790e1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="790e1-116">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="790e1-116">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
