---
title: Texto de descrição do ponto de restauração
description: Quando um aplicativo chama a função SRSetRestorePoint, ele pode fornecer qualquer texto como uma descrição para o ponto de restauração; no entanto, a tabela a seguir mostra o texto de descrição recomendado.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159915"
---
# <a name="restore-point-description-text"></a><span data-ttu-id="583f2-103">Texto de descrição do ponto de restauração</span><span class="sxs-lookup"><span data-stu-id="583f2-103">Restore Point Description Text</span></span>

<span data-ttu-id="583f2-104">Quando um aplicativo chama a função [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , ele pode fornecer qualquer texto como uma descrição para o ponto de restauração; no entanto, a tabela a seguir mostra o texto de descrição recomendado.</span><span class="sxs-lookup"><span data-stu-id="583f2-104">When an application calls the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function, it can provide any text as a description for the restore point; however, the following table shows the recommended description text.</span></span>



| <span data-ttu-id="583f2-105">Modificação do sistema</span><span class="sxs-lookup"><span data-stu-id="583f2-105">System modification</span></span>                            | <span data-ttu-id="583f2-106">Tipo de ponto de restauração</span><span class="sxs-lookup"><span data-stu-id="583f2-106">Restore point type</span></span>      | <span data-ttu-id="583f2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="583f2-107">Description</span></span>            |
|------------------------------------------------|-------------------------|------------------------|
| <span data-ttu-id="583f2-108">Instalação do aplicativo</span><span class="sxs-lookup"><span data-stu-id="583f2-108">Application installation</span></span>                       | <span data-ttu-id="583f2-109">instalação do aplicativo \_</span><span class="sxs-lookup"><span data-stu-id="583f2-109">APPLICATION\_INSTALL</span></span>    | <span data-ttu-id="583f2-110">*AppName* instalado</span><span class="sxs-lookup"><span data-stu-id="583f2-110">Installed *AppName*</span></span>    |
| <span data-ttu-id="583f2-111">Modificação do aplicativo (Adicionar/remover recursos)</span><span class="sxs-lookup"><span data-stu-id="583f2-111">Application modification (add/remove features)</span></span> | <span data-ttu-id="583f2-112">MODIFICAR \_ configurações</span><span class="sxs-lookup"><span data-stu-id="583f2-112">MODIFY\_SETTINGS</span></span>        | <span data-ttu-id="583f2-113">*AppName* configurado</span><span class="sxs-lookup"><span data-stu-id="583f2-113">Configured *AppName*</span></span>   |
| <span data-ttu-id="583f2-114">Remoção do aplicativo</span><span class="sxs-lookup"><span data-stu-id="583f2-114">Application removal</span></span>                            | <span data-ttu-id="583f2-115">desinstalação do aplicativo \_</span><span class="sxs-lookup"><span data-stu-id="583f2-115">APPLICATION\_UNINSTALL</span></span>  | <span data-ttu-id="583f2-116">*AppName* removido</span><span class="sxs-lookup"><span data-stu-id="583f2-116">Removed *AppName*</span></span>      |
| <span data-ttu-id="583f2-117">Instalação do driver de dispositivo</span><span class="sxs-lookup"><span data-stu-id="583f2-117">Device driver installation</span></span>                     | <span data-ttu-id="583f2-118">\_instalação do driver de dispositivo \_</span><span class="sxs-lookup"><span data-stu-id="583f2-118">DEVICE\_DRIVER\_INSTALL</span></span> | <span data-ttu-id="583f2-119">*DriverName* instalado</span><span class="sxs-lookup"><span data-stu-id="583f2-119">Installed *DriverName*</span></span> |



 

<span data-ttu-id="583f2-120">Instaladores, como o Windows Installer e o InstallShield, usam essas convenções para o texto de descrição:</span><span class="sxs-lookup"><span data-stu-id="583f2-120">Installers, such as Windows Installer and InstallShield, use these conventions for the description text:</span></span>

-   <span data-ttu-id="583f2-121">O nome do produto segue o verbo; por exemplo, o *AppName* foi instalado.</span><span class="sxs-lookup"><span data-stu-id="583f2-121">The product name follows the verb; for example, Installed *AppName*.</span></span>
-   <span data-ttu-id="583f2-122">O nome do produto pode ser usado sozinha (*AppName*) ou o nome do produto e o nome da empresa pode ser usado (*MyCompany AppName*).</span><span class="sxs-lookup"><span data-stu-id="583f2-122">The product name can be used alone (*AppName*) or the product name and the company name may both be used (*MyCompany AppName*).</span></span>

 

 




