---
description: O método GetMinIdealImageSize recupera o tamanho mínimo ideal da imagem.
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: Método CBaseControlWindow.GetMinIdealImageSize (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMinIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cab33ac28153f2a22ef4ca07f4c7f83d700377909d404dbfe6d707037423f248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158448"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a>Método CBaseControlWindow.GetMinIdealImageSize

O `GetMinIdealImageSize` método recupera o tamanho mínimo ideal da imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pwidth* 
</dt> <dd>

Ponteiro para a largura ideal mínima, em pixels.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para a altura ideal mínima, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Vários renderadores têm restrições de desempenho quanto ao tamanho das imagens que podem ser exibidas. Embora eles ainda devem funcionar corretamente quando solicitado a exibir imagens maiores que o máximo especificado, os renderizadores podem nomear os tamanhos ideais mínimo e máximo por meio da interface [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Essa interface só pode ser chamada quando o grafo de filtro está em pausa ou em execução, porque não é até lá que os recursos são alocados e o renderista pode reconhecer suas restrições. Se não existir nenhuma restrição, o renderista preencherá os parâmetros *pWidth* e *pHeight* com as dimensões de vídeo nativas e retornará S \_ FALSE. Se existirem restrições, a largura restrita e a altura serão inseridas e a função membro retornará S \_ OK.

As dimensões se aplicam ao tamanho do vídeo de destino e não ao tamanho geral da janela. Portanto, ao calcular o tamanho da janela a ser definida, contabilização dos estilos de janela atuais (por exemplo, LEGENDA do WS \_ e BORDA do \_ WS).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




