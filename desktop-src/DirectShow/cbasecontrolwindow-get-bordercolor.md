---
description: O \_ método Get BorderColor recupera a cor da borda atual.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Método de CBaseControlWindow.get_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a351e794765f3dddb5275d8a588ca54ade06bb789ed720bfb17997fc11e358f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660750"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>CBaseControlWindow. obter \_ método BorderColor

O `get_BorderColor` método recupera a cor da borda atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cor* 
</dt> <dd>

Ponteiro para a cor da borda atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Um aplicativo pode definir um retângulo de destino no qual o vídeo deve ser exibido. Esse retângulo é relativo à área do cliente para a janela. Se isso for feito (o padrão é sempre pintar toda a janela), haverá uma borda ao redor do vídeo. Essa propriedade afeta a cor usada pela borda. Embora o parâmetro seja especificado como um tipo **longo** , na verdade ele é um valor **COLORREF** .

Essa função de membro deve ser chamada por objetos externos por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e, portanto, bloqueia a seção crítica para sincronizar com o filtro associado. Chame a função de membro [**CBaseControlWindow:: GetBorderColour**](cbasecontrolwindow-getbordercolour.md) para recuperar essa propriedade se não estiver chamando de um objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




