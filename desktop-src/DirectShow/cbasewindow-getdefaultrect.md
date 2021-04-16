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
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759147"
---
# <a name="cbasewindowgetdefaultrect-method"></a>Método CBaseWindow. GetDefaultRect

O `GetDefaultRect` método recupera o tamanho padrão da área do cliente.

## <a name="syntax"></a>Sintaxe


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o retângulo padrão.

## <a name="remarks"></a>Comentários

Quando a janela é ativada, o objeto chama esse método para determinar o tamanho que ele deve tornar a área do cliente da janela. Na classe base, esse método retorna um retângulo cuja altura e largura são as constantes definidas DEFHEIGHT e DEFWIDTH. Uma classe derivada deve substituir esse método. Para um processador de vídeo, a classe derivada normalmente retornará o tamanho da imagem de vídeo nativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




