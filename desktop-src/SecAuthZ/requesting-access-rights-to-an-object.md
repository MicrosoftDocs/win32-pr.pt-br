---
description: Quando você abre um identificador para um objeto, o identificador retornado tem alguma combinação de direitos de acesso ao objeto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Solicitando direitos de acesso a um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755965"
---
# <a name="requesting-access-rights-to-an-object"></a><span data-ttu-id="50afb-103">Solicitando direitos de acesso a um objeto</span><span class="sxs-lookup"><span data-stu-id="50afb-103">Requesting Access Rights to an Object</span></span>

<span data-ttu-id="50afb-104">Quando você abre um identificador para um objeto, o identificador retornado tem alguma combinação de direitos de acesso ao objeto.</span><span class="sxs-lookup"><span data-stu-id="50afb-104">When you open a handle to an object, the returned handle has some combination of access rights to the object.</span></span> <span data-ttu-id="50afb-105">Algumas funções, como [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), não exigem um conjunto específico de direitos de acesso solicitados.</span><span class="sxs-lookup"><span data-stu-id="50afb-105">Some functions, such as [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), do not require a specific set of requested access rights.</span></span> <span data-ttu-id="50afb-106">Essas funções sempre tentam abrir o identificador para acesso completo.</span><span class="sxs-lookup"><span data-stu-id="50afb-106">These functions always try to open the handle for full access.</span></span> <span data-ttu-id="50afb-107">Outras funções, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), permitem que você especifique o conjunto de direitos de acesso que deseja.</span><span class="sxs-lookup"><span data-stu-id="50afb-107">Other functions, such as [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), allow you to specify the set of access rights that you want.</span></span> <span data-ttu-id="50afb-108">Você deve solicitar apenas os direitos de acesso de que precisa, em vez de abrir um identificador para acesso completo.</span><span class="sxs-lookup"><span data-stu-id="50afb-108">You should request only the access rights that you need, rather than opening a handle for full access.</span></span> <span data-ttu-id="50afb-109">Isso impede o uso do identificador de maneira não intencional e aumenta as chances de que a solicitação de acesso seja bem-sucedido se a DACL do objeto permitir acesso limitado.</span><span class="sxs-lookup"><span data-stu-id="50afb-109">This prevents using the handle in an unintended way, and increases the chances that the access request will succeed if the object's DACL only allows limited access.</span></span>

<span data-ttu-id="50afb-110">Use [direitos de acesso genéricos](generic-access-rights.md) para especificar o tipo de acesso necessário ao abrir um identificador para um objeto.</span><span class="sxs-lookup"><span data-stu-id="50afb-110">Use [generic access rights](generic-access-rights.md) to specify the type of access needed when opening a handle to an object.</span></span> <span data-ttu-id="50afb-111">Normalmente, isso é mais simples do que especificar todos os direitos padrão e específicos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="50afb-111">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span> <span data-ttu-id="50afb-112">Como alternativa, use a \_ constante máxima permitida para solicitar que o objeto seja aberto com todos os direitos de acesso válidos para o chamador.</span><span class="sxs-lookup"><span data-stu-id="50afb-112">Alternatively, use the MAXIMUM\_ALLOWED constant to request that the object be opened with all the access rights that are valid for the caller.</span></span>

> [!Note]  
> <span data-ttu-id="50afb-113">A \_ constante máxima permitida não pode ser usada em uma ACE.</span><span class="sxs-lookup"><span data-stu-id="50afb-113">The MAXIMUM\_ALLOWED constant cannot be used in an ACE.</span></span>

 

<span data-ttu-id="50afb-114">Para obter ou definir a SACL no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto, solicite o [direito de acesso de \_ \_ segurança do sistema de acesso](sacl-access-right.md) ao abrir um identificador para o objeto.</span><span class="sxs-lookup"><span data-stu-id="50afb-114">To get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), request the [ACCESS\_SYSTEM\_SECURITY access right](sacl-access-right.md) when opening a handle to the object.</span></span>

 

 
