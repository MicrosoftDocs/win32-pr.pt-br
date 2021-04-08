---
description: A função CreateProcess permite que um depurador inicie um processo e depure-o.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Processar funções para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920281"
---
# <a name="process-functions-for-debugging"></a>Processar funções para depuração

A função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite que um depurador inicie um processo e depure-o. O parâmetro *fdwCreate* de **CreateProcess** é usado para especificar o tipo de operação de depuração. Se o sinalizador de processo de depuração \_ for especificado para o parâmetro, um depurador depurará o novo processo e todos os descendentes do processo, desde que os descendentes sejam criados sem o sinalizador de processo de depuração \_ .

Se o processo de depuração \_ e a depuração \_ somente desses sinalizadores de \_ \_ processo forem especificados para *fdwCreate*, um depurador depurará o novo processo, mas nenhum de seus descendentes.

Um depurador pode depurar outro criando um processo com o \_ sinalizador processo de depuração. O novo processo (o depurador que está sendo depurado) deve criar um processo com o \_ sinalizador de processo de depuração.

A função [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) permite que um depurador obtenha o identificador de um processo existente. (A função [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) usa esse identificador para anexar o depurador ao processo.) Normalmente, os depuradores abrem um processo com os sinalizadores de gravação da VM do processo de \_ \_ leitura e processamento da VM \_ \_ . O uso desses sinalizadores permite que o depurador Leia e grave na memória virtual do processo usando as funções [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) e [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) . Para obter mais informações, consulte [**processos e threads**](../procthread/processes-and-threads.md).

 

 
