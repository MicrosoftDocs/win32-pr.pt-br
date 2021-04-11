---
description: Representa os atributos aplicados à tinta quando ele é desenhado.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Classe InkDrawingAttributes (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297230"
---
# <a name="inkdrawingattributes-class"></a>Classe InkDrawingAttributes

Representa os atributos aplicados à tinta quando ele é desenhado.

**InkDrawingAttributes** tem estes tipos de membros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="interfaces"></a>Interfaces

A classe **InkDrawingAttributes** define essas interfaces.



| Interface                 | Descrição                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkDrawingAttributes** | Esse objeto implementa a interface com do **IInkDrawingAttributes** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **InkDrawingAttributes** tem esses métodos.



| Método                         | Descrição                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**8i**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | Cria um objeto [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes** ou [**InkRecognizerContext**](inkrecognizercontext-class.md) duplicado.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **InkDrawingAttributes** tem essas propriedades.



| Propriedade                                                                           | Tipo de acesso           | Descrição                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Suavizado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | Leitura/gravação<br/> | Obtém ou define o valor que especifica se as cores de primeiro plano e de plano de fundo ao longo da borda da tinta são mescladas para aumentar a suavidade de um traço de tinta.<br/> |
| [**Cor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | Leitura/gravação<br/> | Obtém ou define a cor da tinta desenhada com esse objeto **InkDrawingAttributes** .<br/>                                                                                    |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Somente leitura<br/>  | Obtém a coleção de dados definidos pelo aplicativo que são armazenados no objeto **InkDrawingAttributes** .<br/>                                                                |
| [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | Leitura/gravação<br/> | Obtém ou define o valor que especifica se a tinta é renderizada como uma série de curvas, em vez de linhas entre pontos de exemplo de caneta.<br/>                                    |
| [**Altura**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | Leitura/gravação<br/> | Obtém ou define a altura da caneta ao desenhar tinta com este objeto **InkDrawingAttributes** .<br/>                                                                        |
| [**IgnorePressure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | Leitura/gravação<br/> | Obtém ou define o valor que especifica se a tinta desenhada se torna automaticamente mais larga com uma pressão maior da dica de caneta na superfície do Tablet.<br/>                     |
| [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | Leitura/gravação<br/> | Obtém ou define a dica de caneta a ser usada (bola ou retângulo) ao desenhar tinta com este objeto **InkDrawingAttributes** .<br/>                                                       |
| [**RasterOperation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | Leitura/gravação<br/> | Obtém ou define como a cor da caneta interage com as cores de plano de fundo existentes na exibição quando a tinta é desenhada.<br/>                                                    |
| [**Transparência**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | Leitura/gravação<br/> | Obtém ou define o valor de transparência da tinta desenhada. Os valores variam de zero (totalmente opaco) a 255 (totalmente transparente).<br/>                                               |
| [**Largura**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | Leitura/gravação<br/> | Obtém ou define a largura da caneta ao desenhar tinta com este objeto **InkDrawingAttributes** .<br/>                                                                         |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

Esses atributos de desenho podem ser associados a um traço ou cursor e especificar configurações como cor, largura e transparência.

Para especificar os atributos de desenho de um traço, use a propriedade [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) do objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . Para especificar os atributos de desenho de todos os traços dentro de uma coleção de traços, chame o método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

Cada objeto [**InkCollector**](inkcollector-class.md) , objeto [**InkOverlay**](inkoverlay-class.md) e controle [InkPicture](inkpicture-control-reference.md) pode especificar um conjunto diferente de atributos de desenho para o mesmo cursor. Use a propriedade [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) para obter ou definir os atributos de desenho de um cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedade DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**Propriedade DrawingAttributes**
</dt> <dt>

**Propriedade DrawingAttributes**
</dt> <dt>

[**Propriedade DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**Propriedade DefaultDrawingAttributes**
</dt> <dt>

**Propriedade DefaultDrawingAttributes**
</dt> <dt>

[**Método ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

