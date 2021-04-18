---
description: Obtenha o número de vértices na malha.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'Método ID3DX10Mesh:: GetVertexCount (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771578"
---
# <a name="id3dx10meshgetvertexcount-method"></a>Método ID3DX10Mesh:: GetVertexCount

Obtenha o número de vértices na malha. Uma malha pode conter vários buffers de vértice (ou seja, um buffer de vértice pode conter todos os dados de posição, outro pode incluir todos os dados de coordenadas de textura, etc.), no entanto, cada buffer de vértice conterá o mesmo número de elementos.

## <a name="syntax"></a>Sintaxe


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de vértices na malha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
