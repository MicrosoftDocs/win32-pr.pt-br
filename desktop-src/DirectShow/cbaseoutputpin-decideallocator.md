---
description: O método DecideAllocator seleciona um alocador de memória.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Método CBaseOutputPin.DecideAllocator (Amfilter.h)
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
ms.openlocfilehash: 73d822450d635fe5f7620d59f39fcc7ed85fe1e2465f34af3ef561dfc2f3828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814206"
---
# <a name="cbaseoutputpindecideallocator-method"></a>Método CBaseOutputPin.DecideAllocator

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

Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator do**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) alocador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou **um valor HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Esse método é chamado no final do processo de conexão de pino. Ele executa as seguintes etapas:

1.  Chama o [**método IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) para recuperar os requisitos de buffer do pino de entrada, se algum.
2.  Chama o [**método IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) para solicitar um alocador do pino de entrada. Se o pino de entrada não fornecer um alocador, o pino de saída criará um chamando o método de classe [**CBaseOutputPin::InitAllocator.**](cbaseoutputpin-initallocator.md)
3.  Chama o método de classe [**CBaseOutputPin::D eputaçãoBufferSize,**](cbaseoutputpin-decidebuffersize.md) que define as propriedades do alocador. Esse é um método virtual puro; a classe derivada deve implementá-la.
4.  Chama o [**método IMemInputPin::NotifyAllocator,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) que notifica o pino de entrada do alocador que está sendo usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




