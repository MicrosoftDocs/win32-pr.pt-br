---
description: Método CBaseOutputPin. CheckConnect – o método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Método CBaseOutputPin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca35cb98f279674285610fbd06b0399e93a68d59749fe4129475ab8bd970824a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658859"
---
# <a name="cbaseoutputpincheckconnect-method"></a>Método CBaseOutputPin. CheckConnect

O `CheckConnect` método determina se uma conexão de PIN é adequada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                               | Descrição                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Êxito.<br/>                                                         |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>             | O PIN de entrada não dá suporte a [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).<br/> |
| <dl> <dt>**VFW \_ E \_ direção inválida \_**</dt> </dl> | As direções do PIN não são compatíveis.<br/>                               |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) de classe base e, em seguida, consulta o pino de entrada para sua interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




