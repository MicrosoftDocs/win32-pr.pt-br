---
description: A interface IAutomaticUpdatesSettings define os métodos a seguir.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Métodos IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827703"
---
# <a name="iautomaticupdatessettings-methods"></a><span data-ttu-id="a3434-103">Métodos IAutomaticUpdatesSettings</span><span class="sxs-lookup"><span data-stu-id="a3434-103">IAutomaticUpdatesSettings Methods</span></span>

<span data-ttu-id="a3434-104">A interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3434-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following methods.</span></span>



| <span data-ttu-id="a3434-105">Método</span><span class="sxs-lookup"><span data-stu-id="a3434-105">Method</span></span>                                               | <span data-ttu-id="a3434-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3434-106">Description</span></span>                                      |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="a3434-107">**Atualizar**</span><span class="sxs-lookup"><span data-stu-id="a3434-107">**Refresh**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | <span data-ttu-id="a3434-108">Recupera as configurações de Atualizações Automáticas mais recentes.</span><span class="sxs-lookup"><span data-stu-id="a3434-108">Retrieves the latest Automatic Updates settings.</span></span> |
| [<span data-ttu-id="a3434-109">**Salvar**</span><span class="sxs-lookup"><span data-stu-id="a3434-109">**Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | <span data-ttu-id="a3434-110">Aplica as configurações de Atualizações Automáticas atuais.</span><span class="sxs-lookup"><span data-stu-id="a3434-110">Applies the current Automatic Updates settings.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="a3434-111">No Windows RT, você não pode mais usar o método [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) para definir configurações de Windows Update de forma programática.</span><span class="sxs-lookup"><span data-stu-id="a3434-111">On Windows RT, you can no longer use the [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) method to configure Windows Update settings programmatically.</span></span> <span data-ttu-id="a3434-112">A operação de configuração falhará se você usar **salvar** para definir qualquer valor diferente de 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span><span class="sxs-lookup"><span data-stu-id="a3434-112">The configuration operation fails if you use **Save** to set any value other than 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span></span>

 

 

 



