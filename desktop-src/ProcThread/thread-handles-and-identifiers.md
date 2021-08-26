---
description: Quando um novo thread é criado pela função CreateThread ou CreateRemoteThread, um handle para o thread é retornado.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Identificadores e identificadores de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6058388f450b4b44c371fc26b132ea785b22c29bc0a2fd86875f563371608512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031626"
---
# <a name="thread-handles-and-identifiers"></a>Identificadores e identificadores de thread

Quando um novo thread é criado pela [**função CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ou [**CreateRemoteThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) um handle para o thread é retornado. Por padrão, esse handle tem direitos de acesso completo e , sujeitos à verificação de acesso de segurança, pode ser usado em qualquer uma das funções que aceitam um thread handle. Esse handle pode ser herdado por processos filho, dependendo do sinalizador de herança especificado quando ele é criado. O handle pode ser duplicado por [**DuplicateHandle,**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)que permite que você crie um handle de thread com um subconjunto dos direitos de acesso. O handle é válido até ser fechado, mesmo após o thread que ele representa ter sido encerrado.

As [**funções CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) e [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) também retornam um identificador que identifica exclusivamente o thread em todo o sistema. Um thread pode usar a [**função GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) para obter seu próprio identificador de thread. Os identificadores são válidos desde o momento em que o thread é criado até que o thread tenha sido encerrado. Observe que nenhum identificador de thread será 0.

Se você tiver um identificador de thread, poderá obter o identificador de thread chamando a [**função OpenThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) **OpenThread** permite que você especifique os direitos de acesso do handle e se ele pode ser herdado.

Um thread pode usar a [**função GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) para recuperar um *pseudo identificador* para seu próprio objeto de thread. Esse pseudocódigo é válido somente para o processo de chamada; ele não pode ser herdado ou duplicado para uso por outros processos. Para obter o alça real para o thread, dado um pseudocódigo, use a [**função DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

Para enumerar os threads de um processo, use as [**funções Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) e [**Thread32Next.**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next)

 

 
