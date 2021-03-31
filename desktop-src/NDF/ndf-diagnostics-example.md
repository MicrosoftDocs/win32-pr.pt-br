---
title: Exemplo de diagnóstico NDF
description: O exemplo a seguir mostra como iniciar a interface do usuário do NDF e diagnosticar a conectividade com o site http//www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fca4d54519988c3182b50a7c304f9c76a86392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005378"
---
# <a name="ndf-diagnostics-example"></a><span data-ttu-id="ab33d-103">Exemplo de diagnóstico NDF</span><span class="sxs-lookup"><span data-stu-id="ab33d-103">NDF Diagnostics Example</span></span>

<span data-ttu-id="ab33d-104">O exemplo a seguir mostra como iniciar a interface do usuário do NDF e diagnosticar a conectividade com o site https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="ab33d-104">The following example shows how to launch the NDF user interface and diagnose connectivity to the website https://www.microsoft.com.</span></span>


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



<span data-ttu-id="ab33d-105">A interface do usuário do NDF pode ser iniciada como uma janela modal.</span><span class="sxs-lookup"><span data-stu-id="ab33d-105">The NDF UI can be launched as a modal window.</span></span> <span data-ttu-id="ab33d-106">Para fazer isso, altere o segundo parâmetro de [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) de **NULL** para o identificador (HWND) da janela pai.</span><span class="sxs-lookup"><span data-stu-id="ab33d-106">To do so, change the second parameter of [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) from **NULL** to the handle (HWND) of the parent window.</span></span>

<span data-ttu-id="ab33d-107">Este exemplo pode ser modificado para diagnosticar outras áreas de rede.</span><span class="sxs-lookup"><span data-stu-id="ab33d-107">This example can be modified to diagnose other areas of networking.</span></span> <span data-ttu-id="ab33d-108">Para fazer isso, substitua a chamada [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) por uma das outras funções de criação de incidente, como [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) ou [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span><span class="sxs-lookup"><span data-stu-id="ab33d-108">To do so, replace the [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) call with one of the other incident creation functions, such as [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) or [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab33d-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab33d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab33d-110">**NdfCloseIncident**</span><span class="sxs-lookup"><span data-stu-id="ab33d-110">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[<span data-ttu-id="ab33d-111">**NdfCreateWebIncident**</span><span class="sxs-lookup"><span data-stu-id="ab33d-111">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[<span data-ttu-id="ab33d-112">**NdfExecuteDiagnosis**</span><span class="sxs-lookup"><span data-stu-id="ab33d-112">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




