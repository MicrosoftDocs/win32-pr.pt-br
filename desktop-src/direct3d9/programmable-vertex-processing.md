---
description: Ao usar um sombreador de vértice programado, os elementos atualizados no buffer de vértice de destino são controlados pelo programa de funções do sombreador.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Processamento de vértice programável (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105811460"
---
# <a name="programmable-vertex-processing-direct3d-9"></a><span data-ttu-id="04534-103">Processamento de vértice programável (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="04534-103">Programmable Vertex Processing (Direct3D 9)</span></span>

<span data-ttu-id="04534-104">Ao usar um sombreador de vértice programado, os elementos atualizados no buffer de vértice de destino são controlados pelo programa de funções do sombreador.</span><span class="sxs-lookup"><span data-stu-id="04534-104">When using a programmed vertex shader, the elements updated in the destination vertex buffer are controlled by the shader function program.</span></span> <span data-ttu-id="04534-105">Quando o aplicativo grava em um dos registros de vértice de destino, o elemento correspondente dentro de cada vértice do buffer de vértice de destino é atualizado.</span><span class="sxs-lookup"><span data-stu-id="04534-105">When the application writes to one of the destination vertex registers, the corresponding element within each vertex of the destination vertex buffer is updated.</span></span> <span data-ttu-id="04534-106">Os elementos no buffer de vértice de destino que não são gravados pelo aplicativo não são modificados.</span><span class="sxs-lookup"><span data-stu-id="04534-106">Elements in the destination vertex buffer that are not written to by the application are not modified.</span></span> <span data-ttu-id="04534-107">[**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) falhará se o aplicativo gravar em elementos que não estão presentes no buffer de vértice de destino.</span><span class="sxs-lookup"><span data-stu-id="04534-107">[**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) will fail if the application writes to elements that are not present in the destination vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04534-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04534-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04534-109">Buffers de vértice</span><span class="sxs-lookup"><span data-stu-id="04534-109">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
