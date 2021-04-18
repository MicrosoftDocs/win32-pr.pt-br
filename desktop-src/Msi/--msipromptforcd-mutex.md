---
description: O \_ \_ mutex MsiPromptForCD existe quando o instalador solicita que o usuário insira um CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766882"
---
# <a name="__msipromptforcd-mutex"></a><span data-ttu-id="a44e1-103">\_\_Mutex MsiPromptForCD</span><span class="sxs-lookup"><span data-stu-id="a44e1-103">\_\_MsiPromptForCD Mutex</span></span>

<span data-ttu-id="a44e1-104">O \_ \_ mutex MsiPromptForCD existe quando o instalador solicita que o usuário insira um CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="a44e1-104">The \_\_MsiPromptForCD Mutex exists when the installer prompts the user to insert a CD-ROM.</span></span> <span data-ttu-id="a44e1-105">Os programas de reprodução automática devem verificar se o \_ \_ mutex MsiPromptForCD não está definido no momento antes de iniciar.</span><span class="sxs-lookup"><span data-stu-id="a44e1-105">Autoplay programs should check that the \_\_MsiPromptForCD mutex is not currently set before starting.</span></span> <span data-ttu-id="a44e1-106">Observe que é possível que um prompt de CD-ROM ocorra antes que a chave InProgress ou o \_ mutex MSIExecute existam.</span><span class="sxs-lookup"><span data-stu-id="a44e1-106">Note that it is possible for a CD-ROM prompt to occur before either the InProgress key or the \_MSIExecute Mutex exist.</span></span>

 

 



