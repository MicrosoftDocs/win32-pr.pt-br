---
description: O método SetDrawContext define os contextos de dispositivo usados para desenhar.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Método CDrawImage. SetDrawContext (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58a10c9f1a485058ed460f4cd30cd4d3894b471415f131d7d4aa59ee757b87d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055966"
---
# <a name="cdrawimagesetdrawcontext-method"></a>Método CDrawImage. SetDrawContext

O `SetDrawContext` método define os contextos de dispositivo usados para desenhar.

## <a name="syntax"></a>Sintaxe


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método recupera os contextos de dispositivo de janela e de memória do objeto [**CBaseWindow**](cbasewindow.md) proprietário. Chame esse método após a janela ser inicializada, mas antes de começar a desenhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




