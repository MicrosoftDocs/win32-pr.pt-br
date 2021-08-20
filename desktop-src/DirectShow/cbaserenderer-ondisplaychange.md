---
description: O método OnDisplayChange posta um \_ evento EC display \_ Changed no Gerenciador do grafo de filtro.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Método CBaseRenderer. OnDisplayChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f7fc5d733d90ab88f1114558947b6e72958c1d8b18d507ce612c1865fc400e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016874"
---
# <a name="cbaserendererondisplaychange-method"></a>Método CBaseRenderer. OnDisplayChange

O `OnDisplayChange` método posta um evento [**EC \_ Display \_ Changed**](ec-display-changed.md) no Gerenciador do grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna **true** se o evento foi Postado ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Os renderizadores de vídeo devem chamar esse método em resposta às mensagens do WM \_ DISPLAYCHANGE. Se o pino de entrada estiver conectado, o método enviará um evento de exibição de EC \_ \_ alterado para o Gerenciador do grafo de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




