---
title: Método IDWriteFont2 IsColorFont
description: Permite determinar se um caminho de renderização de cor é potencialmente necessário.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Gravação direta do método IsColorFont
- Método IsColorFont Direct Write, interface IDWriteFont2
- IDWriteFont2 interface de gravação direta, método IsColorFont
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369748"
---
# <a name="idwritefont2iscolorfont-method"></a>Método IDWriteFont2:: IsColorFont

Permite determinar se um caminho de renderização de cor é potencialmente necessário.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **bool**

Retornará **true** se a fonte tiver informações de cor (tabelas COLR e Cpal); caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





