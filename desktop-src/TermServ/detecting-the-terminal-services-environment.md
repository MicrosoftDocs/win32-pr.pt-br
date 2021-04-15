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
# <a name="detecting-the-remote-desktop-services-environment"></a><span data-ttu-id="a5e6f-103">Detectando o ambiente de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="a5e6f-103">Detecting the Remote Desktop Services environment</span></span>

<span data-ttu-id="a5e6f-104">Para otimizar o desempenho, é uma boa prática para os aplicativos detectarem se eles estão sendo executados em uma sessão de cliente Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-104">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span> <span data-ttu-id="a5e6f-105">Por exemplo, quando um aplicativo é executado em uma sessão remota, ele deve eliminar efeitos gráficos desnecessários, conforme descrito em [efeitos gráficos](graphic-effects.md).</span><span class="sxs-lookup"><span data-stu-id="a5e6f-105">For example, when an application is running on a remote session, it should eliminate unnecessary graphic effects, as described in [Graphic Effects](graphic-effects.md).</span></span> <span data-ttu-id="a5e6f-106">Se o usuário estiver executando o aplicativo em um ambiente local, não será tão importante para o aplicativo otimizar seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-106">If the user is running the application in a local environment, it is not as critical for the application to optimize its behavior.</span></span>

<span data-ttu-id="a5e6f-107">O exemplo a seguir mostra uma função que retorna **true** se o aplicativo estiver sendo executado em uma sessão remota e **false** se o aplicativo estiver em execução no console do.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-107">The following example shows a function that returns **TRUE** if the application is running in a remote session and **FALSE** if the application is running on the console.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



<span data-ttu-id="a5e6f-108">Para obter mais informações, consulte [vinculação de tempo de execução para Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a5e6f-108">For more information, see [Run-time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="a5e6f-109">Você não deve usar o **GetSystemMetrics (SM \_ REMOTESESSION)** para determinar se seu aplicativo está sendo executado em uma sessão remota no Windows 8 e posterior ou no Windows Server 2012 e posterior se a sessão remota também pode usar os aprimoramentos de vGPU do RemoteFX para o protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-109">You should not use **GetSystemMetrics(SM\_REMOTESESSION)** to determine if your application is running in a remote session in Windows 8 and later or Windows Server 2012 and later if the remote session may also be using the RemoteFX vGPU improvements to the Microsoft Remote Display Protocol (RDP).</span></span> <span data-ttu-id="a5e6f-110">Nesse caso, **GetSystemMetrics (SM \_ REMOTESESSION)** identificará a sessão remota como uma sessão local.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-110">In this case, **GetSystemMetrics(SM\_REMOTESESSION)** will identify the remote session as a local session.</span></span>

<span data-ttu-id="a5e6f-111">Seu aplicativo pode verificar a seguinte chave do registro para determinar se a sessão é uma sessão remota que usa vGPU RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-111">Your application can check the following registry key to determine whether the session is a remote session that uses RemoteFX vGPU.</span></span> <span data-ttu-id="a5e6f-112">Se existir uma sessão local, essa chave do registro fornecerá a ID da sessão local.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-112">If a local session exists, this registry key provides the ID of the local session.</span></span>

<span data-ttu-id="a5e6f-113">**HKEY \_ local \_ \\ System sistema \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**</span><span class="sxs-lookup"><span data-stu-id="a5e6f-113">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Terminal Server\\GlassSessionId**</span></span>

<span data-ttu-id="a5e6f-114">Se a ID da sessão atual na qual o aplicativo está sendo executado for a mesma da chave do registro, o aplicativo será executado em uma sessão local.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-114">If the ID of the current session in which the application is running is the same as in the registry key, the application is running in a local session.</span></span> <span data-ttu-id="a5e6f-115">As sessões identificadas como sessão remota dessa maneira incluem sessões remotas que usam vGPU RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-115">Sessions identified as remote session in this way include remote sessions that use RemoteFX vGPU.</span></span> <span data-ttu-id="a5e6f-116">O código de exemplo a seguir demonstra isso.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-116">The following sample code demonstrates this.</span></span>


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



 

 




