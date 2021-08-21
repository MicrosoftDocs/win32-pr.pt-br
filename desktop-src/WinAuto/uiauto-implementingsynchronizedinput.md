---
title: Padrão de controle SynchronizedInput
description: Descreve diretrizes e convenções para implementar ISynchronizedInputProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle SynchronizedInput
- Automação da Interface do Usuário, padrão de controle SynchronizedInput
- Automação da Interface do Usuário,ISynchronizedInputProvider
- ISynchronizedInputProvider
- implementando Automação da Interface do Usuário de controle SynchronizedInput
- Padrões de controle SynchronizedInput
- padrões de controle, ISynchronizedInputProvider
- padrões de controle, implementando Automação da Interface do Usuário SynchronizedInput
- padrões de controle, SynchronizedInput
- interfaces,ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91aa4ad93a30be26ebcbc463ade3a27d896d61727508965a86d1ed229b7d79be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114847"
---
# <a name="synchronizedinput-control-pattern"></a>Padrão de controle SynchronizedInput

Descreve diretrizes e convenções para implementar [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), incluindo informações sobre propriedades e métodos. O **padrão de controle SynchronizedInput** permite que a Microsoft Automação da Interface do Usuário aplicativos cliente direcionam a entrada do mouse ou do teclado para um elemento de interface do usuário específico.

Esse padrão de controle normalmente é usado em scripts de teste automatizados para enviar entrada de mouse ou teclado para um elemento de interface do usuário específico e, em seguida, verificar se o elemento recebeu a entrada.

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ISynchronizedInputProvider**](#required-members-for-isynchronizedinputprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle SynchronizedInput,** observe as seguintes diretrizes e convenções:

-   Quando o método [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) é chamado, o provedor Automação da Interface do Usuário deve começar a verificar a entrada do tipo especificado e, em seguida, tomar uma das seguintes ações:
    -   Quando a entrada correspondente é encontrada para o elemento , o provedor deve gerar o [**evento \_ InputReachedTargetEventId da UIA.**](uiauto-event-ids.md)
    -   Quando a entrada correspondente é encontrada, mas ela atingiu um elemento diferente, o provedor deve aumentar o [**evento \_ InputReachedOtherElementEventId da UIA.**](uiauto-event-ids.md)
    -   Quando uma entrada incompatibilidade é encontrada, o provedor deve descartar a entrada e agarr o [**evento \_ InputDiscardedEventId da UIA.**](uiauto-event-ids.md)
-   O Automação da Interface do Usuário provedor deve descartar a entrada se for para um elemento diferente do elemento atual.
-   Quando o elemento recebe a entrada ou quando o método [**ISynchronizedInputProvider::Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) é chamado, o provedor para de verificar a entrada e continua normalmente.
-   Se [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) for chamado quando o provedor já estiver escutando a entrada, o provedor deverá retornar [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).

## <a name="required-members-for-isynchronizedinputprovider"></a>Membros necessários para **ISynchronizedInputProvider**

As propriedades, métodos e eventos a seguir são necessários para implementar a interface [**ISynchronizedInputProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider)



| Membros necessários                                                                         | Tipo de membro | Observações |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**Startlistening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Método      | Nenhum  |
| [**Cancelar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Método      | Nenhum  |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) | Evento       | Nenhum  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




