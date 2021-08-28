---
description: Registra modelos personalizados, dado um objeto de enumeração ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'Método ID3DXFile:: RegisterEnumTemplates (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a7c63ed8c4a2c3a65a80ba18f1b0455111917e99dce2982eb7be1d85314b6541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630066"
---
# <a name="id3dxfileregisterenumtemplates-method"></a>Método ID3DXFile:: RegisterEnumTemplates

Registra modelos personalizados, dado um objeto de enumeração [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pEnum* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***

Ponteiro para um objeto de enumeração [**ID3DXFileEnumObject**](id3dxfileenumobject.md) que contém modelos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK.

Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Quando esse método é chamado, ele copia modelos armazenados com o ID3DXFileEnumObject, representando o arquivo, para o repositório de modelos local do objeto [**ID3DXFile**](id3dxfile.md) .

Se um ponteiro [**ID3DXFileEnumObject**](id3dxfileenumobject.md) não estiver disponível, chame o método [**RegisterTemplates**](id3dxfile--registertemplates.md) em vez disso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




