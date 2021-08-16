---
title: Método IDWriteTextLayout3 InvalidateLayout
description: Invalida o layout, forçando o layout a remediá-lo antes de chamar as métricas ou funções de desenho. Isso será útil se a localidade de uma fonte for mudada e o layout deverá ser redesenhado ou se o tamanho de um cliente implementado por IDWriteInlineObject mudar.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Gravação direta do método InvalidateLayout
- Método InvalidateLayout Direct Write , interface IDWriteTextLayout3
- IDWriteTextLayout3 interface Direct Write , Método InvalidateLayout
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af698ce5f94918be281e633342060f70ba3f62655d7aec3794686a7793c4364a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816077"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>Método IDWriteTextLayout3::InvalidateLayout

Invalida o layout, forçando o layout a remediá-lo antes de chamar as métricas ou funções de desenho. Isso será útil se a localidade de uma fonte for mudada e o layout deverá ser redesenhado ou se o tamanho de um cliente implementado por IDWriteInlineObject mudar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

 

 





