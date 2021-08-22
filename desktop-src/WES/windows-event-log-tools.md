---
title: Windows Ferramentas de log de eventos
description: Windows O log de eventos fornece as ferramentas a seguir que você usa para criar seu provedor.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7a0aef85e85e096381b65d41458f1cb955ba9701452498d21c45ff25cb3058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587253"
---
# <a name="windows-event-log-tools"></a>Windows Ferramentas de log de eventos

Windows O log de eventos fornece as ferramentas a seguir que você usa para criar seu provedor.



| Ferramenta                                                           | Descrição                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md)  | Um utilitário de linha de comando usado para compilar manifestos de instrumentação e arquivos de texto de mensagem. |
| WevtUtil.exe                                                   | Um utilitário de linha de comando usado principalmente para registrar seu provedor no computador. Você também pode usá-lo para obter informações de metadados sobre o provedor, seus eventos e os canais para os quais ele registra eventos e para consultar eventos de um canal ou arquivo de log. A ferramenta de WevtUtil.exe está incluída em% windir% \\ System32. Para obter informações de uso, digite "wevtutil/?" em um prompt de comando.<br/> Esse comando é limitado aos membros do grupo Administradores e deve ser executado com privilégios elevados.|
