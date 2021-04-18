---
title: Método IDWriteTextLayout3 SetLineSpacing
description: Definir espaçamento de linha. | Método IDWriteTextLayout3 SetLineSpacing
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Gravação direta do método SetLineSpacing
- Método SetLineSpacing Direct Write, interface IDWriteTextLayout3
- IDWriteTextLayout3 interface de gravação direta, método SetLineSpacing
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
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756947"
---
# <a name="idwritetextlayout3setlinespacing-method"></a>Método IDWriteTextLayout3:: SetLineSpacing

Definir espaçamento de linha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lineSpacingOptions* \[ no\]
</dt> <dd>

Como gerenciar o espaço entre as linhas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                 |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





