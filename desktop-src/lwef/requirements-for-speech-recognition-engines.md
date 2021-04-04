---
title: Requisitos para mecanismos de reconhecimento de fala
description: Requisitos para mecanismos de reconhecimento de fala
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916523"
---
# <a name="requirements-for-speech-recognition-engines"></a>Requisitos para mecanismos de reconhecimento de fala

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Um mecanismo de reconhecimento de fala também deve ser um mecanismo de comando e controle (C&C) totalmente compatível de acordo com o SAPI 4,0. Ele deve dar suporte a várias gramáticas no formato binário descrito na especificação e permitir que essas gramáticas sejam ativadas ou desativadas em tempo real.

Observe que o SAPI 4,0 exige que os mecanismos de reconhecimento de fala ofereçam suporte ao caractere largo, interfaces Unicode. No entanto, no suporte a essas interfaces, o mecanismo não deve depender da conversão de dados Unicode para ANSI, pois o mecanismo pode não funcionar corretamente em alguns sistemas. Por exemplo, um mecanismo japonês que converte Unicode em ANSI pode não funcionar em um sistema em inglês do Microsoft Windows 95.

Além disso, para ser considerado compatível com o Microsoft Agent, o mecanismo deve retornar objetos de resultados após o reconhecimento bem-sucedido de uma frase (por meio de ISRGramNotifySinkW::P hraseFinish). Esses objetos de resultados devem dar suporte a ISRResBasic, conforme a especificação exige. Além disso, eles devem dar suporte a ISRResScore. Embora o Microsoft Agent seja executado com um mecanismo que dá suporte apenas a ISRResBasic, ou mesmo com um mecanismo que não retorna nenhum objeto de resultados, o desempenho geralmente será significativamente mais fraco com esses mecanismos. Muitos aplicativos usam os valores de confiança fornecidos pelo mecanismo para controlar como eles respondem a vários comandos.

 

 




