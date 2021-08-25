---
description: A função CreatePosPassThru cria um objeto CPosPassThru ou um objeto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Função CreatePosPassThru (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0118299bd328d09d77ccbb8d5258b25c0ac57bdc21fc7a47f642374e8be12357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908746"
---
# <a name="createpospassthru-function"></a>Função CreatePosPassThru

A `CreatePosPassThru` função cria um objeto [**CPosPassThru**](cpospassthru.md) ou [**um objeto CRendererPosPassThru.**](crendererpospassthru.md)

## <a name="syntax"></a>Sintaxe


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAgg* 
</dt> <dd>

Ponteiro para o proprietário desse objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, de definido esse parâmetro como **NULL.**

</dd> <dt>

*bRenderer* 
</dt> <dd>

Valor booliana que especifica se o filtro é um renderdor. Use o valor **TRUE** se o filtro for um renderdor ou **FALSE** caso contrário. Se o valor for **TRUE,** esse método criará uma instância da [**classe CRendererPosPassThru.**](crendererpospassthru.md) Se o valor for **FALSE,** o método criará uma instância da **classe CPosPassThru.**

</dd> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) no pino de entrada do filtro.

</dd> <dt>

*ppPassThru* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface **IUnknown do** objeto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido. Caso contrário, retornará **um valor HRESULT** indicando a causa do erro.

## <a name="remarks"></a>Comentários

Esse método usa a interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) para criar o objeto . O objeto é carregado dinamicamente do Quartz.dll.

Se a função for bem-sucedida, a interface **IUnknown** retornada terá uma contagem de referência pendente. O chamador deve liberar a interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




