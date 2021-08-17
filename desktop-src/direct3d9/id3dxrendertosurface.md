---
description: A interface ID3DXRenderToSurface é usada para generalizar o processo de renderização em superfícies.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interface ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 238e1870fd5bf1832ffbb3b5c3a5a49533ef122277a4000bafdbaa10112b4528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729502"
---
# <a name="id3dxrendertosurface-interface"></a>Interface ID3DXRenderToSurface

A interface ID3DXRenderToSurface é usada para generalizar o processo de renderização em superfícies.

## <a name="members"></a>Membros

A interface **ID3DXRenderToSurface** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToSurface** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXRenderToSurface** tem esses métodos.



| Método                                                       | Descrição                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginScene**](id3dxrendertosurface--beginscene.md)       | Inicia uma cena.<br/>                                                                                                                                                                      |
| [**Endcena**](id3dxrendertosurface--endscene.md)           | Encerra uma cena.<br/>                                                                                                                                                                        |
| [**GetDesc**](id3dxrendertosurface--getdesc.md)             | Recupera os parâmetros da superfície de renderização.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | Recupera o dispositivo Direct3D associado à superfície de renderização.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertosurface--onlostdevice.md)   | Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.<br/> |
| [**OnResetDevice**](id3dxrendertosurface--onresetdevice.md) | Use este método para readquirir recursos e salvar o estado inicial.<br/>                                                                                                                      |



 

## <a name="remarks"></a>Comentários

As superfícies podem ser usadas de várias maneiras, incluindo destinos de renderização, renderização fora da tela ou renderização para texturas.

Uma superfície pode ser configurada usando um visor separado usando o método [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md) , para fornecer uma exibição de renderização personalizada. Se a superfície não for um destino de renderização, um destino de renderização compatível será usado e o resultado será copiado para a superfície no final da cena.

A interface **ID3DXRenderToSurface** é obtida chamando a função [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .

O tipo LPD3DXRENDERTOSURFACE é definido como um ponteiro para a interface **ID3DXRenderToSurface** .


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
