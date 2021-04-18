---
description: 'O método QueryFilterInfo recupera informações sobre o filtro. Esse método implementa o método IBaseFilter:: QueryFilterInfo.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Método CBaseFilter. QueryFilterInfo (Amfilter. h)
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
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752515"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>Método CBaseFilter. QueryFilterInfo

O `QueryFilterInfo` método recupera informações sobre o filtro. Esse método implementa o método [**IBaseFilter:: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ informações de filtro**](/windows/win32/api/strmif/ns-strmif-filter_info) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou o \_ ponteiro.

## <a name="remarks"></a>Comentários

Esse método copia o nome do filtro da variável de membro [**CBaseFilter:: m \_ pname**](cbasefilter-m-pname.md) para o membro **achName** da estrutura de \_ informações de filtro. Se **m \_ pname** for **nulo**, o método definirá **achName** como L ' \\ 0 '.

O método define o membro **pGraph** da estrutura de \_ informações de filtro igual à variável de membro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) e incrementa a contagem de referência. O chamador deve liberar a interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




