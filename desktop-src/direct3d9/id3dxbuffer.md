---
description: A interface ID3DXBuffer é usada como um buffer de dados, armazenando vértices, adjacências e informações materiais durante a otimização da malha e operações de carregamento.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interface ID3DXBuffer (D3DX9Mesh. h)
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
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105753512"
---
# <a name="id3dxbuffer-interface"></a>Interface ID3DXBuffer

A interface ID3DXBuffer é usada como um buffer de dados, armazenando vértices, adjacências e informações materiais durante a otimização da malha e operações de carregamento. O objeto buffer é usado para retornar dados de comprimento arbitrário. Além disso, os objetos buffer são usados para retornar código de objeto e mensagens de erro em métodos que montam os sombreadores de vértices e de pixel.

## <a name="members"></a>Membros

A interface **ID3DXBuffer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXBuffer** tem esses métodos.



| Método                                                    | Descrição                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**GetBufferPointer**](id3dxbuffer--getbufferpointer.md) | Recupera um ponteiro para os dados no buffer.<br/>      |
| [**Getbuffersize**](id3dxbuffer--getbuffersize.md)       | Recupera o tamanho total dos dados no buffer.<br/> |



 

## <a name="remarks"></a>Comentários

A interface **ID3DXBuffer** é obtida chamando a função [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .

O tipo LPD3DXBUFFER é definido como um ponteiro para a interface **ID3DXBuffer** .


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
