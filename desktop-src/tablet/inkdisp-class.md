---
description: Classe InkDisp – representa os traços de tinta coletados em um espaço de tinta.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Classe InkDisp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4214d6b03e5823bd5012017e418066763c8132c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109984"
---
# <a name="inkdisp-class"></a>Classe InkDisp

Representa os traços de tinta coletados em um espaço de tinta.

**InkDisp** tem estes tipos de membros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

A classe **InkDisp** tem esses eventos.



| Evento                                    | Descrição                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Ocorre quando um traço é adicionado ao objeto **InkDisp** .<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Ocorre quando um traço é excluído do objeto **InkDisp** .<br/> |



 

### <a name="interfaces"></a>Interfaces

A classe **InkDisp** define essas interfaces.



| Interface    | Descrição                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | Esse objeto implementa a interface com do **IInkDisp** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **InkDisp** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStrokesAtRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Insere uma coleção Stroke no objeto **InkDisp** no retângulo especificado.<br/>                                                                                                       |
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Indica se o [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) pode ser convertido em um objeto **InkDisp** .<br/>                                                                                       |
| [**Clipe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Remove partes de um traço ou coleção de traços que estão fora de um retângulo.<br/>                                                                                                       |
| [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Copia a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para a área de transferência.<br/>                                                                                                           |
| [**ClipboardCopyWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Copia os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contidos no retângulo conhecido para a área de transferência.<br/>                                                               |
| [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Copia o [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) da área de transferência para o objeto **InkDisp** .<br/>                                                                                               |
| [**Clone**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Cria um objeto **InkDisp** duplicado.<br/>                                                                                                                                                   |
| [**CreateStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Cria um traço a partir de pontos ou dados de pacote.<br/>                                                                                                                                              |
| [**Hipertraços**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Cria uma coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para este objeto **InkDisp** .<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Exclui um traço do objeto **InkDisp** .<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Exclui os traços do objeto **InkDisp** .<br/>                                                                                                                                              |
| [**Método ExtractStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Extrai traços do objeto **InkDisp** e retorna um novo objeto **InkDisp** contendo os traços extraídos.<br/>                                                                       |
| [**Método ExtractWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Recorta ou copia traços de um objeto de **classe InkDisp** existente e os cola em um novo objeto de **classe InkDisp** , usando o retângulo conhecido para determinar quais traços extrair.<br/> |
| [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Recupera a caixa delimitadora de todos os traços no objeto **InkDisp** .<br/>                                                                                                               |
| [**HitTestCircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Recupera a coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está completamente dentro ou interseccionada por um círculo conhecido.<br/>                                                  |
| [**HitTestWithLasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Recupera os traços dentro de uma área de seleção de polilinha.<br/>                                                                                                                                   |
| [**HitTestWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Recupera os traços contidos em um retângulo especificado.<br/>                                                                                                                    |
| [**Carregamento**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Popula um novo objeto **InkDisp** com dados binários conhecidos.<br/>                                                                                                                                |
| [**NearestPoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Recupera o [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dentro do objeto **InkDisp** que é mais próximo de um ponto conhecido, fornecendo, opcionalmente, informações adicionais.<br/>                       |
| [**Salvar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Converte a tinta em um formato especificado e retorna os dados binários.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propriedades

A classe **InkDisp** tem essas propriedades.



| Propriedade                                                                           | Tipo de acesso           | Descrição                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Somente leitura<br/>  | Obtém a coleção [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) a ser persistida com a tinta.<br/>                             |
| [**Bit**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Leitura/gravação<br/> | Obtém ou define o valor que indica se um objeto **InkDisp** foi modificado desde a última vez em que a tinta foi salva.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Somente leitura<br/>  | Obtém a coleção de dados definidos pelo aplicativo.<br/>                                                                             |
| [**Traços**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Somente leitura<br/>  | Obtém a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contida no objeto **InkDisp** .<br/>                             |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

> [!Note]  
> A primeira instanciação desse objeto faz com que o GDI+ seja instanciado também. Um efeito colateral é que, se você estiver usando um único objeto de tinta em um loop e criar e destruí-lo no loop, fará com que o GDI+ seja instanciado repetidamente. Isso pode causar uma degradação do desempenho em seu aplicativo. Para evitar isso, mantenha uma única instância de um objeto de tinta em todos os momentos enquanto seu aplicativo estiver usando a tinta.

 

Um objeto **InkDisp** é um contêiner de dados de traço (ponto). Os dados de traço, ou os pontos coletados pela caneta, são colocados em um objeto **InkDisp** . A propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contém os dados para todos os traços dentro do objeto **InkDisp** .

O objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) e o controle [InkPicture](inkpicture-control-reference.md) coleta pontos do dispositivo de entrada e os coloca em um objeto **InkDisp** . Esses objetos, essencialmente, agem como a origem que distribui a tinta em um ou vários objetos **InkDisp** diferentes, que atuam como contêineres que mantêm a tinta distribuída.

O espaço de tinta é um espaço de coordenadas virtual para o qual as coordenadas do contexto do Tablet são mapeadas. Esse espaço é fixado em um sistema de coordenadas HIMETRIC. Em coordenadas de espaço de tinta, uma mudança de 0 para 1 é igual a 1 unidade de HIMETRIC. Esse mapeamento torna mais fácil relacionar vários objetos **InkDisp** .

O objeto [**InkRenderer**](inkrenderer-class.md) gerencia os mapeamentos entre a tinta e a janela de exibição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Interface IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

