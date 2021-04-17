---
title: Tarefas de animação do Windows
description: Os tópicos contidos nesta seção descrevem as tarefas básicas necessárias para os aplicativos que usam o Gerenciador de animação do Windows.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Animação do Windows animações do Windows, tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105794579"
---
# <a name="windows-animation-tasks"></a>Tarefas de animação do Windows

Os tópicos contidos nesta seção descrevem as tarefas básicas necessárias para os aplicativos que usam o Gerenciador de animação do Windows.

Essas tarefas, em ordem, incluem:

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                | Descrição                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criar os objetos de animação principais](adding-animation-to-an-application.md)<br/>               | Para usar a animação do Windows em seu aplicativo, a primeira etapa é criar um pequeno conjunto de objetos de animação principais.<br/>                                                                                                                                                                           |
| [Criar variáveis de animação](create-animation-variables.md)<br/>                              | Um aplicativo deve criar uma variável de animação para cada característica visual que seja animada usando a animação do Windows.<br/>                                                                                                                                                            |
| [Atualizar o Gerenciador de animação e desenhar quadros](introducing-windows-animation-manager.md)<br/> | Cada vez que um aplicativo agenda um storyboard, o aplicativo deve fornecer a hora atual ao Gerenciador de animação. A hora atual também é necessária ao direcionar o Gerenciador de animação para atualizar seu estado e definir todas as variáveis de animação para os valores interpolados apropriados.<br/> |
| [Ler os valores da variável de animação](updating---application-driven-animation.md)<br/>         | Cada vez que seu aplicativo pinta, ele deve ler os valores atuais das variáveis de animação que representam as características visuais a serem animadas.<br/>                                                                                                                                  |
| [Criar um storyboard e adicionar transições](updating---timer-driven-animation.md)<br/>          | Para criar uma animação, um aplicativo deve construir um Storyboard.<br/>                                                                                                                                                                                                                        |
| [Agendar um storyboard](scheduling-a-storyboard.md)<br/>                                      | Depois que um Storyboard é criado, ele é agendado pelo Gerenciador de animação.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da animação do Windows](scenic-animation-api-overview.md)
</dt> <dt>

[Referência de animação do Windows](windows-animation-reference.md)
</dt> <dt>

[Exemplos de animação do Windows](windows-animation-samples.md)
</dt> </dl>

 

 





