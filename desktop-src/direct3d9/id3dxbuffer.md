---
description: A interface ID3DXBuffer é usada como um buffer de dados, armazenar informações de vértice, adjacency e material durante operações de carregamento e otimização de malha.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interface ID3DXBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cc69262949b9cc700f0a7c477bcfacb7dacd1fc51eb836ad76dfaa2fecb7358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121674"
---
# <a name="id3dxbuffer-interface"></a>Interface ID3DXBuffer

A interface ID3DXBuffer é usada como um buffer de dados, armazenar informações de vértice, adjacency e material durante operações de carregamento e otimização de malha. O objeto de buffer é usado para retornar dados de comprimento arbitrário. Além disso, os objetos de buffer são usados para retornar o código do objeto e mensagens de erro em métodos que montam sombreadores de vértice e pixel.

## <a name="members"></a>Membros

A interface **ID3DXBuffer** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXBuffer** tem esses métodos.



| Método                                                    | Descrição                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**GetBufferPointer**](id3dxbuffer--getbufferpointer.md) | Recupera um ponteiro para os dados no buffer.<br/>      |
| [**GetBufferSize**](id3dxbuffer--getbuffersize.md)       | Recupera o tamanho total dos dados no buffer.<br/> |



 

## <a name="remarks"></a>Comentários

A interface **ID3DXBuffer** é obtida chamando a [**função D3DXCreateBuffer.**](d3dxcreatebuffer.md)

O tipo LPD3DXBUFFER é definido como um ponteiro para a interface **ID3DXBuffer.**


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
