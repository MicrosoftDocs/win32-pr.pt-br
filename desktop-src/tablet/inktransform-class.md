---
description: Representa uma matriz 3x3 que, por sua vez, representa uma transformação afim.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Classe InkTransform (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 4bdc93e2c80f1a7ef4a8eacf1a58288c008e1354cda702e492deb2990e8938d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938656"
---
# <a name="inktransform-class"></a>Classe InkTransform

Representa uma matriz 3x3 que, por sua vez, representa uma transformação afim.

**InkTransform** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **InkTransform** tem esses métodos.



| Método                                                  | Descrição                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Recupera o **InkTransform** como 6 floats.<br/>                                                                      |
| [**Reflexão**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Reflete a transformação nas direções horizontal ou vertical.<br/>                                          |
| [**Definido**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Redefine a transformação para seu estado original.<br/>                                                                      |
| [**Girar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Gira a transformação por um ângulo medido em graus e, opcionalmente, especifica um ponto central para a rotação.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Dimensiona a transformação por fatores X e Y.<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Modifica o **InkTransform** usando 6 floats.<br/>                                                                    |
| [**Quantidade**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Aplica uma distorção com os fatores horizontais e verticais especificados.<br/>                                              |
| [**Traduzir**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Move a transformação pelos componentes horizontal e vertical especificados.<br/>                                         |



 

### <a name="properties"></a>Propriedades

A classe **InkTransform** tem essas propriedades.



| Propriedade                                     | Tipo de acesso           | Descrição                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Dado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Leitura/gravação<br/> | Obtém ou define a versão de automação do struct do XFORM do WIN32.<br/>                            |
| [**eDx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Leitura/gravação<br/> | Obtém ou define o número real que especifica o elemento na terceira linha, primeira coluna.<br/>   |
| [**eDy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Leitura/gravação<br/> | Obtém ou define o número real que especifica o elemento na terceira linha, segunda coluna.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Leitura/gravação<br/> | Obtém ou define o número real que especifica o elemento na primeira linha, primeira coluna.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Leitura/gravação<br/> | Obtém ou define o número real que especifica o elemento na primeira linha, segunda coluna.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Leitura/gravação<br/> | Obtém ou define o número real que especifica o elemento na segunda linha, primeira coluna.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Leitura/gravação<br/> | Obtém ou define o número real que especifica o elemento na segunda linha, segunda coluna.<br/> |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

O objeto armazena apenas seis dos nove números em uma matriz de 3x3 porque todas as matrizes de 3x3 que representam as transformações de afinidade têm a mesma terceira coluna (0, 0, 1). Esse objeto, por sua vez, é usado para descrever as operações de transformação, como mover, distorcer, dimensionar ou girar em um objeto [**InkRenderer**](inkrenderer-class.md) , objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ou coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

> [!Note]  
> O objeto **InkTransform** se correlaciona com a estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) .

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

