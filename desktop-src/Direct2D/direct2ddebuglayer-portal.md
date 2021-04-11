---
title: Camada de depuração Direct2D
description: Uma extensão de tempo de execução para Direct2D que oferece mensagens de erro descritivas, detecção de vazamento de objeto, avisos de desempenho e outras indicações para ajudá-lo a criar aplicativos Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363737"
---
# <a name="direct2d-debug-layer"></a>Camada de depuração Direct2D

## <a name="purpose"></a>Finalidade

A camada de depuração Direct2D, implementada separadamente de Direct2D em sua própria DLL chamada d2d1debug.dll, fornece mensagens de depuração de tempo de design para você minimizar a falha do aplicativo em tempo de execução. As mensagens de depuração geralmente resultam de violações de contratos de API, como parâmetros inválidos (podem ser relacionados a Direct3D), recursos inválidos, violações de threading e outros problemas de desempenho, como usar uma camada quando um clipe seria suficiente.

Para ajudá-lo a decidir a quantidade de informações rastreadas pela camada de depuração, a camada de depuração oferece três níveis de depuração: informações, aviso e erro. Esses três níveis são interpretados da seguinte maneira:

-   **Erro:** Direct2D envia mensagens de erro graves para a camada de depuração. Por exemplo, interromper uma restrição de Threading irá gerar um erro grave.

    Além disso, uma mensagem de erro de nível dispara o ponto de interrupção para ajudá-lo a depurar.

-   **AVISO:** O Direct2D envia mensagens de erro e avisos para a camada de depuração para que você possa endereçar qualquer uma dessas mensagens.

-   **Informações:** O Direct2D envia mensagens de erro, avisos e informações adicionais de diagnóstico para a camada de depuração. Por exemplo, as mensagens de melhoria de desempenho serão enviadas neste nível de depuração.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Instalando a camada de depuração Direct2D](installing-the-direct2d-debug-layer.md)<br/> | Descreve como instalar a camada de depuração Direct2D.<br/>      |
| [Visão geral da camada de depuração Direct2D](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Mensagens de depuração](direct2ddebuglayer-debugmessages.md)<br/>                         | Lista as mensagens de depuração da camada de depuração Direct2D.<br/> |



 

 

 





