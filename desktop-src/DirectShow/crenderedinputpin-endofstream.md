---
description: 'O método EndOfStream notifica o PIN de que nenhum dado adicional é esperado, até que um novo comando de execução seja emitido para o filtro. Esse método implementa o método IPin:: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Método CRenderedInputPin. EndOfStream (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752490"
---
# <a name="crenderedinputpinendofstream-method"></a>Método CRenderedInputPin. EndOfStream

O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado, até que um novo comando de execução seja emitido para o filtro. Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.

## <a name="remarks"></a>Comentários

Se o filtro estiver em execução, esse método enviará um evento de [**\_ conclusão do EC**](ec-complete.md) para o Gerenciador do grafo de filtro. Caso contrário, é definido um sinalizador para que o \_ evento de conclusão do EC seja enviado quando o filtro for executado em seguida. A liberação do filtro limpa o sinalizador.

Você deve substituir esse método para manter o bloqueio de streaming do PIN:


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



Além disso, se os processos de filtro **receberem** chamadas de forma assíncrona, o PIN deverá aguardar para enviar o evento de conclusão do EC \_ até que o filtro tenha processado todas as amostras pendentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amextra. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




