---
description: O método FillBuffer preenche um exemplo de mídia com dados.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Método CSourceStream. FillBuffer (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9a522dd2b10e7ced60b65c84621bb1817be4b8abbca8656ba23f49e95fe3892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687396"
---
# <a name="csourcestreamfillbuffer-method"></a>Método CSourceStream. FillBuffer

O `FillBuffer` método preenche um exemplo de mídia com dados.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Fim do fluxo<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito<br/>       |



 

## <a name="remarks"></a>Comentários

A classe derivada deve implementar esse método.

O exemplo de mídia fornecido a esse método não tem carimbos de data/hora. A classe derivada deve chamar o método [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) para definir os carimbos de data/hora. Se apropriado para o tipo de mídia, a classe derivada também deve definir os tempos de mídia, chamando o método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) . Para obter mais informações, consulte [tempo e relógios em DirectShow](time-and-clocks-in-directshow.md).

Retorna S \_ false no final do fluxo. Isso faz com que a classe **CSourceStream** envie a notificação de fim de fluxo e pare o loop de processamento de buffer. Consulte [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) para obter mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




