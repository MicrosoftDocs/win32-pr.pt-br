---
description: As funções a seguir são implementadas por uma DLL de provedor de rede para se comunicar com o roteador de vários provedores (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Funções implementadas por provedores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922529"
---
# <a name="functions-implemented-by-network-providers"></a><span data-ttu-id="ad890-103">Funções implementadas por provedores de rede</span><span class="sxs-lookup"><span data-stu-id="ad890-103">Functions Implemented by Network Providers</span></span>

<span data-ttu-id="ad890-104">As funções a seguir são implementadas por uma DLL de provedor de rede para se comunicar com o [*roteador de vários provedores*](/windows/desktop/SecGloss/m-gly) (MPR).</span><span class="sxs-lookup"><span data-stu-id="ad890-104">The following functions are implemented by a network provider DLL to communicate with the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR).</span></span> <span data-ttu-id="ad890-105">Observe que somente as [funções Capabilities](capabilities-functions.md) devem ser implementadas por um provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="ad890-105">Note that only the [Capabilities Functions](capabilities-functions.md) must be implemented by a network provider.</span></span> <span data-ttu-id="ad890-106">A implementação dos outros tipos de funções é opcional e depende dos requisitos do provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="ad890-106">Implementation of the other types of functions is optional and depends on the requirements of the network provider.</span></span>



| <span data-ttu-id="ad890-107">Conjunto de funções</span><span class="sxs-lookup"><span data-stu-id="ad890-107">Function set</span></span>                                                                                    | <span data-ttu-id="ad890-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad890-108">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad890-109">Funções de recursos</span><span class="sxs-lookup"><span data-stu-id="ad890-109">Capabilities Functions</span></span>](capabilities-functions.md)<br/>                                 | <span data-ttu-id="ad890-110">Permite que o chamador determine os recursos do provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="ad890-110">Allows the caller to determine the capabilities of the network provider.</span></span><br/>                                                                |
| [<span data-ttu-id="ad890-111">Funções de nome de usuário</span><span class="sxs-lookup"><span data-stu-id="ad890-111">User Name Functions</span></span>](user-name-functions.md)<br/>                                       | <span data-ttu-id="ad890-112">Solicita ao provedor de rede o nome de usuário associado a uma conexão.</span><span class="sxs-lookup"><span data-stu-id="ad890-112">Prompts the network provider for the user name associated with a connection.</span></span><br/>                                                            |
| [<span data-ttu-id="ad890-113">Funções de redirecionamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ad890-113">Device-Redirecting Functions</span></span>](device-redirecting-functions.md)<br/>                     | <span data-ttu-id="ad890-114">Permite que um provedor de rede redirecione dispositivos, letras de unidade e portas LPT que são padrão no sistema operacional Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="ad890-114">Allows a network provider to redirect devices, drive letters, and LPT ports that are standard on the Microsoft MS-DOS operating system.</span></span><br/> |
| [<span data-ttu-id="ad890-115">Funções de caixa de diálogo específicas do provedor</span><span class="sxs-lookup"><span data-stu-id="ad890-115">Provider-Specific Dialog Box Functions</span></span>](provider-specific-dialog-box-functions.md)<br/> | <span data-ttu-id="ad890-116">Permite que um provedor de rede exiba ou atue em informações específicas da rede.</span><span class="sxs-lookup"><span data-stu-id="ad890-116">Allows a network provider to display or act on network-specific information.</span></span><br/>                                                            |
| [<span data-ttu-id="ad890-117">Funções administrativas</span><span class="sxs-lookup"><span data-stu-id="ad890-117">Administrative Functions</span></span>](administrative-functions.md)<br/>                             | <span data-ttu-id="ad890-118">Permite que um provedor de rede exiba ou atue em diretórios de rede especiais.</span><span class="sxs-lookup"><span data-stu-id="ad890-118">Allows a network provider to display or act on special network directories.</span></span><br/>                                                             |
| [<span data-ttu-id="ad890-119">Funções de enumeração</span><span class="sxs-lookup"><span data-stu-id="ad890-119">Enumeration Functions</span></span>](enumeration-functions.md)<br/>                                   | <span data-ttu-id="ad890-120">Permite que o usuário procure recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="ad890-120">Allows the user to browse network resources.</span></span><br/>                                                                                            |



 

<span data-ttu-id="ad890-121">Para obter mais informações sobre como criar e registrar um provedor de rede, consulte [implementando um provedor de rede](implementing-a-network-provider.md) e [registrando provedores de rede e gerenciadores de credenciais](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="ad890-121">For more information about how to create and register a network provider, see [Implementing a Network Provider](implementing-a-network-provider.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

