---
description: Contextos de ativação são estruturas de dados na memória que contêm informações que o sistema pode usar para redirecionar um aplicativo para carregar uma versão de DLL específica, instância de objeto COM ou versão de janela personalizada.
ms.assetid: 5416f8c0-d99b-4a5d-a689-a47bd0cf1a88
title: Contextos de ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1f20d747f63ba71eee73fc17c0d5543003e5f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296715"
---
# <a name="activation-contexts"></a>Contextos de ativação

[*Contextos de ativação*](a-sbscs-gly.md) são estruturas de dados na memória que contêm informações que o sistema pode usar para redirecionar um aplicativo para carregar uma versão de DLL específica, instância de objeto com ou versão de janela personalizada. Uma seção do contexto de ativação pode conter informações de redirecionamento de DLL que são usadas pelo carregador de DLL; outra seção pode conter informações do servidor COM. As funções de contexto de ativação usam, criam, ativam e desativam contextos de ativação. As funções de ativação podem redirecionar a associação de um aplicativo para objetos nomeados por versão que especificam versões de DLL específicas, classes de janela, servidores COM, bibliotecas de tipos e interfaces. Para obter mais informações sobre as funções e estruturas de contexto de ativação, consulte a [referência de contexto de ativação](activation-context-reference.md).

A partir do Windows XP, as funções de contexto de ativação permitem que o Windows Use informações em [manifestos](manifests.md) para criar objetos nomeados por versão. Se um aplicativo criar um processo chamando [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), o Windows verificará a existência de um [manifesto do aplicativo](application-manifests.md). Se existir um manifesto, o Windows usará as informações no manifesto para preencher o contexto de ativação. Como os manifestos descrevem a dependência de um aplicativo nas versões do [assembly lado a lado](about-side-by-side-assemblies-.md) , os objetos especificados sem versões no manifesto são mapeados para objetos com nome de versão. Por exemplo, o manifesto pode descrever DLLs, arquivos, classes de janela, servidores COM, bibliotecas de tipos e interfaces.

Quando um objeto global é criado dentro do contexto de ativação, o sistema automaticamente fornece ao objeto um nome específico da versão consultando o manifesto. Quando o aplicativo é executado e solicita um objeto nomeado, ele obtém o objeto com nome de versão. Isso permite que várias versões de um módulo de código sejam executadas no sistema ao mesmo tempo sem interferir umas com as outras. Por exemplo, o [shell do Windows](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)) usa um manifesto para descrever uma dependência da versão 6,0 do Comctl32 e criar versões de classes de janela.

Se um aplicativo criar um recurso chamando [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), o processo especificará um nome de classe para essa função. A chamada para [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx) Obtém o contexto de ativação atual e verifica se existe um mapeamento para o nome de classe fornecido. Se houver um mapeamento, ele usará essa versão do processo de chamada para resolver o mapeamento e fornecer o nome da classe específica da versão. O Windows cria uma janela com o procedimento de janela, os estilos e outros atributos associados a esse nome de classe e versão.

O contexto de ativação é gerenciado pelo sistema na maioria dos casos. Os desenvolvedores de aplicativos e os provedores de assembly normalmente não precisam fazer chamadas para a pilha. Os aplicativos podem gerenciar um contexto de ativação chamando diretamente o contexto de ativação. Para obter mais informações, consulte [usando a API de contexto de ativação](using-the-activation-context-api.md).

 

 
