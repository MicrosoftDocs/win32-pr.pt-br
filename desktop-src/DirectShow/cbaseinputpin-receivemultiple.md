---
description: 'O método ReceiveMultiple recebe uma matriz de amostras. Esse método implementa o método IMemInputPin:: ReceiveMultiple.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Método CBaseInputPin. ReceiveMultiple (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811763"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>Método CBaseInputPin. ReceiveMultiple

O `ReceiveMultiple` método recebe uma matriz de amostras. Esse método implementa o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSamples* 
</dt> <dd>

Endereço de uma matriz de ponteiros [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , de tamanho *nSamples*.

</dd> <dt>

*nSamples* 
</dt> <dd>

Número de amostras a serem processadas.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Ponteiro para uma variável que recebe o número de amostras que foram processadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                             | Descrição                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                                        |
| <dl> <dt>**\_falso**</dt> </dl>                 | O PIN está sendo liberado no momento; o exemplo foi rejeitado.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>               | Argumento de ponteiro **nulo** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de mídia inválido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ erro de tempo de execução \_**</dt> </dl>   | Ocorreu um erro em tempo de execução.<br/>                      |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl>     | O PIN foi interrompido.<br/>                             |



 

## <a name="remarks"></a>Comentários

Esse método se comporta como o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) , mas recebe uma matriz de amostras. Na classe base, o método percorre a matriz e chama **Receive** com cada exemplo. Substitua essa função se o filtro puder processar lotes de amostras com mais eficiência do que processá-los um de cada vez.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




