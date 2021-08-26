---
description: O Direct3D permite que um modo de sombreamento seja selecionado de cada vez.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Configurando o modo de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769908513d4388fafae73f5a6788aef37c3ac9456a00f2e3280c57e04c18b462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068956"
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

 

 
