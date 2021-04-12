---
title: Manipulações
description: Esta seção explica a manipulação de objetos para o Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch, manipulações
- manipulações, sobre
- manipulações, diferenças de gesto
- gestos, diferenças de manipulação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291843"
---
# <a name="manipulations"></a>Manipulações

Esta seção explica a manipulação de objetos para o Windows Touch.

## <a name="manipulation-overview"></a>Visão geral da manipulação

Uma maneira conveniente de pensar sobre as manipulações é considerar um superconjunto de gestos. O que você pode fazer com gestos, você pode fazer com mais flexibilidade e com precisão mais fina usando manipulações. A diferença entre as manipulações e os gestos é melhor demonstrada com um exemplo simples. Você pode expandir um objeto e, ao mesmo tempo, traduzi-lo usando manipulações; com gestos, você pode fazer apenas um de cada vez. Essa capacidade de manipular um objeto em tempo real torna os aplicativos mais intuitivos para os usuários, permitindo uma experiência mais realista.

As APIs de manipulação são usadas para simplificar as operações de transformação em objetos para aplicativos habilitados para toque. As manipulações são executadas no Windows 7 por meio do objeto COM manipulações. Usando manipulações, os desenvolvedores podem dar suporte mais facilmente a inércia (física do objeto) e podem facilmente realizar transformações em objetos de forma consistente com outros aplicativos. As seções a seguir explicam várias maneiras que você pode executar manipulações.



| Seção                                                                                            | Descrição                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Adicionando suporte à manipulação a código não gerenciado](adding-manipulation-support-in-unmanaged-code.md) | Explica como implementar um coletor de eventos para a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) e adicionar manipuladores de eventos ao seu código. |
| [Manipulações avançadas](advanced-manipulations.md)                                               | Explica como executar manipulações complexas.                                                                                                       |
| [Rotação de dedo único](single-finger-rotation.md)                                               | Explica como girar um objeto usando um ponto dinâmico e o processador de manipulação.                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulações e inércia](manipulation-and-inertia.md)
</dt> </dl>

 

 




