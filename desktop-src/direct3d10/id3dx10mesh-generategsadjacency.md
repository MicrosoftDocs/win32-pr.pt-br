---
description: Adiciona dados de adjacency ao buffer de índice da malha. Quando a malha deve ser enviada para um sombreador de geometria que recebe dados de adjacency, é necessário que o buffer de índice da malha contenha dados de adjacency.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: Método ID3DX10Mesh::GenerateGSAdjacency (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3bd6fdcfac53ca4655cc85e0d4373ee862f92f9bad673ed5bb20210ab9b77ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566876"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a>Método ID3DX10Mesh::GenerateGSAdjacency

Adiciona dados de adjacency ao buffer de índice da malha. Quando a malha deve ser enviada para um sombreador de geometria que recebe dados de adjacency, é necessário que o buffer de índice da malha contenha dados de adjacency.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

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

 

 




