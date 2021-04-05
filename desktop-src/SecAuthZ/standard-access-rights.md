---
description: Cada tipo de objeto protegível tem um conjunto de direitos de acesso que correspondem às operações específicas desse tipo de objeto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Direitos de acesso padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827331"
---
# <a name="standard-access-rights"></a><span data-ttu-id="6acc1-103">Direitos de acesso padrão</span><span class="sxs-lookup"><span data-stu-id="6acc1-103">Standard Access Rights</span></span>

<span data-ttu-id="6acc1-104">Cada tipo de objeto protegível tem um conjunto de direitos de acesso que correspondem às operações específicas desse tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="6acc1-104">Each type of securable object has a set of access rights that correspond to operations specific to that type of object.</span></span> <span data-ttu-id="6acc1-105">Além desses direitos de acesso específicos ao objeto, há um conjunto de direitos de acesso padrão que correspondem às operações comuns à maioria dos tipos de objetos protegíveis.</span><span class="sxs-lookup"><span data-stu-id="6acc1-105">In addition to these object-specific access rights, there is a set of standard access rights that correspond to operations common to most types of securable objects.</span></span>

<span data-ttu-id="6acc1-106">O [formato de máscara de acesso](access-mask-format.md) inclui um conjunto de bits para os direitos de acesso padrão.</span><span class="sxs-lookup"><span data-stu-id="6acc1-106">The [access mask format](access-mask-format.md) includes a set of bits for the standard access rights.</span></span> <span data-ttu-id="6acc1-107">As seguintes constantes do Windows para direitos de acesso padrão são definidas em Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="6acc1-107">The following Windows constants for standard access rights are defined in Winnt.h.</span></span>



| <span data-ttu-id="6acc1-108">Constante</span><span class="sxs-lookup"><span data-stu-id="6acc1-108">Constant</span></span>      | <span data-ttu-id="6acc1-109">Significado</span><span class="sxs-lookup"><span data-stu-id="6acc1-109">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6acc1-110">Delete (excluir)</span><span class="sxs-lookup"><span data-stu-id="6acc1-110">DELETE</span></span>        | <span data-ttu-id="6acc1-111">O direito de excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="6acc1-111">The right to delete the object.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6acc1-112">controle de leitura \_</span><span class="sxs-lookup"><span data-stu-id="6acc1-112">READ\_CONTROL</span></span> | <span data-ttu-id="6acc1-113">O direito de ler as informações no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)do objeto, sem incluir as informações na SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="6acc1-113">The right to read the information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), not including the information in the [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> |
| <span data-ttu-id="6acc1-114">SYNCHRONIZE</span><span class="sxs-lookup"><span data-stu-id="6acc1-114">SYNCHRONIZE</span></span>   | <span data-ttu-id="6acc1-115">O direito de usar o objeto para sincronização.</span><span class="sxs-lookup"><span data-stu-id="6acc1-115">The right to use the object for synchronization.</span></span> <span data-ttu-id="6acc1-116">Isso permite que um thread aguarde até que o objeto esteja no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="6acc1-116">This enables a thread to wait until the object is in the signaled state.</span></span> <span data-ttu-id="6acc1-117">Alguns tipos de objeto não dão suporte a esse direito de acesso.</span><span class="sxs-lookup"><span data-stu-id="6acc1-117">Some object types do not support this access right.</span></span>                                                                                                                                                                |
| <span data-ttu-id="6acc1-118">GRAVAR \_ DAC</span><span class="sxs-lookup"><span data-stu-id="6acc1-118">WRITE\_DAC</span></span>    | <span data-ttu-id="6acc1-119">O direito de modificar a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="6acc1-119">The right to modify the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) in the object's security descriptor.</span></span>                                                                                                                    |
| <span data-ttu-id="6acc1-120">proprietário da gravação \_</span><span class="sxs-lookup"><span data-stu-id="6acc1-120">WRITE\_OWNER</span></span>  | <span data-ttu-id="6acc1-121">O direito de alterar o proprietário no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="6acc1-121">The right to change the owner in the object's security descriptor.</span></span>                                                                                                                                                                                                                                                                           |



 

<span data-ttu-id="6acc1-122">O Winnt. h também define as seguintes combinações de constantes de direitos de acesso padrão.</span><span class="sxs-lookup"><span data-stu-id="6acc1-122">Winnt.h also defines the following combinations of the standard access rights constants.</span></span>



| <span data-ttu-id="6acc1-123">Constante</span><span class="sxs-lookup"><span data-stu-id="6acc1-123">Constant</span></span>                   | <span data-ttu-id="6acc1-124">Significado</span><span class="sxs-lookup"><span data-stu-id="6acc1-124">Meaning</span></span>                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6acc1-125">\_ \_ todos os direitos padrão</span><span class="sxs-lookup"><span data-stu-id="6acc1-125">STANDARD\_RIGHTS\_ALL</span></span>      | <span data-ttu-id="6acc1-126">Combina a exclusão, o \_ controle de leitura, a gravação de \_ DAC, o proprietário da gravação \_ e o acesso de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6acc1-126">Combines DELETE, READ\_CONTROL, WRITE\_DAC, WRITE\_OWNER, and SYNCHRONIZE access.</span></span> |
| <span data-ttu-id="6acc1-127">\_execução de direitos padrão \_</span><span class="sxs-lookup"><span data-stu-id="6acc1-127">STANDARD\_RIGHTS\_EXECUTE</span></span>  | <span data-ttu-id="6acc1-128">Definido atualmente para o controle de leitura igual \_ .</span><span class="sxs-lookup"><span data-stu-id="6acc1-128">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="6acc1-129">\_leitura de direitos padrão \_</span><span class="sxs-lookup"><span data-stu-id="6acc1-129">STANDARD\_RIGHTS\_READ</span></span>     | <span data-ttu-id="6acc1-130">Definido atualmente para o controle de leitura igual \_ .</span><span class="sxs-lookup"><span data-stu-id="6acc1-130">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="6acc1-131">\_direitos padrão \_ necessários</span><span class="sxs-lookup"><span data-stu-id="6acc1-131">STANDARD\_RIGHTS\_REQUIRED</span></span> | <span data-ttu-id="6acc1-132">Combina exclusão, \_ controle de leitura, gravação de \_ DAC e \_ acesso de proprietário de gravação.</span><span class="sxs-lookup"><span data-stu-id="6acc1-132">Combines DELETE, READ\_CONTROL, WRITE\_DAC, and WRITE\_OWNER access.</span></span>              |
| <span data-ttu-id="6acc1-133">\_gravação de direitos padrão \_</span><span class="sxs-lookup"><span data-stu-id="6acc1-133">STANDARD\_RIGHTS\_WRITE</span></span>    | <span data-ttu-id="6acc1-134">Definido atualmente para o controle de leitura igual \_ .</span><span class="sxs-lookup"><span data-stu-id="6acc1-134">Currently defined to equal READ\_CONTROL.</span></span>                                         |



 

 

 
