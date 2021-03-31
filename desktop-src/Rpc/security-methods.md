---
title: Métodos de segurança
description: O Microsoft RPC dá suporte a dois métodos diferentes para adicionar segurança ao seu aplicativo distribuído.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005971"
---
# <a name="security-methods"></a><span data-ttu-id="6e9b3-103">Métodos de segurança</span><span class="sxs-lookup"><span data-stu-id="6e9b3-103">Security Methods</span></span>

<span data-ttu-id="6e9b3-104">O Microsoft RPC dá suporte a dois métodos diferentes para adicionar segurança ao seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-104">Microsoft RPC supports two different methods for adding security to your distributed application.</span></span> <span data-ttu-id="6e9b3-105">O primeiro método é usar a interface de provedor de suporte de segurança (SSPI), que pode ser acessada usando as funções RPC.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-105">The first method is to use the Security Support Provider Interface (SSPI), which can be accessed using the RPC functions.</span></span> <span data-ttu-id="6e9b3-106">Em geral, é melhor usar esse método.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-106">In general, it is best to use this method.</span></span> <span data-ttu-id="6e9b3-107">O SSPI fornece os recursos de autenticação mais flexíveis e independentes de rede.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-107">The SSPI provides the most flexible and network-independent authentication features.</span></span>

<span data-ttu-id="6e9b3-108">O segundo método é usar os recursos de segurança incorporados aos protocolos de transporte do sistema.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-108">The second method is to use the security features built into the system transport protocols.</span></span> <span data-ttu-id="6e9b3-109">O método de segurança no nível de transporte não é o método preferencial.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-109">The transport-level security method is not the preferred method.</span></span> <span data-ttu-id="6e9b3-110">Usar o SSPI é recomendado porque funciona em todos os transportes, entre plataformas, e fornece altos níveis de segurança, incluindo privacidade.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-110">Using the SSPI is recommended because it works on all transports, across platforms, and provides high levels of security, including privacy.</span></span>

<span data-ttu-id="6e9b3-111">Esta seção fornece visões gerais de segurança de nível de transporte e SSPI nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6e9b3-111">This section provides overviews of both SSPI and transport-level security in the following topics:</span></span>

-   [<span data-ttu-id="6e9b3-112">SSPI (interface do provedor de suporte de segurança)</span><span class="sxs-lookup"><span data-stu-id="6e9b3-112">Security Support Provider Interface (SSPI)</span></span>](security-support-provider-interface-sspi-.md)
-   [<span data-ttu-id="6e9b3-113">Segurança de transporte</span><span class="sxs-lookup"><span data-stu-id="6e9b3-113">Transport Security</span></span>](transport-security.md)

 

 




