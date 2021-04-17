---
title: Método IDWriteLocalFontFileLoader GetLastWriteTimeFromKey
description: Obtém a hora da última gravação do arquivo da chave de referência do arquivo de fonte.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Gravação direta do método GetLastWriteTimeFromKey
- Método GetLastWriteTimeFromKey Direct Write, interface IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader interface de gravação direta, método GetLastWriteTimeFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782826"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>Método IDWriteLocalFontFileLoader:: GetLastWriteTimeFromKey

Obtém a hora da última gravação do arquivo da chave de referência do arquivo de fonte.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fontFileReferenceKey* \[ no\]
</dt> <dd>

Tipo: **const void \***

A chave de referência do arquivo de fonte que identifica exclusivamente o arquivo de fonte local dentro do escopo do carregador de fonte que está sendo usado.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UINT32**

O tamanho da chave de referência do arquivo de fonte em bytes.

</dd> <dt>

*LastWriteTime* \[ fora\]
</dt> <dd>

Tipo: **FILETIME \***

A hora da última modificação de arquivo de fonte.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





