---
description: Quando um novo processo é criado pela função CreateProcess, os identificadores do novo processo e seu thread primário são retornados.
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: Manipuladores de processo e identificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a1ec0acb6535f8f64b9f4bd0815392d61fccbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296738"
---
# <a name="process-handles-and-identifiers"></a>Manipuladores de processo e identificadores

Quando um novo processo é criado pela função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , os identificadores do novo processo e seu thread primário são retornados. Esses identificadores são criados com direitos de acesso completo e — sujeitos à verificação de acesso de segurança — podem ser usados em qualquer uma das funções que aceitam identificadores de thread ou processo. Esses identificadores podem ser herdados por processos filho, dependendo do sinalizador de herança especificado quando eles são criados. Os identificadores são válidos até serem fechados, mesmo depois que o processo ou thread que eles representam foram encerrados.

A função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) também retorna um identificador que identifica exclusivamente o processo em todo o sistema. Um processo pode usar a função [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) para obter seu próprio identificador de processo (também conhecido como ID do processo ou PID). O identificador é válido desde o momento em que o processo é criado até que o processo seja encerrado. Um processo pode usar a função [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) para obter o identificador de processo de seu processo pai.

Se você tiver um identificador de processo, poderá obter o identificador de processo chamando a função [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) . O **OpenProcess** permite que você especifique os direitos de acesso do identificador e se ele pode ser herdado.

Um processo pode usar a função [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) para recuperar um pseudo identificador para seu próprio objeto de processo. Esse pseudodispositivo é válido somente para o processo de chamada; Ele não pode ser herdado ou duplicado para uso por outros processos. Para obter o identificador real para o processo, chame a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

 

 
