---
description: Representa o gerenciamento de mapeamentos da tinta para a janela de exibição. Use o objeto InkRenderer para exibir a tinta em uma janela. Você também pode usá-lo para reposicionar e redimensionar o traço.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Classe InkRenderer (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: f03b65a1ce009313b996fc7bede03f8c7425ff589fd29506c243f3161a851583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938716"
---
# <a name="inkrenderer-class"></a>Classe InkRenderer

Representa o gerenciamento de mapeamentos da tinta para a janela de exibição. Use o objeto **InkRenderer** para exibir a tinta em uma janela. Você também pode usá-lo para reposicionar e redimensionar o traço.

**InkRenderer** tem estes tipos de membros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)

### <a name="interfaces"></a>Interfaces

A classe **InkRenderer** define essas interfaces.



| Interface        | Descrição                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkRenderer** | Esse objeto implementa a interface com do **IInkRenderer** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **InkRenderer** tem esses métodos.



| Método                                                                     | Descrição                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Desenha traços em um contexto de dispositivo.<br/>                                                                                                            |
| [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Desenha um traço no contexto de dispositivo do Windows especificado.<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Recupera a transformação de objeto que foi usada para renderizar a tinta.<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Recupera a transformação de exibição usada para renderizar a tinta.<br/>                                                                                      |
| [**InkSpaceToPixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Converte um local em coordenadas de espaço de tinta para estar no espaço de pixel.<br/>                                                                            |
| [**InkSpaceToPixelFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Converte uma matriz de pontos em coordenadas de espaço de tinta para o espaço de pixel.<br/>                                                                          |
| [**Medida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Calcula o retângulo no contexto do dispositivo que conteria uma coleção de traços se eles foram desenhados com o objeto **InkRenderer** .<br/> |
| [**MeasureStroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Calcula o retângulo no contexto do dispositivo que conteria um traço se eles fossem desenhados com o objeto **InkRenderer** .<br/>                |
| [**Mover**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Aplica uma tradução à transformação exibir em coordenadas de espaço de tinta.<br/>                                                                         |
| [**PixelToInkSpace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Converte um local em coordenadas de pixel para estar no espaço de tinta.<br/>                                                                                  |
| [**PixelToInkSpaceFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Converte uma matriz de pontos em coordenadas de espaço em pixel para o espaço à tinta.<br/>                                                                          |
| [**Girar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Aplica uma rotação à transformação de exibição.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Dimensiona a transformação da exibição na dimensão X e Y.<br/>                                                                                           |
| [**SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Define a transformação do objeto que é usada para renderizar a tinta.<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Define a transformação de exibição usada para renderizar a tinta.<br/>                                                                                           |



 

## <a name="remarks"></a>Comentários

A impressão também é feita por meio do objeto **InkRenderer** .

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedade do renderizador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**Classe InkDrawingAttributes**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

