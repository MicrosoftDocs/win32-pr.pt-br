---
description: O \_ método Get WindowState recupera o estado da janela atual.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Método de CBaseControlWindow.get_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754568"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>Método WindowState de CBaseControlWindow. get \_

O `get_WindowState` método recupera o estado da janela atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWindowState* 
</dt> <dd>

Ponteiro para o estado da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro retorna um subconjunto dos parâmetros da função Microsoft Win32 **userwindow** . Em particular, ele retorna \_ o SW show e o SW \_ Hide, dependendo da visibilidade atual da janela. Ele também retorna \_ a minimização de SW e \_ o SW maximizar, dependendo se a janela é um ícone ou é expandida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




