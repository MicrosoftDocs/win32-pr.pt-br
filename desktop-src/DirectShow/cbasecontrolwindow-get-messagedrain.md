---
description: O \_ método Get MessageDrain recupera a mensagem atual drenagem.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Método de CBaseControlWindow.get_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a1e63e96950093bb7cc5760032d0b1f622c5df93a6f31673c595f54e5ea8e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017394"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>CBaseControlWindow. obter \_ método MessageDrain

O `get_MessageDrain` método recupera a mensagem de drenagem atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Desperdício* 
</dt> <dd>

Ponteiro para a janela atual recebendo mensagens da janela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

As mensagens enviadas para o filtro de processador de vídeo podem ser postadas em outra janela. A janela registrada para receber essas mensagens (usando a função de membro **CBaseControlWindow:: get \_ MessageDrain** ) é a mensagem atual drenagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




