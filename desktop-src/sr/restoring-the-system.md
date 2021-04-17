---
title: Restaurando o sistema
description: À medida que o computador é usado ao longo do tempo, os pontos de restauração são coletados no arquivo de dados sem qualquer gerenciamento ou intervenção exigida pelo usuário.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763259"
---
# <a name="restoring-the-system"></a><span data-ttu-id="e4d28-103">Restaurando o sistema</span><span class="sxs-lookup"><span data-stu-id="e4d28-103">Restoring the System</span></span>

<span data-ttu-id="e4d28-104">À medida que o computador é usado ao longo do tempo, os pontos de restauração são coletados no arquivo de dados sem qualquer gerenciamento ou intervenção exigida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e4d28-104">As the computer is used over time, restore points are collected in the data archive without any management or intervention required by the user.</span></span> <span data-ttu-id="e4d28-105">Se o usuário precisar restaurar o sistema para um estado anterior, os pontos de restauração disponíveis serão visíveis para o usuário por meio da interface do usuário de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="e4d28-105">If the user ever needs to restore the system to a previous state, the available restore points are made visible to the user through the System Restore user interface.</span></span> <span data-ttu-id="e4d28-106">O usuário pode escolher qualquer um desses pontos de restauração.</span><span class="sxs-lookup"><span data-stu-id="e4d28-106">The user can choose any of these restore points.</span></span> <span data-ttu-id="e4d28-107">A única maneira de acessar esse arquivo de pontos de restauração é por meio da interface do usuário de restauração do sistema e da API de restauração do sistema; Isso é para proteger a integridade dos dados e evitar alterações acidentais feitas pelo usuário, aplicativos ou outros agentes.</span><span class="sxs-lookup"><span data-stu-id="e4d28-107">The only way to access this archive of restore points is through the System Restore user interface and the System Restore API; this is to protect data integrity and prevent accidental changes made by the user, applications, or other agents.</span></span>

<span data-ttu-id="e4d28-108">Para restaurar um sistema, a restauração do sistema desfaz alterações de arquivo feitas em arquivos monitorados, recapturando o estado do arquivo no momento do ponto de restauração selecionado.</span><span class="sxs-lookup"><span data-stu-id="e4d28-108">To restore a system, System Restore undoes file changes made to monitored files, recapturing the file state at the time of the selected restore point.</span></span> <span data-ttu-id="e4d28-109">Em seguida, ele substitui o registro atual pelo que foi salvo para o ponto de restauração selecionado.</span><span class="sxs-lookup"><span data-stu-id="e4d28-109">It then replaces the current registry with the one saved for the selected restore point.</span></span>

<span data-ttu-id="e4d28-110">Para garantir que seu aplicativo tenha o comportamento desejado após uma restauração, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e4d28-110">To ensure that your application has the desired behavior after a restore, do the following:</span></span>

-   <span data-ttu-id="e4d28-111">Não armazene informações no registro que impeçam o acesso do usuário a arquivos de dados pessoais ou aplicativos na restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="e4d28-111">Do not store information in the registry that prevents user access to personal data files or applications on system restore.</span></span> <span data-ttu-id="e4d28-112">Caso contrário, você deve fornecer um mecanismo pelo qual o usuário possa baixar e reinstalar os aplicativos sem precisar pagá-los novamente.</span><span class="sxs-lookup"><span data-stu-id="e4d28-112">Otherwise, you must provide a mechanism by which the user can download and reinstall the applications without having to pay for them again.</span></span>
-   <span data-ttu-id="e4d28-113">Use a [API de restauração do sistema](system-restore-api.md) para criar pontos de restauração significativos na instalação e na desinstalação.</span><span class="sxs-lookup"><span data-stu-id="e4d28-113">Use the [System Restore API](system-restore-api.md) to create meaningful restore points at install and uninstall.</span></span>
-   <span data-ttu-id="e4d28-114">No Windows XP, os principais binários do aplicativo a serem protegidos devem usar extensões consistentes com as usadas no Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="e4d28-114">In Windows XP, the key application binaries to be protected must use extensions consistent with those used in Filelist.xml.</span></span> <span data-ttu-id="e4d28-115">Para obter mais informações, consulte [extensões de nome de arquivo monitorado](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e4d28-115">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span> <span data-ttu-id="e4d28-116">Esse arquivo não é usado pelo Windows 7 e pelo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e4d28-116">This file is not used by Windows 7 and Windows Vista.</span></span> <span data-ttu-id="e4d28-117">Não use tipos de extensão monitorados para arquivos editáveis pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e4d28-117">Do not use monitored extension types for user-editable files.</span></span> <span data-ttu-id="e4d28-118">Por exemplo, se você nomear o arquivo de dados pessoais de um usuário usando a extensão. ini, o usuário poderá perder o trabalho como resultado de uma restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="e4d28-118">For example, if you name a user's personal data file using the extension .ini, the user may lose work as a result of a system restore.</span></span>

 

 




