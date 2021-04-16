---
description: O \_ método Put MessageDrain define a janela para receber mensagens de janela enviadas ao processador de vídeo.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Método de CBaseControlWindow.put_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750685"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>Método CBaseControlWindow. put \_ MessageDrain

O `put_MessageDrain` método define a janela para receber mensagens de janela enviadas ao processador de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Desperdício* 
</dt> <dd>

Janela na qual as mensagens são postadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

As mensagens enviadas para o filtro de processador de vídeo podem ser postadas em outra janela. Essa função de membro registra a janela para receber essas mensagens. Diferentemente da função de membro [**CBaseControlWindow::p UT \_ Owner**](cbasecontrolwindow-put-owner.md) , essa função de membro não torna a janela de vídeo um filho de outra janela. Ele é particularmente útil para renderizadores de vídeo de tela inteira, que não podem ser janelas filhas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




