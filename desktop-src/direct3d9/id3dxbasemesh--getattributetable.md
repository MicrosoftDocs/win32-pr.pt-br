---
description: Método ID3DXBaseMesh::GetAttributeTable – recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributo para uma malha.
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: Método ID3DXBaseMesh::GetAttributeTable (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4933c3e15faee28448a653c5479be0d976abfd7bd913a7b50ef34acf4b52f6f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026496"
---
# <a name="id3dxbasemeshgetattributetable-method"></a>Método ID3DXBaseMesh::GetAttributeTable

Recupera uma tabela de atributo para uma malha ou o número de entradas armazenadas em uma tabela de atributo para uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAttribTable* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***

Ponteiro para uma matriz de [**estruturas D3DXATTRIBUTERANGE,**](d3dxattributerange.md) representando as entradas na tabela de atributos da malha. **Especifique NULL** para recuperar o valor de pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o número de entradas armazenadas em pAttribTable ou um valor a ser preenchido com o número de entradas armazenadas na tabela de atributos da malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Uma tabela de atributos é criada por [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) e passando D3DXMESHOPT \_ ATTRSORT para o parâmetro Flags.

Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, estados de renderização, materiais e assim por diante. Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha, não desenhando um determinado identificador de atributo ao desenhar o quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
