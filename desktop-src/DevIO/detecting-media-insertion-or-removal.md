---
description: O Windows envia todas as janelas de nível superior a um conjunto de mensagens padrão do WM \_ DEVICECHANGE quando novos dispositivos ou mídias (como um CD ou DVD) são adicionados e disponibilizados e quando dispositivos ou mídias existentes são removidos.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Detectando a inserção ou remoção de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6cfd4539d6f2ce5eac41e355f56a5a87835505
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091881"
---
# <a name="detecting-media-insertion-or-removal"></a><span data-ttu-id="1cbc9-103">Detectando a inserção ou remoção de mídia</span><span class="sxs-lookup"><span data-stu-id="1cbc9-103">Detecting Media Insertion or Removal</span></span>

<span data-ttu-id="1cbc9-104">O Windows envia todas as janelas de nível superior a um conjunto de mensagens padrão do [**WM \_ DEVICECHANGE**](wm-devicechange.md) quando novos dispositivos ou mídias (como um CD ou DVD) são adicionados e disponibilizados e quando dispositivos ou mídias existentes são removidos.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-104">Windows sends all top-level windows a set of default [**WM\_DEVICECHANGE**](wm-devicechange.md) messages when new devices or media (such as a CD or DVD) are added and become available, and when existing devices or media are removed.</span></span> <span data-ttu-id="1cbc9-105">Você não precisa se registrar para receber essas mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-105">You do not need to register to receive these default messages.</span></span> <span data-ttu-id="1cbc9-106">Consulte a seção comentários em [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obter detalhes sobre quais mensagens são enviadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details on which messages are sent by default.</span></span> <span data-ttu-id="1cbc9-107">As mensagens no exemplo de código abaixo estão entre as mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-107">The messages in the code example below are among the default messages.</span></span>

> [!Note]  
> <span data-ttu-id="1cbc9-108">O Windows envia somente mensagens do [**WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos de mídia de CD ou DVD para janelas de nível superior que pertencem a aplicativos executados na sessão de console ativa.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-108">Windows only sends [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events to top-level windows that are owned by applications that run in the active console session.</span></span> <span data-ttu-id="1cbc9-109">As janelas de nível superior que pertencem a aplicativos executados em uma sessão de área de trabalho remota não recebem mensagens do [**WM \_ DEVICECHANGE**](wm-devicechange.md) para eventos de mídia de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-109">Top-level windows that are owned by applications that run in a remote desktop session do not receive [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events.</span></span>

 

<span data-ttu-id="1cbc9-110">Cada mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) tem um evento associado que descreve a alteração e uma estrutura que fornece informações detalhadas sobre a alteração.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-110">Each [**WM\_DEVICECHANGE**](wm-devicechange.md) message has an associated event that describes the change, and a structure that provides detailed information about the change.</span></span> <span data-ttu-id="1cbc9-111">A estrutura consiste em um cabeçalho independente de evento, [**\_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), seguido por membros dependentes de evento.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-111">The structure consists of an event-independent header, [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), followed by event-dependent members.</span></span> <span data-ttu-id="1cbc9-112">Os membros dependentes de evento descrevem o dispositivo ao qual o evento se aplica.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-112">The event-dependent members describe the device to which the event applies.</span></span> <span data-ttu-id="1cbc9-113">Para usar essa estrutura, os aplicativos devem primeiro determinar o tipo de evento e o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-113">To use this structure, applications must first determine the event type and the device type.</span></span> <span data-ttu-id="1cbc9-114">Em seguida, eles podem usar a estrutura correta para executar a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-114">Then, they can use the correct structure to take appropriate action.</span></span>

<span data-ttu-id="1cbc9-115">Quando o usuário insere um novo CD ou DVD em uma unidade, os aplicativos recebem uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com um evento [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) .</span><span class="sxs-lookup"><span data-stu-id="1cbc9-115">When the user inserts a new CD or DVD into a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEARRIVAL](dbt-devicearrival.md) event.</span></span> <span data-ttu-id="1cbc9-116">O aplicativo deve verificar o evento para garantir que o tipo de dispositivo que chega é um volume (o membro **dbch \_ DeviceType** é **DBT \_ DEVTYP \_ volume**) e que a alteração afeta a mídia (o membro **\_ sinalizadores dbcv** é a **\_ mídia DBTF**).</span><span class="sxs-lookup"><span data-stu-id="1cbc9-116">The application must check the event to ensure that the type of device arriving is a volume (the **dbch\_devicetype** member is **DBT\_DEVTYP\_VOLUME**) and that the change affects the media (the **dbcv\_flags** member is **DBTF\_MEDIA**).</span></span>

<span data-ttu-id="1cbc9-117">Quando o usuário remove um CD ou DVD de uma unidade, os aplicativos recebem uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com um evento [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="1cbc9-117">When the user removes a CD or DVD from a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) event.</span></span> <span data-ttu-id="1cbc9-118">Novamente, o aplicativo deve verificar o evento para garantir que o dispositivo que está sendo removido seja um volume e que a alteração afete a mídia.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-118">Again, the application must check the event to ensure that the device being removed is a volume and that the change affects the media.</span></span>

<span data-ttu-id="1cbc9-119">O código a seguir demonstra como verificar a inserção ou a remoção de um CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="1cbc9-119">The following code demonstrates how to check for insertion or removal of a CD or DVD.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1cbc9-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1cbc9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cbc9-121">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="1cbc9-121">Device Events</span></span>](device-events.md)
</dt> </dl>

 

 



