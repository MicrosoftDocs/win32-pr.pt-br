---
description: Quando um novo thread é criado pela função CreateThread ou CreateRemoteThread, um identificador para o thread é retornado.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Manipuladores e identificadores de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501d449bdb34d158ad14e52409967d4ef17f62f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828357"
---
# <a name="thread-handles-and-identifiers"></a>Manipuladores e identificadores de thread

Quando um novo thread é criado pela função [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ou [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) , um identificador para o thread é retornado. Por padrão, esse identificador tem direitos de acesso completo e — sujeito à verificação de acesso de segurança — pode ser usado em qualquer uma das funções que aceitam um identificador de thread. Esse identificador pode ser herdado por processos filho, dependendo do sinalizador de herança especificado quando ele é criado. O identificador pode ser duplicado por [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle), o que permite que você crie um identificador de thread com um subconjunto dos direitos de acesso. O identificador é válido até ser fechado, mesmo depois que o thread que ele representa foi encerrado.

As funções [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) e [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) também retornam um identificador que identifica exclusivamente o thread em todo o sistema. Um thread pode usar a função [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) para obter seu próprio identificador de thread. Os identificadores são válidos a partir do momento em que o thread é criado até que o thread seja encerrado. Observe que nenhum identificador de thread nunca será 0.

Se você tiver um identificador de thread, poderá obter o identificador de thread chamando a função [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) . O **OpenThread** permite que você especifique os direitos de acesso do identificador e se ele pode ser herdado.

Um thread pode usar a função [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) para recuperar um *pseudo Handle* para seu próprio objeto thread. Esse pseudodispositivo é válido somente para o processo de chamada; Ele não pode ser herdado ou duplicado para uso por outros processos. Para obter o identificador real para o thread, dado um pseudo-identificador, use a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

Para enumerar os threads de um processo, use as funções [**Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) e [**Thread32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next) .

 

 
