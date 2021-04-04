---
description: Descreve como detectar se um conjunto de API específico está disponível no dispositivo atual.
title: Detectar disponibilidade do conjunto de API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 7117ae82f142315a3e5f28065583381ef6af67f3
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/24/2020
ms.locfileid: "104084996"
---
# <a name="detect-api-set-availability"></a><span data-ttu-id="cf98d-103">Detectar disponibilidade do conjunto de API</span><span class="sxs-lookup"><span data-stu-id="cf98d-103">Detect API set availability</span></span>

<span data-ttu-id="cf98d-104">Em alguns casos, um determinado nome de contrato de conjunto de API pode ser mapeado intencionalmente para um nome de módulo vazio em alguns dispositivos Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf98d-104">In some cases, a given API set contract name may be intentionally mapped to an empty module name on some Windows 10 devices.</span></span> <span data-ttu-id="cf98d-105">Os motivos para isso variam, mas um exemplo comum é que um recurso caro em termos de recursos do sistema pode ser removido do sistema operacional Windows quando configurado para um dispositivo com restrição de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf98d-105">The reasons for this vary, but a common example is that an expensive feature in terms of system resources may be removed from the Windows OS when configured for a resource-constrained device.</span></span> <span data-ttu-id="cf98d-106">Isso representa um desafio para que os aplicativos manipulem normalmente recursos opcionais no nível da API.</span><span class="sxs-lookup"><span data-stu-id="cf98d-106">This poses a challenge for applications to gracefully handle optional features at the API level.</span></span>

<span data-ttu-id="cf98d-107">A abordagem tradicional para testar se uma API Win32 está disponível é usar [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="cf98d-107">The traditional approach for testing whether a Win32 API is available is to use [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="cf98d-108">No entanto, esses não são meios confiáveis para testar os conjuntos de API devido ao suporte de [encaminhamento reverso](api-set-loader-operation.md#reverse-forwarding) no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf98d-108">However, these are not a reliable means for testing API sets because of the [reverse forwarding](api-set-loader-operation.md#reverse-forwarding) support in Windows 10.</span></span> <span data-ttu-id="cf98d-109">Quando o encaminhamento reverso é aplicado a uma determinada API, **LoadLibrary** ou **GetProcAddress** pode resolver para um ponteiro de função válido mesmo nos casos em que a implementação interna foi removida.</span><span class="sxs-lookup"><span data-stu-id="cf98d-109">When reverse forwarding is applied to a given API, **LoadLibrary** or **GetProcAddress** may resolve to a valid function pointer even in cases where the internal implementation has been removed.</span></span> <span data-ttu-id="cf98d-110">Nesse caso, o ponteiro de função estará apontando para uma função de stub que simplesmente retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="cf98d-110">In this case, the function pointer will be pointing to a stub function that simply returns an error.</span></span>

<span data-ttu-id="cf98d-111">Para detectar esse caso, você pode usar a função [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) para consultar a disponibilidade subjacente de uma determinada implementação de API.</span><span class="sxs-lookup"><span data-stu-id="cf98d-111">In order to detect this case, you can use the [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) function to query the underlying availability of a given API implementation.</span></span> <span data-ttu-id="cf98d-112">Esse teste valida que chamar essa função resultará na execução de uma implementação funcional da API.</span><span class="sxs-lookup"><span data-stu-id="cf98d-112">This test validates that calling this function will result in executing a functional implementation of the API.</span></span>

<span data-ttu-id="cf98d-113">O exemplo de código a seguir demonstra como usar **IsApiSetImplemented** para determinar se a função [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) está disponível no dispositivo atual antes de chamá-lo.</span><span class="sxs-lookup"><span data-stu-id="cf98d-113">The following code example demonstrates how to use **IsApiSetImplemented** to determine whether the [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) function is available on the current device before calling it.</span></span> 

```c++
#include <windows.h>
#include <stdio.h>
#include <Wtsapi32.h>

int __cdecl wmain(int /* argc */, PCWSTR /* argv */ [])
{
    PWTS_SESSION_INFO pInfo = {};
    DWORD count = 0;

    if (!IsApiSetImplemented("ext-ms-win-session-wtsapi32-l1-1-0"))
    {
        wprintf(L"IsApiSetImplemented on ext-ms-win-session-wtsapi32-l1-1-0 returns FALSE\n");
    }
    else
    {
        if (WTSEnumerateSessionsW(WTS_CURRENT_SERVER_HANDLE, 0, 1, &pInfo, &count))
        {
            wprintf(L"SessionCount = %d\n", count);

            for (ULONG i = 0; i < count; i++)
            {
                PWTS_SESSION_INFO pCurInfo = &pInfo[i];
                wprintf(L"    %s: ID = %d, state = %d\n", pCurInfo->pWinStationName, 
                    pCurInfo->SessionId, pCurInfo->State);
            }

            WTSFreeMemory(pInfo);
        }
        else
        {
            wprintf(L"WTSEnumerateSessions failure : %x\n", GetLastError());
        }
    }

    return 0;
}
```