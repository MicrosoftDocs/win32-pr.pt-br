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
# <a name="setting-the-shading-mode-direct3d-9"></a>Configurando o modo de sombreamento (Direct3D 9)

O Direct3D permite que um modo de sombreamento seja selecionado de cada vez. Por padrão, o sombreamento de Gouraud é selecionado. Em C++, você pode alterar o modo de sombreamento chamando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/desktop/api) . Defina o parâmetro *State* como D3DRS \_ shadmode. O parâmetro *State* deve ser definido como um membro da enumeração [**D3DSHADEMODE**](./d3dshademode.md) . Os exemplos de código de exemplo a seguir ilustram como o modo de sombreamento atual de um aplicativo Direct3D pode ser definido como modo de sombreamento simples ou Gouraud.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreamento](shading.md)
</dt> </dl>

 

 
