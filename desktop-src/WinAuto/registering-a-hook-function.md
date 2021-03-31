---
title: Registrando uma função de gancho
description: Os aplicativos cliente recebem WinEvents em uma função de retorno de chamada WinEventProc. As ações executadas pela função de retorno de chamada são definidas pelo aplicativo, mas a sintaxe deve ser conforme especificado no protótipo.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822449"
---
# <a name="registering-a-hook-function"></a>Registrando uma função de gancho

Os aplicativos cliente recebem WinEvents em uma função de retorno de chamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) . As ações executadas pela função de retorno de chamada são definidas pelo aplicativo, mas a sintaxe deve ser conforme especificado no protótipo.

Antes que possa receber eventos, a função deve ser registrada chamando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). O cliente pode chamar **SetWinEventHook** mais de uma vez para registrar diferentes funções de gancho ou para definir eventos adicionais para uma função de gancho registrada anteriormente.

Ao chamar [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , o cliente especifica quais eventos receber e como recebê-los. O cliente pode optar por:

-   Receber todos os eventos ou um conjunto específico de eventos.
-   Receber eventos de todos os threads ou de um thread específico.
-   Receber eventos de todos os processos ou de um processo específico.
-   Manipule eventos em processo ou fora do processo.

Quando é gerado um evento que corresponde aos critérios especificados, o sistema chama a função de retorno de chamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) do cliente (ou "procedimento de gancho"). Os parâmetros que a função Hook recebe dizem ao cliente sobre a janela, o objeto e o elemento filho possível que gerou o evento. Um cliente usa esses parâmetros em uma chamada de recuperação de objeto, como [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

 




