---
description: Desenhe várias instâncias do mesmo subconjunto de uma malha.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: 'ID3DX10Mesh: método rawSubsetInstanced de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2e28d7a7d2c1d743090832d68793ec3743662308
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335630"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>ID3DX10Mesh: método rawSubsetInstanced de:D

Desenhe várias instâncias do mesmo subconjunto de uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Atribid* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifica qual subconjunto da malha deve ser desenhada. Esse valor é usado para diferenciar faces em uma malha como pertencente a um ou mais grupos de atributos. Consulte Observações.

</dd> <dt>

*InstanceCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de instâncias a serem renderizadas.

</dd> <dt>

*StartInstanceLocation* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

A qual instância iniciar a busca em cada buffer marcado como dados de instância.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Uma malha contém uma tabela de atributos. A tabela de atributos pode dividir uma malha em subconjuntos, onde cada subconjunto é identificado com uma ID de atributo. Por exemplo, uma malha com 200 rostos, dividida em três subconjuntos, pode ter uma tabela de atributos parecida com esta:



| Subset     | Faces           |
|------------|-----------------|
| AttribId 0 | Faces 0 ~ 50    |
| AttribID 1 | Faces 51 ~ 125  |
| AttribID 2 | Faces 126 ~ 200 |



 

O instanciamento pode estender o desempenho reutilização da mesma geometria para desenhar vários objetos em uma cena. Um exemplo de instanciamento pode ser desenhar o mesmo objeto com diferentes posições e cores. A indexação requer vários buffers de vértice: pelo menos um para dados por vértice e um segundo buffer para dados por instância.

As instâncias de desenho com DrawSubsetInstanced são muito semelhantes ao processo usado com [**ID3D10Device::D rawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) descrito em [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx). A principal diferença ao usar DrawSubsetInstanced é que os buffers de vértice e índice devem ser extraídos do objeto [**interface ID3DX10Mesh**](id3dx10mesh.md) antes que os dados de instanciação possam ser combinados.

O código a seguir ilustra a extração dos buffers de vértice e índice do objeto de malha.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



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

 

 
