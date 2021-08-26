---
description: Quando um novo processo é criado pela função CreateProcess, os handles do novo processo e seu thread primário são retornados.
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: Identificadores e identificadores de processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4603b3d217db0870aeb890b05c7a416f46f2309ea9a0230b33d150387ebc5173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031766"
---
# <a name="process-handles-and-identifiers"></a>Identificadores e identificadores de processo

Quando um novo processo é criado pela [**função CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) os handles do novo processo e seu thread primário são retornados. Esses alças são criados com direitos de acesso completo e , sujeitos à verificação de acesso de segurança, podem ser usados em qualquer uma das funções que aceitam os threads ou os alças de processo. Esses alças podem ser herdados por processos filho, dependendo do sinalizador de herança especificado quando eles são criados. Os alças são válidos até o fechamento, mesmo após o processo ou thread que eles representam ter sido encerrado.

A [**função CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) também retorna um identificador que identifica exclusivamente o processo em todo o sistema. Um processo pode usar a [**função GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) para obter seu próprio identificador de processo (também conhecido como ID do processo ou PID). O identificador é válido desde o momento em que o processo é criado até que o processo seja encerrado. Um processo pode usar a [**função Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) para obter o identificador do processo pai.

Se você tiver um identificador de processo, poderá obter o identificador do processo chamando a [**função OpenProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) **O OpenProcess** permite que você especifique os direitos de acesso do handle e se ele pode ser herdado.

Um processo pode usar a [**função GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) para recuperar um pseudo identificador para seu próprio objeto de processo. Esse pseudocódigo é válido somente para o processo de chamada; ele não pode ser herdado ou duplicado para uso por outros processos. Para obter o alçamento real para o processo, chame a [**função DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

 

 
