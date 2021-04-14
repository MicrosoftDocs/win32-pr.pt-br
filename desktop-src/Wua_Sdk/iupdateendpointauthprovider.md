---
description: Contém os métodos usados para negociar qual tipo de token é usado para autenticar o ponto de extremidade de um serviço.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interface IUpdateEndpointAuthProvider (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501866"
---
# <a name="iupdateendpointauthprovider-interface"></a><span data-ttu-id="1f7c1-103">Interface IUpdateEndpointAuthProvider</span><span class="sxs-lookup"><span data-stu-id="1f7c1-103">IUpdateEndpointAuthProvider interface</span></span>

<span data-ttu-id="1f7c1-104">A interface **IUpdateEndpointAuthProvider** contém os métodos usados para negociar qual tipo de token é usado para autenticar o ponto de extremidade de um serviço.</span><span class="sxs-lookup"><span data-stu-id="1f7c1-104">The **IUpdateEndpointAuthProvider** interface contains the methods used for negotiating which type of token is used for authenticating the endpoint of a service.</span></span>

## <a name="members"></a><span data-ttu-id="1f7c1-105">Membros</span><span class="sxs-lookup"><span data-stu-id="1f7c1-105">Members</span></span>

<span data-ttu-id="1f7c1-106">A interface **IUpdateEndpointAuthProvider** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1f7c1-106">The **IUpdateEndpointAuthProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1f7c1-107">**IUpdateEndpointAuthProvider** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f7c1-107">**IUpdateEndpointAuthProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="1f7c1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f7c1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1f7c1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f7c1-109">Methods</span></span>

<span data-ttu-id="1f7c1-110">A interface **IUpdateEndpointAuthProvider** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1f7c1-110">The **IUpdateEndpointAuthProvider** interface has these methods.</span></span>



| <span data-ttu-id="1f7c1-111">Método</span><span class="sxs-lookup"><span data-stu-id="1f7c1-111">Method</span></span>                                                                                             | <span data-ttu-id="1f7c1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f7c1-112">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f7c1-113">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="1f7c1-113">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)                           | <span data-ttu-id="1f7c1-114">Solicite um token para o ponto de extremidade do serviço usando as credenciais especificadas.</span><span class="sxs-lookup"><span data-stu-id="1f7c1-114">Request a token for the endpoint of the service using the specified credentials.</span></span><br/>    |
| [<span data-ttu-id="1f7c1-115">**GetPreferredEndpointTokenType**</span><span class="sxs-lookup"><span data-stu-id="1f7c1-115">**GetPreferredEndpointTokenType**</span></span>](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | <span data-ttu-id="1f7c1-116">Retorna o tipo preferencial de token de autenticação para o ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="1f7c1-116">Returns the preferred type of authentication token for the endpoint of the service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f7c1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f7c1-117">Remarks</span></span>

<span data-ttu-id="1f7c1-118">O WUA chama o método [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) dessa interface para iniciar o processo de negociação.</span><span class="sxs-lookup"><span data-stu-id="1f7c1-118">WUA calls the [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) method of this interface to start the negotiation process.</span></span> <span data-ttu-id="1f7c1-119">Quando a chamada é feita, o WUA passa no identificador de serviço, o tipo de ponto de extremidade implementado pelo serviço e os tipos de token disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1f7c1-119">When the call is made WUA passes in the service identifier, the type of endpoint implemented by the service, and the token types that are available.</span></span> <span data-ttu-id="1f7c1-120">Em seguida, a implementação dessa interface retorna os tipos de token que ele prefere usar.</span><span class="sxs-lookup"><span data-stu-id="1f7c1-120">The implementation of this interface then returns the token types that it preferes to use.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f7c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f7c1-121">Requirements</span></span>



| <span data-ttu-id="1f7c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f7c1-122">Requirement</span></span> | <span data-ttu-id="1f7c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1f7c1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7c1-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f7c1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7c1-125">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="1f7c1-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="1f7c1-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f7c1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7c1-127">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="1f7c1-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="1f7c1-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f7c1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f7c1-129"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f7c1-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f7c1-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="1f7c1-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f7c1-131"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f7c1-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="1f7c1-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f7c1-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f7c1-133"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f7c1-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f7c1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1f7c1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f7c1-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f7c1-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
