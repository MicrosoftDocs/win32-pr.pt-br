---
description: Adiciona uma referência de dados como um filho deste nó de dados do arquivo ID3DXFileSaveData. A referência de dados aponta para um objeto de dados de arquivo.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'Método ID3DXFileSaveData:: AddDataReference (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930648"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>Método ID3DXFileSaveData:: AddDataReference

Adiciona uma referência de dados como um filho deste nó de dados do arquivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) . A referência de dados aponta para um objeto de dados de arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do objeto de dados a ser adicionado por referência. Especifique **NULL** se o objeto de dados não tiver um nome.

</dd> <dt>

*pid* \[ no\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Ponteiro para um GUID que representa o objeto de dados a ser adicionado por referência. Se for **NULL**, será adicionada uma referência que aponta para o objeto de dados com o nome fornecido por szName.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

O objeto de dados de arquivo que está sendo referenciado deve ter um nome ou um GUID. O objeto de dados de arquivo também deve derivar de um objeto pai [**ID3DXFileSaveData**](id3dxfilesavedata.md) diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
