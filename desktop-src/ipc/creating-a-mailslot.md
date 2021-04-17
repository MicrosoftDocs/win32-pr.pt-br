---
description: 'Como criar processadores de las. As três funções especializadas têm suporte para processadores: CreateMailslot, GetMailslotInfo e SetMailslotInfo. Essas funções são usadas pelo servidor do processador de processadores.'
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: Criando um processador de mala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4cfbcf990162347d1e45da01c815002f39299e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779865"
---
# <a name="creating-a-mailslot"></a>Criando um processador de mala

As três funções especializadas têm suporte para processadores: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)e [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo). Essas funções são usadas pelo servidor do processador de processadores.

O exemplo de código a seguir usa a função [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) para recuperar o identificador para um processador de itens chamado "Sample processador de amostra \_ ". O exemplo de código em [gravação em um processador de texto](writing-to-a-mailslot.md) mostra como o aplicativo cliente pode gravar nesse processador de processadores.


```C++
#include <windows.h>
#include <stdio.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WINAPI MakeSlot(LPCTSTR lpszSlotName) 
{ 
    hSlot = CreateMailslot(lpszSlotName, 
        0,                             // no maximum message size 
        MAILSLOT_WAIT_FOREVER,         // no time-out for operations 
        (LPSECURITY_ATTRIBUTES) NULL); // default security
 
    if (hSlot == INVALID_HANDLE_VALUE) 
    { 
        printf("CreateMailslot failed with %d\n", GetLastError());
        return FALSE; 
    } 
    else printf("Mailslot created successfully.\n"); 
    return TRUE; 
}

void main()
{ 
   MakeSlot(SlotName);
}
```



Para criar um processador de processadores que pode ser herdado por processos filho, um aplicativo deve alterar a estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) passada como o último parâmetro de [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota). Para fazer isso, o aplicativo define o membro **bInheritHandle** dessa estrutura como **true** (a configuração padrão é **false**).

 

 
