---
description: Os aplicativos podem gerenciar um contexto de ativação chamando diretamente as funções de contexto de ativação.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Usando a API de contexto de ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090201"
---
# <a name="using-the-activation-context-api"></a>Usando a API de contexto de ativação

Os aplicativos podem gerenciar um [contexto de ativação](activation-contexts.md) chamando diretamente as funções de contexto de ativação. Contextos de ativação são estruturas de dados na memória. O sistema pode usar as informações no contexto de ativação para redirecionar um aplicativo para carregar uma versão de DLL específica, instância de objeto COM ou versão de janela personalizada. Para obter mais informações, consulte [referência de contexto de ativação](activation-context-reference.md).

A API (interface de programação de aplicativo) pode ser usada para gerenciar o contexto de ativação e criar objetos com nome de versão com [manifestos](manifests.md). Os dois cenários a seguir ilustram como um aplicativo pode gerenciar um contexto de ativação chamando diretamente as funções de contexto de ativação. Na maioria dos casos, no entanto, o contexto de ativação é gerenciado pelo sistema. Os desenvolvedores de aplicativos e os provedores de assembly normalmente não precisam fazer chamadas para a pilha para gerenciar o contexto de ativação.

-   Processos e aplicativos que implementam as camadas de indireção ou de expedição.

    Por exemplo, um usuário Gerenciando contextos de ativação no loop de eventos. Cada vez que a janela é acessada, como movendo o mouse sobre a janela, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) é chamado, o que ativa o contexto de ativação atual para o recurso, conforme mostrado no fragmento de código a seguir.

    <dl> MANIPULAR hActCtx;  
    CreateWindow ();  
    ...  
    GetCurrentActCtx (&ActCtx);  
    ...  
    ReleaseActCtx (&ActCtx);  
    </dl>

    No fragmento de código a seguir, a função de API ativa os contextos de ativação apropriados antes de chamar [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca). Quando **CallWindowProc** é chamado, ele usa esse contexto para passar uma mensagem para o Windows. Quando todas as operações de recurso forem concluídas, a função desativará o contexto.

    <dl> ULONG \_ PTR ulpCookie;  
    MANIPULAR hActCtx;  
    If (ActivateActCtx (hActCtx, &ulpCookie))  
    {  
    ...  
    CallWindowProc(...);  
    ...  
    DeactivateActCtx (0, ulpCookie);  
    }  
    </dl>

-   Camada de expedição do delegante.

    Esse cenário se aplica a gerentes que gerenciam várias entidades com uma camada de API comum, como um Gerenciador de driver. Embora ainda não tenha sido implementado, um exemplo disso seria o driver ODBC.

    Nesse cenário, a camada intermediária torna-se capaz de processar associações de assembly. Para obter o driver de associação específico à versão, os editores devem fornecer um manifesto e especificar dependências em componentes específicos nesse manifesto. O aplicativo base não se vincula dinamicamente aos componentes; no tempo de execução, o Gerenciador de driver gerencia as chamadas. Quando o driver ODBC é chamado com base na cadeia de conexão, ele carrega o driver apropriado. Em seguida, ele cria o contexto de ativação usando as informações no arquivo de manifesto do assembly.

    Sem o manifesto, a ação padrão para o driver é usar o mesmo contexto que o especificado pelo aplicativo — neste exemplo, versão 2 do MSVCRT. Como existe um manifesto, um contexto de ativação separado é estabelecido. Quando o driver ODBC é executado, ele é associado à versão 1 do assembly MSVCRT.

    Cada vez que o Gerenciador de driver chama a camada de expedição, por exemplo, para obter o próximo conjunto de dados, ele usa os assemblies apropriados com base no contexto de ativação. O fragmento de código a seguir ilustra isso.

    <dl> MANIPULAR hActCtx;  
    ULONG \_ PTR ulpCookie;  
    ACTCTX ActCtxToCreate = {...};  
    hActCtx = CreateActCtx (&ActCtxToCreate);  
    ...;  
    If (ActivateActCtx (hActCtx, &ulpCookie))  
    {  
    ...  
    ConnectDb(...);  
    DeactivateActCtx (0, ulpCookie);  
    }  
    ...  
    ReleaseActCtx(hActCtx);  
    </dl>

 

 
