---
title: Método IDWriteLocalFontFileLoader GetFilePathFromKey
description: Obtém o caminho do arquivo de fonte absoluto da chave de referência do arquivo de fonte.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Gravação direta do método GetFilePathFromKey
- Método GetFilePathFromKey Direct Write, interface IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader interface de gravação direta, método GetFilePathFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768770"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>Método IDWriteLocalFontFileLoader:: GetFilePathFromKey

Obtém o caminho do arquivo de fonte absoluto da chave de referência do arquivo de fonte.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
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

*FilePath* \[ fora\]
</dt> <dd>

Tipo: **WCHAR \***

A matriz de caracteres que recebe o caminho do arquivo local.

</dd> <dt>

*filePaths* 
</dt> <dd>

Tipo: **UINT32**

O comprimento da matriz de caracteres do caminho do arquivo.

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

 

 





