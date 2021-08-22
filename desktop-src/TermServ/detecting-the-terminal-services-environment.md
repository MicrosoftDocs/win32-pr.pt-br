---
title: Detectando o ambiente de Serviços de Área de Trabalho Remota
description: Para otimizar o desempenho, é uma boa prática para os aplicativos detectarem se eles estão sendo executados em uma sessão de cliente Serviços de Área de Trabalho Remota.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f54634112b4a6ac3cc1e981421e4a3e33af5e32bae8ab63ec8690f2df12c7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657986"
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

você não deve usar **GetSystemMetrics (SM \_ REMOTESESSION)** para determinar se o aplicativo está sendo executado em uma sessão remota no Windows 8 e posterior ou Windows Server 2012 e posterior se a sessão remota também pode usar as melhorias RemoteFX vGPU no protocolo RDP. Nesse caso, **GetSystemMetrics (SM \_ REMOTESESSION)** identificará a sessão remota como uma sessão local.

seu aplicativo pode verificar a seguinte chave do registro para determinar se a sessão é uma sessão remota que usa RemoteFX vGPU. Se existir uma sessão local, essa chave do registro fornecerá a ID da sessão local.

**HKEY \_ local \_ \\ System sistema \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

Se a ID da sessão atual na qual o aplicativo está sendo executado for a mesma da chave do registro, o aplicativo será executado em uma sessão local. as sessões identificadas como sessão remota dessa maneira incluem sessões remotas que usam RemoteFX vGPU. O código de exemplo a seguir demonstra isso.


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



 

 




