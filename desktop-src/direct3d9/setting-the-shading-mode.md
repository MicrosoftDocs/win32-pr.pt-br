---
description: O Direct3D permite que um modo de sombreamento seja selecionado de cada vez.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Configurando o modo de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456715"
---
# <a name="setting-the-shading-mode-direct3d-9"></a><span data-ttu-id="d8e1b-103">Configurando o modo de sombreamento (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d8e1b-103">Setting the Shading Mode (Direct3D 9)</span></span>

<span data-ttu-id="d8e1b-104">O Direct3D permite que um modo de sombreamento seja selecionado de cada vez.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-104">Direct3D enables one shading mode to be selected at a time.</span></span> <span data-ttu-id="d8e1b-105">Por padrão, o sombreamento de Gouraud é selecionado.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-105">By default, Gouraud shading is selected.</span></span> <span data-ttu-id="d8e1b-106">Em C++, você pode alterar o modo de sombreamento chamando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="d8e1b-106">In C++, you can change the shading mode by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="d8e1b-107">Defina o parâmetro *State* como D3DRS \_ shadmode.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-107">Set the *State* parameter to D3DRS\_SHADEMODE.</span></span> <span data-ttu-id="d8e1b-108">O parâmetro *State* deve ser definido como um membro da enumeração [**D3DSHADEMODE**](./d3dshademode.md) .</span><span class="sxs-lookup"><span data-stu-id="d8e1b-108">The *State* parameter must be set to a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumeration.</span></span> <span data-ttu-id="d8e1b-109">Os exemplos de código de exemplo a seguir ilustram como o modo de sombreamento atual de um aplicativo Direct3D pode ser definido como modo de sombreamento simples ou Gouraud.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-109">The following sample code examples illustrate how the current shading mode of a Direct3D application can be set to flat or Gouraud shading mode.</span></span>


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a><span data-ttu-id="d8e1b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8e1b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8e1b-111">Sombreamento</span><span class="sxs-lookup"><span data-stu-id="d8e1b-111">Shading</span></span>](shading.md)
</dt> </dl>

 

 
