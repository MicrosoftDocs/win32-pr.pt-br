---
description: Interfaces do dispensador de recursos COM+
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: Interfaces do dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a6ea5c5c09f67f86b42ebf5b881f1d19ad1501
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826258"
---
# <a name="com-resource-dispenser-interfaces"></a><span data-ttu-id="1f43f-103">Interfaces do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="1f43f-103">COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="1f43f-104">Os componentes do aplicativo usam dispensadores de recursos para acessar informações compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="1f43f-104">Application components use resource dispensers to access shared information.</span></span> <span data-ttu-id="1f43f-105">As interfaces descritas na tabela a seguir fornecem informações de referência detalhadas para desenvolvedores de dispensadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f43f-105">The interfaces described in the following table provide detailed reference information for developers of resource dispensers.</span></span>



| <span data-ttu-id="1f43f-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="1f43f-106">Interfaces</span></span>                                                | <span data-ttu-id="1f43f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f43f-107">Description</span></span>                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f43f-108">**IDispenserDriver**</span><span class="sxs-lookup"><span data-stu-id="1f43f-108">**IDispenserDriver**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | <span data-ttu-id="1f43f-109">Essa interface é chamada pelo titular do dispensador de recursos para criar, inscrever, avaliar e destruir um recurso.</span><span class="sxs-lookup"><span data-stu-id="1f43f-109">This interface is called by the resource dispenser holder to create, enlist, evaluate, and destroy a resource.</span></span><br/> |
| [<span data-ttu-id="1f43f-110">**IDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="1f43f-110">**IDispenserManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | <span data-ttu-id="1f43f-111">Os dispensadores de recursos usam essa interface para se conectar ao Gerenciador do dispensador.</span><span class="sxs-lookup"><span data-stu-id="1f43f-111">Resource dispensers use this interface to connect to the dispenser manager.</span></span><br/>                                    |
| [<span data-ttu-id="1f43f-112">**IHolder**</span><span class="sxs-lookup"><span data-stu-id="1f43f-112">**IHolder**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | <span data-ttu-id="1f43f-113">Essa interface é usada para preparar e manipular recursos.</span><span class="sxs-lookup"><span data-stu-id="1f43f-113">This interface is used to prepare and handle resources.</span></span><br/>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="1f43f-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f43f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f43f-115">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="1f43f-115">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="1f43f-116">Tipos usados em interfaces de dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="1f43f-116">Types Used in COM+ Resource Dispenser Interfaces</span></span>](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




