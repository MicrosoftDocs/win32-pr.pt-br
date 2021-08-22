---
description: Método ID3DX10Mesh::D rawSubset – desenha um subconjunto de uma malha.
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: Método ID3DX10Mesh::D rawSubset (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 75723819ab7a4f82f25a68dfc2f0017e8b871130a8e0fbe70c939a95de221426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753096"
---
# <a name="id3dx10meshdrawsubset-method"></a>Método ID3DX10Mesh::D rawSubset

Desenha um subconjunto de uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AttribId* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Especifica qual subconjunto da malha desenhar. Esse valor é usado para diferenciar rostos em uma malha como pertencentes a um ou mais grupos de atributos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, estados de renderização, materiais e assim por diante. Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha, não desenhando um determinado identificador de atributo (AttribId) ao desenhar o quadro.

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

 

 
