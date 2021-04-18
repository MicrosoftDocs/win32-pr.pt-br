---
title: Elemento Task (Definitiontype)
description: Define um evento específico de tarefa que seu provedor pode registrar. | Elemento Task (Definitiontype)
ms.assetid: 0e880720-1896-43cf-b702-cabca8ab1430
keywords:
- elemento de tarefa EventLog
topic_type:
- apiref
api_name:
- task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35fe629c17b8ede4064de3fb11d05c8e8c84f202
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788814"
---
# <a name="task-definitiontype-element"></a><span data-ttu-id="bc9fe-105">Elemento Task (Definitiontype)</span><span class="sxs-lookup"><span data-stu-id="bc9fe-105">task (DefinitionType) Element</span></span>

<span data-ttu-id="bc9fe-106">\[A partir do compilador de mensagens fornecido com a versão do Windows 7 do SDK do Windows, esse elemento não estará mais disponível.\]</span><span class="sxs-lookup"><span data-stu-id="bc9fe-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="bc9fe-107">Define um evento específico de tarefa que seu provedor pode registrar.</span><span class="sxs-lookup"><span data-stu-id="bc9fe-107">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:element name="task"
    type="TaskEventDefinitionType"
 />
```

<span data-ttu-id="bc9fe-108">O elemento **Task** é definido pelo tipo complexo [**definitiontype**](eventmanifestschema-definitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bc9fe-108">The **task** element is defined by the [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc9fe-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc9fe-109">Requirements</span></span>



| <span data-ttu-id="bc9fe-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc9fe-110">Requirement</span></span> | <span data-ttu-id="bc9fe-111">Valor</span><span class="sxs-lookup"><span data-stu-id="bc9fe-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc9fe-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc9fe-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bc9fe-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc9fe-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc9fe-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc9fe-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bc9fe-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc9fe-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc9fe-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc9fe-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc9fe-117">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="bc9fe-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="bc9fe-118">**eventos (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="bc9fe-118">**events (ProviderType)**</span></span>](eventmanifestschema-events-providertype-element.md)
</dt> </dl>

 

 





