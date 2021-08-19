---
description: Método CTransformFilter.CheckConnect – o método CheckConnect determina se uma conexão de pino é adequada.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Método CTransformFilter.CheckConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a148e9edbc1cef42ecc2d1158dd18afcc908cf4d7549912b52f363aaa54cedb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953625"
---
# <a name="ctransformfiltercheckconnect-method"></a>Método CTransformFilter.CheckConnect

O `CheckConnect` método determina se uma conexão de pino é adequada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dir* 
</dt> <dd>

Membro do tipo [**enumerado PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando qual pino no filtro está fazendo a conexão.

</dd> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro pino nesta tentativa de conexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os [**métodos CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) e [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) chamam esse método durante o processo de conexão de pino. Esse método não faz nada na classe base. A classe derivada pode substituí-la. Por exemplo, a classe derivada pode consultar o outro pino para uma interface específica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




