---
description: O método GetDefaultRect recupera o tamanho padrão da área do cliente.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Método CBaseWindow. GetDefaultRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e64d13a3fe77370d4b5bbefb7d493738b035c40ceebd13cd7f6f0f5c6d03f783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074610"
---
# <a name="cbasewindowgetdefaultrect-method"></a>Método CBaseWindow. GetDefaultRect

O `GetDefaultRect` método recupera o tamanho padrão da área do cliente.

## <a name="syntax"></a>Sintaxe


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o retângulo padrão.

## <a name="remarks"></a>Comentários

Quando a janela é ativada, o objeto chama esse método para determinar o tamanho que ele deve tornar a área do cliente da janela. Na classe base, esse método retorna um retângulo cuja altura e largura são as constantes definidas DEFHEIGHT e DEFWIDTH. Uma classe derivada deve substituir esse método. Para um processador de vídeo, a classe derivada normalmente retornará o tamanho da imagem de vídeo nativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




