---
title: Serviços de autorização
description: Um serviço de autorização é o método que o SSP usa para autorizar o acesso a um procedimento remoto. Os SSPs podem fornecer mais de um serviço de autorização. No entanto, normalmente, eles selecionam um como padrão.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005828"
---
# <a name="authorization-services"></a><span data-ttu-id="425bb-105">Serviços de autorização</span><span class="sxs-lookup"><span data-stu-id="425bb-105">Authorization Services</span></span>

<span data-ttu-id="425bb-106">Um serviço de autorização é o método que o SSP usa para autorizar o acesso a um procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="425bb-106">An authorization service is the method that the SSP uses to authorize access to a remote procedure.</span></span> <span data-ttu-id="425bb-107">Os SSPs podem fornecer mais de um serviço de autorização.</span><span class="sxs-lookup"><span data-stu-id="425bb-107">SSPs can provide more than one authorization service.</span></span> <span data-ttu-id="425bb-108">No entanto, normalmente, eles selecionam um como padrão.</span><span class="sxs-lookup"><span data-stu-id="425bb-108">However, they usually select one as a default.</span></span>

<span data-ttu-id="425bb-109">Seu aplicativo pode usar o método de autorização padrão para o SSP atual ou pode especificar um.</span><span class="sxs-lookup"><span data-stu-id="425bb-109">Your application can use the default authorization method for the current SSP, or it can specify one.</span></span> <span data-ttu-id="425bb-110">No momento, o Microsoft RPC dá suporte a dois métodos de autorização.</span><span class="sxs-lookup"><span data-stu-id="425bb-110">At present, Microsoft RPC supports two methods of authorization.</span></span> <span data-ttu-id="425bb-111">Uma é para o servidor fornecer autorização com base no nome do programa cliente.</span><span class="sxs-lookup"><span data-stu-id="425bb-111">One is for the server to provide authorization based on the name of the client program.</span></span> <span data-ttu-id="425bb-112">O outro é que o servidor Compare as credenciais de autenticação do cliente com a ACL (lista de controle de acesso) do servidor.</span><span class="sxs-lookup"><span data-stu-id="425bb-112">The other is for the server to compare the client's authentication credentials against the server's access control list (ACL).</span></span>

<span data-ttu-id="425bb-113">Para obter uma lista de serviços de autorização, consulte [constantes de serviço de autorização](authorization-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="425bb-113">For a list of authorization services, see [Authorization-Service Constants](authorization-service-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="425bb-114">É recomendável que os desenvolvedores usem RPC \_ C \_ AUTHZ \_ None.</span><span class="sxs-lookup"><span data-stu-id="425bb-114">It is recommended that developers use RPC\_C\_AUTHZ\_NONE.</span></span>

 

 

 




