---
description: O Windows 8 e o Windows Server 2012 incluem os novos recursos a seguir para serviços.
ms.assetid: 42BC7325-4FAC-493E-95AC-AEF660F499C0
title: Novidades em serviços para o Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0087739c503a05875ba1a7eac5f77d33d8d1abac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501968"
---
# <a name="whats-new-in-services-for-windows-8"></a><span data-ttu-id="93771-103">O que há de novo nos serviços do Windows 8</span><span class="sxs-lookup"><span data-stu-id="93771-103">What's New in Services for Windows 8</span></span>

<span data-ttu-id="93771-104">O Windows 8 e o Windows Server 2012 incluem os novos recursos a seguir para serviços.</span><span class="sxs-lookup"><span data-stu-id="93771-104">Windows 8 and Windows Server 2012 include the following new capabilities for services.</span></span>

## <a name="new-service-functions"></a><span data-ttu-id="93771-105">Novas funções de serviço</span><span class="sxs-lookup"><span data-stu-id="93771-105">New Service Functions</span></span>



| <span data-ttu-id="93771-106">Função</span><span class="sxs-lookup"><span data-stu-id="93771-106">Function</span></span>                                                                            | <span data-ttu-id="93771-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="93771-107">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="93771-108">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="93771-108">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)<br/> | <span data-ttu-id="93771-109">Recupera informações dinâmicas relacionadas ao início do serviço atual.</span><span class="sxs-lookup"><span data-stu-id="93771-109">Retrieves dynamic information related to the current service start.</span></span><br/> |



 

## <a name="updated-api-elements"></a><span data-ttu-id="93771-110">Elementos de API atualizados</span><span class="sxs-lookup"><span data-stu-id="93771-110">Updated API Elements</span></span>



| <span data-ttu-id="93771-111">Elemento API</span><span class="sxs-lookup"><span data-stu-id="93771-111">API Element</span></span>                                                                                     | <span data-ttu-id="93771-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="93771-112">Description</span></span>                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93771-113">**HandlerEx**</span><span class="sxs-lookup"><span data-stu-id="93771-113">**HandlerEx**</span></span>](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                                                       | <span data-ttu-id="93771-114">Adicionado **\_ \_ USERMODEREBOOT de controle de serviço**.</span><span class="sxs-lookup"><span data-stu-id="93771-114">Added **SERVICE\_CONTROL\_USERMODEREBOOT**.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="93771-115">**STATUS do serviço \_**</span><span class="sxs-lookup"><span data-stu-id="93771-115">**SERVICE\_STATUS**</span></span>](/windows/desktop/api/Winsvc/ns-winsvc-service_status)<br/>                                        | <span data-ttu-id="93771-116">**USERMODEREBOOT de \_ aceitação \_ de serviço** adicionado.</span><span class="sxs-lookup"><span data-stu-id="93771-116">Added **SERVICE\_ACCEPT\_USERMODEREBOOT**.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="93771-117">**\_item de \_ \_ dados específico do gatilho \_ de serviço**</span><span class="sxs-lookup"><span data-stu-id="93771-117">**SERVICE\_TRIGGER\_SPECIFIC\_DATA\_ITEM**</span></span>](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | <span data-ttu-id="93771-118">**Nível de \_ \_ tipo de \_ dados \_ do gatilho de serviço** adicionado, tipo de dados de gatilho de **serviço \_ \_ \_ \_ \_ qualquer** e **tipo de dados de gatilho de serviço \_ \_ \_ \_ \_ All**.</span><span class="sxs-lookup"><span data-stu-id="93771-118">Added **SERVICE\_TRIGGER\_DATA\_TYPE\_LEVEL**, **SERVICE\_TRIGGER\_DATA\_TYPE\_KEYWORD\_ANY**, and **SERVICE\_TRIGGER\_DATA\_TYPE\_KEYWORD\_ALL**.</span></span><br/> |



 

 

 




