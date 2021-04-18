---
description: Recupera um ponteiro para o nome de um objeto de arquivo do DirectX. Preterido.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'Método IDirectXFileObject:: GetName (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788145"
---
# <a name="idirectxfileobjectgetname-method"></a>Método IDirectXFileObject:: GetName

Recupera um ponteiro para o nome de um objeto de arquivo do DirectX. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pstrNameBuf* \[ fora\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Ponteiro para o buffer no qual o nome do objeto do arquivo do DirectX será copiado. Defina como **NULL** se apenas o tamanho do buffer for necessário.

</dd> <dt>

*pdwBufLen* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Ponteiro para um DWORD especificando o comprimento do buffer apontado por pstrNameBuf. O valor do parâmetro pdwBufLen será modificado para o comprimento do buffer necessário para manter o nome do objeto, mesmo se pstrNameBuf for **nulo**. Em ambos os casos, a função retornará DXFILEERR \_ BADVALUE se o valor original de pdwBufLen não for tão grande quanto ou maior que o comprimento necessário para manter o nome do objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 
