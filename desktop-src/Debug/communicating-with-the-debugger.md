---
description: A função OutputDebugString envia uma cadeia de caracteres do processo que está sendo depurado para o depurador, gerando um evento de depuração de evento de cadeia de depuração de saída \_ \_ \_ . Um processo pode detectar se está sendo depurado chamando a função IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicando-se com o depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826096"
---
# <a name="communicating-with-the-debugger"></a>Comunicando-se com o depurador

A função [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) envia uma cadeia de caracteres do processo que está sendo depurado para o depurador, gerando um evento de depuração de evento de cadeia de depuração de saída \_ \_ \_ . Um processo pode detectar se está sendo depurado chamando a função [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .

A função [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) causa uma exceção de ponto de interrupção no processo atual. Um ponto de interrupção é um local em um programa em que a execução é interrompida para permitir que o desenvolvedor examine o código, as variáveis e os valores de registro do programa e, conforme necessário, para fazer alterações, continuar a execução ou encerrar a execução.

A função [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) encerra o processo atual e fornece controle de execução para o depurador, mas ao contrário de [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), ele não gera uma exceção. Essa função só deve ser usada como último recurso, pois nem sempre libera a memória do processo nem fecha seus arquivos.

 

 
