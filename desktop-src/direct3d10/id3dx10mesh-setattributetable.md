---
description: 'Método ID3DX10Mesh:: SetAttributeTable – define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'Método ID3DX10Mesh:: SetAttributeTable (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6cdaedef52693810519ebb92e6f523afbfe078df68a2a13b7fae7ce0fad98fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634536"
---
# <a name="id3dx10meshsetattributetable-method"></a>Método ID3DX10Mesh:: SetAttributeTable

Define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAttribTable* \[ no\]
</dt> <dd>

Tipo: **\* [**intervalo de \_ atributos \_ const D3DX10**](d3dx10-attribute-range.md)**

Ponteiro para uma matriz de \_ estruturas de intervalo de atributos D3DX10 \_ , representando as entradas na tabela de atributos de malha.

</dd> <dt>

*cAttribTableSize* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de atributos na tabela de atributos de malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Se um aplicativo acompanhar as informações em uma tabela de atributos e reorganizar a tabela como resultado de alterações em atributos ou rostos, esse método permitirá que o aplicativo atualize as tabelas de atributos em vez de chamar ID3DX10Mesh:: Optimize novamente.

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

 

 
