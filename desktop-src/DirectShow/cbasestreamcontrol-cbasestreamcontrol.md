---
description: Método de construtor.
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Construtor CBaseStreamControl. CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d325a48476fe2a80b7424850eb71a9d667cb60e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754992"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a>Construtor CBaseStreamControl. CBaseStreamControl

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Se o Construtor falhar, esse parâmetro receberá um código de erro. Se isso ocorrer, o objeto não está em um estado válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




