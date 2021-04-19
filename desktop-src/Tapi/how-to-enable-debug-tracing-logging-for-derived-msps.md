---
description: O procedimento a seguir descreve como habilitar o rastreamento de depuração e o registro em log.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Como habilitar o rastreamento/log de depuração para MSPs derivadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3883d12c050f245cc58595c9a52586c4f01ba27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767762"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Como habilitar o rastreamento/log de depuração para MSPs derivadas

Primeiro, certifique-se de que a implementação do MSP derivado seguiu as diretrizes na seção anterior com relação ao rastreamento de depuração (definindo o símbolo de pré-processador MSPLOG, registrando para rastreamento durante DllMain e usando a macro de LOG para rastreamento). Descubra o nome que o MSP usa ao se registrar para o rastreamento (isso normalmente deve ser o nome da DLL; ele é mencionado abaixo como " &lt; nome da dll &gt; "). Para habilitar o rastreamento, use um editor de registro ("Regedit.exe" ou "Regedt32.exe") para localizar a chave "HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Tracing" e faça o seguinte. Observe que todos os valores mencionados abaixo, exceto o valor de EnableDebuggerTracing, devem ser criados automaticamente após a execução do MSP pela primeira vez.

-   Para habilitar o rastreamento para os depuradores de modo kernel e usuário, defina o valor **DWORD** <dll name> \\ EnableDebuggerTracing como 1. Opcionalmente, use o  valor DWORD <dll name> \\ ConsoleTracing Mask para habilitar ou desabilitar vários níveis de saída de rastreamento (o padrão é 0xFFFF0000, que habilita todos os níveis de rastreamento).
-   Para habilitar o rastreamento em um arquivo, defina o valor **DWORD** <dll name> \\ EnableFileTracing como 1. Opcionalmente, use o valor da cadeia de caracteres <dll name> \\ fileDirectory para ajustar o local do arquivo de log. Opcionalmente, use o  valor DWORD <dll name> \\ FileTracingMask para habilitar ou desabilitar vários níveis de saída de rastreamento (o padrão é 0xFFFF0000, que habilita todos os níveis de rastreamento).
-   Para habilitar o rastreamento para uma janela de console separada, separada por DLL, defina o valor **DWORD** EnableConsoleTracing como 1 e também defina o valor **DWORD** <dll name> \\ EnableConsoleTracing como 1. Opcionalmente, use o  valor DWORD <dll name> \\ ConsoleTracing Mask para habilitar ou desabilitar vários níveis de saída de rastreamento (o padrão é 0xFFFF0000, que habilita todos os níveis de rastreamento).

 

 



