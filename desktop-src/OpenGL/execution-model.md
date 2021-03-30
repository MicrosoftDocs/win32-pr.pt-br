---
title: Modelo de execução
description: Modelo de execução
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modelo de execução
- modelo de execução OpenGL
- OpenGL, modelo de cliente/servidor
- modelo de cliente/servidor OpenGL
- OpenGL, rede transparente
- framebuffers, modelo de execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916533"
---
# <a name="execution-model"></a>Modelo de execução

O modelo de interpretação de comandos OpenGL é cliente/servidor. O código do aplicativo (o cliente) emite comandos, que são interpretados e processados pelo OpenGL (o servidor). O servidor pode ou não operar no mesmo computador que o cliente. Nesse sentido, o OpenGL é transparente para a rede. Um servidor pode manter vários contextos OpenGL, cada um dos quais é um estado de OpenGL encapsulado. Um cliente pode se conectar a qualquer um desses contextos. O protocolo de rede necessário pode ser implementado aumentando um protocolo já existente (como o do sistema X Window) ou usando um protocolo independente. Nenhum comando OpenGL é fornecido para obter a entrada do usuário.

O sistema de janelas que aloca recursos framebuffer, por fim, controla os efeitos dos comandos OpenGL no framebuffer. O sistema de janelas:

-   Determina quais partes do framebuffer OpenGL podem acessar em um determinado momento.
-   Comunica-se com OpenGL como essas partes são estruturadas.

Portanto, não há comandos OpenGL para configurar o framebuffer ou inicializar OpenGL. A configuração do buffer de quadro é feita fora do OpenGL em conjunto com o sistema de janelas; A inicialização do OpenGL ocorre quando o sistema de janelas aloca uma janela para a renderização OpenGL.

 

 




