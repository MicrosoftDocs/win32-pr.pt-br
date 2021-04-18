---
description: 'O método CheckCapabilities consulta se o fluxo especificou recursos de busca. Esse método implementa o método IMediaSeeking:: CheckCapabilities.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Método CSourceSeeking. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748622"
---
# <a name="csourceseekingcheckcapabilities-method"></a>Método CSourceSeeking. CheckCapabilities

O `CheckCapabilities` método consulta se o fluxo especificou recursos de busca. Esse método implementa o método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Ponteiro para uma combinação de bits de um ou mais atributos de [**\_ \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) em busca.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>   | Nem todos os recursos do *pCapabilities* estão presentes.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Todos os recursos do *pCapabilities* estão presentes.<br/>            |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo** .<br/>                                  |



 

## <a name="remarks"></a>Comentários

Conforme implementado, esse método verifica o valor de *\* pCapabilities* em relação à variável de membro [**CSourceSeeking:: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) . No entanto, ele não define *\* pCapabilities* igual a **m \_ dwSeekingCaps**, conforme descrito para o método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) . Além disso, no caso em que nenhum dos recursos especificados está disponível, o método não retorna E \_ falha. Uma implementação mais completa seria a seguinte:


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




