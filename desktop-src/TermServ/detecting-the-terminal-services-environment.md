---
title: Detectando o ambiente de Serviços de Área de Trabalho Remota
description: Para otimizar o desempenho, é uma boa prática para os aplicativos detectarem se eles estão sendo executados em uma sessão de cliente Serviços de Área de Trabalho Remota.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde3263925a3b8bf4921dd0dfc95842a5dc5b4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498704"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>Detectando o ambiente de Serviços de Área de Trabalho Remota

Para otimizar o desempenho, é uma boa prática para os aplicativos detectarem se eles estão sendo executados em uma sessão de cliente Serviços de Área de Trabalho Remota. Por exemplo, quando um aplicativo é executado em uma sessão remota, ele deve eliminar efeitos gráficos desnecessários, conforme descrito em [efeitos gráficos](graphic-effects.md). Se o usuário estiver executando o aplicativo em um ambiente local, não será tão importante para o aplicativo otimizar seu comportamento.

O exemplo a seguir mostra uma função que retorna **true** se o aplicativo estiver sendo executado em uma sessão remota e **false** se o aplicativo estiver em execução no console do.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Para obter mais informações, consulte [vinculação de tempo de execução para Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Você não deve usar o **GetSystemMetrics (SM \_ REMOTESESSION)** para determinar se seu aplicativo está sendo executado em uma sessão remota no Windows 8 e posterior ou no Windows Server 2012 e posterior se a sessão remota também pode usar os aprimoramentos de vGPU do RemoteFX para o protocolo RDP. Nesse caso, **GetSystemMetrics (SM \_ REMOTESESSION)** identificará a sessão remota como uma sessão local.

Seu aplicativo pode verificar a seguinte chave do registro para determinar se a sessão é uma sessão remota que usa vGPU RemoteFX. Se existir uma sessão local, essa chave do registro fornecerá a ID da sessão local.

**HKEY \_ local \_ \\ System sistema \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

Se a ID da sessão atual na qual o aplicativo está sendo executado for a mesma da chave do registro, o aplicativo será executado em uma sessão local. As sessões identificadas como sessão remota dessa maneira incluem sessões remotas que usam vGPU RemoteFX. O código de exemplo a seguir demonstra isso.


```C++
#define TERMINAL_SERVER_KEY _T("SYSTEM\\CurrentControlSet\\Control\\Terminal Server\\")
#define GLASS_SESSION_ID    _T("GlassSessionId")

BOOL
IsCurrentSessionRemoteable()
{
    BOOL fIsRemoteable = FALSE;
                                       
    if (GetSystemMetrics(SM_REMOTESESSION)) 
    {
        fIsRemoteable = TRUE;
    }
    else
    {
        HKEY hRegKey = NULL;
        LONG lResult;

        lResult = RegOpenKeyEx(
            HKEY_LOCAL_MACHINE,
            TERMINAL_SERVER_KEY,
            0, // ulOptions
            KEY_READ,
            &hRegKey
            );

        if (lResult == ERROR_SUCCESS)
        {
            DWORD dwGlassSessionId;
            DWORD cbGlassSessionId = sizeof(dwGlassSessionId);
            DWORD dwType;

            lResult = RegQueryValueEx(
                hRegKey,
                GLASS_SESSION_ID,
                NULL, // lpReserved
                &dwType,
                (BYTE*) &dwGlassSessionId,
                &cbGlassSessionId
                );

            if (lResult == ERROR_SUCCESS)
            {
                DWORD dwCurrentSessionId;

                if (ProcessIdToSessionId(GetCurrentProcessId(), &dwCurrentSessionId))
                {
                    fIsRemoteable = (dwCurrentSessionId != dwGlassSessionId);
                }
            }
        }

        if (hRegKey)
        {
            RegCloseKey(hRegKey);
        }
    }

    return fIsRemoteable;
}
```



 

 




