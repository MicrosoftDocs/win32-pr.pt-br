---
description: 'O método GetAllocatorRequirements recupera as propriedades de alocador solicitadas pelo PIN. Esse método implementa o método IMemInputPin:: GetAllocatorRequirements.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Método CTransInPlaceInputPin. GetAllocatorRequirements (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758443"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a>Método CTransInPlaceInputPin. GetAllocatorRequirements

O `GetAllocatorRequirements` método recupera as propriedades de alocador solicitadas pelo PIN. Esse método implementa o método [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProps* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , que é preenchida com os requisitos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                               | Descrição                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Sucesso<br/>                                                                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | O pino de saída não está conectado ou o pino de entrada downstream não oferece suporte ao método.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo**<br/>                                                                 |



 

## <a name="remarks"></a>Comentários

Se o pino de saída estiver conectado, esse método passará a chamada para o pino de entrada downstream. Caso contrário, retornará E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




