---
description: 'O método Stop interrompe o filtro. Esse método implementa o método IMediaFilter:: Stop.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Método CBaseFilter. Stop (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 659ad34c01ca6c74a24f6bbf5f5bef42df46f94f06b7e03541f9caf3398b39e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768186"
---
# <a name="cbasefilterstop-method"></a>Método CBaseFilter. Stop

O `Stop` método para o filtro. Esse método implementa o método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Esse método chama o método [**CBasePin:: Inactive**](cbasepin-inactive.md) em cada um dos Pins conectados do filtro. Ele também define o estado do filtro como estado \_ parado.

Quando o filtro é interrompido, ele deve rejeitar amostras de upstream, parar de entregar amostras downstream, desligar threads de trabalho e liberar todos os recursos usados para streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




