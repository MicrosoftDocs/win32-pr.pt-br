---
description: O método PrepareReceive prepara o filtro para renderizar um exemplo.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Método CBaseRenderer. PrepareReceive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747600"
---
# <a name="cbaserendererpreparereceive-method"></a>Método CBaseRenderer. PrepareReceive

O `PrepareReceive` método prepara o filtro para renderizar um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                             | Descrição                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                        |
| <dl> <dt>**E \_ falha**</dt> </dl>                  | Falhou.<br/>                         |
| <dl> <dt>**E \_ inesperado**</dt> </dl>            | Erro inesperado.<br/>               |
| <dl> <dt>**VFW \_ E \_ amostra \_ rejeitadas**</dt> </dl> | O filtro está descartando este exemplo.<br/> |



 

## <a name="remarks"></a>Comentários

O filtro chama esse método de dentro do método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) , antes de renderizar um exemplo. Se o filtro estiver em execução, esse método agendará o exemplo para renderização.

Se o filtro já tiver um exemplo pendente ou se o fim do fluxo já tiver sido atingido, o método retornará E \_ inesperado. Possivelmente, o filtro upstream não está serializando suas chamadas de streaming corretamente.

Se o algoritmo de agendamento determinar que o exemplo deve ser descartado (consulte [**CBaseRenderer:: ScheduleSample**](cbaserenderer-schedulesample.md)), o método retornará VFW \_ E \_ Sample \_ rejeitado. No entanto, o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do pino de entrada não passa esse código de erro para o filtro upstream, pois remover um exemplo não é um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




