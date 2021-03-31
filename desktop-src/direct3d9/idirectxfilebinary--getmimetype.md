---
description: Recupera o tipo MIME (Multipurpose Internet Mail Extensions) para os dados binários. Preterido.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'Método IDirectXFileBinary:: getMimeType (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930580"
---
# <a name="idirectxfilebinarygetmimetype-method"></a>Método IDirectXFileBinary:: getMimeType

Recupera o tipo MIME (Multipurpose Internet Mail Extensions) para os dados binários. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszMimeType* \[ fora\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Endereço de um ponteiro para receber a cadeia de caracteres do tipo MIME.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Quando não houver nenhum tipo MIME especificado em um arquivo do DirectX para um objeto binário, a função definirá pszMimeType como **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
