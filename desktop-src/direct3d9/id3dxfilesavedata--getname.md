---
description: Recupera o nome deste nó de dados do arquivo ID3DXFileSaveData.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: 'Método ID3DXFileSaveData:: GetName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00fa8c60f423343d3d4c594d31141a2f192802d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012124"
---
# <a name="id3dxfilesavedatagetname-method"></a>Método ID3DXFileSaveData:: GetName

Recupera o nome deste nó de dados do arquivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szName* \[ no\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Endereço de um ponteiro para receber o nome deste nó de dados do arquivo. Se esse parâmetro for **NULL**, *puiSize* retornará o tamanho da cadeia de caracteres. Se szName apontar para uma memória válida, o nome desse nó de dados do arquivo será copiado para o szName até o número de caracteres fornecidos pelo *puiSize* .

</dd> <dt>

*puiSize* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***

Ponteiro para o tamanho da cadeia de caracteres que representa o nome desse nó de dados do arquivo. Esse parâmetro poderá ser **nulo** se szName fornecer uma referência ao nome. Esse parâmetro retornará o tamanho da cadeia de caracteres se szName for **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Para que esse método tenha sucesso, *szName* ou *puiSize* deve ser não **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
