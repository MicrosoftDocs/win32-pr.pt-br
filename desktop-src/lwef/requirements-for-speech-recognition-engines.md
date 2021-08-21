---
title: Requisitos para mecanismos de reconhecimento de fala
description: Requisitos para mecanismos de reconhecimento de fala
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1315d395e3053d5f6f71fd7f8ff17cb815bea26fc4875878da74dd77113d5e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975746"
---
# <a name="requirements-for-speech-recognition-engines"></a>Requisitos para mecanismos de reconhecimento de fala

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Um mecanismo de reconhecimento de fala também deve ser um mecanismo de comando e controle (C&C) totalmente compatível de acordo com o SAPI 4,0. Ele deve dar suporte a várias gramáticas no formato binário descrito na especificação e permitir que essas gramáticas sejam ativadas ou desativadas em tempo real.

Observe que o SAPI 4,0 exige que os mecanismos de reconhecimento de fala ofereçam suporte ao caractere largo, interfaces Unicode. No entanto, no suporte a essas interfaces, o mecanismo não deve depender da conversão de dados Unicode para ANSI, pois o mecanismo pode não funcionar corretamente em alguns sistemas. por exemplo, um mecanismo japonês que converte Unicode em ANSI pode não funcionar em um sistema Microsoft Windows 95 em inglês.

Além disso, para ser considerado compatível com o Microsoft Agent, o mecanismo deve retornar objetos de resultados após o reconhecimento bem-sucedido de uma frase (por meio de ISRGramNotifySinkW::P hraseFinish). Esses objetos de resultados devem dar suporte a ISRResBasic, conforme a especificação exige. Além disso, eles devem dar suporte a ISRResScore. Embora o Microsoft Agent seja executado com um mecanismo que dá suporte apenas a ISRResBasic, ou mesmo com um mecanismo que não retorna nenhum objeto de resultados, o desempenho geralmente será significativamente mais fraco com esses mecanismos. Muitos aplicativos usam os valores de confiança fornecidos pelo mecanismo para controlar como eles respondem a vários comandos.

 

 




