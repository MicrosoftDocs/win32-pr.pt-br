---
description: O fragmento de código a seguir ilustra a publicação de um objeto de usuário em um servidor ILS. Depois que um objeto de usuário é publicado, partes remotas podem usar o objeto de usuário para fazer chamadas para o usuário especificado.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Adicionando um objeto de usuário a um servidor ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646970"
---
# <a name="adding-a-user-object-to-an-ils-server"></a><span data-ttu-id="e976d-104">Adicionando um objeto de usuário a um servidor ILS</span><span class="sxs-lookup"><span data-stu-id="e976d-104">Adding a User Object to an ILS Server</span></span>

<span data-ttu-id="e976d-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e976d-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e976d-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e976d-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e976d-107">O fragmento de código a seguir ilustra a publicação de um objeto de usuário em um servidor ILS.</span><span class="sxs-lookup"><span data-stu-id="e976d-107">The following code fragment illustrates publishing a user object in an ILS server.</span></span> <span data-ttu-id="e976d-108">Depois que um objeto de usuário é publicado, partes remotas podem usar o objeto de usuário para fazer chamadas para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="e976d-108">After a user object is published, remote parties can use the user object to make calls to the specified user.</span></span>

<span data-ttu-id="e976d-109">Este fragmento pressupõe que [a conexão com um servidor ILS](connecting-to-an-ils-server.md) já foi executada.</span><span class="sxs-lookup"><span data-stu-id="e976d-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a><span data-ttu-id="e976d-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e976d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e976d-111">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="e976d-111">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="e976d-112">**ITDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="e976d-112">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="e976d-113">**ITDirectoryObjectUser**</span><span class="sxs-lookup"><span data-stu-id="e976d-113">**ITDirectoryObjectUser**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



