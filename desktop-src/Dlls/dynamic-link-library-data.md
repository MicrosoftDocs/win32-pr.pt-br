---
description: Uma biblioteca Dynamic-Link dados (DLL) pode conter dados globais ou locais.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dynamic-Link dados da biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8902eb6388624d958c7176a14b8893f8e2245ddd9370f6ba2ac71605b2379cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048436"
---
# <a name="dynamic-link-library-data"></a>Dynamic-Link dados da biblioteca

Uma biblioteca Dynamic-Link dados (DLL) pode conter dados globais ou locais.

## <a name="variable-scope"></a>{1&gt;Escopo de variáveis&lt;1}

As variáveis declaradas como globais em um arquivo de código-fonte DLL são tratadas como variáveis globais pelo compilador e pelo vinculador, mas cada processo que carrega uma determinada DLL obtém sua própria cópia das variáveis globais dessa DLL. O escopo de variáveis estáticas é limitado ao bloco no qual as variáveis estáticas são declaradas. Como resultado, cada processo tem sua própria instância das variáveis globais e estáticas da DLL por padrão.

> [!Note]  
> Suas ferramentas de desenvolvimento podem permitir que você substitua o comportamento padrão. Por exemplo, o compilador Visual C++ dá suporte **\# à seção pragma** e o linker dá suporte à opção /SECTION. Para obter mais informações, consulte a documentação incluída com suas ferramentas de desenvolvimento.

 

## <a name="dynamic-memory-allocation"></a>alocação Memória Dinâmica dados

Quando uma DLL aloca memória usando qualquer uma das funções de alocação de memória [**(GlobalAlloc,**](/windows/desktop/api/winbase/nf-winbase-globalalloc) [**LocalAlloc,**](/windows/desktop/api/winbase/nf-winbase-localalloc) [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)e [**VirtualAlloc),**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)a memória é alocada no espaço de endereço virtual do processo de chamada e é acessível somente aos threads desse processo.

Uma DLL pode usar o mapeamento de arquivos para alocar memória que pode ser compartilhada entre processos. Para uma discussão geral sobre como usar o mapeamento de arquivos para criar memória compartilhada nomeada, consulte [Mapeamento de arquivos](/windows/desktop/Memory/file-mapping). Para ver um exemplo que usa a [**função DllMain**](dllmain.md) para configurar a memória compartilhada usando o mapeamento de arquivo, consulte [Using Shared Memory in a Dynamic-Link Library](using-shared-memory-in-a-dynamic-link-library.md).

## <a name="thread-local-storage"></a>Armazenamento local de thread

As funções de armazenamento local de thread (TLS) permitem que uma DLL aloce um índice para armazenar e recuperar um valor diferente para cada thread de um processo multithread. Por exemplo, um aplicativo de planilha pode criar uma nova instância do mesmo thread sempre que o usuário abrir uma nova planilha. Uma DLL que fornece as funções para várias operações de planilha pode usar tLS para salvar informações sobre o estado atual de cada planilha (linha, coluna e assim por diante). Para uma discussão geral sobre o armazenamento local do thread, consulte [Thread Local Armazenamento](/windows/desktop/ProcThread/thread-local-storage). Para ver um exemplo que usa a [**função DllMain**](dllmain.md) para configurar o armazenamento local do thread, consulte Usando o [thread local Armazenamento em](using-thread-local-storage-in-a-dynamic-link-library.md)uma biblioteca Dynamic-Link .

**Windows Server 2003 e Windows XP:** O Visual C++ compilador dá suporte a uma sintaxe que permite declarar variáveis locais de thread: **\_ declspec(thread).** Se você usar essa sintaxe em uma DLL, não poderá carregar a DLL explicitamente usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) em versões do Windows antes do Windows Vista. Se a DLL for carregada explicitamente, você deverá usar as funções de armazenamento local do thread em vez **\_ de declspec(thread).**

 

 
