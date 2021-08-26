---
description: O método EndOfStream notifica o pin de que nenhum dado adicional é esperado até que um novo comando de executar seja emitido para o filtro. Esse método implementa o método IPin::EndOfStream.
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Método CRenderedInputPin.EndOfStream (Amextra.h)
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
ms.openlocfilehash: 26f7a5075e06a3943978a8e938f034fbabcaddfa31c9ffa2a2b37d33a0120640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107986"
---
# <a name="crenderedinputpinendofstream-method"></a>Método CRenderedInputPin.EndOfStream

O método notifica o pin de que nenhum dado adicional é esperado até que um novo comando de executar `EndOfStream` seja emitido para o filtro. Esse método implementa o [**método IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou um código de erro caso contrário.

## <a name="remarks"></a>Comentários

Se o filtro estiver em execução, esse método enviará um [**evento EC \_ COMPLETE**](ec-complete.md) para o Gerenciador Graph Filtro. Caso contrário, define um sinalizador para que o evento EC \_ COMPLETE seja enviado quando o filtro for executado na próxima vez. A liberação do filtro limpa o sinalizador.

Você deve substituir esse método para manter o bloqueio de streaming do pino:


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



Além disso, se  o filtro processa Receber chamadas de forma assíncrona, o pino deverá aguardar para enviar o evento EC COMPLETE até que o filtro tenha processado todos os \_ exemplos pendentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amextra.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




