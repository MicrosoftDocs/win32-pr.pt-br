---
description: Construtor de CMediaControl. CMediaControl-método de construtor.
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Construtor CMediaControl. CMediaControl (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099204"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a>Construtor CMediaControl. CMediaControl

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para o nome do objeto para fins de depuração.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Aloque o parâmetro *pname* na memória estática. Esse nome aparece no terminal de depuração após a criação e a exclusão do objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




