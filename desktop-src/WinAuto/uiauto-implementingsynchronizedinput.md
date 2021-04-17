---
title: Padrão de controle SynchronizedInput
description: Descreve as diretrizes e convenções para implementar o ISynchronizedInputProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automação da interface do usuário, implementando o padrão de controle SynchronizedInput
- Automação da interface do usuário, padrão de controle SynchronizedInput
- Automação da interface do usuário, ISynchronizedInputProvider
- ISynchronizedInputProvider
- Implementando padrões de controle SynchronizedInput de automação da interface do usuário
- Padrões de controle SynchronizedInput
- padrões de controle, ISynchronizedInputProvider
- padrões de controle, implementando a automação da interface do usuário SynchronizedInput
- padrões de controle, SynchronizedInput
- interfaces, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798385"
---
# <a name="synchronizedinput-control-pattern"></a>Padrão de controle SynchronizedInput

Descreve as diretrizes e convenções para implementar o [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **SynchronizedInput** permite que os aplicativos cliente do Microsoft UI Automation direcionem a entrada do mouse ou do teclado para um elemento específico da interface do usuário.

Esse padrão de controle normalmente é usado em scripts de teste automatizados para enviar entrada de mouse ou de teclado para um elemento de interface de usuário específico e, em seguida, verificar se o elemento recebeu a entrada.

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ISynchronizedInputProvider**](#required-members-for-isynchronizedinputprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **SynchronizedInput** , observe as seguintes diretrizes e convenções:

-   Quando o método [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) é chamado, o provedor de automação da interface do usuário deve iniciar a verificação da entrada do tipo especificado e, em seguida, executar uma das seguintes ações:
    -   Quando a entrada correspondente é encontrada para o elemento, o provedor deve gerar o evento [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) .
    -   Quando a entrada correspondente é encontrada, mas ela atingiu um elemento diferente, o provedor deve gerar o evento [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md) .
    -   Quando uma entrada incompatível é encontrada, o provedor deve descartar a entrada e gerar o evento [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md) .
-   O provedor de automação de interface do usuário deve descartar a entrada se for para um elemento que não seja o elemento atual.
-   Quando o elemento recebe a entrada, ou quando o método [**ISynchronizedInputProvider:: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) é chamado, o provedor para de verificar a entrada e continua normalmente.
-   Se [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) for chamado quando o provedor já estiver ouvindo a entrada, o provedor deverá retornar [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).

## <a name="required-members-for-isynchronizedinputprovider"></a>Membros necessários para **ISynchronizedInputProvider**

As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) .



| Membros necessários                                                                         | Tipo de membro | Observações |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Método      | Nenhum  |
| [**Cancelar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Método      | Nenhum  |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) | Evento       | Nenhum  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




