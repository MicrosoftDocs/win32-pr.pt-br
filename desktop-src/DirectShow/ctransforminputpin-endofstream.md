---
description: 'O método EndOfStream notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método IPin:: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Método CTransformInputPin. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759261"
---
# <a name="ctransforminputpinendofstream-method"></a>Método CTransformInputPin. EndOfStream

O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                         |
| <dl> <dt>**\_falso**</dt> </dl>               | O PIN está sendo liberado no momento.<br/>       |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O pino de saída não está conectado.<br/> |
| <dl> <dt>**VFW \_ E \_ erro de tempo de execução \_**</dt> </dl> | Ocorreu um erro em tempo de execução.<br/>       |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl>   | O PIN foi interrompido.<br/>              |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CTransformFilter:: EndOfStream**](ctransformfilter-endofstream.md) do filtro para entregar o downstream de notificação de fim de fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




