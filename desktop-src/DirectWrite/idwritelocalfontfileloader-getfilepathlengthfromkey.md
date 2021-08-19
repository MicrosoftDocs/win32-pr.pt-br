---
title: Método GetFilePathLengthFromKey de IDWriteLocalFontFileLoader
description: Obtém o comprimento do caminho de arquivo absoluto da chave de referência do arquivo de fonte.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Gravação direta do método GetFilePathLengthFromKey
- Método GetFilePathLengthFromKey Direct Write, interface IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader interface Direct Write , GetFilePathLengthFromKey method
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587f432f006493097ec8262fcc2201e2c3b67abe7115c395332671ec35efeba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816347"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>Método IDWriteLocalFontFileLoader::GetFilePathLengthFromKey

Obtém o comprimento do caminho de arquivo absoluto da chave de referência do arquivo de fonte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fontFileReferenceKey* \[ Em\]
</dt> <dd>

Tipo: **const \* void**

Chave de referência de arquivo de fonte que identifica exclusivamente o arquivo de fonte local dentro do escopo do carregador de fonte que está sendo usado.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UINT32**

Tamanho da chave de referência do arquivo de fonte em bytes.

</dd> <dt>

*filePathLength* \[ out\]
</dt> <dd>

Tipo: **UINT32 \***

Comprimento da cadeia de caracteres de caminho do arquivo, não incluindo o caractere **NULL** encerrado.

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

 

 





