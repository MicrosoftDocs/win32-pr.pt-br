---
description: O método Init Inicializa o objeto.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Método t CSeekingPassThru.Ini(Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751888"
---
# <a name="cseekingpassthruinit-method"></a>Método t CSeekingPassThru.Ini

O `Init` método inicializa o objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bSupportRendering* \[ no\]
</dt> <dd>

Valor booliano que especifica se o filtro é um renderizador. Use o valor **true** se o filtro for um renderizador ou **false** caso contrário.

</dd> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) no pino de entrada do filtro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                |
| <dl> <dt>**E \_ falha**</dt> </dl>        | O objeto já foi inicializado.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória suficiente para criar o objeto.<br/> |



 

## <a name="remarks"></a>Comentários

Se o valor de *bSupportRendering* for **true**, esse método criará uma instância da classe [**CRendererPosPassThru**](crendererpospassthru.md) . Caso contrário, ele cria uma instância da classe [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Seekpt. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 




