---
description: DACL para um novo objeto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL para um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090921"
---
# <a name="dacl-for-a-new-object"></a><span data-ttu-id="a32b4-103">DACL para um novo objeto</span><span class="sxs-lookup"><span data-stu-id="a32b4-103">DACL for a New Object</span></span>

<span data-ttu-id="a32b4-104">O sistema usa o seguinte algoritmo para criar uma DACL para a maioria dos tipos de novos objetos protegíveis:</span><span class="sxs-lookup"><span data-stu-id="a32b4-104">The system uses the following algorithm to build a DACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="a32b4-105">A DACL do objeto é a DACL do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) especificado pelo criador do objeto.</span><span class="sxs-lookup"><span data-stu-id="a32b4-105">The object's DACL is the DACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="a32b4-106">O sistema mescla quaisquer ACEs herdáveis na DACL especificada, a menos que o \_ bit de controle de DACL \_ protegido seja definido nos bits de controles do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="a32b4-106">The system merges any inheritable ACEs into the specified DACL unless the SE\_DACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span>
2.  <span data-ttu-id="a32b4-107">Se o criador não especificar um descritor de segurança, o sistema criará a DACL do objeto de ACEs herdáveis.</span><span class="sxs-lookup"><span data-stu-id="a32b4-107">If the creator does not specify a security descriptor, the system builds the object's DACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="a32b4-108">Se nenhum descritor de segurança for especificado e não houver ACEs herdáveis, a DACL do objeto será a DACL padrão do token [*primário*](/windows/desktop/SecGloss/p-gly) ou de [*representação*](/windows/desktop/SecGloss/i-gly) do criador.</span><span class="sxs-lookup"><span data-stu-id="a32b4-108">If no security descriptor is specified and there are no inheritable ACEs, the object's DACL is the default DACL from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creator.</span></span>
4.  <span data-ttu-id="a32b4-109">Se não houver nenhuma DACL especificada, herdada ou padrão, o sistema criará o objeto sem nenhuma DACL, o que permitirá que todos tenham acesso completo ao objeto.</span><span class="sxs-lookup"><span data-stu-id="a32b4-109">If there is no specified, inherited, or default DACL, the system creates the object with no DACL, which allows everyone full access to the object.</span></span>

<span data-ttu-id="a32b4-110">O sistema usa um algoritmo diferente para criar uma DACL para um novo objeto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a32b4-110">The system uses a different algorithm to build a DACL for a new Active Directory object.</span></span> <span data-ttu-id="a32b4-111">Para obter mais informações, consulte [como descritores de segurança são definidos em novos objetos de diretório](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="a32b4-111">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
