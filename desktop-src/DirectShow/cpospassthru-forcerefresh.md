---
description: O método ForceRefresh é obsoleto.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Método CPosPassThru. ForceRefresh (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 738a528562afd04e27105691b001958f130e353ec52aa60da86bec47c81b5ba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915516"
---
# <a name="cpospassthruforcerefresh-method"></a>Método CPosPassThru. ForceRefresh

O `ForceRefresh` método está obsoleto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Originalmente, essa classe foi projetada para armazenar em cache ponteiros para as interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do PIN conectado. O `ForceRefresh` método liberou essas interfaces.

Como implementado atualmente, essa classe não armazena em cache essas interfaces. Para compatibilidade, o `ForceRefresh` método ainda é incluído, mas ele retorna S \_ OK sem fazer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




