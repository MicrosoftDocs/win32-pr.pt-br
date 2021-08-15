---
description: Um aplicativo recebe um evento de dispositivo DBT DEVICEQUERYREMOVE quando um recurso no sistema decide \_ remover um dispositivo especificado.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Processamento de uma solicitação para remover um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6432ba2709dd05589acd5f8e0a2d1de6547216c9d24d4c9d742b9ad6dcc838e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956775"
---
# <a name="processing-a-request-to-remove-a-device"></a>Processamento de uma solicitação para remover um dispositivo

Um aplicativo recebe um evento de dispositivo [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) quando um recurso no sistema decide remover um dispositivo especificado. Quando o aplicativo recebe esse evento, ele deve determinar se está usando o dispositivo especificado e cancelar ou se preparar para a remoção.

No exemplo a seguir, um aplicativo mantém um controle aberto, hFile, para o arquivo ou dispositivo representado por FileName. O aplicativo registra-se para notificação de evento do dispositivo no dispositivo subjacente chamando a função [**RegisterDeviceNotification,**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) usando um filtro de notificação de tipo **\_ \_ HANDLE DEVTYP DBT** e especificando a variável hFile no membro **do identificador dbch \_** do filtro.

O aplicativo processa o evento de dispositivo [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) fechando o handle de arquivo aberto para o dispositivo que deve ser removido. Caso a remoção desse dispositivo seja cancelada, o aplicativo processa o evento de dispositivo [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) para reabrir o handle para o dispositivo. Depois que o dispositivo tiver sido removido do sistema, o aplicativo processa os eventos do dispositivo [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) e [DBT \_ DEVICEREMOVEPENDING,](dbt-deviceremovepending.md) removendo o registro do seu handle de notificação para o dispositivo e fechando todos os alças que ainda estão abertos para o dispositivo.


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
  // ...

INT_PTR WINAPI WinProcCallback( HWND hWnd,
                                UINT message,
                                WPARAM wParam,
                                LPARAM lParam )
{
  LPCTSTR FileName = NULL;              // path to the file or device of interest
  HANDLE  hFile = INVALID_HANDLE_VALUE; // handle to the file or device

  PDEV_BROADCAST_HDR    pDBHdr;
  PDEV_BROADCAST_HANDLE pDBHandle;
  TCHAR szMsg[80];

  switch (message)
  {
  //...
  case WM_DEVICECHANGE:
    switch (wParam)
    {
      case DBT_DEVICEQUERYREMOVE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // A request has been made to remove the device;
            // close any open handles to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }
        }
        return TRUE;

      case DBT_DEVICEQUERYREMOVEFAILED:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // Removal of the device has failed;
            // reopen a handle to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            hFile = CreateFile(FileName,
                       GENERIC_READ,
                       FILE_SHARE_READ,
                       NULL,
                       OPEN_EXISTING,
                       FILE_ATTRIBUTE_NORMAL,
                       NULL);
            if (hFile == INVALID_HANDLE_VALUE) 
            {
              StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                               TEXT("CreateFile failed: %lx.\n"), 
                               GetLastError());
              MessageBox(hWnd, szMsg, TEXT("CreateFile"), MB_OK);
            }
        }
        return TRUE;

      case DBT_DEVICEREMOVEPENDING:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
          
            // The device is being removed;
            // close any open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      case DBT_DEVICEREMOVECOMPLETE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            // The device has been removed from the system;
            // unregister its notification handle

            UnregisterDeviceNotification(
              pDBHandle->dbch_hdevnotify);
              
            // The device has been removed;
            // close any remaining open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      default:
        return TRUE;
    }
  }
  default:
    return TRUE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de evento de dispositivo](device-event-types.md)
</dt> </dl>

 

 



