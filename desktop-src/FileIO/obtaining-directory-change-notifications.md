---
description: Um aplicativo pode monitorar o conteúdo de um diretório e seus subdireários usando notificações de alteração.
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: Obtendo notificações de alteração de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d94bd2b86aacaf7b32191fd68208bd1400a4b56cf4c55b13102210ffb50f7ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047996"
---
# <a name="obtaining-directory-change-notifications"></a>Obtendo notificações de alteração de diretório

Um aplicativo pode monitorar o conteúdo de um diretório e seus subdireários usando notificações de alteração. Aguardar uma notificação de alteração é semelhante a ter uma operação de leitura pendente em um diretório e, se necessário, seus subdireários. Quando algo muda dentro do diretório que está sendo observado, a operação de leitura é concluída. Por exemplo, um aplicativo pode usar essas funções para atualizar uma listagem de diretório sempre que um nome de arquivo dentro do diretório monitorado for atualizado.

Um aplicativo pode especificar um conjunto de condições que disparam uma notificação de alteração usando a [**função FindFirstChangeNotification.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) As condições incluem alterações em nomes de arquivo, nomes de diretório, atributos, tamanho do arquivo, hora da última gravação e segurança. Essa função também retorna um alça que pode ser aguardado usando as [funções de espera](/windows/desktop/Sync/wait-functions). Se a condição de espera for atendida, [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) poderá ser usado para fornecer um handle de notificação para aguardar as alterações subsequentes. No entanto, essas funções não indicam a alteração real que atendia à condição de espera.

Use [**FindCloseChangeNotification para**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) fechar o alçamento de notificação.

Para recuperar informações sobre a alteração específica como parte da notificação, use a [**função ReadDirectoryChangesW.**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) Essa função também permite que você forneça uma rotina de conclusão.

Para acompanhar as alterações em um volume, consulte [alterar diários](change-journals.md).

O exemplo a seguir monitora a árvore de diretório para alterações de nome de diretório. Ele também monitora um diretório para alterações de nome de arquivo. O exemplo usa a [**função FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) para criar dois alças de notificação e a [**função WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) para aguardar os alças. Sempre que um diretório é criado ou excluído na árvore, o exemplo deve atualizar toda a árvore de diretórios. Sempre que um arquivo é criado ou excluído no diretório, o exemplo deve atualizar o diretório.

> [!Note]
>
> Este exemplo simplista usa a função [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) para encerramento e limpeza, mas aplicativos mais complexos sempre devem usar o gerenciamento de recursos apropriado, como [**FindCloseChangeNotification,**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) quando apropriado.

 


```C++
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <tchar.h>

void RefreshDirectory(LPTSTR);
void RefreshTree(LPTSTR);
void WatchDirectory(LPTSTR);

void _tmain(int argc, TCHAR *argv[])
{
    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
        return;
    }

    WatchDirectory(argv[1]);
}

void WatchDirectory(LPTSTR lpDir)
{
   DWORD dwWaitStatus; 
   HANDLE dwChangeHandles[2]; 
   TCHAR lpDrive[4];
   TCHAR lpFile[_MAX_FNAME];
   TCHAR lpExt[_MAX_EXT];

   _tsplitpath_s(lpDir, lpDrive, 4, NULL, 0, lpFile, _MAX_FNAME, lpExt, _MAX_EXT);

   lpDrive[2] = (TCHAR)'\\';
   lpDrive[3] = (TCHAR)'\0';
 
// Watch the directory for file creation and deletion. 
 
   dwChangeHandles[0] = FindFirstChangeNotification( 
      lpDir,                         // directory to watch 
      FALSE,                         // do not watch subtree 
      FILE_NOTIFY_CHANGE_FILE_NAME); // watch file name changes 
 
   if (dwChangeHandles[0] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 
// Watch the subtree for directory creation and deletion. 
 
   dwChangeHandles[1] = FindFirstChangeNotification( 
      lpDrive,                       // directory to watch 
      TRUE,                          // watch the subtree 
      FILE_NOTIFY_CHANGE_DIR_NAME);  // watch dir name changes 
 
   if (dwChangeHandles[1] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 

// Make a final validation check on our handles.

   if ((dwChangeHandles[0] == NULL) || (dwChangeHandles[1] == NULL))
   {
     printf("\n ERROR: Unexpected NULL from FindFirstChangeNotification.\n");
     ExitProcess(GetLastError()); 
   }

// Change notification is set. Now wait on both notification 
// handles and refresh accordingly. 
 
   while (TRUE) 
   { 
   // Wait for notification.
 
      printf("\nWaiting for notification...\n");

      dwWaitStatus = WaitForMultipleObjects(2, dwChangeHandles, 
         FALSE, INFINITE); 
 
      switch (dwWaitStatus) 
      { 
         case WAIT_OBJECT_0: 
 
         // A file was created, renamed, or deleted in the directory.
         // Refresh this directory and restart the notification.
 
             RefreshDirectory(lpDir); 
             if ( FindNextChangeNotification(dwChangeHandles[0]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_OBJECT_0 + 1: 
 
         // A directory was created, renamed, or deleted.
         // Refresh the tree and restart the notification.
 
             RefreshTree(lpDrive); 
             if (FindNextChangeNotification(dwChangeHandles[1]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_TIMEOUT:

         // A timeout occurred, this would happen if some value other 
         // than INFINITE is used in the Wait call and no changes occur.
         // In a single-threaded environment you might not want an
         // INFINITE wait.
 
            printf("\nNo changes in the timeout period.\n");
            break;

         default: 
            printf("\n ERROR: Unhandled dwWaitStatus.\n");
            ExitProcess(GetLastError());
            break;
      }
   }
}

void RefreshDirectory(LPTSTR lpDir)
{
   // This is where you might place code to refresh your
   // directory listing, but not the subtree because it
   // would not be necessary.

   _tprintf(TEXT("Directory (%s) changed.\n"), lpDir);
}

void RefreshTree(LPTSTR lpDrive)
{
   // This is where you might place code to refresh your
   // directory listing, including the subtree.

   _tprintf(TEXT("Directory tree (%s) changed.\n"), lpDrive);
}
```



 

 
