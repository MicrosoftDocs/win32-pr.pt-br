---
description: A função OutputDebugString envia uma cadeia de caracteres do processo que está sendo depurado para o depurador gerando um evento DE depuração OUTPUT \_ DEBUG \_ STRING \_ EVENT. Um processo pode detectar se ele está sendo depurado chamando a função IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicando-se com o depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee4d78fc2b0cef1df9f0597a816966585d00e1041711d4712d1a1fa66639e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692056"
---
# <a name="communicating-with-the-debugger"></a>Comunicando-se com o depurador

A [**função OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) envia uma cadeia de caracteres do processo que está sendo depurado para o depurador gerando um evento DE depuração OUTPUT \_ DEBUG STRING \_ \_ EVENT. Um processo pode detectar se ele está sendo depurado chamando a [**função IsDebuggerPresent.**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)

A [**função DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) causa uma exceção de ponto de interrupção no processo atual. Um ponto de interrupção é um local em um programa em que a execução é interrompida para permitir que o desenvolvedor examine o código, as variáveis e os valores de registro do programa e, conforme necessário, para fazer alterações, continuar a execução ou encerrar a execução.

A [**função FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) encerra o processo atual e fornece controle de execução ao depurador, mas, ao contrário [**de DebugBreak,**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)ela não gera uma exceção. Essa função só deve ser usada como último recurso, porque nem sempre libera a memória do processo nem fecha seus arquivos.

 

 
