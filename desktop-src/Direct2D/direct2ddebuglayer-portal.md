---
title: Direct2D Camada de depuração
description: Uma extensão de runtime para Direct2D que oferece mensagens de erro descritivas, detecção de vazamento de objeto, avisos de desempenho e outras responsabilidades para ajudá-lo a criar Direct2D aplicativos.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29cb01c2f8f4f4b14694da94262847ae0def0817a13ffffc48f5c414a8eacda7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044356"
---
# <a name="direct2d-debug-layer"></a>Direct2D Camada de depuração

## <a name="purpose"></a>Finalidade

A Direct2D de depuração, implementada separadamente do Direct2D em sua própria DLL chamada d2d1debug.dll, fornece mensagens de depuração em tempo de design para minimizar a falha do aplicativo de runtime. As mensagens de depuração geralmente resultam de violações de contratos de API, como parâmetros inválidos (podem ser relacionados ao Direct3D), recursos inválidos, violações de threading e outros problemas de desempenho, como usar uma camada quando um clipe seria suficiente.

Para ajudá-lo a decidir quantas informações são rastreadas pela camada de depuração, a camada de depuração oferece três níveis de depuração: informações, aviso e erro. Esses três níveis são interpretados da seguinte maneira:

-   **Erro: Direct2D** envia mensagens de erro graves para a camada de depuração. Por exemplo, a quebra de uma restrição de threading gerará um erro grave.

    Além disso, uma mensagem de erro de nível dispara o ponto de interrupção para ajudá-lo a depurar.

-   **Aviso:** Direct2D envia mensagens de erro e avisos para a camada de depuração para que você possa resolver qualquer uma dessas mensagens.

-   **Informações:** Direct2D envia mensagens de erro, avisos e informações de diagnóstico adicionais para a camada de depuração. Por exemplo, as mensagens de melhoria de desempenho serão enviadas nesse nível de depuração.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Instalando a camada Direct2D de depuração](installing-the-direct2d-debug-layer.md)<br/> | Descreve como instalar a camada de Direct2D depuração.<br/>      |
| [Direct2D Visão geral da camada de depuração](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Depurar mensagens](direct2ddebuglayer-debugmessages.md)<br/>                         | Lista as mensagens de depuração da camada Direct2D de depuração.<br/> |



 

 

 





