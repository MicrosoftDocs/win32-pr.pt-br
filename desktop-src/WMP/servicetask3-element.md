---
title: Elemento ServiceTask3
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento ServiceTask3 representa o terceiro painel de tarefas da loja online.
ms.assetid: 3d08f9ff-d75b-4967-90f8-23ab71d38883
keywords:
- Elemento ServiceTask3 do Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask3 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d78b9e70c7e6933693f4d29750e9e3c0b4e897a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751582"
---
# <a name="servicetask3-element"></a><span data-ttu-id="6cb57-106">Elemento ServiceTask3</span><span class="sxs-lookup"><span data-stu-id="6cb57-106">ServiceTask3 Element</span></span>

> [!Note]  
> <span data-ttu-id="6cb57-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="6cb57-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6cb57-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="6cb57-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6cb57-109">O elemento **ServiceTask3** representa o terceiro painel de tarefas da loja online.</span><span class="sxs-lookup"><span data-stu-id="6cb57-109">The **ServiceTask3** element represents the third online store task pane.</span></span>

``` syntax
<ServiceTask3
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="6cb57-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="6cb57-110">Attributes</span></span>



| <span data-ttu-id="6cb57-111">Termo</span><span class="sxs-lookup"><span data-stu-id="6cb57-111">Term</span></span>                                                                                                                             | <span data-ttu-id="6cb57-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cb57-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6cb57-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="6cb57-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="6cb57-114">URL da página da Web exibida pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6cb57-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="6cb57-115">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="6cb57-115">Parent/Child Elements</span></span>



| <span data-ttu-id="6cb57-116">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="6cb57-116">Hierarchy</span></span>       | <span data-ttu-id="6cb57-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="6cb57-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="6cb57-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6cb57-118">Parent elements</span></span> | <span data-ttu-id="6cb57-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="6cb57-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="6cb57-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6cb57-120">Child elements</span></span>  | <span data-ttu-id="6cb57-121">**ButtonText**, **ButtonTip**</span><span class="sxs-lookup"><span data-stu-id="6cb57-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6cb57-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cb57-122">Remarks</span></span>

<span data-ttu-id="6cb57-123">**ServiceTask1** é considerado o painel de tarefas principal para envolvimento em atividades comerciais.</span><span class="sxs-lookup"><span data-stu-id="6cb57-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="6cb57-124">É o painel de tarefas exibido quando o usuário escolhe comprar música.</span><span class="sxs-lookup"><span data-stu-id="6cb57-124">It is the task pane that displays when the user chooses to purchase music.</span></span> <span data-ttu-id="6cb57-125">Use **ServiceTask3** para outra atividade de loja online.</span><span class="sxs-lookup"><span data-stu-id="6cb57-125">Use **ServiceTask3** for other online store activity.</span></span>

> [!Note]  
> <span data-ttu-id="6cb57-126">O Windows Media Player 10 tem três painéis de tarefas em que um repositório online pode exibir suas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="6cb57-126">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="6cb57-127">O repositório online pode optar por usar um, dois ou todos os três painéis de tarefas.</span><span class="sxs-lookup"><span data-stu-id="6cb57-127">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="6cb57-128">O Windows Media Player 11 tem apenas um painel de tarefas, que pode ser exibido pelo usuário clicando na guia **lojas online** . o Windows Media Player 11 ignora os elementos **ServiceTask2** e **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="6cb57-128">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="6cb57-129">Os painéis de tarefas de lojas online compartilham uma única instância do navegador.</span><span class="sxs-lookup"><span data-stu-id="6cb57-129">Online stores task panes share a single browser instance.</span></span> <span data-ttu-id="6cb57-130">Isso significa que você não deve escrever o código de script em sua página da Web que você espera que continue a ser executado quando o usuário mudar para a tarefa de serviço atual.</span><span class="sxs-lookup"><span data-stu-id="6cb57-130">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="6cb57-131">Quando o usuário alterna os painéis de tarefas, o Windows Media Player armazena a URL e os cookies de sessão.</span><span class="sxs-lookup"><span data-stu-id="6cb57-131">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="6cb57-132">Quando o usuário volta ao painel de tarefas, o Player restaura a URL e os cookies.</span><span class="sxs-lookup"><span data-stu-id="6cb57-132">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="6cb57-133">Se o usuário optar por usar uma loja online diferente, os dados da URL e da sessão serão apagados.</span><span class="sxs-lookup"><span data-stu-id="6cb57-133">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="6cb57-134">A tabela a seguir detalha os parâmetros enviados com a solicitação de URL.</span><span class="sxs-lookup"><span data-stu-id="6cb57-134">The following table details the parameters sent with the URL request.</span></span>



| <span data-ttu-id="6cb57-135">Nome</span><span class="sxs-lookup"><span data-stu-id="6cb57-135">Name</span></span>         | <span data-ttu-id="6cb57-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb57-136">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb57-137">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="6cb57-137">*geoid*</span></span>      | <span data-ttu-id="6cb57-138">ID da localização geográfica do Windows.</span><span class="sxs-lookup"><span data-stu-id="6cb57-138">Windows geographical location ID.</span></span> <span data-ttu-id="6cb57-139">A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6cb57-139">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="6cb57-140">*locale*</span><span class="sxs-lookup"><span data-stu-id="6cb57-140">*locale*</span></span>     | <span data-ttu-id="6cb57-141">ID de localidade do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6cb57-141">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="6cb57-142">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="6cb57-142">*userlocale*</span></span> | <span data-ttu-id="6cb57-143">IDENTIFICAÇÃO de localidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="6cb57-143">Windows locale ID.</span></span> <span data-ttu-id="6cb57-144">A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6cb57-144">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="6cb57-145">*version*</span><span class="sxs-lookup"><span data-stu-id="6cb57-145">*version*</span></span>    | <span data-ttu-id="6cb57-146">Número de versão do Windows Media Player usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="6cb57-146">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="6cb57-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cb57-147">Requirements</span></span>



| <span data-ttu-id="6cb57-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cb57-148">Requirement</span></span> | <span data-ttu-id="6cb57-149">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb57-149">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="6cb57-150">Versão</span><span class="sxs-lookup"><span data-stu-id="6cb57-150">Version</span></span><br/> | <span data-ttu-id="6cb57-151">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6cb57-151">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6cb57-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cb57-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb57-153">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="6cb57-153">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="6cb57-154">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="6cb57-154">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="6cb57-155">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="6cb57-155">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





