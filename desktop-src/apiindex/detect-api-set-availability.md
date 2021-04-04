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
# <a name="detect-api-set-availability"></a>Detectar disponibilidade do conjunto de API

Em alguns casos, um determinado nome de contrato de conjunto de API pode ser mapeado intencionalmente para um nome de módulo vazio em alguns dispositivos Windows 10. Os motivos para isso variam, mas um exemplo comum é que um recurso caro em termos de recursos do sistema pode ser removido do sistema operacional Windows quando configurado para um dispositivo com restrição de recursos. Isso representa um desafio para que os aplicativos manipulem normalmente recursos opcionais no nível da API.

A abordagem tradicional para testar se uma API Win32 está disponível é usar [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). No entanto, esses não são meios confiáveis para testar os conjuntos de API devido ao suporte de [encaminhamento reverso](api-set-loader-operation.md#reverse-forwarding) no Windows 10. Quando o encaminhamento reverso é aplicado a uma determinada API, **LoadLibrary** ou **GetProcAddress** pode resolver para um ponteiro de função válido mesmo nos casos em que a implementação interna foi removida. Nesse caso, o ponteiro de função estará apontando para uma função de stub que simplesmente retorna um erro.

Para detectar esse caso, você pode usar a função [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) para consultar a disponibilidade subjacente de uma determinada implementação de API. Esse teste valida que chamar essa função resultará na execução de uma implementação funcional da API.

O exemplo de código a seguir demonstra como usar **IsApiSetImplemented** para determinar se a função [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) está disponível no dispositivo atual antes de chamá-lo. 

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