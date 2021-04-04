---
description: O método KsQueryMediums recupera os meios com suporte por um PIN.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'Método IKsPin:: KsQueryMediums (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645918"
---
# <a name="ikspinksquerymediums-method"></a>Método IKsPin:: KsQueryMediums

O `KsQueryMediums` método recupera os meios com suporte por um PIN.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PPMI* \[ fora\]
</dt> <dd>

Endereço de um ponteiro para uma estrutura de [**\_ Item KSMULTIPLE**](ksmultiple-item.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método retorna uma estrutura de [**\_ Item KSMULTIPLE**](ksmultiple-item.md) alocada para tarefa, que é seguida por zero ou mais estruturas [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) . O membro **Count** da estrutura **do \_ Item KSMULTIPLE** especifica o número de estruturas **REGPINMEDIUM** . Cada estrutura **REGPINMEDIUM** define um meio com suporte do PIN.

O chamador deve liberar as estruturas retornadas, usando a função **CoTaskMemFree** .

Você deve incluir KS. h antes de ksproxy. h.

## <a name="examples"></a>Exemplos

A função auxiliar a seguir tenta corresponder a um PIN em uma mídia especificada.


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**Interface IKsPin**](ikspin.md)
</dt> <dt>

[Filtros de driver de classe WDM](wdm-class-driver-filters.md)
</dt> </dl>

 

 




