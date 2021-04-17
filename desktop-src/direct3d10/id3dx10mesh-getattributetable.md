---
description: Recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'Método ID3DX10Mesh:: getattributetable (D3DX10. h)'
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
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782715"
---
# <a name="id3dx10meshgetattributetable-method"></a>Método ID3DX10Mesh:: getattributetable

Recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAttribTable* \[ no\]
</dt> <dd>

Tipo: **[ **\_ \_ intervalo de atributos D3DX10**](d3dx10-attribute-range.md)\***

Ponteiro para uma matriz de \_ estruturas de intervalo de atributos D3DX10 \_ , representando as entradas na tabela de atributos da malha. Especifique **NULL** para recuperar o valor de pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para o número de entradas armazenadas em pAttribTable ou um valor a ser preenchido com o número de entradas armazenadas na tabela de atributos para a malha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante. Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha não desenhando um determinado identificador de atributo ao desenhar o quadro.

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

 

 
