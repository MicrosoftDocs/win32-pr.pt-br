---
description: O método GetMaxIdealImageSize recupera o tamanho máximo de imagem ideal.
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: Método CBaseControlWindow. GetMaxIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff87648e8f3866eaa4869f45dd0467cde614eb6b2d1405006b3df89966d8c8c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001031"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a>Método CBaseControlWindow. GetMaxIdealImageSize

O `GetMaxIdealImageSize` método recupera o tamanho máximo de imagem ideal.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Ponteiro para a largura máxima ideal, em pixels.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para a altura ideal máxima, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Vários renderizadores têm restrições de desempenho quanto ao tamanho das imagens que podem ser exibidas. Embora eles ainda devam funcionar corretamente quando solicitados a exibir imagens maiores do que o máximo especificado, os renderizadores podem indicar os tamanhos ideais mínimo e máximo por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Essa interface pode ser chamada somente quando o grafo de filtro é pausado ou está em execução, porque não é até que os recursos sejam alocados e o renderizador possa reconhecer suas restrições. Se não houver restrições, o renderizador preencherá os parâmetros *pWidth* e *pHeight* com as dimensões de vídeo nativa e retornará S \_ false. Se houver restrições, a largura e a altura restritas serão inseridas e a função de membro retornará S \_ OK.

As dimensões se aplicam ao tamanho do vídeo de destino e não ao tamanho geral da janela. Portanto, ao calcular o tamanho da janela a ser definida, a conta para os estilos de janela atuais (por exemplo, WS \_ Caption e WS \_ Border).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




