---
description: O método SetConfigInfo especifica o ponteiro IGraphConfig e o evento stop.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Método CDynamicOutputPin. SetConfigInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749019"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>Método CDynamicOutputPin. SetConfigInfo

O `SetConfigInfo` método especifica o ponteiro [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e o evento stop.

## <a name="syntax"></a>Sintaxe


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGraphConfig* 
</dt> <dd>

Ponteiro para a interface [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) ou **NULL**.

</dd> <dt>

*hStopEvent* 
</dt> <dd>

Identificador para um evento que é sinalizado quando o filtro é interrompido ou **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro deve chamar esse método quando ele ingressar no grafo de filtro. O Gerenciador do grafo de filtro dá suporte a **IGraphConfig**. Para o parâmetro *hStopEvent* , crie um evento de redefinição manual. Quando o filtro deixa o gráfico de filtro, chame esse método novamente com **NULL** para ambos os parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




