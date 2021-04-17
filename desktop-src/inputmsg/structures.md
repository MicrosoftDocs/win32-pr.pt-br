---
title: Estruturas (mensagens de entrada do ponteiro e notificações)
description: Os tópicos nesta seção fornecem as especificações de referência para mensagens de entrada de ponteiro e estruturas de notificações.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105798314"
---
# <a name="pointer-input-messages-and-notifications-structures"></a>Estruturas de mensagens e notificações de entrada de ponteiro

Os tópicos nesta seção fornecem as especificações de referência para [mensagens de entrada de ponteiro e](messages-and-notifications-portal.md) estruturas de notificações.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INPUT_TRANSFORM**](/previous-versions/windows/desktop/api)<br/>                           | Define a matriz que representa uma transformação em um consumidor de mensagem. Essa matriz pode ser usada para transformar dados de entrada de ponteiro de coordenadas de cliente em coordenadas de tela, enquanto o inverso pode ser usado para transformar dados de entrada de ponteiro de coordenadas de tela em coordenadas de cliente. <br/>                                                                 |
| [**POINTER_INFO**](/previous-versions/windows/desktop/api)<br/>                          | Contém informações básicas de ponteiros comuns a todos os tipos de ponteiro. Os aplicativos podem recuperar essas informações usando as funções [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) e [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) . <br/> |
| [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)<br/>                 | Define informações básicas sobre a caneta comum a todos os tipos de ponteiro. <br/>                                                                                                                                                                                                                                                                                                |
| [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)<br/>             | Define informações de toque básico comuns a todos os tipos de ponteiro.<br/>                                                                                                                                                                                                                                                                                               |
| [**TOUCHPREDICTIONPARAMETERS**](/previous-versions/windows/desktop/api)<br/> | Contém detalhes de entrada de hardware que podem ser usados para prever destinos de toque e ajudar a compensar a latência de hardware ao processar a entrada de toque e de gesto que contém dados de distância e velocidade.<br/>                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de mensagem de entrada do ponteiro](wmpointer-reference.md)
</dt> </dl>

 

 





