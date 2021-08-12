---
description: 'O método QueryVendorInfo recupera uma cadeia de caracteres que contém informações do fornecedor. Esse método implementa o método IBaseFilter:: QueryVendorInfo.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Método CBaseFilter. QueryVendorInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff1cd8b966456df631a573ab2e8691b3be5d8bda47b21b042986204144e639b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659799"
---
# <a name="cbasefilterqueryvendorinfo-method"></a>Método CBaseFilter. QueryVendorInfo

O `QueryVendorInfo` método recupera uma cadeia de caracteres que contém informações do fornecedor. Esse método implementa o método [**IBaseFilter:: QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVendorInfo* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para uma cadeia de caracteres largos contendo as informações do fornecedor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Para fornecer informações de fornecedor para um filtro, substitua esse método. Se você implementar esse método, use a função **CoTaskMemAlloc** para alocar memória para a cadeia de caracteres. O chamador é responsável por chamar a função **CoTaskMemFree** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




