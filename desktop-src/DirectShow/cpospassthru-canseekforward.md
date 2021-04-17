---
description: 'O método CanSeekForward determina se o fluxo pode ser buscado em frente. Esse método implementa o método IMediaPosition:: CanSeekForward.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Método CPosPassThru. CanSeekForward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768654"
---
# <a name="cpospassthrucanseekforward-method"></a>Método CPosPassThru. CanSeekForward

O `CanSeekForward` método determina se o fluxo pode ser buscado em frente. Esse método implementa o método [**IMediaPosition:: CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCanSeekForward* 
</dt> <dd>

Ponteiro para uma variável que recebe o valor OATRUE se o filtro puder ser encaminhado ou OAFALSE caso contrário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




