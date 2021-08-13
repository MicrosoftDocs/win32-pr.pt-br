---
title: Método SetLineSpacing de IDWriteTextLayout3
description: Definir o espaçamento de linha. | Método SetLineSpacing de IDWriteTextLayout3
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Gravação direta do método SetLineSpacing
- Método SetLineSpacing Direct Write , interface IDWriteTextLayout3
- IDWriteTextLayout3 interface Direct Write , Método SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1c054fd63beb85303a7d163a16b55f07613b687085be53e22d814b0003c63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649374"
---
# <a name="idwritetextlayout3setlinespacing-method"></a>Método IDWriteTextLayout3::SetLineSpacing

Definir o espaçamento de linha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lineSpacingOptions* \[ Em\]
</dt> <dd>

Como gerenciar o espaço entre linhas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                 |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





