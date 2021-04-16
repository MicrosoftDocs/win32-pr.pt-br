---
description: Este tópico descreve como detectar a perda de dispositivo ao usar um dispositivo de captura de vídeo.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Lidando com a perda de dispositivo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d083ebeb1203b0bba49a63745f62a4dff6b231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808195"
---
# <a name="handling-video-device-loss"></a><span data-ttu-id="9173d-103">Lidando com a perda de dispositivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="9173d-103">Handling Video Device Loss</span></span>

<span data-ttu-id="9173d-104">Este tópico descreve como detectar a perda de dispositivo ao usar um dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9173d-104">This topic describes how to detect device loss when using a video capture device.</span></span> <span data-ttu-id="9173d-105">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="9173d-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="9173d-106">Registrar para notificação de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9173d-106">Register For Device Notification</span></span>](#register-for-device-notification)
-   [<span data-ttu-id="9173d-107">Obter o link simbólico do dispositivo</span><span class="sxs-lookup"><span data-stu-id="9173d-107">Get the Symbolic Link of the Device</span></span>](#get-the-symbolic-link-of-the-device)
-   [<span data-ttu-id="9173d-108">Manipular o WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="9173d-108">Handle WM\_DEVICECHANGE</span></span>](/windows)
-   [<span data-ttu-id="9173d-109">Cancelar o registro para notificação</span><span class="sxs-lookup"><span data-stu-id="9173d-109">Unregister For Notification</span></span>](#unregister-for-notification)
-   [<span data-ttu-id="9173d-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9173d-110">Related topics</span></span>](#related-topics)

## <a name="register-for-device-notification"></a><span data-ttu-id="9173d-111">Registrar para notificação de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9173d-111">Register For Device Notification</span></span>

<span data-ttu-id="9173d-112">Antes de iniciar a captura do dispositivo, chame a função [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) para registrar notificações de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9173d-112">Before you start capturing from the device, call the [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) function to register for device notifications.</span></span> <span data-ttu-id="9173d-113">Registre-se para a classe de dispositivo de **\_ captura KSCATEGORY** , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9173d-113">Register for the **KSCATEGORY\_CAPTURE** device class, as shown in the following code.</span></span>


```C++
#include <Dbt.h>
#include <ks.h>
#include <ksmedia.h>

HDEVNOTIFY  g_hdevnotify = NULL;

BOOL RegisterForDeviceNotification(HWND hwnd)
{
    DEV_BROADCAST_DEVICEINTERFACE di = { 0 };
    di.dbcc_size = sizeof(di);
    di.dbcc_devicetype  = DBT_DEVTYP_DEVICEINTERFACE;
    di.dbcc_classguid  = KSCATEGORY_CAPTURE; 

    g_hdevnotify = RegisterDeviceNotification(
        hwnd,
        &di,
        DEVICE_NOTIFY_WINDOW_HANDLE
        );

    if (g_hdevnotify == NULL)
    {
        return FALSE;
    }

    return TRUE;
}
```



## <a name="get-the-symbolic-link-of-the-device"></a><span data-ttu-id="9173d-114">Obter o link simbólico do dispositivo</span><span class="sxs-lookup"><span data-stu-id="9173d-114">Get the Symbolic Link of the Device</span></span>

<span data-ttu-id="9173d-115">Enumere os dispositivos de vídeo no sistema, conforme descrito em [enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="9173d-115">Enumerate the video devices on the system, as described in [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span> <span data-ttu-id="9173d-116">Escolha um dispositivo na lista e, em seguida, consulte o objeto de ativação para o atributo de [ \_ DEVSOURCE MF tipo de \_ \_ fonte VIDCAP de \_ \_ \_ \_ link simbólico](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9173d-116">Choose a device from the list, and then query the activation object for the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute, as shown in the following code.</span></span>


```C++
WCHAR      *g_pwszSymbolicLink = NULL;
UINT32     g_cchSymbolicLink = 0;

HRESULT GetSymbolicLink(IMFActivate *pActivate)
{
    return pActivate->GetAllocatedString(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
        &g_pwszSymbolicLink,
        &g_cchSymbolicLink
        );
}
```



## <a name="handle-wm_devicechange"></a><span data-ttu-id="9173d-117">Manipular o WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="9173d-117">Handle WM\_DEVICECHANGE</span></span>

<span data-ttu-id="9173d-118">Em seu loop de mensagem, ouça as mensagens do [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="9173d-118">In your message loop, listen for [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) messages.</span></span> <span data-ttu-id="9173d-119">O parâmetro de mensagem *lParam* é um ponteiro para uma estrutura [**HDR de \_ difusão \_ de dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="9173d-119">The *lParam* message parameter is a pointer to a [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span>


```C++
    case WM_DEVICECHANGE:
        if (lParam != 0)
        {
            HRESULT hr = S_OK;
            BOOL bDeviceLost = FALSE;

            hr = CheckDeviceLost((PDEV_BROADCAST_HDR)lParam, &bDeviceLost);

            if (FAILED(hr) || bDeviceLost)
            {
                CloseDevice();

                MessageBox(hwnd, L"Lost the capture device.", NULL, MB_OK);
            }
        }
        return TRUE;
```



<span data-ttu-id="9173d-120">Em seguida, compare a mensagem de notificação do dispositivo com o link simbólico do seu dispositivo, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9173d-120">Next, compare the device notification message against the symbolic link of your device, as follows:</span></span>

1.  <span data-ttu-id="9173d-121">Verifique o membro **dbch \_ DeviceType** da [**estrutura \_ \_ HDR de difusão de dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="9173d-121">Check the **dbch\_devicetype** member of the [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="9173d-122">Se o valor for **DBT \_ DEVTYP \_ DEVICEINTERFACE**, converta o ponteiro de estrutura para uma estrutura [**\_ \_ DEVICEINTERFACE de difusão de desenvolvimento**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) .</span><span class="sxs-lookup"><span data-stu-id="9173d-122">If the value is **DBT\_DEVTYP\_DEVICEINTERFACE**, cast the structure pointer to a [**DEV\_BROADCAST\_DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) structure.</span></span>
2.  <span data-ttu-id="9173d-123">Compare o membro do **DBCC \_ Name** dessa estrutura com o link simbólico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9173d-123">Compare the **dbcc\_name** member of this structure to the symbolic link of the device.</span></span>


```C++
HRESULT CheckDeviceLost(DEV_BROADCAST_HDR *pHdr, BOOL *pbDeviceLost)
{
    DEV_BROADCAST_DEVICEINTERFACE *pDi = NULL;

    if (pbDeviceLost == NULL)
    {
        return E_POINTER;
    }

    *pbDeviceLost = FALSE;
    
    if (g_pSource == NULL)
    {
        return S_OK;
    }
    if (pHdr == NULL)
    {
        return S_OK;
    }
    if (pHdr->dbch_devicetype != DBT_DEVTYP_DEVICEINTERFACE)
    {
        return S_OK;
    }

    // Compare the device name with the symbolic link.

    pDi = (DEV_BROADCAST_DEVICEINTERFACE*)pHdr;

    if (g_pwszSymbolicLink)
    {
        if (_wcsicmp(g_pwszSymbolicLink, pDi->dbcc_name) == 0)
        {
            *pbDeviceLost = TRUE;
        }
    }

    return S_OK;
}
```



## <a name="unregister-for-notification"></a><span data-ttu-id="9173d-124">Cancelar o registro para notificação</span><span class="sxs-lookup"><span data-stu-id="9173d-124">Unregister For Notification</span></span>

<span data-ttu-id="9173d-125">Antes de o aplicativo sair, chame [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) para cancelar o registro para notificações do dispositivo/</span><span class="sxs-lookup"><span data-stu-id="9173d-125">Before the application exits, call [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) to unregister for device notifications/</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    if (g_hdevnotify)
    {
        UnregisterDeviceNotification(g_hdevnotify);
    }

    PostQuitMessage(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="9173d-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9173d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9173d-127">Enumerando dispositivos de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="9173d-127">Enumerating Video Capture Devices</span></span>](enumerating-video-capture-devices.md)
</dt> <dt>

[<span data-ttu-id="9173d-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="9173d-128">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
