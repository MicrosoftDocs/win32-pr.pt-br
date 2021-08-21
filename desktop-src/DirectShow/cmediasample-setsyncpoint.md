---
description: O método SetSyncPoint especifica se o início deste exemplo é um ponto de sincronização. Esse método implementa o método IMediaSample::SetSyncPoint.
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Método CMediaSample.SetSyncPoint (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0be51ed18e25bcbd12e33f9167493d73f0c140480f4ec0042fb0c43928720d3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156518"
---
# <a name="cmediasamplesetsyncpoint-method"></a>Método CMediaSample.SetSyncPoint

O `SetSyncPoint` método especifica se o início deste exemplo é um ponto de sincronização. Esse método implementa o [**método IMediaSample::SetSyncPoint.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bIsSyncPoint* 
</dt> <dd>

Valor booliana que especifica se este é um ponto de sincronização. Se **TRUE**, este é um ponto de sincronização.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método atualiza a variável de membro [**CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) que especifica a propriedade synchronization-point.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




