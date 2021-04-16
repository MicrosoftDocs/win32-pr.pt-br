---
description: O método DecideAllocator seleciona um alocador de memória.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Método CBaseOutputPin. DecideAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751267"
---
# <a name="cbaseoutputpindecideallocator-method"></a>Método CBaseOutputPin. DecideAllocator

O `DecideAllocator` método seleciona um alocador de memória.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) do pino de entrada.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Esse método é chamado no final do processo de conexão do PIN. Ele executa as seguintes etapas:

1.  Chama o método [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) para recuperar os requisitos de buffer do pino de entrada, se houver.
2.  Chama o método [**IMemInputPin:: Getalocador**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) para solicitar um alocador do PIN de entrada. Se o pino de entrada não fornecer um alocador, o pino de saída criará um chamando o método de classe [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) .
3.  Chama o método de classe [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , que define as propriedades do alocador. Esse é um método virtual puro; a classe derivada deve implementá-la.
4.  Chama o método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , que notifica o pino de entrada do alocador que está sendo usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




