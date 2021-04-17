---
description: Como gravar em um processador de processadores. Gravar em um processador de texto é semelhante a gravar em um arquivo de disco padrão.
ms.assetid: a69ba953-cd5c-487f-b9e0-dbd6c44b88b8
title: Gravando em um processador de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568727f7a83d46925f3e681f3dec4906903ca8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761254"
---
# <a name="writing-to-a-mailslot"></a>Gravando em um processador de texto

Gravar em um processador de texto é semelhante a gravar em um arquivo de disco padrão. O código a seguir usa as funções [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para colocar uma mensagem curta em um processador de mensagens. A mensagem é transmitida para o servidor do processador de mensagens chamado "exemplo de processador de mensagens \_ " no computador local. O código opera sob a suposição de que o servidor do processador de processadores já foi criado.


```C++
#include <windows.h>
#include <stdio.h>

LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WriteSlot(HANDLE hSlot, LPCTSTR lpszMessage)
{
   BOOL fResult; 
   DWORD cbWritten; 
 
   fResult = WriteFile(hSlot, 
     lpszMessage, 
     (DWORD) (lstrlen(lpszMessage)+1)*sizeof(TCHAR),  
     &cbWritten, 
     (LPOVERLAPPED) NULL); 
 
   if (!fResult) 
   { 
      printf("WriteFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   printf("Slot written to successfully.\n"); 

   return TRUE;
}

int main()
{ 
   HANDLE hFile; 

   hFile = CreateFile(SlotName, 
     GENERIC_WRITE, 
     FILE_SHARE_READ,
     (LPSECURITY_ATTRIBUTES) NULL, 
     OPEN_EXISTING, 
     FILE_ATTRIBUTE_NORMAL, 
     (HANDLE) NULL); 
 
   if (hFile == INVALID_HANDLE_VALUE) 
   { 
      printf("CreateFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   WriteSlot(hFile, TEXT("Message one for mailslot."));
   WriteSlot(hFile, TEXT("Message two for mailslot."));

   Sleep(5000);

   WriteSlot(hFile, TEXT("Message three for mailslot."));
 
   CloseHandle(hFile); 
 
   return TRUE;
}
```



A seguir está a saída que é exibida quando este exemplo é executado com o servidor de processador de processadores mostrado na [leitura de um processador de](reading-from-a-mailslot.md)itens.

``` syntax
Slot written to successfully.
Slot written to successfully.
Slot written to successfully.
```

 

 
