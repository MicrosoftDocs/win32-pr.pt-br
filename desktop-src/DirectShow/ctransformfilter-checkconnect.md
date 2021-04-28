---
description: Método CTransformFilter. CheckConnect – o método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Método CTransformFilter. CheckConnect (Transfrm. h)
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
ms.openlocfilehash: 5927aac2fa58322c93a23489a22dc96a1e2a67f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085094"
---
# <a name="ctransformfiltercheckconnect-method"></a>Método CTransformFilter. CheckConnect

O `CheckConnect` método determina se uma conexão de PIN é adequada.

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

Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando qual Pin no filtro está fazendo a conexão.

</dd> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN nesta tentativa de conexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os métodos [**CTransformInputPin:: CheckConnect**](ctransforminputpin-checkconnect.md) e [**CTransformOutputPin:: CheckConnect**](ctransformoutputpin-checkconnect.md) chamam esse método durante o processo de conexão do PIN. Esse método não faz nada na classe base. A classe derivada pode substituí-la. Por exemplo, a classe derivada pode consultar o outro PIN para uma interface específica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




