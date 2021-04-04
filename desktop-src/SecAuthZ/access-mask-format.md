---
description: Todos os objetos protegíveis organizam seus direitos de acesso usando o formato de máscara de acesso mostrado na ilustração a seguir.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Formato de máscara de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828832"
---
# <a name="access-mask-format"></a><span data-ttu-id="d61d1-103">Formato de máscara de acesso</span><span class="sxs-lookup"><span data-stu-id="d61d1-103">Access Mask Format</span></span>

<span data-ttu-id="d61d1-104">Todos os objetos protegíveis organizam seus direitos de acesso usando o formato de [*máscara de acesso*](/windows/desktop/SecGloss/a-gly) mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="d61d1-104">All securable objects arrange their access rights by using the [*access mask*](/windows/desktop/SecGloss/a-gly) format shown in the following illustration.</span></span>

![formato de máscara de acesso](images/accctrl4.png)

<span data-ttu-id="d61d1-106">Nesse formato, os 16 bits de ordem inferior são para direitos de acesso específicos de objeto, os próximos 8 bits são para [direitos de acesso padrão](standard-access-rights.md), que se aplicam à maioria dos tipos de objetos e os quatro bits de ordem superior são usados para especificar [direitos de acesso genéricos](generic-access-rights.md) que cada tipo de objeto pode mapear para um conjunto de direitos padrão e específicos de objeto.</span><span class="sxs-lookup"><span data-stu-id="d61d1-106">In this format, the low-order 16 bits are for object-specific access rights, the next 8 bits are for [standard access rights](standard-access-rights.md), which apply to most types of objects, and the 4 high-order bits are used to specify [generic access rights](generic-access-rights.md) that each object type can map to a set of standard and object-specific rights.</span></span> <span data-ttu-id="d61d1-107">O bit de segurança do sistema de acesso \_ \_ corresponde ao [direito de acessar a SACL do objeto](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="d61d1-107">The ACCESS\_SYSTEM\_SECURITY bit corresponds to the [right to access the object's SACL](sacl-access-right.md).</span></span>

 

 
