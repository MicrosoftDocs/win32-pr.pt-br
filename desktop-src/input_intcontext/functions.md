---
title: Funções de contexto de interação
description: Os tópicos nesta seção fornecem as especificações de referência para funções de contexto de interação.
ms.assetid: 0F34F181-D92C-4B08-9F1D-62379D4A2B15
keywords:
- interação do usuário
- input
- ponteiro
- touch
- mouse
- caneta
- caneta
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 7f57bf6ac2b5d9bc7f17a43cd84a6e8eb7d828a4
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/07/2020
ms.locfileid: "105780744"
---
# <a name="interaction-context-functions"></a>Funções de contexto de interação

Os tópicos nesta seção fornecem as especificações de referência para funções de [contexto de interação](interaction-context-portal.md) .

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|---|---|
| [**AddPointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Inclua o ponteiro especificado no conjunto de ponteiros processados pelo objeto de [contexto de interação](interaction-context-portal.md) . <br/> |
| [**BufferPointerPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Adiciona o histórico de um único ponteiro de entrada para o buffer do objeto de [contexto de interação](interaction-context-portal.md) .<br/> |
| [**CreateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Cria e inicializa um objeto de [contexto de interação](interaction-context-portal.md) .<br/> |
| [**DestroyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Destrói o objeto de [contexto de interação](interaction-context-portal.md) especificado.<br/> |
| [**GetCrossSlideParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Obtém o comportamento de interação entre slides. <br/> |
| [**GetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Obtém o comportamento inércia de uma manipulação (tradução, rotação, dimensionamento). <br/> |
| [**GetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Obtém o estado da configuração de interação para o objeto de [contexto de interação](interaction-context-portal.md) .<br/> |
| [**GetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Obtém o estado da roda do mouse para o objeto de [contexto de interação](interaction-context-portal.md) . <br/> |
| [**GetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Obtém Propriedades do objeto de [contexto de interação](interaction-context-portal.md) .<br/> |
| [**GetStateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Obtém o estado de [contexto de interação](interaction-context-portal.md) atual e a hora em que o contexto retornará ao estado ocioso. <br/> |
| [**ProcessBufferedPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Processar pacotes em buffer no final de um quadro de entrada do ponteiro.<br/> |
| [**ProcessInertiaInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Envia a entrada do temporizador para o objeto de [contexto de interação](interaction-context-portal.md) para o processamento de inércia.<br/> |
| [**ProcessPointerFramesInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Processa um conjunto de quadros de entrada do ponteiro.<br/> |
| [**RegisterOutputCallbackInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Registra um retorno de chamada para receber eventos de interação de um objeto de [contexto de interação](interaction-context-portal.md) .<br/> |
| [**RemovePointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Remove o ponteiro especificado do conjunto de ponteiros processados pelo objeto de [contexto de interação](interaction-context-portal.md) . <br/> |
| [**ResetInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Redefine o [**estado de interação**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state), as definições de configuração de interação e todos os parâmetros para o estado inicial. As interações atuais são canceladas sem notificações. <br/> O [contexto de interação](interaction-context-portal.md) deve ser reconfigurado antes do próximo uso.<br/> |
| [**SetCrossSlideParametersInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Configura a interação entre slides. <br/> |
| [**SetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Configura o comportamento inércia de uma manipulação (conversão, rotação, dimensionamento) depois que o contato é levantado. <br/> | [**SetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Configura o objeto de [contexto de interação](interaction-context-portal.md) para processar as manipulações especificadas.<br/> |
| [**SetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Define os valores de parâmetro para a entrada da roda do mouse. <br/> |
| [**SetPivotInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Define o ponto central e o raio dinâmico do ponto central, para uma manipulação de rotação usando um único ponteiro de entrada. <br/> |
| [**SetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Define propriedades de objeto de [contexto de interação](interaction-context-portal.md) .<br/> |
| [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Define o [**estado de interação**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) para \_ estado de interação \_ ocioso e deixa todos os parâmetros e definições de configuração de interação intactos. As interações atuais são canceladas e notificações enviadas conforme necessário.<br/> O [contexto de interação](interaction-context-portal.md) não precisa ser reconfigurado antes do próximo uso.<br/> |

## <a name="related-topics"></a>Tópicos relacionados

[Referência de contexto de interação](interaction-context-reference.md)
