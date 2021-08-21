---
description: A TAPI fornece várias funções para manipular identificadores de chamada, determinando a relação entre linhas, chamadas e endereço, e assim por diante.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Manipulação de identificador de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68be27add43b57dc1905a63d1a2ffffb8ae41f69efb195d21aa91ca65a5dff4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870326"
---
# <a name="call-handle-manipulation"></a>Manipulação de identificador de chamada

A TAPI fornece várias funções para manipular identificadores de chamada, determinando a relação entre linhas, chamadas e endereço, e assim por diante. A maior parte dessa funcionalidade é implementada estritamente na TAPI sem referência ao provedor de serviços, exceto para [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid). Essa função recupera o identificador de endereço de uma chamada existente dentro de sua linha. Os provedores de serviço que modelam uma linha como um grupo de identificadores de endereço podem escolher um endereço imprevisível para uma nova chamada de entrada ou saída. Essa função fornece à TAPI informações suficientes para implementar a operação [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) quando ela é chamada com a \_ opção de endereço LINECALLSELECT.

 

 
