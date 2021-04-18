---
description: Explica considerações sobre a implementação de funções de exportação de filtro de senha.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Considerações sobre programação de filtro de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778666"
---
# <a name="password-filter-programming-considerations"></a><span data-ttu-id="12103-103">Considerações sobre programação de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="12103-103">Password Filter Programming Considerations</span></span>

<span data-ttu-id="12103-104">Ao implementar funções de exportação de [*filtro de senha*](/windows/desktop/SecGloss/p-gly) , tenha em mente as seguintes considerações:</span><span class="sxs-lookup"><span data-stu-id="12103-104">When implementing [*password filter*](/windows/desktop/SecGloss/p-gly) export functions, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="12103-105">Tome muito cuidado ao trabalhar com senhas de [*texto sem formatação*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="12103-105">Take great care when working with [*plaintext*](/windows/desktop/SecGloss/p-gly) passwords.</span></span> <span data-ttu-id="12103-106">O envio de senhas de texto sem formatação por redes pode comprometer a segurança.</span><span class="sxs-lookup"><span data-stu-id="12103-106">Sending plaintext passwords over networks could compromise security.</span></span> <span data-ttu-id="12103-107">Os "farejadores" de rede podem facilmente inspecionar o tráfego de senha de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="12103-107">Network "sniffers" can easily watch for plaintext password traffic.</span></span>
-   <span data-ttu-id="12103-108">Apague toda a memória usada para armazenar senhas chamando a função [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) antes de liberar memória.</span><span class="sxs-lookup"><span data-stu-id="12103-108">Erase all memory used to store passwords by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function before freeing memory.</span></span>
-   <span data-ttu-id="12103-109">Todos os buffers passados para a notificação de senha e as rotinas de filtro devem ser tratados como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="12103-109">All buffers passed into password notification and filter routines should be treated as read-only.</span></span> <span data-ttu-id="12103-110">Gravar dados nesses buffers pode causar comportamento instável.</span><span class="sxs-lookup"><span data-stu-id="12103-110">Writing data to these buffers may cause unstable behavior.</span></span>
-   <span data-ttu-id="12103-111">Todas as notificações de senha e as rotinas de filtro devem ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="12103-111">All password notification and filter routines should be thread-safe.</span></span> <span data-ttu-id="12103-112">Use seções críticas ou outras técnicas de programação síncronas para proteger os dados quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="12103-112">Use critical sections or other synchronous programming techniques to protect data where appropriate.</span></span>
-   <span data-ttu-id="12103-113">A notificação e a filtragem de senha ocorrem somente no computador que hospeda a conta.</span><span class="sxs-lookup"><span data-stu-id="12103-113">Password notification and filtering take place only on the computer that houses the account.</span></span>
-   <span data-ttu-id="12103-114">Todos os controladores de domínio são graváveis, portanto, os pacotes de filtro de senha devem estar presentes em todos os controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="12103-114">All domain controllers are writeable, therefore password filter packages must be present on all domain controllers.</span></span>

    <span data-ttu-id="12103-115">**Domínios do Windows NT 4,0:** A notificação em contas de domínio só ocorre no controlador de domínio primário.</span><span class="sxs-lookup"><span data-stu-id="12103-115">**Windows NT 4.0 domains:** Notification on domain accounts takes place only on the primary domain controller.</span></span> <span data-ttu-id="12103-116">Além do controlador de domínio primário, os pacotes de filtro de senha devem ser instalados em todos os controladores de domínio de backup para permitir que as notificações continuem no caso de alterações na função do servidor.</span><span class="sxs-lookup"><span data-stu-id="12103-116">In addition to the primary domain controller, the password filter packages should be installed on all backup domain controllers to allow notifications to continue in the event of server role changes.</span></span>

-   <span data-ttu-id="12103-117">Todas as DLLs de filtro de senha são executadas no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) da conta do sistema local.</span><span class="sxs-lookup"><span data-stu-id="12103-117">All password filter DLLs run in the [*security context*](/windows/desktop/SecGloss/s-gly) of the local system account.</span></span>



| <span data-ttu-id="12103-118">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="12103-118">For information about</span></span>                                                                                                                     | <span data-ttu-id="12103-119">Consulte</span><span class="sxs-lookup"><span data-stu-id="12103-119">See</span></span>                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12103-120">Como instalar e registrar sua própria DLL de [*filtro de senha*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="12103-120">How to install and register your own [*password filter*](/windows/desktop/SecGloss/p-gly) DLL.</span></span> | [<span data-ttu-id="12103-121">Instalando e registrando uma DLL de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="12103-121">Installing and Registering a Password Filter DLL</span></span>](installing-and-registering-a-password-filter-dll.md) |
| <span data-ttu-id="12103-122">A DLL de filtro de senha fornecida pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="12103-122">The password filter DLL provided by Microsoft.</span></span>                                                                                            | [<span data-ttu-id="12103-123">Imposição de senha forte e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="12103-123">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)         |
| <span data-ttu-id="12103-124">Funções de exportação implementadas por uma DLL de filtro de senha.</span><span class="sxs-lookup"><span data-stu-id="12103-124">Export functions implemented by a password filter DLL.</span></span>                                                                                    | [<span data-ttu-id="12103-125">Funções de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="12103-125">Password Filter Functions</span></span>](management-functions.md)                          |



 

 

 
