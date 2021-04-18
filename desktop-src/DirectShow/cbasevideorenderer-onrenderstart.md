---
description: O método OnRenderStart define informações para renderização.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Método CBaseVideoRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757330"
---
# <a name="cbasevideorendereronrenderstart-method"></a>Método CBaseVideoRenderer. OnRenderStart

O `OnRenderStart` método define informações para renderização.

## <a name="syntax"></a>Sintaxe


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para o exemplo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro recupera a hora do relógio atual do sistema e a armazena em uma variável de membro a ser usada quando o desenho for concluído. A função também executa o log de desempenho. Essa função de membro deve ser chamada logo antes do início do desenho.

Essa função de membro substitui [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




