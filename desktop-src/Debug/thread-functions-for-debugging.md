---
description: Saiba como usar a função CreateThread para criar um novo thread para um processo. Normalmente, os depurador precisam examinar ou alterar o conteúdo dos registros de um thread.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funções de thread para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403979"
---
# <a name="thread-functions-for-debugging"></a>Funções de thread para depuração

A [**função CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) cria um novo thread para um processo. Normalmente, os depurador precisam examinar ou alterar o conteúdo dos registros de um thread. Para fazer isso, um depurador deve obter um tratamento para o thread usando a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) e especificando o acesso apropriado ao thread (THREAD GET CONTEXT, THREAD SET CONTEXT ou \_ \_ \_ \_ ambos). A [**função OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite que um depurador obtenha o identificador de um thread existente.

Um processo com acesso apropriado a um thread pode examinar os registros do thread usando a função [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) e definir o conteúdo dos registros do thread usando a [**função SetThreadContext.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)

Um processo também pode obter acesso THREAD \_ SUSPEND RESUME a um \_ thread. Esse tipo de acesso permite que um depurador controle a execução de um thread com as funções [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) e [**ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) Para obter mais informações sobre threads, consulte [Processos e threads.](../procthread/processes-and-threads.md)

 

 
