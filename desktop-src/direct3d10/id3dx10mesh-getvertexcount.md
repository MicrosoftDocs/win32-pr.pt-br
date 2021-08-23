---
description: Obter o número de vértices na malha.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: Método ID3DX10Mesh::GetVertexCount (D3DX10.h)
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
ms.openlocfilehash: 00fd0cd84aedb32e2da567a92ffc421f41394a991872f9216b06a4f28f895183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566886"
---
# <a name="id3dx10meshgetvertexcount-method"></a>Método ID3DX10Mesh::GetVertexCount

Obter o número de vértices na malha. Uma malha pode conter vários buffers de vértice (ou seja, um buffer de vértice pode conter todos os dados de posição, outro pode conter todos os dados de coordenadas de textura etc.), no entanto, cada buffer de vértice conterá o mesmo número de elementos.

## <a name="syntax"></a>Sintaxe


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de vértices na malha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
