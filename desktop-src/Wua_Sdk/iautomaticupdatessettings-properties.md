---
description: A interface IAutomaticUpdatesSettings define as propriedades a seguir.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Propriedades de IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920973"
---
# <a name="iautomaticupdatessettings-properties"></a><span data-ttu-id="14d3a-103">Propriedades de IAutomaticUpdatesSettings</span><span class="sxs-lookup"><span data-stu-id="14d3a-103">IAutomaticUpdatesSettings Properties</span></span>

<span data-ttu-id="14d3a-104">A interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="14d3a-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following properties.</span></span>



| <span data-ttu-id="14d3a-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="14d3a-105">Property</span></span>                                                                                 | <span data-ttu-id="14d3a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="14d3a-106">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14d3a-107">**NotificationLevel**</span><span class="sxs-lookup"><span data-stu-id="14d3a-107">**NotificationLevel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | <span data-ttu-id="14d3a-108">Obtém e define como os usuários são notificados sobre eventos de atualização automática.</span><span class="sxs-lookup"><span data-stu-id="14d3a-108">Gets and sets how users are notified about Automatic Update events.</span></span>                              |
| [<span data-ttu-id="14d3a-109">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="14d3a-109">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | <span data-ttu-id="14d3a-110">Obtém um valor booliano que indica se as configurações de atualização automática são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="14d3a-110">Gets a Boolean value that indicates whether the Automatic Update settings are read-only.</span></span>         |
| [<span data-ttu-id="14d3a-111">**Necessário**</span><span class="sxs-lookup"><span data-stu-id="14d3a-111">**Required**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | <span data-ttu-id="14d3a-112">Obtém um valor booliano que indica se Política de Grupo requer o serviço Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="14d3a-112">Gets a Boolean value that indicates whether Group Policy requires the Automatic Updates service.</span></span> |
| [<span data-ttu-id="14d3a-113">**ScheduledInstallationDay**</span><span class="sxs-lookup"><span data-stu-id="14d3a-113">**ScheduledInstallationDay**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | <span data-ttu-id="14d3a-114">Obtém e define os dias da semana em que Atualizações Automáticas instala ou desinstala atualizações.</span><span class="sxs-lookup"><span data-stu-id="14d3a-114">Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates.</span></span>    |
| [<span data-ttu-id="14d3a-115">**ScheduledInstallationTime**</span><span class="sxs-lookup"><span data-stu-id="14d3a-115">**ScheduledInstallationTime**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | <span data-ttu-id="14d3a-116">Obtém e define a hora em que o Atualizações Automáticas instala ou desinstala atualizações.</span><span class="sxs-lookup"><span data-stu-id="14d3a-116">Gets and sets the time at which Automatic Updates installs or uninstalls updates.</span></span>                |



 

> [!Note]  
> <span data-ttu-id="14d3a-117">O Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2 fornecem apenas suporte limitado para [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) e [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="14d3a-117">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2 provide only limited support for [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) and [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="14d3a-118">Se o computador tiver sido configurado por meio de Política de Grupo para usar um dia e hora de instalação agendada, as propriedades **ScheduledInstallationDay** e **ScheduledInstallationTime** retornarão esse dia e hora agendados.</span><span class="sxs-lookup"><span data-stu-id="14d3a-118">If the computer has been configured through Group Policy to use a scheduled installation day and time, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return this scheduled day and time.</span></span> <span data-ttu-id="14d3a-119">Se o computador não tiver sido configurado por meio de Política de Grupo dessa forma, as propriedades **ScheduledInstallationDay** e **ScheduledInstallationTime** retornarão valores padrão e não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="14d3a-119">If the computer hasn't been configured through Group Policy in this way, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return default and unreliable values.</span></span> <span data-ttu-id="14d3a-120">Se você tentar modificar o dia e a hora da instalação agendada nesses sistemas operacionais, **ScheduledInstallationDay** e **ScheduledInstallationTime** parecem ter sucesso, mas não têm efeito.</span><span class="sxs-lookup"><span data-stu-id="14d3a-120">If you try to modify the scheduled installation day and time on these operating systems, **ScheduledInstallationDay** and **ScheduledInstallationTime** appear to succeed but have no effect.</span></span>

 

 

 



