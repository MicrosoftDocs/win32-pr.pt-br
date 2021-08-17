---
description: O método QueryFilterInfo recupera informações sobre o filtro. Esse método implementa o método IBaseFilter::QueryFilterInfo.
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Método CBaseFilter.QueryFilterInfo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31eb135a29a6e8e1c4f27c28d24b5cbf50eba3bb87b99ba9a1d3a5868c2fbc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341735"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>Método CBaseFilter.QueryFilterInfo

O `QueryFilterInfo` método recupera informações sobre o filtro. Esse método implementa o [**método IBaseFilter::QueryFilterInfo.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pinfo* 
</dt> <dd>

Ponteiro para uma [**estrutura FILTER \_ INFO.**](/windows/win32/api/strmif/ns-strmif-filter_info)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ POINTER.

## <a name="remarks"></a>Comentários

Esse método copia o nome do filtro da variável de membro [**CBaseFilter::m \_ pName**](cbasefilter-m-pname.md) para o membro **achName** da estrutura FILTER \_ INFO. Se **m \_ pName** for **NULL,** o método define **achName** como L' \\ 0'.

O método define o **membro pGraph** da estrutura FILTER INFO igual à variável de membro \_ [**CBaseFilter::m \_ pGraph**](cbasefilter-m-pgraph.md) e incrementa a contagem de referência. O chamador deve liberar a interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




