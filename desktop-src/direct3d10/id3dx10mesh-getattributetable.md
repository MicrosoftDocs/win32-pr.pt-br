---
description: Método ID3DX10Mesh::GetAttributeTable – recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributo para uma malha.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: Método ID3DX10Mesh::GetAttributeTable (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce1f2464882bfdece8997aeea23f2bb42c276b3f6ce49b13cb242d517a522250
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540286"
---
# <a name="id3dx10meshgetattributetable-method"></a>Método ID3DX10Mesh::GetAttributeTable

Recupera uma tabela de atributo para uma malha ou o número de entradas armazenadas em uma tabela de atributo para uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAttribTable* \[ Em\]
</dt> <dd>

Tipo: **[ **INTERVALO DE ATRIBUTOS \_ \_ D3DX10**](d3dx10-attribute-range.md)\***

Ponteiro para uma matriz de estruturas D3DX10 ATTRIBUTE RANGE, representando as entradas na tabela \_ \_ de atributos da malha. **Especifique NULL** para recuperar o valor de pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para o número de entradas armazenadas em pAttribTable ou um valor a ser preenchido com o número de entradas armazenadas na tabela de atributos da malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, estados de renderização, materiais e assim por diante. Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha, não desenhando um determinado identificador de atributo ao desenhar o quadro.

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

 

 
