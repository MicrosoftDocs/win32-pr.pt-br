---
description: O método GetMinIdealImageSize recupera o tamanho mínimo da imagem ideal.
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: Método CBaseControlWindow. GetMinIdealImageSize (Ctlutil. h)
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
ms.openlocfilehash: 24eeb4cdb5972f81e6dd66a812c9a38b61dcab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749046"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a>Método CBaseControlWindow. GetMinIdealImageSize

O `GetMinIdealImageSize` método recupera o tamanho mínimo da imagem ideal.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Aponta para a largura mínima ideal, em pixels.

</dd> <dt>

*pHeight* 
</dt> <dd>

Aponta para a altura ideal mínima, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Vários renderizadores têm restrições de desempenho quanto ao tamanho das imagens que podem ser exibidas. Embora eles ainda devam funcionar corretamente quando solicitados a exibir imagens maiores do que o máximo especificado, os renderizadores podem indicar os tamanhos ideais mínimo e máximo por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Essa interface pode ser chamada somente quando o grafo de filtro é pausado ou está em execução, porque não é até que os recursos sejam alocados e o renderizador possa reconhecer suas restrições. Se não houver restrições, o renderizador preencherá os parâmetros *pWidth* e *pHeight* com as dimensões de vídeo nativa e retornará S \_ false. Se houver restrições, a largura e a altura restritas serão inseridas e a função de membro retornará S \_ OK.

As dimensões se aplicam ao tamanho do vídeo de destino e não ao tamanho geral da janela. Portanto, ao calcular o tamanho da janela a ser definida, a conta para os estilos de janela atuais (por exemplo, WS \_ Caption e WS \_ Border).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




