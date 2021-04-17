---
title: Ferramentas de log de eventos do Windows
description: O log de eventos do Windows fornece as ferramentas a seguir que você usa para criar seu provedor.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104365792"
---
# <a name="windows-event-log-tools"></a>Ferramentas de log de eventos do Windows

O log de eventos do Windows fornece as ferramentas a seguir que você usa para criar seu provedor.



| Ferramenta                                                           | Descrição                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md)  | Um utilitário de linha de comando usado para compilar manifestos de instrumentação e arquivos de texto de mensagem. |
| WevtUtil.exe                                                   | Um utilitário de linha de comando usado principalmente para registrar seu provedor no computador. Você também pode usá-lo para obter informações de metadados sobre o provedor, seus eventos e os canais para os quais ele registra eventos e para consultar eventos de um canal ou arquivo de log. A ferramenta de WevtUtil.exe está incluída em% windir% \\ System32. Para obter informações de uso, digite "wevtutil/?" em um prompt de comando.<br/> Esse comando é limitado aos membros do grupo Administradores e deve ser executado com privilégios elevados.|
