---
description: O método \_ get Visible recupera a visibilidade da janela atual.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: CBaseControlWindow.get_Visible método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef75aaf396e8677e9c470239d5dfca747729b534b67f8fef53a065280175f017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017374"
---
# <a name="cbasecontrolwindowget_visible-method"></a>Método CBaseControlWindow.get \_ Visible

O `get_Visible` método recupera a visibilidade da janela atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVisible* 
</dt> <dd>

Ponteiro para um sinalizador booliana de automação (0 está desligado, 1 está on).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro retornará 1 se a janela tiver o estilo VISÍVEL do \_ WS; caso contrário, 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




