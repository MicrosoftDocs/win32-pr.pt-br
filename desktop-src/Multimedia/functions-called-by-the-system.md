---
title: Funções chamadas pelo sistema
description: Funções chamadas pelo sistema
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- áudio multimídia, funções do ACM
- áudio, funções do ACM
- gerenciador de compactação de áudio (ACM), funções
- ACM (gerenciador de compactação de áudio), funções
- Funções do ACM
- funções de retorno de chamada
- gerenciador de compactação de áudio (ACM), funções de retorno de chamada
- ACM (gerenciador de compactação de áudio), funções de retorno de chamada
- procedimentos de gancho
- procedimentos de driver
- gerenciador de compactação de áudio (ACM), procedimentos de gancho
- ACM (gerenciador de compactação de áudio), procedimentos de gancho
- gerenciador de compactação de áudio (ACM), procedimentos de driver
- ACM (gerenciador de compactação de áudio), procedimentos de driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b8a8c3615ae0124d4701f8d37d332e652d8390ef165cec8dc57d881cd328fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678608"
---
# <a name="functions-called-by-the-system"></a>Funções chamadas pelo sistema

O sistema chama três tipos diferentes de funções definidas pelo aplicativo. As funções de retorno de chamada são funções em seu aplicativo que o sistema chama em resposta a uma solicitação feita por um aplicativo. Os procedimentos de gancho ajudam um aplicativo a manipular a personalização de caixas de diálogo. Um procedimento de driver é a implementação de um aplicativo de seu próprio codec, conversor ou filtro.

As funções de retorno de chamada têm os seguintes nomes:

-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))

A maioria das funções de enumeração no ACM usa funções de retorno de chamada. Por exemplo, quando você chama uma função de enumeração, o ACM enumera os itens chamando repetidamente o aplicativo por meio da função de retorno de chamada.

Algumas funções não podem ser chamadas de dentro dessas funções de retorno de chamada. Funções que não podem ser chamadas manipulam estruturas ACM internas que são usadas pelas funções de enumeração. As seguintes funções não devem ser chamadas de dentro de uma função de retorno de chamada:

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

O sistema chama as seguintes funções para ajudar um aplicativo a lidar com a personalização de caixas de diálogo:

-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

A função a seguir é especificada como um protótipo que permite que um aplicativo use um codec, conversor ou filtro personalizado. Uma função em conformidade com esse protótipo pode ser passada como um argumento para [**a função acmDriverAdd.**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)

-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 