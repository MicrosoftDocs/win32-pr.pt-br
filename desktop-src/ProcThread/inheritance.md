---
description: Um processo filho pode herdar várias propriedades e recursos de seu processo pai.
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: Herança (processos e threads)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f50b191ee24783f7213ac15f61c435ebd696175a3042d79e2f359ef61097fe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032586"
---
# <a name="inheritance"></a>Herança

Um processo filho pode herdar várias propriedades e recursos de seu processo pai. Você também pode impedir que um processo filho herde Propriedades de seu processo pai. O seguinte pode ser herdado:

-   Identificadores abertos retornados pela função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Isso inclui identificadores para arquivos, buffers de entrada do console, buffers de tela do console, pipes nomeados, dispositivos de comunicação serial e processadores de memória.
-   Abra identificadores para processar, thread, mutex, evento, semáforo, pipe nomeado, pipe anônimo e objetos de mapeamento de arquivo. Elas são retornadas pelas funções [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa), [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**createsemáforo**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), [**CreateNamedPipe**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea), [**CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)e [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) , respectivamente.
-   Variáveis de ambiente.
-   O diretório atual.
-   O console, a menos que o processo seja desanexado ou um novo console seja criado. Um processo de console filho também pode herdar os identificadores padrão do pai, bem como o acesso ao buffer de entrada e ao buffer de tela ativo.
-   O modo de erro, conforme definido pela função [**SetError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) .
-   A máscara de afinidade do processador.
-   A associação a um trabalho.

O processo filho não herda o seguinte:

-   Classe de prioridade.
-   Identificadores retornados por [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)e [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc).
-   Pseudo-alças, como nos identificadores retornados pela função [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) ou [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) . Esses identificadores são válidos somente para o processo de chamada.
-   Identificadores de módulo DLL retornados pela função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) .
-   As alças GDI ou USER, como **HBITMAP** ou **HMENU**.

## <a name="inheriting-handles"></a>Herdando identificadores

Um processo filho pode herdar alguns de seus identificadores pai, mas não herdar outros. Para fazer com que um identificador seja herdado, você deve fazer duas coisas:

-   Especifique que o identificador deve ser herdado quando você criar, abrir ou duplicar o identificador. Normalmente, as funções de criação usam o membro **bInheritHandle** de uma estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) para essa finalidade. [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) usa o parâmetro *bInheritHandles* .
-   Especifique que os identificadores herdáveis devem ser herdados definindo o parâmetro *bInheritHandles* como true ao chamar a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Além disso, para herdar a entrada padrão, a saída padrão e os identificadores de erro padrão, o membro **dwFlags** da estrutura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) deve incluir STARTF \_ USESTDHANDLES.

Para especificar uma lista de identificadores que devem ser herdados por um processo filho específico, chame a função [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) com o sinalizador *PROC_THREAD_ATTRIBUTE_HANDLE_LIST* .

Um identificador herdado se refere ao mesmo objeto no processo filho como faz no processo pai. Ele também tem o mesmo valor e privilégios de acesso. Portanto, quando um processo altera o estado do objeto, a alteração afeta ambos os processos. Para usar um identificador, o processo filho deve recuperar o valor do identificador e "saber" o objeto ao qual se refere. Normalmente, o processo pai comunica essas informações ao processo filho por meio de sua linha de comando, bloco de ambiente ou alguma forma de [comunicação entre processos](/windows/desktop/ipc/interprocess-communications).

Use a função [**SetHandleInformation**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) para controlar se um identificador existente é herdável ou não.

## <a name="inheriting-environment-variables"></a>Herdando variáveis de ambiente

Um processo filho herda as variáveis de ambiente de seu processo pai por padrão. No entanto, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite que o processo pai especifique um bloco diferente de variáveis de ambiente. Para obter mais informações, consulte [variáveis de ambiente](environment-variables.md).

## <a name="inheriting-the-current-directory"></a>Herdando o diretório atual

A função [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) recupera o diretório atual do processo de chamada. Um processo filho herda o diretório atual de seu processo pai por padrão. No entanto, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite que o processo pai especifique um diretório atual diferente para o processo filho. Para alterar o diretório atual do processo de chamada, use a função [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) .
