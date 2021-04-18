---
description: O SCM dá suporte a tipos de identificadores para permitir o acesso aos objetos a seguir.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Identificadores SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749452"
---
# <a name="scm-handles"></a><span data-ttu-id="35cff-103">Identificadores SCM</span><span class="sxs-lookup"><span data-stu-id="35cff-103">SCM Handles</span></span>

<span data-ttu-id="35cff-104">O SCM dá suporte a tipos de identificadores para permitir o acesso aos objetos a seguir.</span><span class="sxs-lookup"><span data-stu-id="35cff-104">The SCM supports handle types to allow access to the following objects.</span></span>

-   <span data-ttu-id="35cff-105">O banco de dados dos serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="35cff-105">The database of installed services.</span></span>
-   <span data-ttu-id="35cff-106">Um serviço.</span><span class="sxs-lookup"><span data-stu-id="35cff-106">A service.</span></span>
-   <span data-ttu-id="35cff-107">O bloqueio do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35cff-107">The database lock.</span></span>

<span data-ttu-id="35cff-108">Um objeto SCManager representa o banco de dados dos serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="35cff-108">An SCManager object represents the database of installed services.</span></span> <span data-ttu-id="35cff-109">É um objeto de contêiner que mantém objetos de serviço.</span><span class="sxs-lookup"><span data-stu-id="35cff-109">It is a container object that holds service objects.</span></span> <span data-ttu-id="35cff-110">A função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) retorna um identificador para um objeto SCManager em um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="35cff-110">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function returns a handle to an SCManager object on a specified computer.</span></span> <span data-ttu-id="35cff-111">Esse identificador é usado ao instalar, excluir, abrir e enumerar serviços e ao bloquear o banco de dados de serviços.</span><span class="sxs-lookup"><span data-stu-id="35cff-111">This handle is used when installing, deleting, opening, and enumerating services and when locking the services database.</span></span>

<span data-ttu-id="35cff-112">Um objeto de serviço representa um serviço instalado.</span><span class="sxs-lookup"><span data-stu-id="35cff-112">A service object represents an installed service.</span></span> <span data-ttu-id="35cff-113">As funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) retornam identificadores para os serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="35cff-113">The [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions return handles to installed services.</span></span>

<span data-ttu-id="35cff-114">As funções [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) podem solicitar tipos diferentes de acesso a SCManager e a objetos de serviço.</span><span class="sxs-lookup"><span data-stu-id="35cff-114">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea), and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions can request different types of access to SCManager and service objects.</span></span> <span data-ttu-id="35cff-115">O acesso solicitado é concedido ou negado, dependendo do token de acesso do processo de chamada e do descritor de segurança associado ao objeto SCManager ou Service.</span><span class="sxs-lookup"><span data-stu-id="35cff-115">The requested access is granted or denied depending on the access token of the calling process and the security descriptor associated with the SCManager or service object.</span></span>

<span data-ttu-id="35cff-116">A função [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) fecha identificadores para SCManager e objetos de serviço.</span><span class="sxs-lookup"><span data-stu-id="35cff-116">The [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) function closes handles to SCManager and service objects.</span></span> <span data-ttu-id="35cff-117">Quando você não precisar mais desses identificadores, não deixe de fechá-los.</span><span class="sxs-lookup"><span data-stu-id="35cff-117">When you no longer need these handles, be sure to close them.</span></span>

 

 



