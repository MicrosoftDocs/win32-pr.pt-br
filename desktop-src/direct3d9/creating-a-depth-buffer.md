---
description: Um buffer de profundidade é uma propriedade do dispositivo. Para criar um buffer de profundidade gerenciado pelo Direct3D, de definir os membros apropriados da estrutura D3DPRESENT PARAMETERS, conforme mostrado no \_ exemplo de código a seguir.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Criando um buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2f79e6ad32aa2c10b92d0233f85d86744d0a2c562b1991c89990d61bad506c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527918"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Criando um buffer de profundidade (Direct3D 9)

Um buffer de profundidade é uma propriedade do dispositivo. Para criar um buffer de profundidade gerenciado pelo Direct3D, de definir os membros apropriados da estrutura [**D3DPRESENT \_ PARAMETERS,**](d3dpresent-parameters.md) conforme mostrado no exemplo de código a seguir.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Ao definir o membro EnableAutoDepthStencil como **TRUE,** você instrui o Direct3D a gerenciar buffers de profundidade para o aplicativo. Observe que AutoDepthStencilFormat deve ser definido como um formato de buffer de profundidade válido. O sinalizador D3DFMT D16 especifica um buffer de profundidade de \_ 16 bits, se um estiver disponível.

A chamada a seguir para [**o método IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) cria um dispositivo que cria um buffer de profundidade.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



O buffer de profundidade é definido automaticamente como o destino de renderização do dispositivo. Quando o dispositivo é redefinido, o buffer de profundidade é destruído automaticamente e re-criado no novo tamanho.

Para criar uma nova superfície de buffer de profundidade, use o [**método IDirect3DDevice9::CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)

Para definir uma nova superfície de buffer de profundidade para o dispositivo, use o [**método IDirect3DDevice9::SetDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface)

Para usar o buffer de profundidade em seu aplicativo, você precisa habilitar o buffer de profundidade. Para obter detalhes, consulte [Habilitando o buffer de profundidade (Direct3D 9)](enabling-depth-buffering.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de profundidade](depth-buffers.md)
</dt> </dl>

 

 
