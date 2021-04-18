---
description: O método WaitForRenderTime aguarda o tempo de apresentação do exemplo atual.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Método CBaseRenderer. WaitForRenderTime (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749626"
---
# <a name="cbaserendererwaitforrendertime-method"></a>Método CBaseRenderer. WaitForRenderTime

O `WaitForRenderTime` método aguarda o tempo de apresentação do exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                           | Descrição                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                                                       |
| <dl> <dt>**VFW \_ E \_ estado \_ alterado**</dt> </dl> | O estado do filtro foi alterado antes de o tempo de apresentação chegar.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método aguarda até que ocorra um dos seguintes:

-   O tempo de apresentação do exemplo chega, no ponto em que o exemplo pode ser renderizado.
-   O filtro para ou começa a liberar dados.

Se o tempo de apresentação chegar, o evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) será sinalizado. Se o estado for alterado, o evento [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) será sinalizado. Esse método espera em ambos os eventos. A classe derivada pode substituir esse método para aguardar eventos adicionais, se necessário.

Esse método chama o método [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) quando a espera começa e o método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) quando a espera é concluída. Nenhum método faz nada na classe base, mas a classe derivada pode substituí-los.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




