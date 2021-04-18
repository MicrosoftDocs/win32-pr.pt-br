---
title: Elemento ServiceTask1
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento ServiceTask1 representa o primeiro painel de tarefas da loja online.
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- Elemento ServiceTask1 do Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ca83f5f7935e8d1dfd376f569bd61f68d7e93bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752184"
---
# <a name="servicetask1-element"></a><span data-ttu-id="d480a-106">Elemento ServiceTask1</span><span class="sxs-lookup"><span data-stu-id="d480a-106">ServiceTask1 Element</span></span>

> [!Note]  
> <span data-ttu-id="d480a-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="d480a-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d480a-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="d480a-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d480a-109">O elemento **ServiceTask1** representa o primeiro painel de tarefas da loja online.</span><span class="sxs-lookup"><span data-stu-id="d480a-109">The **ServiceTask1** element represents the first online store task pane.</span></span>

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="d480a-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d480a-110">Attributes</span></span>



| <span data-ttu-id="d480a-111">Termo</span><span class="sxs-lookup"><span data-stu-id="d480a-111">Term</span></span>                                                                                                                             | <span data-ttu-id="d480a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d480a-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d480a-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="d480a-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="d480a-114">URL da página da Web exibida pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d480a-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="d480a-115">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="d480a-115">Parent/Child Elements</span></span>



| <span data-ttu-id="d480a-116">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="d480a-116">Hierarchy</span></span>       | <span data-ttu-id="d480a-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="d480a-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="d480a-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d480a-118">Parent elements</span></span> | <span data-ttu-id="d480a-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="d480a-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="d480a-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d480a-120">Child elements</span></span>  | <span data-ttu-id="d480a-121">**ButtonText**, **ButtonTip**</span><span class="sxs-lookup"><span data-stu-id="d480a-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d480a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d480a-122">Remarks</span></span>

<span data-ttu-id="d480a-123">**ServiceTask1** é considerado o painel de tarefas principal para envolvimento em atividades comerciais.</span><span class="sxs-lookup"><span data-stu-id="d480a-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="d480a-124">É o painel de tarefas exibido quando o usuário escolhe comprar música.</span><span class="sxs-lookup"><span data-stu-id="d480a-124">It is the task pane that displays when the user chooses to purchase music.</span></span>

> [!Note]  
> <span data-ttu-id="d480a-125">O Windows Media Player 10 tem três painéis de tarefas em que um repositório online pode exibir suas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="d480a-125">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="d480a-126">O repositório online pode optar por usar um, dois ou todos os três painéis de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d480a-126">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="d480a-127">O Windows Media Player 11 tem apenas um painel de tarefas, representado por **ServiceTask1**, que o usuário pode exibir clicando na guia **lojas online** .</span><span class="sxs-lookup"><span data-stu-id="d480a-127">Windows Media Player 11 has only one task pane, represented by **ServiceTask1**, which the user can view by clicking on the **Online Stores** tab.</span></span>

 

<span data-ttu-id="d480a-128">Os painéis de tarefas da loja online compartilham uma única instância do navegador.</span><span class="sxs-lookup"><span data-stu-id="d480a-128">Online store task panes share a single browser instance.</span></span> <span data-ttu-id="d480a-129">Isso significa que você não deve escrever o código de script em sua página da Web que você espera que continue a ser executado quando o usuário mudar para a tarefa de serviço atual.</span><span class="sxs-lookup"><span data-stu-id="d480a-129">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="d480a-130">Quando o usuário alterna os painéis de tarefas, o Windows Media Player armazena a URL e os cookies de sessão.</span><span class="sxs-lookup"><span data-stu-id="d480a-130">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="d480a-131">Quando o usuário volta ao painel de tarefas, o Player restaura a URL e os cookies.</span><span class="sxs-lookup"><span data-stu-id="d480a-131">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="d480a-132">Se o usuário optar por usar uma loja online diferente, os dados da URL e da sessão serão apagados.</span><span class="sxs-lookup"><span data-stu-id="d480a-132">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="d480a-133">A tabela a seguir detalha os parâmetros enviados com a solicitação de URL.</span><span class="sxs-lookup"><span data-stu-id="d480a-133">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="d480a-134">Outros podem estar presentes para fins de compatibilidade herdada.</span><span class="sxs-lookup"><span data-stu-id="d480a-134">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="d480a-135">Nome</span><span class="sxs-lookup"><span data-stu-id="d480a-135">Name</span></span>         | <span data-ttu-id="d480a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="d480a-136">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d480a-137">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="d480a-137">*geoid*</span></span>      | <span data-ttu-id="d480a-138">ID da localização geográfica do Windows.</span><span class="sxs-lookup"><span data-stu-id="d480a-138">Windows geographical location ID.</span></span> <span data-ttu-id="d480a-139">A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="d480a-139">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="d480a-140">*locale*</span><span class="sxs-lookup"><span data-stu-id="d480a-140">*locale*</span></span>     | <span data-ttu-id="d480a-141">ID de localidade do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d480a-141">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="d480a-142">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="d480a-142">*userlocale*</span></span> | <span data-ttu-id="d480a-143">IDENTIFICAÇÃO de localidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="d480a-143">Windows locale ID.</span></span> <span data-ttu-id="d480a-144">A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="d480a-144">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="d480a-145">*version*</span><span class="sxs-lookup"><span data-stu-id="d480a-145">*version*</span></span>    | <span data-ttu-id="d480a-146">Número de versão do Windows Media Player usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="d480a-146">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="d480a-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d480a-147">Requirements</span></span>



| <span data-ttu-id="d480a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="d480a-148">Requirement</span></span> | <span data-ttu-id="d480a-149">Valor</span><span class="sxs-lookup"><span data-stu-id="d480a-149">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="d480a-150">Versão</span><span class="sxs-lookup"><span data-stu-id="d480a-150">Version</span></span><br/> | <span data-ttu-id="d480a-151">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d480a-151">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d480a-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="d480a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d480a-153">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="d480a-153">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="d480a-154">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="d480a-154">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="d480a-155">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="d480a-155">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





