---
description: A especificação TSPI está muito relacionada às especificações da TAPI 2,2 (TAPI/C).
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: Comparação geral com a TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecedd5a53fd30e2a49b6d44e90d30f86ff8469f002166ca3328f3146a2748b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002804"
---
# <a name="overall-comparison-with-tapi"></a>Comparação geral com a TAPI

A especificação TSPI está muito relacionada às especificações da TAPI 2,2 (TAPI/C). A maioria das funções em uma tem uma função correspondente no outro. A correspondência usual é a seguinte:

-   As funções TSPI têm os mesmos nomes que as funções TAPI, exceto que elas são precedidas por "**TSPI \_**". Por exemplo, a função TAPI [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept) corresponde à função TSPI [**TSPI \_ lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept).
-   Procedimentos que permitem a operação assíncrona inserem um parâmetro *dwRequestID* do tipo [drv \_ REQUESTID](drv-requestid.md) como seu primeiro parâmetro. Esse parâmetro especifica o valor a ser retornado para indicar a operação assíncrona e para reportar a conclusão assíncrona.
-   os parâmetros *hCall* do tipo hCall são substituídos por parâmetros *HdCall* do tipo [HDRVCALL](hdrvline.md), indicando o identificador do provedor de serviços para a chamada.
-   os parâmetros *hLine* do tipo hLine são substituídos por parâmetros *HdLine* do tipo [HDRVLINE](hdrvline.md), indicando o identificador do provedor de serviços para a linha.
-   os parâmetros *hPhone* do tipo hPhone são substituídos por parâmetros *HdPhone* do tipo [HDRVPHONE](hdrvphone.md), indicando o identificador do provedor de serviços para o telefone.
-   Procedimentos que criam uma nova chamada, como [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), substituem um único parâmetro *lphCall* por dois parâmetros: um *htCall* do parâmetro Type [HTAPICALL](htapicall.md) que passa no identificador TAPI para a chamada e um *lphdCall* do tipo LPHDRVCALL que indica o local para o qual o provedor de serviços deve gravar seu novo identificador para a chamada. Uma divisão de parâmetros semelhante ocorre em [**TSPI \_ LineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) e [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen).
-   No nível de TSPI, não há noção de "privilégio" associado a identificadores de dispositivo. Além disso, no nível da API, cada aplicativo que tem um dispositivo ou identificador de chamada tem um identificador diferente, mas a TAPI mescla esses em um único identificador no lado do provedor de serviço. Como consequência, os códigos de erro e as mensagens de status relacionadas ao privilégio e ao número de clientes que usam um dispositivo não aparecem no nível de TSPI.

O conjunto de funções TAPI não mapeia um para um no conjunto de funções TSPI. Em particular, as funções relacionadas ao privilégio, à conversão de números de telefone e à comunicação entre aplicativos são manipuladas pela TAPI e não têm nenhuma função correspondente no TSPI. Outras funções, como as usadas para a configuração e a inicialização do provedor de serviços, não têm funções correspondentes na TAPI.

 

 
