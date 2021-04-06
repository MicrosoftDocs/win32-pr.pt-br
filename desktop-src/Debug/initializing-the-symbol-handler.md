---
description: O código a seguir demonstra como inicializar o manipulador de símbolo.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Inicializando o manipulador de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920174"
---
# <a name="initializing-the-symbol-handler"></a>Inicializando o manipulador de símbolo

O código a seguir demonstra como inicializar o manipulador de símbolo. A função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) adia o carregamento de símbolos até que as informações de símbolo sejam solicitadas. O código carrega os símbolos para cada módulo no processo especificado, passando um valor de **true** para o parâmetro *BInvade* da função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . (Essa função chama a função [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) para cada módulo que o processo mapeou em seu espaço de endereço.)

Se o processo especificado não for o processo que chamou [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), o código passará um identificador de processo como o primeiro parâmetro de **SymInitialize**.

A especificação de **NULL** como o segundo parâmetro de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indica que o manipulador de símbolo deve usar o caminho de pesquisa padrão para localizar arquivos de símbolo. Para obter informações detalhadas sobre como o manipulador de símbolo localiza arquivos de símbolo ou como um aplicativo pode especificar um caminho de pesquisa de símbolo, consulte [caminhos de símbolo](symbol-paths.md).


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



