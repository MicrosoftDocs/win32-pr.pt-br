---
description: Define um quadro de coordenadas ou &\# 0034; quadro de referência. &\# 0034; O modelo de quadro está aberto e pode conter qualquer objeto. As funções de carregamento de malha D3DX reconhecem instâncias de modelo de malha, FrameTransformMatrix e quadro como objetos filho ao carregar uma instância de frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Quadro (gráficos do Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825606"
---
# <a name="frame-direct3d-9-graphics"></a><span data-ttu-id="b5d3a-104">Quadro (gráficos do Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b5d3a-104">Frame (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="b5d3a-105">Define um quadro de coordenadas ou "quadro de referência".</span><span class="sxs-lookup"><span data-stu-id="b5d3a-105">Defines a coordinate frame, or "frame of reference."</span></span> <span data-ttu-id="b5d3a-106">O modelo de quadro está aberto e pode conter qualquer objeto.</span><span class="sxs-lookup"><span data-stu-id="b5d3a-106">The Frame template is open and can contain any object.</span></span> <span data-ttu-id="b5d3a-107">As funções de carregamento de malha D3DX reconhecem instâncias de modelo de [**malha**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md)e **quadro** como objetos filho ao carregar uma instância de **frame** .</span><span class="sxs-lookup"><span data-stu-id="b5d3a-107">The D3DX mesh-loading functions recognize [**Mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md), and **Frame** template instances as child objects when loading a **Frame** instance.</span></span>

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

<span data-ttu-id="b5d3a-108">O modelo de quadro reconhece o **quadro** filho e os nós de [**malha**](mesh.md) dentro de um quadro e pode reconhecer modelos definidos pelo usuário por meio de uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b5d3a-108">The frame template recognizes child **Frame** and [**Mesh**](mesh.md) nodes inside a frame and can recognize user-defined templates through a callback function.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5d3a-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5d3a-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d3a-110">Modelos</span><span class="sxs-lookup"><span data-stu-id="b5d3a-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



