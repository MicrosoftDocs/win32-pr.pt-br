---
title: Exemplo de diagnóstico NDF
description: O exemplo a seguir mostra como iniciar a interface do usuário do NDF e diagnosticar a conectividade com o site http//www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa1971da12b7d707dc74b34497dff630ee8fdd8f93d5737ae3757bdde129fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802366"
---
# <a name="ndf-diagnostics-example"></a>Exemplo de diagnóstico NDF

O exemplo a seguir mostra como iniciar a interface do usuário do NDF e diagnosticar a conectividade com o site https://www.microsoft.com .


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



A interface do usuário do NDF pode ser iniciada como uma janela modal. Para fazer isso, altere o segundo parâmetro de [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) de **NULL** para o identificador (HWND) da janela pai.

Este exemplo pode ser modificado para diagnosticar outras áreas de rede. Para fazer isso, substitua a chamada [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) por uma das outras funções de criação de incidente, como [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) ou [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




