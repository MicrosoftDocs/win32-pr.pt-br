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
# <a name="handling-video-device-loss"></a>Lidando com a perda de dispositivo de vídeo

Este tópico descreve como detectar a perda de dispositivo ao usar um dispositivo de captura de vídeo. Ele contém as seções a seguir:

-   [Registrar para notificação de dispositivo](#register-for-device-notification)
-   [Obter o link simbólico do dispositivo](#get-the-symbolic-link-of-the-device)
-   [Manipular o WM \_ DEVICECHANGE](/windows)
-   [Cancelar o registro para notificação](#unregister-for-notification)
-   [Tópicos relacionados](#related-topics)

## <a name="register-for-device-notification"></a>Registrar para notificação de dispositivo

Antes de iniciar a captura do dispositivo, chame a função [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) para registrar notificações de dispositivo. Registre-se para a classe de dispositivo de **\_ captura KSCATEGORY** , conforme mostrado no código a seguir.


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



## <a name="get-the-symbolic-link-of-the-device"></a>Obter o link simbólico do dispositivo

Enumere os dispositivos de vídeo no sistema, conforme descrito em [enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md). Escolha um dispositivo na lista e, em seguida, consulte o objeto de ativação para o atributo de [ \_ DEVSOURCE MF tipo de \_ \_ fonte VIDCAP de \_ \_ \_ \_ link simbólico](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , conforme mostrado no código a seguir.


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



## <a name="handle-wm_devicechange"></a>Manipular o WM \_ DEVICECHANGE

Em seu loop de mensagem, ouça as mensagens do [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) . O parâmetro de mensagem *lParam* é um ponteiro para uma estrutura [**HDR de \_ difusão \_ de dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .


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



Em seguida, compare a mensagem de notificação do dispositivo com o link simbólico do seu dispositivo, da seguinte maneira:

1.  Verifique o membro **dbch \_ DeviceType** da [**estrutura \_ \_ HDR de difusão de dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) . Se o valor for **DBT \_ DEVTYP \_ DEVICEINTERFACE**, converta o ponteiro de estrutura para uma estrutura [**\_ \_ DEVICEINTERFACE de difusão de desenvolvimento**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) .
2.  Compare o membro do **DBCC \_ Name** dessa estrutura com o link simbólico do dispositivo.


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



## <a name="unregister-for-notification"></a>Cancelar o registro para notificação

Antes de o aplicativo sair, chame [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) para cancelar o registro para notificações do dispositivo/


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 
