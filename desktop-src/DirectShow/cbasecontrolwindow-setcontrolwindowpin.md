---
description: O método SetControlWindowPin define o PIN com o qual sincronizar.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Método CBaseControlWindow. SetControlWindowPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751276"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>Método CBaseControlWindow. SetControlWindowPin

O `SetControlWindowPin` método define o PIN com o qual sincronizar.

## <a name="syntax"></a>Sintaxe


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para o PIN com o qual a interface é sincronizada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Essa função de membro define a \_ variável de membro m pPin igual ao parâmetro pPin. Conforme descrito no construtor, a interface pode ser chamada somente quando o filtro tiver sido conectado com êxito. O objeto é transmitido por meio dessa função de membro para o PIN com o qual deve ser sincronizado; na maioria dos casos, ele determinará se o PIN está conectado sempre que ele tiver um método de interface chamado e retornará VFW \_ e \_ não \_ conectado se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




