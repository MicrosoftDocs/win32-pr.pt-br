---
description: O método SetConfigInfo especifica o ponteiro IGraphConfig e o evento stop.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Método CDynamicOutputPin.SetConfigInfo (Amfilter.h)
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
ms.openlocfilehash: 23b492eaf4b5f712a51132eefcceac12a772b17b8285d8c6edb1a6cec268b1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074230"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>Método CDynamicOutputPin.SetConfigInfo

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

Ponteiro para a interface [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) ou **NULL.**

</dd> <dt>

*hStopEvent* 
</dt> <dd>

Manipular para um evento que é sinalizado quando o filtro é interrompido ou **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro deve chamar esse método ao ingressar no grafo de filtro. O gerenciador de grafo de filtro dá **suporte a IGraphConfig.** Para o *parâmetro hStopEvent,* crie um evento de redefinição manual. Quando o filtro sair do grafo de filtro, chame esse método novamente com **NULL** para ambos os parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




