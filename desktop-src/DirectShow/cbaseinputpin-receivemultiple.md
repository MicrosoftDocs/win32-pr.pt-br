---
description: O método ReceiveMultiple recebe uma matriz de exemplos. Esse método implementa o método IMemInputPin::ReceiveMultiple.
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Método CBaseInputPin.ReceiveMultiple (Amfilter.h)
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
ms.openlocfilehash: 63d71f47978a2eefdcbdacbe1c31bfe69c732c24a0479357b35aa1ddd2b0a9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079396"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>Método CBaseInputPin.ReceiveMultiple

O `ReceiveMultiple` método recebe uma matriz de exemplos. Esse método implementa o [**método IMemInputPin::ReceiveMultiple.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)

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

Endereço de uma matriz de [**ponteiros IMediaSample,**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de *tamanho nSamples.*

</dd> <dt>

*nSamples* 
</dt> <dd>

Número de exemplos a processar.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Ponteiro para uma variável que recebe o número de amostras que foram processadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles listados na tabela a seguir.



| Código de retorno                                                                                             | Descrição                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | O pino está sendo liberado no momento; O exemplo foi rejeitado.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>               | Argumento de ponteiro **NULL.**<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de mídia inválido.<br/>                             |
| <dl> <dt>**ERRO DE \_ \_ RUNTIME DO VFW E \_**</dt> </dl>   | Ocorreu um erro em tempo de run time.<br/>                      |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ ERRADO**</dt> </dl>     | O pino é interrompido.<br/>                             |



 

## <a name="remarks"></a>Comentários

Esse método se comporta como o [**método CBaseInputPin::Receive,**](cbaseinputpin-receive.md) mas recebe uma matriz de exemplos. Na classe base, o método faz um loop pela matriz e chama **Receber** com cada amostra. Substitua essa função se o filtro puder processar lotes de amostras com mais eficiência do que processá-los um por vez.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




