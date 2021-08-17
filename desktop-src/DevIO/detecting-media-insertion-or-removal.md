---
description: Windows envia todas as janelas de nível superior a um conjunto de mensagens padrão do WM \_ DEVICECHANGE quando novos dispositivos ou mídias (como um CD ou DVD) são adicionados e disponibilizados e quando dispositivos ou mídias existentes são removidos.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Detectando a inserção ou remoção de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3f6d579ed654ae2d2f77d00f70b88dc1441d03bbce59c0f8cb39ca6800c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318346"
---
# <a name="detecting-media-insertion-or-removal"></a>Detectando a inserção ou remoção de mídia

Windows envia todas as janelas de nível superior a um conjunto de mensagens padrão do [**WM \_ DEVICECHANGE**](wm-devicechange.md) quando novos dispositivos ou mídias (como um CD ou DVD) são adicionados e disponibilizados e quando dispositivos ou mídias existentes são removidos. Você não precisa se registrar para receber essas mensagens padrão. Consulte a seção comentários em [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obter detalhes sobre quais mensagens são enviadas por padrão. As mensagens no exemplo de código abaixo estão entre as mensagens padrão.

> [!Note]  
> Windows envia apenas [**mensagens \_ DEVICECHANGE do WM**](wm-devicechange.md) para eventos de mídia de CD ou DVD para janelas de nível superior que pertencem a aplicativos executados na sessão de console ativa. As janelas de nível superior que pertencem a aplicativos executados em uma sessão de área de trabalho remota não recebem mensagens do [**WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos de mídia de CD ou DVD.

 

Cada mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) tem um evento associado que descreve a alteração e uma estrutura que fornece informações detalhadas sobre a alteração. A estrutura consiste em um cabeçalho independente de evento, [**\_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), seguido por membros dependentes de evento. Os membros dependentes de evento descrevem o dispositivo ao qual o evento se aplica. Para usar essa estrutura, os aplicativos devem primeiro determinar o tipo de evento e o tipo de dispositivo. Em seguida, eles podem usar a estrutura correta para executar a ação apropriada.

Quando o usuário insere um novo CD ou DVD em uma unidade, os aplicativos recebem uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com um evento [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) . O aplicativo deve verificar o evento para garantir que o tipo de dispositivo que chega é um volume (o membro **dbch \_ DeviceType** é **DBT \_ DEVTYP \_ volume**) e que a alteração afeta a mídia (o membro **\_ sinalizadores dbcv** é a **\_ mídia DBTF**).

Quando o usuário remove um CD ou DVD de uma unidade, os aplicativos recebem uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com um evento [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) . Novamente, o aplicativo deve verificar o evento para garantir que o dispositivo que está sendo removido seja um volume e que a alteração afete a mídia.

O código a seguir demonstra como verificar a inserção ou a remoção de um CD ou DVD.


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
#pragma comment(lib, "user32.lib" )

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam );
char FirstDriveFromMask( ULONG unitmask );  //prototype

/*------------------------------------------------------------------
   Main_OnDeviceChange( hwnd, wParam, lParam )

   Description
      Handles WM_DEVICECHANGE messages sent to the application's
      top-level window.
--------------------------------------------------------------------*/

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam )
 {
  PDEV_BROADCAST_HDR lpdb = (PDEV_BROADCAST_HDR)lParam;
  TCHAR szMsg[80];

  switch(wParam )
   {
    case DBT_DEVICEARRIVAL:
      // Check whether a CD or DVD was inserted into a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media has arrived.\n"), 
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE"), MB_OK );
         }
       }
      break;

    case DBT_DEVICEREMOVECOMPLETE:
      // Check whether a CD or DVD was removed from a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media was removed.\n" ),
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE" ), MB_OK );
         }
       }
      break;

    default:
      /*
        Process other WM_DEVICECHANGE notifications for other 
        devices or reasons.
      */ 
      ;
   }
}

/*------------------------------------------------------------------
   FirstDriveFromMask( unitmask )

   Description
     Finds the first valid drive letter from a mask of drive letters.
     The mask must be in the format bit 0 = A, bit 1 = B, bit 2 = C, 
     and so on. A valid drive letter is defined when the 
     corresponding bit is set to 1.

   Returns the first drive letter that was found.
--------------------------------------------------------------------*/

char FirstDriveFromMask( ULONG unitmask )
 {
  char i;

  for (i = 0; i < 26; ++i)
   {
    if (unitmask & 0x1)
      break;
    unitmask = unitmask >> 1;
   }

  return( i + 'A' );
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> </dl>

 

 



