---
description: O qualificador dinâmico indica uma classe cujas instâncias são criadas dinamicamente. O valor desse qualificador deve ser definido como TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Qualificador dinâmico
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827841"
---
# <a name="dynamic-qualifier"></a><span data-ttu-id="467a7-104">Qualificador dinâmico</span><span class="sxs-lookup"><span data-stu-id="467a7-104">Dynamic Qualifier</span></span>

<span data-ttu-id="467a7-105">O qualificador **dinâmico** indica uma classe cujas instâncias são criadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="467a7-105">The **Dynamic** qualifier indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="467a7-106">O valor desse qualificador deve ser definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="467a7-106">The value of this qualifier must be set to **TRUE**.</span></span>

<span data-ttu-id="467a7-107">O qualificador **dinâmico** deve ser especificado em todas as classes que contêm dados e para quais instâncias são criadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="467a7-107">The **Dynamic** qualifier must be specified on all classes that contain data and for which instances are created dynamically.</span></span> <span data-ttu-id="467a7-108">O qualificador de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) normalmente também é especificado para identificar o provedor responsável por fornecer os dados.</span><span class="sxs-lookup"><span data-stu-id="467a7-108">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is typically also specified to identify the provider responsible for supplying the data.</span></span>

<span data-ttu-id="467a7-109">As classes que contêm apenas métodos que precisam de implementação não exigem o qualificador **dinâmico** .</span><span class="sxs-lookup"><span data-stu-id="467a7-109">Classes that contain only methods that need implementation do not require the **Dynamic** qualifier.</span></span> <span data-ttu-id="467a7-110">Somente o qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) é necessário para especificar o nome do provedor para fornecer a implementação.</span><span class="sxs-lookup"><span data-stu-id="467a7-110">Only the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is required to specify the name of the provider to supply the implementation.</span></span>

<span data-ttu-id="467a7-111">Todas as classes derivadas de uma classe dinâmica devem ser dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="467a7-111">All classes derived from a dynamic class must be dynamic.</span></span> <span data-ttu-id="467a7-112">Você não pode derivar uma classe estática de uma classe dinâmica.</span><span class="sxs-lookup"><span data-stu-id="467a7-112">You cannot derive a static class from a dynamic class.</span></span>

<span data-ttu-id="467a7-113">Quando **Dynamic** é especificado em uma propriedade de uma instância, o qualificador **PropertyContext** também deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="467a7-113">When **Dynamic** is specified on a property of an instance, the **PropertyContext** qualifier must also be specified.</span></span>

## <a name="requirements"></a><span data-ttu-id="467a7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="467a7-114">Requirements</span></span>



| <span data-ttu-id="467a7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="467a7-115">Requirement</span></span> | <span data-ttu-id="467a7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="467a7-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="467a7-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="467a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="467a7-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="467a7-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="467a7-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="467a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="467a7-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="467a7-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="467a7-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="467a7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="467a7-122">**Qualificadores WMI padrão**</span><span class="sxs-lookup"><span data-stu-id="467a7-122">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="467a7-123">Qualificadores WMI</span><span class="sxs-lookup"><span data-stu-id="467a7-123">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="467a7-124">Adicionando um qualificador</span><span class="sxs-lookup"><span data-stu-id="467a7-124">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




