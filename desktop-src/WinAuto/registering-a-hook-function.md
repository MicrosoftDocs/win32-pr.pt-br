---
title: Registrando uma função de gancho
description: Os aplicativos cliente recebem WinEvents em uma função de retorno de chamada WinEventProc. As ações executadas pela função de retorno de chamada são definidas pelo aplicativo, mas a sintaxe deve ser conforme especificado no protótipo.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c444d2ee291cb07386e775a649ba0c3d42486c45b70e4d3f4629b9b67274f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564646"
---
# <a name="registering-a-hook-function"></a>Registrando uma função de gancho

Os aplicativos cliente recebem WinEvents em uma função de retorno de chamada [*WinEventProc.*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) As ações executadas pela função de retorno de chamada são definidas pelo aplicativo, mas a sintaxe deve ser conforme especificado no protótipo.

Antes de receber eventos, a função deve ser registrada chamando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). O cliente pode chamar **SetWinEventHook** mais de uma vez para registrar funções de gancho diferentes ou definir eventos adicionais para uma função de gancho registrada anteriormente.

Ao chamar [**SetWinEventHook,**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) o cliente especifica quais eventos receber e como recebê-los. O cliente pode optar por:

-   Receber todos os eventos ou um conjunto específico de eventos.
-   Receber eventos de todos os threads ou de um thread específico.
-   Receber eventos de todos os processos ou de um processo específico.
-   Manipular eventos em processo ou fora do processo.

Quando um evento é gerado que corresponde aos critérios especificados, o sistema chama a função de retorno de chamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) do cliente (ou "procedimento de gancho"). Os parâmetros que a função de gancho recebe dizem ao cliente sobre a janela, o objeto e o possível elemento filho que gerou o evento. Um cliente usa esses parâmetros em uma chamada de recuperação de objeto, [**como AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

 




