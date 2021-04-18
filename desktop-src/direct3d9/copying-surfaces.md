---
description: O termo blit é a abreviação de &\# 0034; transferência de bloco de bits, &\# 0034; que é o processo de transferência de blocos de dados de um local na memória para outro.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copiando superfícies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796117"
---
# <a name="copying-surfaces-direct3d-9"></a><span data-ttu-id="fd266-103">Copiando superfícies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fd266-103">Copying Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="fd266-104">O termo blit é a abreviação de "transferência de bloco de bits", que é o processo de transferência de blocos de dados de um local na memória para outro.</span><span class="sxs-lookup"><span data-stu-id="fd266-104">The term blit is shorthand for "bit block transfer," which is the process of transferring blocks of data from one place in memory to another.</span></span> <span data-ttu-id="fd266-105">A interface de driver de dispositivo de transferência de bits (DDI) continua sendo usada no Direct3D 9 como o mecanismo principal para mover grandes retângulos de pixels em uma base por quadro, o mecanismo por trás do IDirect3DDevice9 orientado a cópia [**::P método reenviado**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="fd266-105">The blitting device driver interface (DDI) continues to be used in Direct3D 9 as the primary mechanism for moving large rectangles of pixels on a per-frame basis, the mechanism behind the copy-oriented [**IDirect3DDevice9::Present**](/windows/desktop/api) method.</span></span> <span data-ttu-id="fd266-106">O transporte do trabalho artístico na operação blit é executado pelo método [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="fd266-106">The transportation of artwork in the blit operation is performed by the [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api) method.</span></span> <span data-ttu-id="fd266-107">O trabalho artístico também pode ser copiado no Direct3D 9 usando o método [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , que copia um subconjunto retangular de pixels.</span><span class="sxs-lookup"><span data-stu-id="fd266-107">Artwork can also be copied in Direct3D 9 by using the [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) method, which copies a rectangular subset of pixels.</span></span>

> [!Note]  
> <span data-ttu-id="fd266-108">O Direct3D 9 fornece funções D3DX que permitem que você carregue a arte de arquivos, aplique a conversão de cores e redimensione a arte.</span><span class="sxs-lookup"><span data-stu-id="fd266-108">Direct3D 9 provides D3DX functions that enable you to load artwork from files, apply color conversion, and resize artwork.</span></span> <span data-ttu-id="fd266-109">Para obter mais informações sobre as funções disponíveis, consulte [funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span><span class="sxs-lookup"><span data-stu-id="fd266-109">For more information about the available functions see [Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fd266-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd266-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd266-111">Superfícies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="fd266-111">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="fd266-112">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="fd266-112">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

<span data-ttu-id="fd266-113">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="fd266-113">**IDirect3DDevice9::StretchRect**</span></span>
</dt> </dl>

 

 
