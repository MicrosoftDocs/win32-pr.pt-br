---
description: O COM+ gerencia threads para você. Cada componente COM tem uma propriedade ThreadingModel que você pode especificar ao desenvolver o componente. Essa propriedade determina como os objetos de componentes são atribuídos a threads para execução de método.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Atributo de modelo de Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370390"
---
# <a name="threading-model-attribute"></a><span data-ttu-id="7290d-105">Atributo de modelo de Threading</span><span class="sxs-lookup"><span data-stu-id="7290d-105">Threading Model Attribute</span></span>

<span data-ttu-id="7290d-106">O COM+ gerencia threads para você.</span><span class="sxs-lookup"><span data-stu-id="7290d-106">COM+ manages threads for you.</span></span> <span data-ttu-id="7290d-107">Cada componente COM tem uma propriedade **ThreadingModel** que você pode especificar ao desenvolver o componente.</span><span class="sxs-lookup"><span data-stu-id="7290d-107">Every COM component has a **ThreadingModel** property that you can specify when you develop the component.</span></span> <span data-ttu-id="7290d-108">Essa propriedade determina como os objetos do componente são atribuídos a threads para execução de método.</span><span class="sxs-lookup"><span data-stu-id="7290d-108">This property determines how the component's objects are assigned to threads for method execution.</span></span>

<span data-ttu-id="7290d-109">Você pode usar a ferramenta administrativa serviços de componentes para exibir a propriedade Threading-Model clicando com o botão direito do mouse em um componente na pasta **componentes** , clicando em **Propriedades** e, em seguida, clicando na guia **simultaneidade** . No **modelo de Threading**, os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7290d-109">You can use the Component Services administrative tool to view the threading-model property by right-clicking a component in the **Components** folder, clicking **Properties**, and then clicking the **Concurrency** tab. Under **Threading Model**, the possible values are as follows:</span></span>

-   <span data-ttu-id="7290d-110">**Principal thread apartment**</span><span class="sxs-lookup"><span data-stu-id="7290d-110">**Main Thread Apartment**</span></span>
-   <span data-ttu-id="7290d-111">**Single thread apartment**</span><span class="sxs-lookup"><span data-stu-id="7290d-111">**Single Thread Apartment**</span></span>
-   <span data-ttu-id="7290d-112">**Thread apartment gratuito**</span><span class="sxs-lookup"><span data-stu-id="7290d-112">**Free Thread Apartment**</span></span>
-   <span data-ttu-id="7290d-113">**Apartamento neutro**</span><span class="sxs-lookup"><span data-stu-id="7290d-113">**Neutral Apartment**</span></span>
-   <span data-ttu-id="7290d-114">**Qualquer apartamento**</span><span class="sxs-lookup"><span data-stu-id="7290d-114">**Any Apartment**</span></span>

<span data-ttu-id="7290d-115">O modelo de Threading preferencial para COM+ é o [apartamento neutro](neutral-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="7290d-115">The preferred threading model for COM+ is the [neutral apartment](neutral-apartments.md).</span></span> <span data-ttu-id="7290d-116">No entanto, se você não especificar um modelo de threading para seu componente, o COM+ usará o principal thread apartment, que é o padrão.</span><span class="sxs-lookup"><span data-stu-id="7290d-116">However, if you do not specify a threading model for your component, COM+ uses the main thread apartment, which is the default.</span></span>

> [!Note]  
> <span data-ttu-id="7290d-117">Para obter informações mais detalhadas, consulte [escolhendo o modelo de Threading](/windows/desktop/com/choosing-the-threading-model).</span><span class="sxs-lookup"><span data-stu-id="7290d-117">For more detailed information, see [Choosing the Threading Model](/windows/desktop/com/choosing-the-threading-model).</span></span>

 

<span data-ttu-id="7290d-118">A tabela a seguir mostra o modelo de programação para Apartments no COM+.</span><span class="sxs-lookup"><span data-stu-id="7290d-118">The following table shows the programming model for apartments in COM+.</span></span>



| <span data-ttu-id="7290d-119">Modelar</span><span class="sxs-lookup"><span data-stu-id="7290d-119">Model</span></span>                     | <span data-ttu-id="7290d-120">Sta</span><span class="sxs-lookup"><span data-stu-id="7290d-120">Apartment</span></span>                                                 | <span data-ttu-id="7290d-121">Gratuita</span><span class="sxs-lookup"><span data-stu-id="7290d-121">Free</span></span>                               | <span data-ttu-id="7290d-122">Ambos</span><span class="sxs-lookup"><span data-stu-id="7290d-122">Both</span></span>                               | <span data-ttu-id="7290d-123">Neutro</span><span class="sxs-lookup"><span data-stu-id="7290d-123">Neutral</span></span>                      | <span data-ttu-id="7290d-124">Não especificado</span><span class="sxs-lookup"><span data-stu-id="7290d-124">Not Specified</span></span>                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| <span data-ttu-id="7290d-125">Thread único, não principal</span><span class="sxs-lookup"><span data-stu-id="7290d-125">Single-threaded, not main</span></span> | <span data-ttu-id="7290d-126">Criado no apartamento atual</span><span class="sxs-lookup"><span data-stu-id="7290d-126">Created in current apartment</span></span>                              | <span data-ttu-id="7290d-127">Criado em apartamento multithread</span><span class="sxs-lookup"><span data-stu-id="7290d-127">Created in multithreaded apartment</span></span> | <span data-ttu-id="7290d-128">Criado no apartamento atual</span><span class="sxs-lookup"><span data-stu-id="7290d-128">Created in current apartment</span></span>       | <span data-ttu-id="7290d-129">Criado em apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="7290d-129">Created in neutral apartment</span></span> | <span data-ttu-id="7290d-130">Criado no Apartment segmentado principal</span><span class="sxs-lookup"><span data-stu-id="7290d-130">Created in main threaded apartment</span></span> |
| <span data-ttu-id="7290d-131">Thread único, principal</span><span class="sxs-lookup"><span data-stu-id="7290d-131">Single-threaded, main</span></span>     | <span data-ttu-id="7290d-132">Criado no apartamento atual</span><span class="sxs-lookup"><span data-stu-id="7290d-132">Created in current apartment</span></span>                              | <span data-ttu-id="7290d-133">Criado em apartamento multithread</span><span class="sxs-lookup"><span data-stu-id="7290d-133">Created in multithreaded apartment</span></span> | <span data-ttu-id="7290d-134">Criado no apartamento atual</span><span class="sxs-lookup"><span data-stu-id="7290d-134">Created in current apartment</span></span>       | <span data-ttu-id="7290d-135">Criado em apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="7290d-135">Created in neutral apartment</span></span> | <span data-ttu-id="7290d-136">Criado no apartamento atual</span><span class="sxs-lookup"><span data-stu-id="7290d-136">Created in current apartment</span></span>       |
| <span data-ttu-id="7290d-137">Multithread</span><span class="sxs-lookup"><span data-stu-id="7290d-137">Multithreaded</span></span>             | <span data-ttu-id="7290d-138">Criado em um apartamento de thread único de host</span><span class="sxs-lookup"><span data-stu-id="7290d-138">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="7290d-139">Criado em apartamento multithread</span><span class="sxs-lookup"><span data-stu-id="7290d-139">Created in multithreaded apartment</span></span> | <span data-ttu-id="7290d-140">Criado em apartamento multithread</span><span class="sxs-lookup"><span data-stu-id="7290d-140">Created in multithreaded apartment</span></span> | <span data-ttu-id="7290d-141">Criado em apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="7290d-141">Created in neutral apartment</span></span> | <span data-ttu-id="7290d-142">Criado no Apartment segmentado principal</span><span class="sxs-lookup"><span data-stu-id="7290d-142">Created in main threaded apartment</span></span> |
| <span data-ttu-id="7290d-143">Neutro (no thread STA)</span><span class="sxs-lookup"><span data-stu-id="7290d-143">Neutral (on STA thread)</span></span>   | <span data-ttu-id="7290d-144">Criado no Apartment de thread único do host para este thread</span><span class="sxs-lookup"><span data-stu-id="7290d-144">Created in host single-threaded apartment for this thread</span></span> | <span data-ttu-id="7290d-145">Criado em apartamento multithread</span><span class="sxs-lookup"><span data-stu-id="7290d-145">Created in multithreaded apartment</span></span> | <span data-ttu-id="7290d-146">Criado em apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="7290d-146">Created in neutral apartment</span></span>       | <span data-ttu-id="7290d-147">Criado em apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="7290d-147">Created in neutral apartment</span></span> | <span data-ttu-id="7290d-148">Criado no Apartment segmentado principal</span><span class="sxs-lookup"><span data-stu-id="7290d-148">Created in main threaded apartment</span></span> |
| <span data-ttu-id="7290d-149">Neutro (no thread MTA)</span><span class="sxs-lookup"><span data-stu-id="7290d-149">Neutral (on MTA thread)</span></span>   | <span data-ttu-id="7290d-150">Criado em um apartamento de thread único de host</span><span class="sxs-lookup"><span data-stu-id="7290d-150">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="7290d-151">Criado em apartamento multithread</span><span class="sxs-lookup"><span data-stu-id="7290d-151">Created in multithreaded apartment</span></span> | <span data-ttu-id="7290d-152">Criado em apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="7290d-152">Created in neutral apartment</span></span>       | <span data-ttu-id="7290d-153">Criado em apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="7290d-153">Created in neutral apartment</span></span> | <span data-ttu-id="7290d-154">Criado no Apartment segmentado principal</span><span class="sxs-lookup"><span data-stu-id="7290d-154">Created in main threaded apartment</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7290d-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7290d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7290d-156">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="7290d-156">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
