---
description: Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'Método ID3DX10Mesh:: Optimize (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298704"
---
# <a name="id3dx10meshoptimize-method"></a>Método ID3DX10Mesh:: Optimize

Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifica o tipo de otimização a ser executado. Esse parâmetro pode ser definido como uma combinação de um ou mais sinalizadores de D3DXMESHOPT e D3DXMESH (exceto D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WriteOnly e D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pFaceRemap* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Uma matriz de UINTs, uma por face, que identifica a face de malha original que corresponde a cada face na malha otimizada. Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.

</dd> <dt>

*ppVertexRemap* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Endereço de um ponteiro para uma [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos. Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Esse método gera uma nova malha. Antes de executar Optimize, um aplicativo deve gerar um buffer de adjacência chamando [**ID3DX10Mesh:: GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md). O buffer de adjacência contém dados de adjacência, como uma lista de bordas e as faces que são adjacentes entre si.

Esse método é muito semelhante ao método [**ID3DX10Mesh:: CloneMesh**](id3dx10mesh-clonemesh.md) , exceto pelo fato de que ele pode executar a otimização ao gerar o novo clone da malha. A malha de saída herda todos os parâmetros de criação da malha de entrada.

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

 

 
