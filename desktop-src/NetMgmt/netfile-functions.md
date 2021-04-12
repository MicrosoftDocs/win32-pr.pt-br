---
title: Funções de netfile (gerenciamento de rede)
description: As funções de arquivo de gerenciamento de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor. As funções de arquivo são listadas a seguir.
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499217"
---
# <a name="netfile-functions-network-management"></a><span data-ttu-id="86b3b-104">Funções de netfile (gerenciamento de rede)</span><span class="sxs-lookup"><span data-stu-id="86b3b-104">NetFile Functions (Network Management)</span></span>

<span data-ttu-id="86b3b-105">As funções de arquivo de gerenciamento de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="86b3b-105">The network management file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="86b3b-106">As funções de arquivo são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="86b3b-106">The file functions are listed following.</span></span>



| <span data-ttu-id="86b3b-107">Função</span><span class="sxs-lookup"><span data-stu-id="86b3b-107">Function</span></span>                                | <span data-ttu-id="86b3b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="86b3b-108">Description</span></span>                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="86b3b-109">**NetFileClose**</span><span class="sxs-lookup"><span data-stu-id="86b3b-109">**NetFileClose**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="86b3b-110">Força o fechamento de um recurso.</span><span class="sxs-lookup"><span data-stu-id="86b3b-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="86b3b-111">**NetFileEnum**</span><span class="sxs-lookup"><span data-stu-id="86b3b-111">**NetFileEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="86b3b-112">Retorna informações sobre arquivos abertos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="86b3b-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="86b3b-113">**NetFileGetInfo**</span><span class="sxs-lookup"><span data-stu-id="86b3b-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="86b3b-114">Retorna informações sobre uma abertura específica de um recurso de servidor.</span><span class="sxs-lookup"><span data-stu-id="86b3b-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="86b3b-115">Chame a função [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) quando o arquivo não puder ser fechado por outros meios.</span><span class="sxs-lookup"><span data-stu-id="86b3b-115">Call the [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="86b3b-116">Essa função deve ser usada com cautela porque o **NetFileClose** não grava dados armazenados em cache no sistema cliente para o arquivo antes de fechar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="86b3b-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="86b3b-117">A função [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) retorna informações sobre os recursos abertos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="86b3b-117">The [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="86b3b-118">Um arquivo pode ser aberto uma ou mais vezes por um ou mais aplicativos.</span><span class="sxs-lookup"><span data-stu-id="86b3b-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="86b3b-119">Cada abertura de arquivo é identificada exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="86b3b-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="86b3b-120">A função **NetFileEnum** retorna uma entrada para cada abertura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="86b3b-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="86b3b-121">A função [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) retorna informações sobre uma abertura de um recurso.</span><span class="sxs-lookup"><span data-stu-id="86b3b-121">The [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="86b3b-122">As informações do arquivo estão disponíveis nos seguintes níveis:</span><span class="sxs-lookup"><span data-stu-id="86b3b-122">File information is available at the following levels:</span></span>

-   [<span data-ttu-id="86b3b-123">**Informações do arquivo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="86b3b-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [<span data-ttu-id="86b3b-124">**Informações do arquivo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="86b3b-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

<span data-ttu-id="86b3b-125">Não há suporte para os níveis 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="86b3b-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="86b3b-126">O nível 2 retorna apenas o número de identificação atribuído ao recurso quando ele foi aberto.</span><span class="sxs-lookup"><span data-stu-id="86b3b-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="86b3b-127">O nível 3 retorna o número de identificação, as permissões, os bloqueios de arquivo e o nome do usuário que abriu o recurso.</span><span class="sxs-lookup"><span data-stu-id="86b3b-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="86b3b-128">Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) .</span><span class="sxs-lookup"><span data-stu-id="86b3b-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="86b3b-129">Para obter mais informações, consulte [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="86b3b-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
