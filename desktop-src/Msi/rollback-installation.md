---
description: Quando o Windows Installer processa o script de instalação para a instalação de um produto ou aplicativo, ele gera simultaneamente um script de reversão e salva uma cópia de todos os arquivos excluídos durante a instalação.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Reverter instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091129"
---
# <a name="rollback-installation"></a><span data-ttu-id="60e93-103">Reverter instalação</span><span class="sxs-lookup"><span data-stu-id="60e93-103">Rollback Installation</span></span>

<span data-ttu-id="60e93-104">Quando o Windows Installer processa o script de instalação para a instalação de um produto ou aplicativo, ele gera simultaneamente um script de reversão e salva uma cópia de todos os arquivos excluídos durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="60e93-104">When the Windows Installer processes the installation script for the installation of a product or application, it simultaneously generates a rollback script and saves a copy of every file deleted during the installation.</span></span> <span data-ttu-id="60e93-105">Esses arquivos são mantidos em um diretório de sistema oculto e são excluídos automaticamente quando a instalação é concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="60e93-105">These files are kept in a hidden system directory and are automatically deleted once the installation is successfully completed.</span></span> <span data-ttu-id="60e93-106">Se, no entanto, a instalação não for bem-sucedida, o instalador executará automaticamente uma reversão da instalação que retorna o sistema ao seu estado original.</span><span class="sxs-lookup"><span data-stu-id="60e93-106">If however the installation is unsuccessful, the installer automatically performs a rollback installation that returns the system to its original state.</span></span>

<span data-ttu-id="60e93-107">A reversão automática de uma instalação malsucedida é o comportamento padrão do instalador.</span><span class="sxs-lookup"><span data-stu-id="60e93-107">Automatic rollback of an unsuccessful installation is the default behavior of the installer.</span></span> <span data-ttu-id="60e93-108">Para desabilitar a reversão durante uma instalação, use um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="60e93-108">To disable rollback during an installation use one of the following:</span></span>

-   [<span data-ttu-id="60e93-109">**Propriedade DISABLEROLLBACK**</span><span class="sxs-lookup"><span data-stu-id="60e93-109">**DISABLEROLLBACK Property**</span></span>](-disablerollback.md)
-   [<span data-ttu-id="60e93-110">**Propriedade PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="60e93-110">**PROMPTROLLBACKCOST Property**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="60e93-111">Ação DisableRollback</span><span class="sxs-lookup"><span data-stu-id="60e93-111">DisableRollback Action</span></span>](disablerollback-action.md)
-   [<span data-ttu-id="60e93-112">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="60e93-112">DisableRollback</span></span>](disablerollback.md)
-   [<span data-ttu-id="60e93-113">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="60e93-113">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

<span data-ttu-id="60e93-114">Sempre que a reversão é desabilitada, o instalador define a propriedade [**RollbackDisabled**](rollbackdisabled.md) .</span><span class="sxs-lookup"><span data-stu-id="60e93-114">Whenever rollback is disabled, the installer sets the [**RollbackDisabled**](rollbackdisabled.md) property.</span></span>

<span data-ttu-id="60e93-115">Se uma instalação usar [ações personalizadas](custom-actions.md), será necessária a criação adicional do pacote de instalação para usar a funcionalidade de reversão.</span><span class="sxs-lookup"><span data-stu-id="60e93-115">If an installation uses [custom actions](custom-actions.md), additional authoring of the installation package is required to use rollback functionality.</span></span> <span data-ttu-id="60e93-116">Para obter mais informações, consulte [Rollback Custom Actions](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="60e93-116">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



