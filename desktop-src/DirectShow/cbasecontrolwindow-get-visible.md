---
description: O \_ método Get Visible recupera a visibilidade da janela atual.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Método de CBaseControlWindow.get_Visible (Ctlutil. h)
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
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778646"
---
# <a name="cbasecontrolwindowget_visible-method"></a>CBaseControlWindow. obter \_ método visível

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

Ponteiro para um sinalizador booliano de automação (0 está desativado, 1 está ativado).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro retornará 1 se a janela tiver o \_ estilo WS visível; caso contrário, 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




