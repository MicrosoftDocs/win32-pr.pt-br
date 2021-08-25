---
description: O manipulador de símbolo carregará símbolos quando você chamar a função SymInitialize com o parâmetro fInvadeProcess definido como TRUE ou quando você chamar a função SymLoadModuleEx para especificar um módulo.
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: Carregamento de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1459f0fd05b490730739852b77edd29df38c04cbe246699552a53b7e30decf11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912348"
---
# <a name="symbol-loading"></a>Carregamento de símbolos

O manipulador de símbolo carregará símbolos quando você chamar a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) com o parâmetro *FInvadeProcess* definido como **true** ou quando você chamar a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) para especificar um módulo. Em ambos os casos, o manipulador de símbolo carrega os símbolos ou adia o carregamento do símbolo até que os símbolos sejam solicitados, dependendo das opções definidas pela função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

O manipulador de símbolo pode ser usado para recuperar informações simbólicas de qualquer módulo; Ele não precisa estar associado a um processo especificado na chamada [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Para usar um módulo arbitrário, especifique o caminho completo para a imagem do módulo no parâmetro *ImageName* . Você pode usar um caminho para qualquer módulo executável que tenha informações de depuração (.exe, .dll,. drv, .sys,. SCR, .cpl ou. com). Use o parâmetro *BaseOfDll* para especificar qualquer endereço de carga e os endereços de símbolo serão baseados nesse endereço.

Pode não ser necessário manter um módulo de símbolo carregado por meio da duração de um aplicativo. Para liberar o módulo de símbolo da lista de módulos do manipulador de símbolos, use a função [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) . Essa função libera a memória alocada para o módulo de símbolo. Para usar os símbolos para esse módulo novamente, você deve chamar a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) mesmo se a opção de carga adiada de símbolo estiver definida.

## <a name="diagnosing-symbol-load-problems"></a>Diagnosticando problemas de carregamento de símbolo

Para exibir todas as tentativas de carregar símbolos, chame [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) com SYMOPT \_ debug. Isso faz com que o DbgHelp chame a função [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) com informações detalhadas sobre pesquisas de símbolos, como os diretórios que estão pesquisando e mensagens de erro. Se seu código usar [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback), dbghelp chamará sua função de retorno de chamada em vez de chamar **OutputDebugString**. O parâmetro *ActionCode* é definido como \_ informações de depuração do CBA \_ e o parâmetro *CallbackData* é uma cadeia de caracteres que pode ser exibida.

Para permitir que essa saída de depuração seja exibida para o console sem alterar o código-fonte, defina a \_ variável de ambiente dbghelp DBGOUT como um valor não **nulo** antes de chamar a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Para registrar as informações em um arquivo, defina a \_ variável de ambiente de log dbghelp como o nome do arquivo de log a ser usado.

Observe que esses recursos devem ser usados somente quando necessário. Eles podem reduzir o carregamento de símbolos de módulos que contêm muitos símbolos.

 

 
