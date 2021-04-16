---
description: Um serviço não deve acessar o HKEY \_ Current \_ User ou HKEY \_ classes \_ root, especialmente ao representar um usuário. Em vez disso, use a função RegOpenCurrentUser ou RegOpenUserClassesRoot.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Serviços e o registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754111"
---
# <a name="services-and-the-registry"></a><span data-ttu-id="e6a72-104">Serviços e o registro</span><span class="sxs-lookup"><span data-stu-id="e6a72-104">Services and the Registry</span></span>

<span data-ttu-id="e6a72-105">Um serviço não deve acessar o **HKEY \_ Current \_ User** ou **HKEY \_ classes \_ root**, especialmente ao representar um usuário.</span><span class="sxs-lookup"><span data-stu-id="e6a72-105">A service should not access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT**, especially when impersonating a user.</span></span> <span data-ttu-id="e6a72-106">Em vez disso, use a função [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) ou [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .</span><span class="sxs-lookup"><span data-stu-id="e6a72-106">Instead, use the [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) or [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) function.</span></span>

<span data-ttu-id="e6a72-107">Se você tentar acessar **HKEY \_ Current \_ User** ou **HKEY \_ classes \_ root** de um serviço pode falhar, ou pode parecer funcionar, mas há um vazamento subjacente que pode levar a problemas ao carregar ou descarregar o perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="e6a72-107">If you attempt to access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT** from a service it may fail, or it may appear to work but there is an underlying leak that can lead to problems loading or unloading the user profile.</span></span>

 

 
