---
title: Funções modais do usuário
description: As funções modais do usuário de gerenciamento de rede obtêm e definem parâmetros de todo o sistema relacionados ao comportamento do sistema de segurança.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917611"
---
# <a name="user-modal-functions"></a><span data-ttu-id="79b96-103">Funções modais do usuário</span><span class="sxs-lookup"><span data-stu-id="79b96-103">User Modal Functions</span></span>

<span data-ttu-id="79b96-104">As funções modais do usuário de gerenciamento de rede obtêm e definem parâmetros de todo o sistema relacionados ao comportamento do sistema de segurança.</span><span class="sxs-lookup"><span data-stu-id="79b96-104">The network management user modal functions get and set system-wide parameters related to security system behavior.</span></span>

<span data-ttu-id="79b96-105">As funções modais do usuário são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="79b96-105">The user modal functions are listed following.</span></span>



| <span data-ttu-id="79b96-106">Função</span><span class="sxs-lookup"><span data-stu-id="79b96-106">Function</span></span>                                     | <span data-ttu-id="79b96-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="79b96-107">Description</span></span>                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79b96-108">**NetUserModalsGet**</span><span class="sxs-lookup"><span data-stu-id="79b96-108">**NetUserModalsGet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | <span data-ttu-id="79b96-109">Retorna informações globais para todos os usuários e grupos globais no banco de dados de segurança, que é o banco de dados SAM (Gerenciador de contas de segurança) ou, no caso de controladores de domínio, o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79b96-109">Returns global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.</span></span> |
| [<span data-ttu-id="79b96-110">**NetUserModalsSet**</span><span class="sxs-lookup"><span data-stu-id="79b96-110">**NetUserModalsSet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | <span data-ttu-id="79b96-111">Define informações globais para todos os usuários e grupos globais no banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="79b96-111">Sets global information for all users and global groups in the security database.</span></span>                                                                                                                       |



 

<span data-ttu-id="79b96-112">As funções **NetUserModalsGet** e **NetUserModalsSet** examinam e modificam as configurações de janela restrita, que são parâmetros globais que afetam cada conta no banco de dados de segurança (por exemplo, o comprimento mínimo permitido da senha).</span><span class="sxs-lookup"><span data-stu-id="79b96-112">The **NetUserModalsGet** and **NetUserModalsSet** functions examine and modify the modal settings, which are global parameters that affect every account in the security database (for example, the minimum allowable password length).</span></span> <span data-ttu-id="79b96-113">Todas as configurações de janela restrita podem ser alteradas chamando **NetUserModalsSet**.</span><span class="sxs-lookup"><span data-stu-id="79b96-113">All modal settings can be altered by calling **NetUserModalsSet**.</span></span> <span data-ttu-id="79b96-114">A maioria das modalidades também pode ser alterada usando o comando **net accounts** .</span><span class="sxs-lookup"><span data-stu-id="79b96-114">Most of the modals can also be altered by using the **net accounts** command.</span></span> <span data-ttu-id="79b96-115">As funções modais do usuário de gerenciamento de rede não exigem que o servidor tenha segurança em nível de usuário.</span><span class="sxs-lookup"><span data-stu-id="79b96-115">The network management user modal functions do not require the server to have user-level security.</span></span>

<span data-ttu-id="79b96-116">As informações modais do usuário estão disponíveis nos seguintes níveis:</span><span class="sxs-lookup"><span data-stu-id="79b96-116">User modal information is available at the following levels:</span></span>

-   [<span data-ttu-id="79b96-117">**Informações de modal do usuário \_ \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="79b96-117">**USER\_MODALS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [<span data-ttu-id="79b96-118">**Informações de modal do usuário \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="79b96-118">**USER\_MODALS\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [<span data-ttu-id="79b96-119">**Informações de modal do usuário \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="79b96-119">**USER\_MODALS\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [<span data-ttu-id="79b96-120">**Informações de modal do usuário \_ \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="79b96-120">**USER\_MODALS\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

<span data-ttu-id="79b96-121">Os níveis de informações a seguir são válidos somente para [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) e substituem a maneira mais antiga de passar um *Parmnum* para definir um campo específico:</span><span class="sxs-lookup"><span data-stu-id="79b96-121">The following information levels are valid only for [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) and replace the older way of passing in a *Parmnum* to set a specific field:</span></span>

-   [<span data-ttu-id="79b96-122">**Informações de modal do usuário \_ \_ \_ 1001**</span><span class="sxs-lookup"><span data-stu-id="79b96-122">**USER\_MODALS\_INFO\_1001**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [<span data-ttu-id="79b96-123">**Informações de modal do usuário \_ \_ \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="79b96-123">**USER\_MODALS\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [<span data-ttu-id="79b96-124">**Informações de modal do usuário \_ \_ \_ 1003**</span><span class="sxs-lookup"><span data-stu-id="79b96-124">**USER\_MODALS\_INFO\_1003**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [<span data-ttu-id="79b96-125">**Informações de modal do usuário \_ \_ \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="79b96-125">**USER\_MODALS\_INFO\_1004**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [<span data-ttu-id="79b96-126">**Informações de modal do usuário \_ \_ \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="79b96-126">**USER\_MODALS\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [<span data-ttu-id="79b96-127">**Informações de modal do usuário \_ \_ \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="79b96-127">**USER\_MODALS\_INFO\_1006**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [<span data-ttu-id="79b96-128">**Informações de modal do usuário \_ \_ \_ 1007**</span><span class="sxs-lookup"><span data-stu-id="79b96-128">**USER\_MODALS\_INFO\_1007**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

<span data-ttu-id="79b96-129">Se você estiver programando para Active Directory, poderá chamar determinados métodos de interface do Active Directory Service (ADSI) para obter a mesma funcionalidade que pode obter ao chamar as funções modais do usuário de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="79b96-129">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions.</span></span> <span data-ttu-id="79b96-130">Para obter mais informações, consulte [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span><span class="sxs-lookup"><span data-stu-id="79b96-130">For more information, see [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span></span>

 

 