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
# <a name="call-handle-manipulation"></a><span data-ttu-id="2049b-103">Manipulação de identificador de chamada</span><span class="sxs-lookup"><span data-stu-id="2049b-103">Call Handle Manipulation</span></span>

<span data-ttu-id="2049b-104">A TAPI fornece várias funções para manipular identificadores de chamada, determinando a relação entre linhas, chamadas e endereço, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2049b-104">TAPI provides a number of functions for manipulating call handles, determining the relationship among lines, calls, and address, and so on.</span></span> <span data-ttu-id="2049b-105">A maior parte dessa funcionalidade é implementada estritamente na TAPI sem referência ao provedor de serviços, exceto para [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span><span class="sxs-lookup"><span data-stu-id="2049b-105">Most of this functionality is implemented strictly within TAPI without reference to the service provider, except for [**TSPI\_lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span></span> <span data-ttu-id="2049b-106">Essa função recupera o identificador de endereço de uma chamada existente dentro de sua linha.</span><span class="sxs-lookup"><span data-stu-id="2049b-106">This function retrieves the address identifier of an existing call within its line.</span></span> <span data-ttu-id="2049b-107">Os provedores de serviço que modelam uma linha como um grupo de identificadores de endereço podem escolher um endereço imprevisível para uma nova chamada de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="2049b-107">Service providers that model a line as a group of address identifiers can choose an unpredictable address for a new inbound or outbound call.</span></span> <span data-ttu-id="2049b-108">Essa função fornece à TAPI informações suficientes para implementar a operação [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) quando ela é chamada com a \_ opção de endereço LINECALLSELECT.</span><span class="sxs-lookup"><span data-stu-id="2049b-108">This function gives TAPI sufficient information to implement the [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) operation when it is invoked with the LINECALLSELECT\_ADDRESS option.</span></span>

 

 
