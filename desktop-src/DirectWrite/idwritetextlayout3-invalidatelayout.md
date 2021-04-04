---
title: Método IDWriteTextLayout3 InvalidateLayout
description: Invalida o layout, forçando o layout a ser remedido antes de chamar as métricas ou as funções de desenho. Isso será útil se a localidade de uma fonte for alterada, e o layout deve ser redesenhado ou se o tamanho de um cliente implementado IDWriteInlineObject for alterado.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Gravação direta do método InvalidateLayout
- Método InvalidateLayout Direct Write, interface IDWriteTextLayout3
- IDWriteTextLayout3 interface de gravação direta, método InvalidateLayout
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
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085797"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>Método IDWriteTextLayout3:: InvalidateLayout

Invalida o layout, forçando o layout a ser remedido antes de chamar as métricas ou as funções de desenho. Isso será útil se a localidade de uma fonte for alterada, e o layout deve ser redesenhado ou se o tamanho de um cliente implementado IDWriteInlineObject for alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

 

 





