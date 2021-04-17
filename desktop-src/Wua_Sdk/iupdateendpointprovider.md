---
description: Contém o método usado para obter um ponto de extremidade que é usado para se conectar a um serviço.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Interface IUpdateEndpointProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762172"
---
# <a name="iupdateendpointprovider-interface"></a><span data-ttu-id="05e75-103">Interface IUpdateEndpointProvider</span><span class="sxs-lookup"><span data-stu-id="05e75-103">IUpdateEndpointProvider interface</span></span>

<span data-ttu-id="05e75-104">Contém o método usado para obter um ponto de extremidade que é usado para se conectar a um serviço.</span><span class="sxs-lookup"><span data-stu-id="05e75-104">Contains the method used to get an endpoint that is used to connect to a service.</span></span> <span data-ttu-id="05e75-105">Essa interface é implementada durante a gravação de um provedor de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="05e75-105">This interface is implemented when writing an endpoint provider.</span></span>

## <a name="members"></a><span data-ttu-id="05e75-106">Membros</span><span class="sxs-lookup"><span data-stu-id="05e75-106">Members</span></span>

<span data-ttu-id="05e75-107">A interface **IUpdateEndpointProvider** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="05e75-107">The **IUpdateEndpointProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="05e75-108">**IUpdateEndpointProvider** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="05e75-108">**IUpdateEndpointProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="05e75-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="05e75-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="05e75-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="05e75-110">Methods</span></span>

<span data-ttu-id="05e75-111">A interface **IUpdateEndpointProvider** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="05e75-111">The **IUpdateEndpointProvider** interface has these methods.</span></span>



| <span data-ttu-id="05e75-112">Método</span><span class="sxs-lookup"><span data-stu-id="05e75-112">Method</span></span>                                                                       | <span data-ttu-id="05e75-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="05e75-113">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="05e75-114">**Getserviceendpoint**</span><span class="sxs-lookup"><span data-stu-id="05e75-114">**GetServiceEndpoint**</span></span>](iupdateendpointauthprovider-getserviceendpoint.md) | <span data-ttu-id="05e75-115">Solicita um ponto de extremidade que é usado para se conectar a um serviço.</span><span class="sxs-lookup"><span data-stu-id="05e75-115">Requests an endpoint that is used to connect to a service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="05e75-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="05e75-116">Remarks</span></span>

<span data-ttu-id="05e75-117">O WUA chama o método [**getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) para iniciar o processo de negociação.</span><span class="sxs-lookup"><span data-stu-id="05e75-117">WUA calls the [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) method to start the negotiation process.</span></span> <span data-ttu-id="05e75-118">Quando a chamada é feita, o WUA passa nos tipos de token registrados e a implementação dessa interface retorna os tipos de token que ele prefere usar.</span><span class="sxs-lookup"><span data-stu-id="05e75-118">When the call is made, WUA passes in the registered token types, and the implementation of this interface returns the token types that it prefers to use.</span></span>

 

 
