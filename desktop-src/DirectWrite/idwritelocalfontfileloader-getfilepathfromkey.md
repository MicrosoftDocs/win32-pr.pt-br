---
title: Método GetFilePathFromKey de IDWriteLocalFontFileLoader
description: Obtém o caminho do arquivo de fonte absoluto da chave de referência do arquivo de fonte.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Gravação direta do método GetFilePathFromKey
- Método GetFilePathFromKey Direct Write , interface IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader interface Direct Write , GetFilePathFromKey method
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
ms.openlocfilehash: 7739cfa4a03abb3506bd63a84e0c747021110198f7d0ffefa69116656cbfa616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928026"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>Método IDWriteLocalFontFileLoader::GetFilePathFromKey

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

*fontFileReferenceKey* \[ Em\]
</dt> <dd>

Tipo: **const \* void**

A chave de referência do arquivo de fonte que identifica exclusivamente o arquivo de fonte local dentro do escopo do carregador de fonte que está sendo usado.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UINT32**

O tamanho da chave de referência do arquivo de fonte em bytes.

</dd> <dt>

*filePath* \[ out\]
</dt> <dd>

Tipo: **WCHAR \***

A matriz de caracteres que recebe o caminho do arquivo local.

</dd> <dt>

*filePathSize* 
</dt> <dd>

Tipo: **UINT32**

O comprimento da matriz de caracteres do caminho do arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





