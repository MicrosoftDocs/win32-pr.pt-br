---
description: Adiciona dados de adjacência ao buffer de índice da malha. Quando a malha é enviada para um sombreador de geometria que usa dados de adjacência, é necessário que o buffer de índice da malha contenha dados de adjacência.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'Método ID3DX10Mesh:: GenerateGSAdjacency (D3DX10. h)'
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
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012130"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a>Método ID3DX10Mesh:: GenerateGSAdjacency

Adiciona dados de adjacência ao buffer de índice da malha. Quando a malha é enviada para um sombreador de geometria que usa dados de adjacência, é necessário que o buffer de índice da malha contenha dados de adjacência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

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

 

 




