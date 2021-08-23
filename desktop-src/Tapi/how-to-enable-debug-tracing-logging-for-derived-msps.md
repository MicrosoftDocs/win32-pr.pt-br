---
description: O procedimento a seguir descreve como habilitar o rastreamento e o registro em log de depuração.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Como habilitar o rastreamento/registro em log de depuração para MSPs derivados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565b66055a43edbe7556e640f8e368aab84fab206bced431c22578a7e21a94ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140519"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Como habilitar o rastreamento/registro em log de depuração para MSPs derivados

Primeiro, certifique-se de que a implementação do MSP derivado seguiu as diretrizes na seção anterior em relação ao rastreamento de depuração (definindo o símbolo de pré-processador MSPLOG, registrando-se para rastreamento durante DllMain e usando a macro LOG para rastreamento). Descubra qual nome o MSP usa ao se registrar para rastreamento (esse geralmente deve ser o nome da DLL; ele é conhecido abaixo como " &lt; dll name &gt; "). Para habilitar o rastreamento, use um editor do Registro ("Regedit.exe" ou "Regedt32.exe") para localizar a chave "HKEY LOCAL MACHINE Software Microsoft Tracing" e \_ faça o \_ \\ \\ \\ seguinte. Observe que todos os valores mencionados abaixo, exceto o valor EnableDebuggerTracing, devem ser criados automaticamente depois de executar o MSP pela primeira vez.

-   Para habilitar o rastreamento para depurador de modo de usuário e kernel, de definido o valor **DWORD** <dll name> \\ EnableDebuggerTracing como 1. Opcionalmente, use o valor **DWORD** ConsoleTracing Mask para habilitar ou desabilitar vários níveis de saída de rastreamento (o padrão é 0xFFFF0000, que habilita todos os <dll name> \\ níveis de rastreamento).
-   Para habilitar o rastreamento para um arquivo, de definido o **valor DWORD** <dll name> \\ EnableFileTracing como 1. Opcionalmente, use o valor de cadeia de <dll name> \\ caracteres FileDirectory para ajustar o local do arquivo de log. Opcionalmente, use o valor **DWORD** <dll name> FileTracingMask para habilitar ou desabilitar vários níveis de saída de rastreamento (o padrão é 0xFFFF0000, que habilita todos os níveis \\ de rastreamento).
-   Para habilitar o rastreamento para uma janela de console separada, separada por DLL, de definir o valor **DWORD** EnableConsoleTracing como 1 e também definir o valor **DWORD** <dll name> \\ EnableConsoleTracing como 1. Opcionalmente, use o valor **DWORD** ConsoleTracing Mask para habilitar ou desabilitar vários níveis de saída de rastreamento (o padrão é 0xFFFF0000, que habilita todos os <dll name> \\ níveis de rastreamento).

 

 



