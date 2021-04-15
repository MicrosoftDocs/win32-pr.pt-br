---
description: O tipo de direitos de acesso a objeto de conta tem os seguintes tipos de acesso.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Direitos de acesso a objeto de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506059"
---
# <a name="account-object-access-rights"></a><span data-ttu-id="ec904-103">Direitos de acesso a objeto de conta</span><span class="sxs-lookup"><span data-stu-id="ec904-103">Account Object Access Rights</span></span>

<span data-ttu-id="ec904-104">O tipo de direitos de acesso a objeto de conta tem os seguintes tipos de acesso.</span><span class="sxs-lookup"><span data-stu-id="ec904-104">The Account Object Access Rights type has the following access types.</span></span>



| <span data-ttu-id="ec904-105">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="ec904-105">Access type</span></span>                     | <span data-ttu-id="ec904-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec904-106">Description</span></span>                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec904-107">exibição de conta \_</span><span class="sxs-lookup"><span data-stu-id="ec904-107">ACCOUNT\_VIEW</span></span>                   | <span data-ttu-id="ec904-108">Esse tipo de acesso é necessário para ler as informações da conta.</span><span class="sxs-lookup"><span data-stu-id="ec904-108">This access type is required to read the account information.</span></span> <span data-ttu-id="ec904-109">Isso inclui os [*privilégios*](/windows/desktop/SecGloss/p-gly) atribuídos à conta, cotas de memória atribuídas e todos os tipos de acesso especiais concedidos.</span><span class="sxs-lookup"><span data-stu-id="ec904-109">This includes the [*privileges*](/windows/desktop/SecGloss/p-gly) assigned to the account, memory quotas assigned, and any special access types granted.</span></span> |
| <span data-ttu-id="ec904-110">\_privilégios de ajuste de conta \_</span><span class="sxs-lookup"><span data-stu-id="ec904-110">ACCOUNT\_ADJUST\_PRIVILEGES</span></span>     | <span data-ttu-id="ec904-111">Esse tipo de acesso é necessário para atribuir privilégios ou remover privilégios de uma conta.</span><span class="sxs-lookup"><span data-stu-id="ec904-111">This access type is required to assign privileges to or remove privileges from an account.</span></span>                                                                                                                                                            |
| <span data-ttu-id="ec904-112">\_cotas de ajuste de conta \_</span><span class="sxs-lookup"><span data-stu-id="ec904-112">ACCOUNT\_ADJUST\_QUOTAS</span></span>         | <span data-ttu-id="ec904-113">Esse tipo de acesso é necessário para alterar as cotas de sistema atribuídas a uma conta.</span><span class="sxs-lookup"><span data-stu-id="ec904-113">This access type is required to change the system quotas assigned to an account.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="ec904-114">CONTA \_ ajustar \_ acesso ao sistema \_</span><span class="sxs-lookup"><span data-stu-id="ec904-114">ACCOUNT\_ADJUST\_SYSTEM\_ACCESS</span></span> | <span data-ttu-id="ec904-115">Esse tipo de acesso é necessário para atualizar os sinalizadores de acesso do sistema para a conta.</span><span class="sxs-lookup"><span data-stu-id="ec904-115">This access type is required to update the system access flags for the account.</span></span>                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="ec904-116">Máscaras de acesso genérico</span><span class="sxs-lookup"><span data-stu-id="ec904-116">Generic Access Masks</span></span>

<span data-ttu-id="ec904-117">O objeto de [**conta**](account-object.md) publica os seguintes mapeamentos de tipos de acesso genéricos para tipos de acesso específicos.</span><span class="sxs-lookup"><span data-stu-id="ec904-117">The [**Account**](account-object.md) object publishes the following mappings from generic access types to specific access types.</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="ec904-118">Tipos de acesso padrão</span><span class="sxs-lookup"><span data-stu-id="ec904-118">Standard Access Types</span></span>

<span data-ttu-id="ec904-119">Este objeto não dá suporte ao tipo de acesso padrão (opcional) SYNCHRONIZE.</span><span class="sxs-lookup"><span data-stu-id="ec904-119">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="ec904-120">Todos os tipos de acesso necessários têm suporte.</span><span class="sxs-lookup"><span data-stu-id="ec904-120">All required access types are supported.</span></span> <span data-ttu-id="ec904-121">A máscara de todos os tipos de acesso com suporte para esse tipo de objeto é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="ec904-121">The mask of all supported access types for this object type is as follows.</span></span>

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
