---
title: Método GetLastWriteTimeFromKey de IDWriteLocalFontFileLoader
description: Obtém a hora da última gravação do arquivo da chave de referência do arquivo de fonte.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Gravação direta do método GetLastWriteTimeFromKey
- Interface GetLastWriteTimeFromKey , IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader interface Direct Write , GetLastWriteTimeFromKey method
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
ms.openlocfilehash: a2fb3d79475a943c3a635b347cfd6dbe41e8b3a8903022bae9089e1d6a9847c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816310"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>Método IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey

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

*lastWriteTime* \[ out\]
</dt> <dd>

Tipo: **FILETIME \***

A hora da última modificação do arquivo de fonte.

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

 

 





