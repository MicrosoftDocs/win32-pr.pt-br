---
description: A função CreateThread cria um novo thread para um processo.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funções de thread para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500955"
---
# <a name="thread-functions-for-debugging"></a>Funções de thread para depuração

A função [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) cria um novo thread para um processo. Os depuradores normalmente precisam examinar ou alterar o conteúdo dos registros de um thread. Para fazer isso, um depurador deve obter um identificador para o thread usando a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) e especificando o acesso apropriado ao thread (contexto de obtenção de thread \_ \_ , \_ contexto de conjunto de threads \_ ou ambos). A função [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite que um depurador obtenha o identificador de um thread existente.

Um processo com acesso apropriado a um thread pode examinar os registros do thread usando a função [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) e definir o conteúdo dos registros do thread usando a função [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .

Um processo também pode obter \_ acesso de \_ retomada de thread de suspensão a um thread. Esse tipo de acesso permite que um depurador controle a execução de um thread com as funções [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) e [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) . Para obter mais informações sobre threads, consulte [processos e threads](../procthread/processes-and-threads.md).

 

 
