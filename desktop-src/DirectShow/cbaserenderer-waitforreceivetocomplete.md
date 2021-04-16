---
description: 'O método WaitForReceiveToComplete aguarda o método CBaseRenderer:: Receive ser concluído.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Método CBaseRenderer. WaitForReceiveToComplete (Renbase. h)
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
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757427"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>Método CBaseRenderer. WaitForReceiveToComplete

O `WaitForReceiveToComplete` método aguarda o método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) ser concluído.

## <a name="syntax"></a>Sintaxe


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chamam esse método para sincronizar a alteração de estado com o método **Receive** .

Especificamente, esse método despacha mensagens enquanto aguarda que o sinalizador [**CBaseRenderer:: m \_ bInReceive**](cbaserenderer-m-binreceive.md) se torne **falso**. O sinalizador se torna **verdadeiro** no [**método CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md) e alterna de volta para **false** depois que o método **Receive** chama o método [**CBaseRenderer::P reparerender**](cbaserenderer-preparerender.md) . A classe derivada pode usar **PrepareRender** para definir a paleta. Aguardar a conclusão de **PrepareRender** garante que as mensagens de alteração de paleta sejam expedidas antes que a alteração de estado ocorra. Isso evita um deadlock potencial.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




