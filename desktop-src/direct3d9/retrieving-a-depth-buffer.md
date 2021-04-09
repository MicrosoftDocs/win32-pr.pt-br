---
description: 'O exemplo de código a seguir mostra como usar o método IDirect3DDevice9:: GetDepthStencilSurface para recuperar um ponteiro para a superfície de buffer de profundidade de Propriedade do dispositivo.'
ms.assetid: cd5c158a-d2c4-4ced-aa6f-cd8c0e426a74
title: Recuperando um buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae914b8506fd0c4169f0cfec0d78d7c3bd9b9d61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087815"
---
# <a name="retrieving-a-depth-buffer-direct3d-9"></a><span data-ttu-id="0ae3e-103">Recuperando um buffer de profundidade (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0ae3e-103">Retrieving a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="0ae3e-104">O exemplo de código a seguir mostra como usar o método [**IDirect3DDevice9:: GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) para recuperar um ponteiro para a superfície de buffer de profundidade de Propriedade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ae3e-104">The following code example shows how to use the [**IDirect3DDevice9::GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) method to retrieve a pointer to the depth-buffer surface owned by the device.</span></span>


```
LPDIRECT3DSURFACE9 pZBuffer;

m_d3dDevice->GetDepthStencilSurface( &pZBuffer );
```



## <a name="related-topics"></a><span data-ttu-id="0ae3e-105">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ae3e-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ae3e-106">Buffers de profundidade</span><span class="sxs-lookup"><span data-stu-id="0ae3e-106">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
