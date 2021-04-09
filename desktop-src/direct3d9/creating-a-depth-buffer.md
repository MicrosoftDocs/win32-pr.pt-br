---
description: Um buffer de profundidade é uma propriedade do dispositivo. Para criar um buffer de profundidade gerenciado pelo Direct3D, defina os membros apropriados da estrutura de parâmetros D3DPRESENT, \_ conforme mostrado no exemplo de código a seguir.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Criando um buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088991"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Criando um buffer de profundidade (Direct3D 9)

Um buffer de profundidade é uma propriedade do dispositivo. Para criar um buffer de profundidade gerenciado pelo Direct3D, defina os membros apropriados da estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) , conforme mostrado no exemplo de código a seguir.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Ao definir o membro EnableAutoDepthStencil como **true**, você instrui o Direct3D a gerenciar buffers de profundidade para o aplicativo. Observe que AutoDepthStencilFormat deve ser definido como um formato de buffer de profundidade válido. O \_ sinalizador D3DFMT D16 especifica um buffer de profundidade de 16 bits, se houver um disponível.

A seguinte chamada para o método [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) cria um dispositivo que cria um buffer de profundidade.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



O buffer de profundidade é definido automaticamente como o destino de renderização do dispositivo. Quando o dispositivo é redefinido, o buffer de profundidade é automaticamente destruído e recriado no novo tamanho.

Para criar uma nova superfície de buffer de profundidade, use o método [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

Para definir uma nova superfície de buffer de profundidade para o dispositivo, use o método [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .

Para usar o buffer de profundidade em seu aplicativo, você precisa habilitar o buffer de profundidade. Para obter detalhes, consulte [habilitando o buffer de profundidade (Direct3D 9)](enabling-depth-buffering.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de profundidade](depth-buffers.md)
</dt> </dl>

 

 
