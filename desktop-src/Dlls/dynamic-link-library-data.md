---
description: Uma biblioteca de Dynamic-Link (DLL) pode conter dados globais ou locais.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dynamic-Link dados da biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83280d3bfc449061c44f9e8bfd9b47833e7eca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755127"
---
# <a name="dynamic-link-library-data"></a>Dynamic-Link dados da biblioteca

Uma biblioteca de Dynamic-Link (DLL) pode conter dados globais ou locais.

## <a name="variable-scope"></a>{1&gt;Escopo de variáveis&lt;1}

As variáveis declaradas como globais em um arquivo de código-fonte DLL são tratadas como variáveis globais pelo compilador e pelo vinculador, mas cada processo que carrega uma determinada DLL obtém sua própria cópia das variáveis globais dessa DLL. O escopo de variáveis estáticas é limitado ao bloco no qual as variáveis estáticas são declaradas. Como resultado, cada processo tem sua própria instância das variáveis global e estática de DLL por padrão.

> [!Note]  
> Suas ferramentas de desenvolvimento podem permitir que você substitua o comportamento padrão. Por exemplo, o compilador Visual C++ dá suporte à **\# seção pragma** e o vinculador dá suporte à opção/Section. Para obter mais informações, consulte a documentação incluída com suas ferramentas de desenvolvimento.

 

## <a name="dynamic-memory-allocation"></a>Alocação de Memória Dinâmica

Quando uma DLL aloca memória usando qualquer uma das funções de alocação de memória ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)e [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)), a memória é alocada no espaço de endereço virtual do processo de chamada e é acessível somente para os threads desse processo.

Uma DLL pode usar o mapeamento de arquivo para alocar memória que pode ser compartilhada entre processos. Para obter uma discussão geral sobre como usar o mapeamento de arquivo para criar a memória compartilhada nomeada, consulte [mapeamento de arquivo](/windows/desktop/Memory/file-mapping). Para obter um exemplo que usa a função [**DllMain**](dllmain.md) para configurar a memória compartilhada usando o mapeamento de arquivo, consulte [usando a memória compartilhada em uma biblioteca de Dynamic-Link](using-shared-memory-in-a-dynamic-link-library.md).

## <a name="thread-local-storage"></a>Armazenamento local de thread

As funções de armazenamento local de thread (TLS) permitem que uma DLL aloque um índice para armazenar e recuperar um valor diferente para cada thread de um processo multi-threaded. Por exemplo, um aplicativo de planilha pode criar uma nova instância do mesmo thread cada vez que o usuário abrir uma nova planilha. Uma DLL que fornece as funções para várias operações de planilha pode usar o TLS para salvar informações sobre o estado atual de cada planilha (linha, coluna e assim por diante). Para uma discussão geral sobre o armazenamento local de thread, consulte [armazenamento local de thread](/windows/desktop/ProcThread/thread-local-storage). Para obter um exemplo que usa a função [**DllMain**](dllmain.md) para configurar o armazenamento local de thread, consulte [usando o armazenamento local de thread em uma biblioteca de Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

**Windows Server 2003 e Windows XP:** O compilador Visual C++ dá suporte a uma sintaxe que permite declarar variáveis locais de thread: **\_ declspec (thread)**. Se você usar essa sintaxe em uma DLL, não será possível carregar a DLL explicitamente usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) em versões do Windows anteriores ao Windows Vista. Se sua DLL for carregada explicitamente, você deverá usar as funções de armazenamento local de thread em vez de **\_ declspec (thread)**.

 

 
