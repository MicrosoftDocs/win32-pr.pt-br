---
title: Windows Tarefas de animação
description: Os tópicos contidos nesta seção descrevem as tarefas básicas necessárias para aplicativos que usam Windows Animation Manager.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Windows Animação Windows animação , tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8f5116a6e36697e649ad81bfbad883c57aee50440c3ba80734419ce2fb372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058144"
---
# <a name="windows-animation-tasks"></a>Windows Tarefas de animação

Os tópicos contidos nesta seção descrevem as tarefas básicas necessárias para aplicativos que usam Windows Animation Manager.

Essas tarefas, na ordem, incluem:

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                | Descrição                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criar os objetos de animação principais](adding-animation-to-an-application.md)<br/>               | Para usar Windows Animação em seu aplicativo, a primeira etapa é criar um pequeno conjunto de objetos de animação principais.<br/>                                                                                                                                                                           |
| [Criar variáveis de animação](create-animation-variables.md)<br/>                              | Um aplicativo deve criar uma variável de animação para cada característica visual que deve ser animada usando Windows Animação.<br/>                                                                                                                                                            |
| [Atualizar o Gerenciador de Animação e desenhar quadros](introducing-windows-animation-manager.md)<br/> | Sempre que um aplicativo agenda um storyboard, o aplicativo deve fornecer a hora atual para o gerenciador de animação. A hora atual também é necessária ao direcionar o gerenciador de animação para atualizar seu estado e definir todas as variáveis de animação para os valores interpolados apropriados.<br/> |
| [Ler os valores de variável de animação](updating---application-driven-animation.md)<br/>         | Cada vez que seu aplicativo pinta, ele deve ler os valores atuais das variáveis de animação que representam as características visuais a serem animadas.<br/>                                                                                                                                  |
| [Criar um storyboard e adicionar transições](updating---timer-driven-animation.md)<br/>          | Para criar uma animação, um aplicativo deve construir um storyboard.<br/>                                                                                                                                                                                                                        |
| [Agendar um storyboard](scheduling-a-storyboard.md)<br/>                                      | Depois que um storyboard é criado, ele é agendado pelo gerenciador de animação.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Visão geral da animação](scenic-animation-api-overview.md)
</dt> <dt>

[Windows Referência de animação](windows-animation-reference.md)
</dt> <dt>

[Windows Exemplos de animação](windows-animation-samples.md)
</dt> </dl>

 

 





