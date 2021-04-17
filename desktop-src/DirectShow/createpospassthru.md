---
description: A função CreatePosPassThru cria um objeto CPosPassThru ou um objeto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Função CreatePosPassThru (Ctlutil. h)
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
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789698"
---
# <a name="createpospassthru-function"></a>Função CreatePosPassThru

A `CreatePosPassThru` função cria um objeto [**CPosPassThru**](cpospassthru.md) ou um objeto [**CRendererPosPassThru**](crendererpospassthru.md) .

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

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*bRenderer* 
</dt> <dd>

Valor booliano que especifica se o filtro é um renderizador. Use o valor **true** se o filtro for um renderizador ou **false** caso contrário. Se o valor for **true**, esse método criará uma instância da classe [**CRendererPosPassThru**](crendererpospassthru.md) . Se o valor for **false**, o método criará uma instância da classe **CPosPassThru** .

</dd> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) no pino de entrada do filtro.

</dd> <dt>

*ppPassThru* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface **IUnknown** do objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido. Caso contrário, retorna um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Esse método usa a interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) para criar o objeto. O objeto é carregado dinamicamente do Quartz.dll.

Se a função for realizada com sucesso, a interface **IUnknown** retornada terá uma contagem de referência pendente. O chamador deve liberar a interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




