---
description: O método InactivateWindow inativa a janela. Na classe base, esse método oculta a janela.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Método CBaseWindow.InactivateWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3cf175a55ab5739b0fa171fe4c9553d3691be82d71b38fd5eb480d6e28043440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567456"
---
# <a name="cbasewindowinactivatewindow-method"></a>Método CBaseWindow.InactivateWindow

O `InactivateWindow` método inativa a janela. Na classe base, esse método oculta a janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                    |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | A janela já está inativa.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




