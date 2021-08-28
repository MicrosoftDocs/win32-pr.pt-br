---
description: Recupera o nome deste objeto de dados de arquivo.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'Método ID3DXFileData:: GetName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f98e20d5bfa5efdb756e414808cda2506fda56fdf417f54b658f17d0b5c9658b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847926"
---
# <a name="id3dxfiledatagetname-method"></a>Método ID3DXFileData:: GetName

Recupera o nome deste objeto de dados de arquivo.

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

Endereço de um ponteiro para receber o nome deste objeto de dados de arquivo. Se esse parâmetro for **NULL**, puiSize retornará o tamanho da cadeia de caracteres. Se szName apontar para uma memória válida, o nome desse objeto de dados de arquivo será copiado para szName até o número de caracteres fornecidos por puiSize.

</dd> <dt>

*puiSize* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***

Ponteiro para o tamanho da cadeia de caracteres que representa o nome desse objeto de dados de arquivo. Esse parâmetro poderá ser **nulo** se szName fornecer uma referência ao nome. Esse parâmetro retornará o tamanho da cadeia de caracteres se szName for **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Para que esse método tenha sucesso, szName ou *puiSize* deve ser não **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
