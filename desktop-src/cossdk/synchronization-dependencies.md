---
description: Os valores de sincronização podem ser determinados ou restritos automaticamente pela configuração de outras propriedades, como requisitos transacionais e ativação JIT (just-in-time).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dependências de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826314"
---
# <a name="synchronization-dependencies"></a><span data-ttu-id="81de3-103">Dependências de sincronização</span><span class="sxs-lookup"><span data-stu-id="81de3-103">Synchronization Dependencies</span></span>

<span data-ttu-id="81de3-104">Os valores de sincronização podem ser determinados ou restritos automaticamente pela configuração de outras propriedades, como requisitos transacionais e ativação JIT (just-in-time).</span><span class="sxs-lookup"><span data-stu-id="81de3-104">Synchronization values can be automatically determined or constrained by the configuration of other properties, such as transactional requirements and just-in-time (JIT) activation.</span></span> <span data-ttu-id="81de3-105">Por exemplo, COM+ impõe a sincronização para os componentes transacionais e ativados por JIT.</span><span class="sxs-lookup"><span data-stu-id="81de3-105">For example, COM+ enforces synchronization both for transactional and for JIT-activated components.</span></span>

<span data-ttu-id="81de3-106">Essas dependências existem porque os componentes que são ativados por JIT ou que participam de transações devem ter isolamento adequado e comportamento de simultaneidade.</span><span class="sxs-lookup"><span data-stu-id="81de3-106">These dependencies exist because components that are JIT-activated or participating in transactions must have proper isolation and concurrency behavior.</span></span> <span data-ttu-id="81de3-107">Portanto, o COM+ exige que o acesso a esses componentes seja serializado por meio da imposição da sincronização.</span><span class="sxs-lookup"><span data-stu-id="81de3-107">Therefore, COM+ requires that access to these components be serialized by enforcing synchronization.</span></span> <span data-ttu-id="81de3-108">(Para obter detalhes sobre essas dependências, consulte [ativação Just-in-time do com+](com--just-in-time-activation.md).)</span><span class="sxs-lookup"><span data-stu-id="81de3-108">(For details on these dependencies, see [COM+ Just-in-Time Activation](com--just-in-time-activation.md).)</span></span>

<span data-ttu-id="81de3-109">As tabelas a seguir mostram as características dos valores de atributo de sincronização COM+.</span><span class="sxs-lookup"><span data-stu-id="81de3-109">The following tables show the characteristics of the COM+ synchronization attribute values.</span></span>

### <a name="transactional-requirement"></a><span data-ttu-id="81de3-110">Requisito transacional</span><span class="sxs-lookup"><span data-stu-id="81de3-110">Transactional requirement</span></span>



| <span data-ttu-id="81de3-111">Quando as transações são definidas como</span><span class="sxs-lookup"><span data-stu-id="81de3-111">When transactions are set to</span></span> | <span data-ttu-id="81de3-112">A sincronização pode ser definida como</span><span class="sxs-lookup"><span data-stu-id="81de3-112">Synchronization can be set to</span></span>                    |
|------------------------------|--------------------------------------------------|
| <span data-ttu-id="81de3-113">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="81de3-113">Disabled</span></span><br/>          | <span data-ttu-id="81de3-114">Qualquer coisa, dependendo da ativação JIT</span><span class="sxs-lookup"><span data-stu-id="81de3-114">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="81de3-115">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="81de3-115">Not Supported</span></span><br/>     | <span data-ttu-id="81de3-116">Qualquer coisa, dependendo da ativação JIT</span><span class="sxs-lookup"><span data-stu-id="81de3-116">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="81de3-117">Com suporte</span><span class="sxs-lookup"><span data-stu-id="81de3-117">Supported</span></span><br/>         | <span data-ttu-id="81de3-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="81de3-118">Required</span></span><br/>                              |
| <span data-ttu-id="81de3-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="81de3-119">Required</span></span><br/>          | <span data-ttu-id="81de3-120">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="81de3-120">Required</span></span><br/>                              |
| <span data-ttu-id="81de3-121">Requer novo</span><span class="sxs-lookup"><span data-stu-id="81de3-121">Requires New</span></span><br/>      | <span data-ttu-id="81de3-122">Necessário ou requer novo</span><span class="sxs-lookup"><span data-stu-id="81de3-122">Required or Requires New</span></span><br/>              |



 

### <a name="jit-activation"></a><span data-ttu-id="81de3-123">Ativação JIT</span><span class="sxs-lookup"><span data-stu-id="81de3-123">JIT Activation</span></span>



| <span data-ttu-id="81de3-124">Quando a ativação JIT é definida como</span><span class="sxs-lookup"><span data-stu-id="81de3-124">When JIT Activation is set to</span></span> | <span data-ttu-id="81de3-125">A sincronização pode ser definida como</span><span class="sxs-lookup"><span data-stu-id="81de3-125">Synchronization can be set to</span></span>       |
|-------------------------------|-------------------------------------|
| <span data-ttu-id="81de3-126">habilitado</span><span class="sxs-lookup"><span data-stu-id="81de3-126">Enabled</span></span><br/>            | <span data-ttu-id="81de3-127">Necessário ou requer novo</span><span class="sxs-lookup"><span data-stu-id="81de3-127">Required or Requires New</span></span><br/> |
| <span data-ttu-id="81de3-128">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="81de3-128">Disabled</span></span><br/>           | <span data-ttu-id="81de3-129">Dado</span><span class="sxs-lookup"><span data-stu-id="81de3-129">Anything</span></span><br/>                 |



 

<span data-ttu-id="81de3-130">Para obter mais detalhes sobre como a transação, ativação JIT e atributos de sincronização se comportam, consulte [Configurando transações](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="81de3-130">For more detail about how transaction, JIT Activation, and Synchronization attributes behave together, see [Configuring Transactions](configuring-transactions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81de3-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81de3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81de3-132">Configurando o atributo de sincronização</span><span class="sxs-lookup"><span data-stu-id="81de3-132">Setting the Synchronization Attribute</span></span>](setting-the-synchronization-attribute.md)
</dt> <dt>

[<span data-ttu-id="81de3-133">Valores de atributo de sincronização</span><span class="sxs-lookup"><span data-stu-id="81de3-133">Synchronization Attribute Values</span></span>](synchronization-attribute-values.md)
</dt> </dl>

 

 




