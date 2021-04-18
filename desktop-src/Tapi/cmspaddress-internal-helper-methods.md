---
description: A lista a seguir contém os métodos internos de endereço CMSP.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Métodos auxiliares internos do CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767770"
---
# <a name="cmspaddress-internal-helper-methods"></a><span data-ttu-id="ea0f6-103">Métodos auxiliares internos do CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="ea0f6-103">CMSPAddress Internal Helper Methods</span></span>



| <span data-ttu-id="ea0f6-104">Métodos auxiliares internos do CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="ea0f6-104">CMSPAddress internal helper methods</span></span>                                        | <span data-ttu-id="ea0f6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea0f6-105">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea0f6-106">**GetStaticTerminals**</span><span class="sxs-lookup"><span data-stu-id="ea0f6-106">**GetStaticTerminals**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | <span data-ttu-id="ea0f6-107">Chamado por [**Get \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) e [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) para obter uma matriz de terminais estáticos que podem ser usados nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-107">Called by [**get\_StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) and [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) to get an array of static terminals that can be used on this address.</span></span>                                     |
| [<span data-ttu-id="ea0f6-108">**GetDynamicTerminalClasses**</span><span class="sxs-lookup"><span data-stu-id="ea0f6-108">**GetDynamicTerminalClasses**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | <span data-ttu-id="ea0f6-109">Chamado por [**Get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) e [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) para obter uma matriz de classes de terminal dinâmicas que podem ser usadas nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-109">Called by [**get\_DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) and [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) to get an array of dynamic terminal classes that can be used on this address.</span></span> |
| [<span data-ttu-id="ea0f6-110">**UpdateTerminalList**</span><span class="sxs-lookup"><span data-stu-id="ea0f6-110">**UpdateTerminalList**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | <span data-ttu-id="ea0f6-111">Popula a lista de terminais estáticos do MSP.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-111">Populates the MSP's list of static terminals.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="ea0f6-112">**ReceiveTSPAddressData**</span><span class="sxs-lookup"><span data-stu-id="ea0f6-112">**ReceiveTSPAddressData**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | <span data-ttu-id="ea0f6-113">Chamado quando uma mensagem de dados do TSP é destinada a ser processada pelo endereço em vez de por uma chamada específica.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-113">Called when a TSP data message is intended to be processed by the address rather than by a specific call.</span></span>                                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="ea0f6-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea0f6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea0f6-115">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="ea0f6-115">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
