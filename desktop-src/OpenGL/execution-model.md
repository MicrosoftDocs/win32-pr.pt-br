---
title: Modelo de execução
description: Modelo de execução
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modelo de execução
- modelo de execução OpenGL
- OpenGL, modelo de cliente/servidor
- cliente/modelo de servidor OpenGL
- OpenGL, transparente de rede
- framebuffers, modelo de execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7cb7c3c06baa0a56f4c59b14744b73962fced369d56f00cbf887b9ae6d09e2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082456"
---
# <a name="execution-model"></a>Modelo de execução

O modelo para interpretação de comandos OpenGL é cliente/servidor. O código do aplicativo (o cliente) emite comandos, que são interpretados e processados pelo OpenGL (o servidor). O servidor pode ou não operar no mesmo computador que o cliente. Nesse sentido, o OpenGL é transparente de rede. Um servidor pode manter vários contextos OpenGL, cada um dos quais é um estado OpenGL encapsulado. Um cliente pode se conectar a qualquer um desses contextos. O protocolo de rede necessário pode ser implementado aumentando um protocolo já existente (como o do Sistema de Janela X) ou usando um protocolo independente. Nenhum comando OpenGL é fornecido para obter a entrada do usuário.

O sistema de janelas que aloca recursos de framebuffer, por fim, controla os efeitos dos comandos OpenGL no framebuffer. O sistema de janelas:

-   Determina quais partes do framebuffer OpenGL podem acessar a qualquer momento.
-   Comunica-se ao OpenGL como essas partes são estruturadas.

Portanto, não há comandos OpenGL para configurar o framebuffer ou inicializar o OpenGL. A configuração do buffer de quadros é feita fora do OpenGL em conjunto com o sistema de janelas; A inicialização do OpenGL ocorre quando o sistema de janelas aloca uma janela para renderização OpenGL.

 

 




