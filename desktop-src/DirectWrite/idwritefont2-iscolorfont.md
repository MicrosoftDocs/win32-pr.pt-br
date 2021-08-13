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
ms.openlocfilehash: 144aded290c7a4121dd785a1844971e3c1b5501b8ae78707d8da5378c44b002a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650180"
---
# <a name="idwritefont2iscolorfont-method"></a>Método IDWriteFont2:: IsColorFont

Permite determinar se um caminho de renderização de cor é potencialmente necessário.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **bool**

Retornará **true** se a fonte tiver informações de cor (tabelas COLR e Cpal); caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





