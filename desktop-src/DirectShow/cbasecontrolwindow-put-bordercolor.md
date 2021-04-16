---
description: O \_ método Put BorderColor altera a cor da borda.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Método de CBaseControlWindow.put_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751279"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a>Método BorderColor CBaseControlWindow. put \_

O `put_BorderColor` método altera a cor da borda.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cor* 
</dt> <dd>

Nova cor da borda.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Um aplicativo pode estabelecer um retângulo de destino no qual o vídeo deve ser exibido. Esse retângulo é relativo à área do cliente para a janela. Se isso for feito (o padrão é sempre pintar toda a janela), haverá uma borda ao redor do vídeo. Essa propriedade afeta a cor usada pela borda. Embora o parâmetro seja especificado como um tipo **longo** , na verdade ele é um valor **COLORREF** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




