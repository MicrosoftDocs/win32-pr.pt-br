---
description: Cria uma instância de um objeto DirectXfile. Preterido.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Função DirectXFileCreate (DXFile. h)
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
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793992"
---
# <a name="directxfilecreate-function"></a>Função DirectXFileCreate

Cria uma instância de um objeto DirectXfile. Preterido.

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

Endereço de um ponteiro para uma interface [**IDirectXFile**](idirectxfile.md) , que representa o objeto directxfile criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Depois de usar essa função, use [**RegisterTemplates**](idirectxfile--registertemplates.md) para registrar modelos, [**createenumobject**](idirectxfile--createenumobject.md) para criar um objeto enumerador ou [**createsaveobject**](idirectxfile--createsaveobject.md) para criar um objeto Save.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dxof.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de arquivo X](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[**Createenumobject**](idirectxfile--createenumobject.md)
</dt> <dt>

[**Createsaveobject**](idirectxfile--createsaveobject.md)
</dt> <dt>

[**RegisterTemplates**](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




