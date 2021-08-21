---
description: O método WaitForReceiveToComplete aguarda a conclusão do método CBaseRenderer::Receive.
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Método CBaseRenderer.WaitForReceiveToComplete (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1f63efa53cc8e8829aba825e831f95595b16faf97bdf29777918c599aadade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016784"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>Método CBaseRenderer.WaitForReceiveToComplete

O `WaitForReceiveToComplete` método aguarda a conclusão do método [**CBaseRenderer::Receive.**](cbaserenderer-receive.md)

## <a name="syntax"></a>Sintaxe


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os [**métodos CBaseRenderer::Stop**](cbaserenderer-stop.md) e [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) chamam esse método para sincronizar a alteração de estado com o **método Receive.**

Especificamente, esse método envia mensagens enquanto aguarda o [**sinalizador CBaseRenderer::m \_ bInReceive**](cbaserenderer-m-binreceive.md) se tornar **FALSE.** O sinalizador se torna **TRUE** no método [**CBaseRenderer::P repareReceive**](cbaserenderer-preparereceive.md) e alterna de volta para **FALSE** depois que o método **Receive** chama o [**método CBaseRenderer::P repareRender.**](cbaserenderer-preparerender.md) A classe derivada pode usar **PrepareRender** para definir a paleta. Aguardar a **conclusão de PrepareRender** garante que as mensagens de alteração de paleta sejam expedidas antes que a alteração de estado ocorra. Isso evita um possível deadlock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




