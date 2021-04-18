---
description: Um proprietário de objetos implicitamente tem \_ acesso de DAC de gravação ao objeto. Isso significa que o proprietário pode modificar a DACL (lista de controle de acesso discricionário) dos objetos e, portanto, pode controlar o acesso ao objeto.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Proprietário de um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756384"
---
# <a name="owner-of-a-new-object"></a><span data-ttu-id="fbb5b-104">Proprietário de um novo objeto</span><span class="sxs-lookup"><span data-stu-id="fbb5b-104">Owner of a New Object</span></span>

<span data-ttu-id="fbb5b-105">O proprietário de um objeto implicitamente tem \_ acesso de DAC de gravação ao objeto.</span><span class="sxs-lookup"><span data-stu-id="fbb5b-105">An object's owner implicitly has WRITE\_DAC access to the object.</span></span> <span data-ttu-id="fbb5b-106">Isso significa que o proprietário pode modificar a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do objeto e, portanto, pode controlar o acesso ao objeto.</span><span class="sxs-lookup"><span data-stu-id="fbb5b-106">This means that the owner can modify the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), and thus, can control access to the object.</span></span>

<span data-ttu-id="fbb5b-107">O proprietário de um novo objeto é o Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) padrão do proprietário do [*token de representação*](/windows/desktop/SecGloss/i-gly) ou [*primário*](/windows/desktop/SecGloss/p-gly) do [*processo*](/windows/desktop/SecGloss/p-gly)de criação.</span><span class="sxs-lookup"><span data-stu-id="fbb5b-107">The owner of a new object is the default owner [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creating [*process*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="fbb5b-108">Para obter ou definir o proprietário padrão em um [*token de acesso*](/windows/desktop/SecGloss/a-gly), chame a função [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) ou [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) com a estrutura de [**\_ proprietário do token**](/windows/desktop/api/Winnt/ns-winnt-token_owner) .</span><span class="sxs-lookup"><span data-stu-id="fbb5b-108">To get or set the default owner in an [*access token*](/windows/desktop/SecGloss/a-gly), call the [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) or [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) function with the [**TOKEN\_OWNER**](/windows/desktop/api/Winnt/ns-winnt-token_owner) structure.</span></span> <span data-ttu-id="fbb5b-109">O sistema não permite que você defina o proprietário padrão de um token para um SID que não seja válido, como o SID da conta de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="fbb5b-109">The system does not allow you to set a token's default owner to a SID that is not valid, such as the SID of another user's account.</span></span>

<span data-ttu-id="fbb5b-110">Um processo com o \_ privilégio se assumir \_ propriedade habilitado pode se definir como o proprietário de um objeto.</span><span class="sxs-lookup"><span data-stu-id="fbb5b-110">A process with the SE\_TAKE\_OWNERSHIP privilege enabled can set itself as the owner of an object.</span></span> <span data-ttu-id="fbb5b-111">Um processo com o \_ privilégio do nome de restauração se \_ habilitado ou com acesso de proprietário de gravação \_ ao objeto pode definir qualquer Sid válido de usuário ou grupo como o proprietário de um objeto.</span><span class="sxs-lookup"><span data-stu-id="fbb5b-111">A process with the SE\_RESTORE\_NAME privilege enabled or with WRITE\_OWNER access to the object can set any valid user or group SID as the owner of an object.</span></span>

 

 
