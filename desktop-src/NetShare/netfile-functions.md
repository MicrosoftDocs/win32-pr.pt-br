---
description: As funções de arquivo de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor. As funções de arquivo são listadas a seguir.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Funções de netfile (gerenciamento de compartilhamento de rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df51d556647f16cc30ec51182fde5dd5551831d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757752"
---
# <a name="netfile-functions-network-share-management"></a><span data-ttu-id="ecc17-104">Funções de netfile (gerenciamento de compartilhamento de rede)</span><span class="sxs-lookup"><span data-stu-id="ecc17-104">NetFile Functions (Network Share Management)</span></span>

<span data-ttu-id="ecc17-105">As funções de arquivo de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="ecc17-105">The network file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="ecc17-106">As funções de arquivo são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ecc17-106">The file functions are listed following.</span></span>



| <span data-ttu-id="ecc17-107">Função</span><span class="sxs-lookup"><span data-stu-id="ecc17-107">Function</span></span>                                 | <span data-ttu-id="ecc17-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ecc17-108">Description</span></span>                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="ecc17-109">**NetFileClose**</span><span class="sxs-lookup"><span data-stu-id="ecc17-109">**NetFileClose**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="ecc17-110">Força o fechamento de um recurso.</span><span class="sxs-lookup"><span data-stu-id="ecc17-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="ecc17-111">**NetFileEnum**</span><span class="sxs-lookup"><span data-stu-id="ecc17-111">**NetFileEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="ecc17-112">Retorna informações sobre arquivos abertos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="ecc17-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="ecc17-113">**NetFileGetInfo**</span><span class="sxs-lookup"><span data-stu-id="ecc17-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="ecc17-114">Retorna informações sobre uma abertura específica de um recurso de servidor.</span><span class="sxs-lookup"><span data-stu-id="ecc17-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="ecc17-115">Chame a função [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) quando o arquivo não puder ser fechado por outros meios.</span><span class="sxs-lookup"><span data-stu-id="ecc17-115">Call the [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="ecc17-116">Essa função deve ser usada com cautela porque o **NetFileClose** não grava dados armazenados em cache no sistema cliente para o arquivo antes de fechar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ecc17-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="ecc17-117">A função [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) retorna informações sobre os recursos abertos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="ecc17-117">The [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="ecc17-118">Um arquivo pode ser aberto uma ou mais vezes por um ou mais aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ecc17-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="ecc17-119">Cada abertura de arquivo é identificada exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="ecc17-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="ecc17-120">A função **NetFileEnum** retorna uma entrada para cada abertura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ecc17-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="ecc17-121">A função [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) retorna informações sobre uma abertura de um recurso.</span><span class="sxs-lookup"><span data-stu-id="ecc17-121">The [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="ecc17-122">As informações do arquivo estão disponíveis nos seguintes níveis.</span><span class="sxs-lookup"><span data-stu-id="ecc17-122">File information is available at the following levels.</span></span>

<dl>

[<span data-ttu-id="ecc17-123">**Informações do arquivo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ecc17-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[<span data-ttu-id="ecc17-124">**Informações do arquivo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ecc17-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

<span data-ttu-id="ecc17-125">Não há suporte para os níveis 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="ecc17-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="ecc17-126">O nível 2 retorna apenas o número de identificação atribuído ao recurso quando ele foi aberto.</span><span class="sxs-lookup"><span data-stu-id="ecc17-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="ecc17-127">O nível 3 retorna o número de identificação, as permissões, os bloqueios de arquivo e o nome do usuário que abriu o recurso.</span><span class="sxs-lookup"><span data-stu-id="ecc17-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="ecc17-128">Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) .</span><span class="sxs-lookup"><span data-stu-id="ecc17-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="ecc17-129">Para obter mais informações, consulte [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="ecc17-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
