---
description: A TAPI fornece várias funções para manipular identificadores de chamada, determinando a relação entre linhas, chamadas e endereço, e assim por diante.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Manipulação de identificador de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813072"
---
# <a name="call-handle-manipulation"></a>Manipulação de identificador de chamada

A TAPI fornece várias funções para manipular identificadores de chamada, determinando a relação entre linhas, chamadas e endereço, e assim por diante. A maior parte dessa funcionalidade é implementada estritamente na TAPI sem referência ao provedor de serviços, exceto para [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid). Essa função recupera o identificador de endereço de uma chamada existente dentro de sua linha. Os provedores de serviço que modelam uma linha como um grupo de identificadores de endereço podem escolher um endereço imprevisível para uma nova chamada de entrada ou saída. Essa função fornece à TAPI informações suficientes para implementar a operação [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) quando ela é chamada com a \_ opção de endereço LINECALLSELECT.

 

 
