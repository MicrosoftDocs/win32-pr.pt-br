---
description: Os metaqualificadores refinam a definição de metaconstruções no modelo CIM, esclarecendo o uso real de uma classe ou declaração de propriedade dentro da sintaxe do MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Metaqualificadores
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755268"
---
# <a name="meta-qualifiers"></a><span data-ttu-id="f797c-103">Metaqualificadores</span><span class="sxs-lookup"><span data-stu-id="f797c-103">Meta Qualifiers</span></span>

<span data-ttu-id="f797c-104">Os metaqualificadores refinam a definição de metaconstruções no modelo CIM, esclarecendo o uso real de uma classe ou declaração de propriedade dentro da sintaxe do MOF.</span><span class="sxs-lookup"><span data-stu-id="f797c-104">Meta qualifiers refine the definition of meta-constructs in the CIM model by clarifying the actual usage of a class or property declaration within the MOF syntax.</span></span>

<dt>

<span data-ttu-id="f797c-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Associação**</span><span class="sxs-lookup"><span data-stu-id="f797c-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**</span></span>
</dt> <dd>

<span data-ttu-id="f797c-106">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f797c-106">Data type: **boolean**</span></span>

<span data-ttu-id="f797c-107">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="f797c-107">Applies to: classes</span></span>

<span data-ttu-id="f797c-108">Indica se a classe é uma classe de associação usada para descrever uma relação entre duas outras classes.</span><span class="sxs-lookup"><span data-stu-id="f797c-108">Indicates whether the class is an association class used to describe a relationship between two other classes.</span></span> <span data-ttu-id="f797c-109">A ausência desse qualificador indica que a classe não é uma classe de associação.</span><span class="sxs-lookup"><span data-stu-id="f797c-109">The absence of this qualifier indicates that the class is not an association class.</span></span> <span data-ttu-id="f797c-110">Esse qualificador é mutuamente exclusivo com a **indicação**.</span><span class="sxs-lookup"><span data-stu-id="f797c-110">This qualifier is mutually exclusive with **Indication**.</span></span> <span data-ttu-id="f797c-111">Para obter mais informações, consulte [declarando uma classe de associação](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="f797c-111">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="f797c-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indicações**</span><span class="sxs-lookup"><span data-stu-id="f797c-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**</span></span>
</dt> <dd>

<span data-ttu-id="f797c-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f797c-113">Data type: **boolean**</span></span>

<span data-ttu-id="f797c-114">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="f797c-114">Applies to: classes</span></span>

<span data-ttu-id="f797c-115">Indica se a classe de objeto define uma indicação.</span><span class="sxs-lookup"><span data-stu-id="f797c-115">Indicates whether the object class defines an indication.</span></span> <span data-ttu-id="f797c-116">Esse qualificador é mutuamente exclusivo com **Associação**.</span><span class="sxs-lookup"><span data-stu-id="f797c-116">This qualifier is mutually exclusive with **Association**.</span></span> <span data-ttu-id="f797c-117">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="f797c-117">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f797c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f797c-118">Requirements</span></span>



| <span data-ttu-id="f797c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f797c-119">Requirement</span></span> | <span data-ttu-id="f797c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f797c-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f797c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f797c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f797c-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f797c-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f797c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f797c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f797c-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f797c-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f797c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f797c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f797c-126">Qualificadores WMI</span><span class="sxs-lookup"><span data-stu-id="f797c-126">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="f797c-127">Adicionando um qualificador</span><span class="sxs-lookup"><span data-stu-id="f797c-127">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




