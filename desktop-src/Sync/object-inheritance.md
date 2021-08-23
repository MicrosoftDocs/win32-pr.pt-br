---
description: Ao criar um processo com a função CreateProcess, você pode especificar que o processo herde os alças para objetos mutex, event, semáforo ou timer usando a estrutura SECURITY \_ ATTRIBUTES.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Herança de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab6d2380ac0012e0f1005df2dfc4b820bee82a7974f3ca03d856c7df9fb8446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661376"
---
# <a name="object-inheritance"></a>Herança de objetos

Ao criar um processo com a função [**CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) você pode especificar que o processo herde os alças para objetos mutex, event, semáforo ou timer usando a estrutura [**SECURITY \_ ATTRIBUTES.**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) O identificador herdado pelo processo tem o mesmo acesso ao objeto que o identificador original. O alça herdado aparece na tabela de alça do processo criado, mas você deve comunicar o valor do handle para o processo criado. Você pode fazer isso especificando o valor como um argumento de linha de comando ao chamar **CreateProcess**. Em seguida, o processo criado usa a [**função GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) para recuperar a cadeia de caracteres de linha de comando e converter o argumento handle em um alçado para uso. Para obter mais informações, consulte [Herança](../procthread/inheritance.md).

 

 
