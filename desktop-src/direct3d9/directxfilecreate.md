---
description: Cria uma instância de um objeto DirectXFile. Preterido.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Função DirectXFileCreate (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 6dbcf4836c33fd2acfc1adc21e47430a54ba7c54aeb2b220199846d31572619e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952176"
---
# <a name="directxfilecreate-function"></a>Função DirectXFileCreate

Cria uma instância de um objeto DirectXFile. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Tipo: **[ **LPDIRECTXFILE**](idirectxfile.md)\***

Endereço de um ponteiro para uma interface [**IDirectXFile,**](idirectxfile.md) que representa o objeto DirectXFile criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Depois de usar essa função, use [**RegisterTemplates**](idirectxfile--registertemplates.md) para registrar modelos, [**CreateEnumObject**](idirectxfile--createenumobject.md) para criar um objeto enumerador ou [**CreateSaveObject**](idirectxfile--createsaveobject.md) para criar um objeto save.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dxof.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de arquivo X](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](idirectxfile--createsaveobject.md)
</dt> <dt>

[**RegisterTemplates**](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




