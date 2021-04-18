---
title: Funções chamadas pelo sistema
description: Funções chamadas pelo sistema
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- áudio de multimídia, funções do ACM
- áudio, funções do ACM
- Gerenciador de compactação de áudio (ACM), funções
- ACM (Gerenciador de compactação de áudio), funções
- Funções do ACM
- funções de retorno de chamada
- Gerenciador de compactação de áudio (ACM), funções de retorno de chamada
- ACM (Gerenciador de compactação de áudio), funções de retorno de chamada
- procedimentos de gancho
- procedimentos de driver
- Gerenciador de compactação de áudio (ACM), procedimentos de conexão
- ACM (Gerenciador de compactação de áudio), procedimentos de conexão
- Gerenciador de compactação de áudio (ACM), procedimentos de driver
- ACM (Gerenciador de compactação de áudio), procedimentos de driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105749775"
---
# <a name="functions-called-by-the-system"></a>Funções chamadas pelo sistema

O sistema chama três tipos diferentes de funções definidas pelo aplicativo. As funções de retorno de chamada são funções em seu aplicativo que o sistema chama em resposta a uma solicitação feita por um aplicativo. Os procedimentos de gancho ajudam um aplicativo a lidar com a personalização de caixas de diálogo. Um procedimento de driver é a implementação de um aplicativo de seu próprio codec, conversor ou filtro.

As funções de retorno de chamada têm os seguintes nomes:

-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))

A maioria das funções de enumeração no ACM usa funções de retorno de chamada. Por exemplo, quando você chama uma função de enumeração, o ACM enumera os itens chamando repetidamente o aplicativo por meio da função de retorno de chamada.

Algumas funções não podem ser chamadas de dentro dessas funções de retorno de chamada. Funções que não podem ser chamadas manipular estruturas do ACM internas que são usadas pelas funções de enumeração. As funções a seguir não devem ser chamadas de dentro de uma função de retorno de chamada:

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

O sistema chama as seguintes funções para ajudar um aplicativo a lidar com a personalização de caixas de diálogo:

-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

A função a seguir é especificada como um protótipo que permite que um aplicativo use um codec, conversor ou filtro personalizado. Uma função que está de acordo com esse protótipo pode ser passada como um argumento para a função [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .

-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 