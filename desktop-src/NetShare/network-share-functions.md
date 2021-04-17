---
description: As funções de compartilhamento de rede controlam recursos compartilhados. Um recurso compartilhado é um recurso local em um servidor (por exemplo, um diretório de disco, um dispositivo de impressão ou um pipe nomeado) que pode ser acessado por usuários e aplicativos na rede.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Funções de compartilhamento de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761410"
---
# <a name="network-share-functions"></a><span data-ttu-id="544b0-104">Funções de compartilhamento de rede</span><span class="sxs-lookup"><span data-stu-id="544b0-104">Network Share Functions</span></span>

<span data-ttu-id="544b0-105">As funções de compartilhamento de rede controlam recursos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="544b0-105">The network share functions control shared resources.</span></span> <span data-ttu-id="544b0-106">Um recurso compartilhado é um recurso local em um servidor (por exemplo, um diretório de disco, um dispositivo de impressão ou um pipe nomeado) que pode ser acessado por usuários e aplicativos na rede.</span><span class="sxs-lookup"><span data-stu-id="544b0-106">A shared resource is a local resource on a server (for example, a disk directory, print device, or named pipe) that can be accessed by users and applications on the network.</span></span>

<span data-ttu-id="544b0-107">As funções de compartilhamento são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="544b0-107">The share functions are listed following.</span></span>



| <span data-ttu-id="544b0-108">Função</span><span class="sxs-lookup"><span data-stu-id="544b0-108">Function</span></span>                                   | <span data-ttu-id="544b0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="544b0-109">Description</span></span>                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="544b0-110">**NetShareAdd**</span><span class="sxs-lookup"><span data-stu-id="544b0-110">**NetShareAdd**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | <span data-ttu-id="544b0-111">Compartilha um recurso em um servidor.</span><span class="sxs-lookup"><span data-stu-id="544b0-111">Shares a resource on a server.</span></span>                                       |
| [<span data-ttu-id="544b0-112">**NetShareCheck**</span><span class="sxs-lookup"><span data-stu-id="544b0-112">**NetShareCheck**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | <span data-ttu-id="544b0-113">Consulta se um servidor está compartilhando um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="544b0-113">Queries whether a server is sharing a device.</span></span>                        |
| [<span data-ttu-id="544b0-114">**NetShareDel**</span><span class="sxs-lookup"><span data-stu-id="544b0-114">**NetShareDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | <span data-ttu-id="544b0-115">Exclui um nome de compartilhamento da lista de recursos compartilhados de um servidor.</span><span class="sxs-lookup"><span data-stu-id="544b0-115">Deletes a share name from a server's list of shared resources.</span></span>       |
| [<span data-ttu-id="544b0-116">**NetShareEnum**</span><span class="sxs-lookup"><span data-stu-id="544b0-116">**NetShareEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | <span data-ttu-id="544b0-117">Recupera informações de compartilhamento sobre cada recurso compartilhado em um servidor.</span><span class="sxs-lookup"><span data-stu-id="544b0-117">Retrieves share information about each shared resource on a server.</span></span>  |
| [<span data-ttu-id="544b0-118">**NetShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="544b0-118">**NetShareGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | <span data-ttu-id="544b0-119">Recupera informações sobre um recurso compartilhado especificado em um servidor.</span><span class="sxs-lookup"><span data-stu-id="544b0-119">Retrieves information about a specified shared resource on a server.</span></span> |
| [<span data-ttu-id="544b0-120">**NetShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="544b0-120">**NetShareSetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | <span data-ttu-id="544b0-121">Define os parâmetros de um recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="544b0-121">Sets a shared resource's parameters.</span></span>                                 |



 

<span data-ttu-id="544b0-122">A função [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) permite que um usuário ou aplicativo Compartilhe um recurso de um tipo específico usando o nome de compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="544b0-122">The [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) function allows a user or application to share a resource of a specific type using the specified share name.</span></span> <span data-ttu-id="544b0-123">A função **NetShareAdd** requer o nome do compartilhamento e o nome do dispositivo local para compartilhar o recurso.</span><span class="sxs-lookup"><span data-stu-id="544b0-123">The **NetShareAdd** function requires the share name and local device name to share the resource.</span></span> <span data-ttu-id="544b0-124">Um usuário ou aplicativo deve ter uma conta no servidor para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="544b0-124">A user or application must have an account on the server to access the resource.</span></span>

<span data-ttu-id="544b0-125">Você também pode especificar um descritor de segurança a ser associado a um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="544b0-125">You can also specify a security descriptor to be associated with a share.</span></span> <span data-ttu-id="544b0-126">Descritores de segurança especificam quais usuários têm permissão para acessar arquivos por meio do compartilhamento e com que tipo de acesso.</span><span class="sxs-lookup"><span data-stu-id="544b0-126">Security descriptors specify which users are allowed to access files through the share, and with what type of access.</span></span> <span data-ttu-id="544b0-127">Especifique um [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) com o nível de informações do [**share \_ info \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) ao chamar [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) ou [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span><span class="sxs-lookup"><span data-stu-id="544b0-127">Specify a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) with the [**SHARE\_INFO\_502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) information level when calling [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) or [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span></span> <span data-ttu-id="544b0-128">O **NetShareSetInfo** dá suporte ao nível de informação [**\_ \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) de informações de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="544b0-128">**NetShareSetInfo** supports the [**SHARE\_INFO\_1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) information level.</span></span> <span data-ttu-id="544b0-129">Para obter mais informações sobre descritores de segurança, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="544b0-129">For more information about security descriptors, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="544b0-130">As funções de gerenciamento de rede usam os seguintes nomes de compartilhamento especiais para IPC (comunicação entre processos) e administração remota do servidor:</span><span class="sxs-lookup"><span data-stu-id="544b0-130">The network management functions use the following special share names for interprocess communication (IPC) and remote administration of the server:</span></span>

-   <span data-ttu-id="544b0-131">IPC $, reservado para comunicação entre processos</span><span class="sxs-lookup"><span data-stu-id="544b0-131">IPC$, reserved for interprocess communication</span></span>
-   <span data-ttu-id="544b0-132">ADMIN $, reservado para administração remota</span><span class="sxs-lookup"><span data-stu-id="544b0-132">ADMIN$, reserved for remote administration</span></span>
-   <span data-ttu-id="544b0-133">R $, B $, C $ (e outros nomes de disco locais seguidos de um cifrão), atribuídos aos dispositivos de disco locais</span><span class="sxs-lookup"><span data-stu-id="544b0-133">A$, B$, C$ (and other local disk names followed by a dollar sign), assigned to local disk devices</span></span>

<span data-ttu-id="544b0-134">Para listar todas as conexões feitas a um recurso compartilhado em um servidor ou para listar todas as conexões estabelecidas de um determinado computador, chame a função [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) .</span><span class="sxs-lookup"><span data-stu-id="544b0-134">To list all connections made to a shared resource on a server, or to list all connections established from a particular computer, call the [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) function.</span></span> <span data-ttu-id="544b0-135">Você pode chamar **NetConnectionEnum** nas informações [**de \_ conexão \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) e informações de [**conexão \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) níveis de informação.</span><span class="sxs-lookup"><span data-stu-id="544b0-135">You can call **NetConnectionEnum** at the [**CONNECTION\_INFO\_0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) and [**CONNECTION\_INFO\_1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) information levels.</span></span>

<span data-ttu-id="544b0-136">As funções de compartilhamento estão disponíveis nos seguintes níveis de informações:</span><span class="sxs-lookup"><span data-stu-id="544b0-136">Share functions are available at the following information levels:</span></span>

<dl>

[<span data-ttu-id="544b0-137">**Informações de compartilhamento \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="544b0-137">**SHARE\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[<span data-ttu-id="544b0-138">**Informações de compartilhamento \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="544b0-138">**SHARE\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[<span data-ttu-id="544b0-139">**Informações de compartilhamento \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="544b0-139">**SHARE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[<span data-ttu-id="544b0-140">**Informações de compartilhamento \_ \_ 501**</span><span class="sxs-lookup"><span data-stu-id="544b0-140">**SHARE\_INFO\_501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[<span data-ttu-id="544b0-141">**Informações de compartilhamento \_ \_ 502**</span><span class="sxs-lookup"><span data-stu-id="544b0-141">**SHARE\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[<span data-ttu-id="544b0-142">**Informações de compartilhamento \_ \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="544b0-142">**SHARE\_INFO\_1005**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

<span data-ttu-id="544b0-143">Os seguintes níveis de informações são válidos somente para [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span><span class="sxs-lookup"><span data-stu-id="544b0-143">The following information levels are valid only for [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span></span>

<dl>

[<span data-ttu-id="544b0-144">**Informações de compartilhamento \_ \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="544b0-144">**SHARE\_INFO\_1004**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[<span data-ttu-id="544b0-145">**Informações de compartilhamento \_ \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="544b0-145">**SHARE\_INFO\_1006**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[<span data-ttu-id="544b0-146">**Informações de compartilhamento \_ \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="544b0-146">**SHARE\_INFO\_1501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

<span data-ttu-id="544b0-147">Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções de compartilhamento de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="544b0-147">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions.</span></span> <span data-ttu-id="544b0-148">Para obter mais informações, consulte [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span><span class="sxs-lookup"><span data-stu-id="544b0-148">For more information, see [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span></span>

 

 
