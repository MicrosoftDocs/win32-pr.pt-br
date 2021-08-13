---
title: Interfaces de transição
description: Esta seção contém as especificações de referência para as interfaces Windows Animation Manager que suportam transições.
ms.assetid: 581C853D-F213-4227-AC61-4ED2E5D4EF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5791de6e2ca148e42ef836c8bb9be2d9dc96304df00a856b1bc036e05fca3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418596"
---
# <a name="transition-interfaces"></a>Interfaces de transição

Esta seção contém as especificações de referência para as interfaces Windows Animation Manager que suportam transições.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                     | Descrição                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator)<br/>                                   | Define métodos para criar um interpolador personalizado.<br/>                                                                                                                                                                                                             |
| [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2)<br/>                                 | Estende a interface [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) que define métodos para criar um interpolador personalizado. [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2) dá suporte à interpolação em uma determinada dimensão. <br/>        |
| [**IUIAnimationPrimitiveInterpolation**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprimitiveinterpolation)<br/>               | Define um método que permite que um interpolador personalizado forneça informações de transição, na forma de uma curva polinomial cúbica, para o gerenciador de animação.<br/>                                                                                                        |
| [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition)<br/>                                       | Define uma transição, que determina como uma variável de animação muda ao longo do tempo.<br/>                                                                                                                                                                             |
| [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)<br/>                                     | Estende a interface [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition) que define uma transição. Uma [**transição IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2) determina como uma variável de animação muda ao longo do tempo em uma determinada dimensão.<br/> |
| [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)<br/>                         | Define um método para criar transições de interpoladores personalizados.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionFactory2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory2)<br/>                       | Define um método para criar transições de interpoladores personalizados.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)<br/>                         | Define uma biblioteca de transições padrão. <br/>                                                                                                                                                                                                                     |
| [**IUIAnimationTransitionLibrary2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary2)<br/>                       | Define uma biblioteca de transições padrão para uma dimensão especificada.<br/>                                                                                                                                                                                            |
| [**IUIAnimationVariable**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable)<br/>                                           | Define uma variável de animação, que representa um elemento visual que pode ser animado.<br/>                                                                                                                                                                          |
| [**IUIAnimationVariable2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable2)<br/>                                         | Define uma variável de animação, que representa um elemento visual que pode ser animado em várias dimensões.<br/>                                                                                                                                                   |
| [**IUIAnimationVariableChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler)<br/>                 | Define um método para manipular eventos relacionados a atualizações de variáveis de animação.<br/>                                                                                                                                                                                     |
| [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2)<br/>               | Define um método para manipular eventos de atualização de variável de animação. [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2) lida com eventos que ocorrem em uma dimensão especificada.<br/>                                                            |
| [**IUIAnimationVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler)<br/>   | Define um método para manipular eventos de atualização de variável de animação.<br/>                                                                                                                                                                                                 |
| [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2)<br/> | Define um método para manipular eventos de atualização de variável de animação. [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2) lida com eventos que ocorrem em uma dimensão especificada.<br/>                                              |
| [**IUIAnimationVariableCurveChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablecurvechangehandler2)<br/>     | Define um método para manipular eventos de atualização de curva de animação. <br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces](windows-animation-reference.md)
</dt> </dl>

 

 





