---
description: Gera uma malha simplificada usando os pesos fornecidos que são o mais próximo possível do MinValue especificado.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Função D3DXSimplifyMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812273"
---
# <a name="d3dxsimplifymesh-function"></a>Função D3DXSimplifyMesh

Gera uma malha simplificada usando os pesos fornecidos que são o mais próximo possível do MinValue especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha de origem.

</dd> <dt>

*pAdjacency* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha a ser simplificada.

</dd> <dt>

*pVertexAttributeWeights* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

Ponteiro para uma estrutura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) , que contém o peso de cada componente de vértice. Se esse parâmetro for definido como **NULL**, uma estrutura padrão será usada. Consulte Observações.

</dd> <dt>

*pVertexWeights* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de pesos de vértice. Se esse parâmetro for definido como **NULL**, todos os pesos de vértice serão definidos como 1,0.

</dd> <dt>

*MinValue* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices ou rostos, dependendo do sinalizador definido no parâmetro *Options* , por meio do qual simplificar a malha de origem.

</dd> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica opções de simplificação para a malha. Um dos sinalizadores em [**D3DXMESHSIMP**](./d3dxmeshsimp.md) pode ser definido.

</dd> <dt>

*ppMesh* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha de simplificação retornada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função gera uma malha que tem vértices de *MinValue* ou rostos.

Se o processo de simplificação não puder reduzir a malha para *MinValue*, a chamada ainda terá sucesso porque *MinValue* é um mínimo desejado, não um mínimo absoluto.

Se *pVertexAttributeWeights* for definido como **NULL**, os valores a seguir serão atribuídos à estrutura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) padrão.


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



Essa estrutura padrão é o que a maioria dos aplicativos deve usar, pois considera apenas o ajuste geométrico e normal. Somente em casos especiais, os outros campos de membro precisarão ser modificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
