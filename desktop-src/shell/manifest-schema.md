---
description: Esses elementos compõem o esquema XML usado na publicação da Web e no manifesto de transferência dos assistentes de ordenação de impressão online.
title: Transferir esquema de manifesto
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989048"
---
# <a name="transfer-manifest-schema"></a><span data-ttu-id="a65e0-103">Transferir esquema de manifesto</span><span class="sxs-lookup"><span data-stu-id="a65e0-103">Transfer Manifest Schema</span></span>

<span data-ttu-id="a65e0-104">Esses elementos compõem o esquema XML usado na publicação da Web e no manifesto de transferência dos assistentes de ordenação de impressão online.</span><span class="sxs-lookup"><span data-stu-id="a65e0-104">These elements make up the XML schema used in the Web Publishing and Online Print Ordering wizards' transfer manifest.</span></span>

<span data-ttu-id="a65e0-105">Os elementos a seguir são definidos para o manifesto de transferência.</span><span class="sxs-lookup"><span data-stu-id="a65e0-105">The following elements are defined for the transfer manifest.</span></span>

-   [<span data-ttu-id="a65e0-106">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="a65e0-106">cancelledpage</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-107">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-108">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-110">failurepage</span><span class="sxs-lookup"><span data-stu-id="a65e0-110">failurepage</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-111">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-112">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-114">preferência</span><span class="sxs-lookup"><span data-stu-id="a65e0-114">favorite</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-115">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-116">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-117">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-117">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-118">file</span><span class="sxs-lookup"><span data-stu-id="a65e0-118">file</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-119">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-120">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-121">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-121">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-122">File</span><span class="sxs-lookup"><span data-stu-id="a65e0-122">filelist</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-123">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-124">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-125">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-126">pasta</span><span class="sxs-lookup"><span data-stu-id="a65e0-126">folder</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-127">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-128">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-129">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-129">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-130">pastalist</span><span class="sxs-lookup"><span data-stu-id="a65e0-130">folderlist</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-131">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-131">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-132">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-133">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-133">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-134">formdata</span><span class="sxs-lookup"><span data-stu-id="a65e0-134">formdata</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-135">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-135">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-136">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-136">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-137">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-137">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-138">htmlui</span><span class="sxs-lookup"><span data-stu-id="a65e0-138">htmlui</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-139">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-139">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-140">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-140">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-141">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-141">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-142">ImageProperty</span><span class="sxs-lookup"><span data-stu-id="a65e0-142">imageproperty</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-143">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-143">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-144">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-144">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-145">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-145">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-146">los</span><span class="sxs-lookup"><span data-stu-id="a65e0-146">metadata</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-147">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-147">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-148">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-148">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-149">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-149">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-150">netplace</span><span class="sxs-lookup"><span data-stu-id="a65e0-150">netplace</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-151">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-151">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-152">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-152">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-153">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-153">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-154">Postar</span><span class="sxs-lookup"><span data-stu-id="a65e0-154">post</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-155">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-155">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-156">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-156">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-157">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-157">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-158">alonga</span><span class="sxs-lookup"><span data-stu-id="a65e0-158">resize</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-159">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-159">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-160">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-160">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-161">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-161">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-162">successpage</span><span class="sxs-lookup"><span data-stu-id="a65e0-162">successpage</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-163">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-163">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-164">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-164">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-165">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-165">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-166">destino</span><span class="sxs-lookup"><span data-stu-id="a65e0-166">target</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-167">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-167">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-168">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-168">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-169">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-169">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-170">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="a65e0-170">transfermanifest</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-171">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-171">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-172">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-172">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-173">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-173">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a65e0-174">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-174">uploadinfo</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-175">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65e0-175">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="a65e0-176">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-176">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="a65e0-177">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-177">Element Information</span></span>](#element-information)

## <a name="cancelledpage"></a><span data-ttu-id="a65e0-178">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="a65e0-178">cancelledpage</span></span>

<span data-ttu-id="a65e0-179">Especifica a página HTML do lado do servidor a ser exibida antes que o assistente seja fechado quando o usuário clicar no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="a65e0-179">Specifies the server-side HTML page to display before the wizard is closed when the user clicks the **Cancel** button.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-180">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-180">Syntax</span></span>


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-181">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-181">Attributes</span></span>



| <span data-ttu-id="a65e0-182">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-182">Attribute</span></span> | <span data-ttu-id="a65e0-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-183">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-184">href</span><span class="sxs-lookup"><span data-stu-id="a65e0-184">href</span></span>      | <span data-ttu-id="a65e0-185">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-185">Required.</span></span> <span data-ttu-id="a65e0-186">A URL da página HTML do lado do servidor a ser exibida quando o usuário clica no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="a65e0-186">The URL of the server-side HTML page to display when the user clicks the **Cancel** button.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-187">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-187">Element Information</span></span>



| <span data-ttu-id="a65e0-188">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-188">Parent Element</span></span>        | <span data-ttu-id="a65e0-189">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-189">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="a65e0-190">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-190">uploadinfo</span></span>](#syntax) | <span data-ttu-id="a65e0-191">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a65e0-191">None</span></span>           |



 

## <a name="failurepage"></a><span data-ttu-id="a65e0-192">failurepage</span><span class="sxs-lookup"><span data-stu-id="a65e0-192">failurepage</span></span>

<span data-ttu-id="a65e0-193">Especifica a página HTML do lado do servidor a ser exibida se o carregamento não for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-193">Specifies the server-side HTML page to display if the upload is not successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-194">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-194">Syntax</span></span>


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-195">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-195">Attributes</span></span>



| <span data-ttu-id="a65e0-196">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-196">Attribute</span></span> | <span data-ttu-id="a65e0-197">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-197">Description</span></span>                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-198">href</span><span class="sxs-lookup"><span data-stu-id="a65e0-198">href</span></span>      | <span data-ttu-id="a65e0-199">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-199">Required.</span></span> <span data-ttu-id="a65e0-200">A URL da página HTML do lado do servidor a ser exibida se o carregamento não for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-200">The URL of the server-side HTML page to display if the upload is not successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-201">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-201">Element Information</span></span>



| <span data-ttu-id="a65e0-202">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-202">Parent Element</span></span>        | <span data-ttu-id="a65e0-203">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-203">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="a65e0-204">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-204">uploadinfo</span></span>](#syntax) | <span data-ttu-id="a65e0-205">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-205">None.</span></span> <span data-ttu-id="a65e0-206">O texto é permitido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-206">Text is allowed.</span></span> |



 

## <a name="favorite"></a><span data-ttu-id="a65e0-207">favorito</span><span class="sxs-lookup"><span data-stu-id="a65e0-207">favorite</span></span>

<span data-ttu-id="a65e0-208">Instrui o assistente a criar uma entrada de site favorita no menu **favoritos** para a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="a65e0-208">Instructs the wizard to create a favorite website entry in the **Favorites** menu for the given URL.</span></span> <span data-ttu-id="a65e0-209">Se esse elemento não for especificado, o elemento [htmlui](#syntax) será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="a65e0-209">If this element is not specified, then the [htmlui](#syntax) element is used in its place.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-210">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-210">Syntax</span></span>


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-211">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-211">Attributes</span></span>



| <span data-ttu-id="a65e0-212">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-212">Attribute</span></span> | <span data-ttu-id="a65e0-213">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-213">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-214">comentário</span><span class="sxs-lookup"><span data-stu-id="a65e0-214">comment</span></span>   | <span data-ttu-id="a65e0-215">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-215">Required.</span></span> <span data-ttu-id="a65e0-216">O comentário associado à entrada de **favoritos** .</span><span class="sxs-lookup"><span data-stu-id="a65e0-216">The comment associated with the **Favorites** entry.</span></span>         |
| <span data-ttu-id="a65e0-217">href</span><span class="sxs-lookup"><span data-stu-id="a65e0-217">href</span></span>      | <span data-ttu-id="a65e0-218">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-218">Required.</span></span> <span data-ttu-id="a65e0-219">A URL da entrada de **favoritos** .</span><span class="sxs-lookup"><span data-stu-id="a65e0-219">The URL of the **Favorites** entry.</span></span>                          |
| <span data-ttu-id="a65e0-220">name</span><span class="sxs-lookup"><span data-stu-id="a65e0-220">name</span></span>      | <span data-ttu-id="a65e0-221">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-221">Required.</span></span> <span data-ttu-id="a65e0-222">O nome da URL que aparece no menu **favoritos** .</span><span class="sxs-lookup"><span data-stu-id="a65e0-222">The name for the URL that appears in the **Favorites** menu.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-223">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-223">Element Information</span></span>



| <span data-ttu-id="a65e0-224">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-224">Parent Element</span></span>        | <span data-ttu-id="a65e0-225">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-225">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="a65e0-226">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-226">uploadinfo</span></span>](#syntax) | <span data-ttu-id="a65e0-227">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-227">None.</span></span> <span data-ttu-id="a65e0-228">O texto é permitido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-228">Text is allowed.</span></span> |



 

## <a name="file"></a><span data-ttu-id="a65e0-229">arquivo</span><span class="sxs-lookup"><span data-stu-id="a65e0-229">file</span></span>

<span data-ttu-id="a65e0-230">Descreve um único arquivo a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-230">Describes a single file to be copied.</span></span> <span data-ttu-id="a65e0-231">Vários elementos de [arquivo](#syntax) podem estar contidos em um único nó [FileList](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-231">Multiple [file](#syntax) elements may be contained under a single [filelist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-232">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-232">Syntax</span></span>


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-233">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-233">Attributes</span></span>



| <span data-ttu-id="a65e0-234">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-234">Attribute</span></span>   | <span data-ttu-id="a65e0-235">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-235">Description</span></span>                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-236">ContentType</span><span class="sxs-lookup"><span data-stu-id="a65e0-236">contenttype</span></span> | <span data-ttu-id="a65e0-237">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a65e0-237">Optional.</span></span> <span data-ttu-id="a65e0-238">O tipo MIME do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a65e0-238">The MIME type of the file.</span></span>                                                                                                                                         |
| <span data-ttu-id="a65e0-239">destino</span><span class="sxs-lookup"><span data-stu-id="a65e0-239">destination</span></span> | <span data-ttu-id="a65e0-240">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-240">Required.</span></span> <span data-ttu-id="a65e0-241">Um caminho sugerido para o arquivo depois que ele é carregado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-241">A suggested path for the file once it is uploaded.</span></span> <span data-ttu-id="a65e0-242">Esse caminho é relativo à URL de destino do site de carregamento.</span><span class="sxs-lookup"><span data-stu-id="a65e0-242">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="a65e0-243">O site de upload pode modificar esse valor conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="a65e0-243">The upload site can modify this value as necessary.</span></span> |
| <span data-ttu-id="a65e0-244">extensão</span><span class="sxs-lookup"><span data-stu-id="a65e0-244">extension</span></span>   | <span data-ttu-id="a65e0-245">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a65e0-245">Optional.</span></span> <span data-ttu-id="a65e0-246">A extensão de nome de arquivo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a65e0-246">The file name extension of the file.</span></span>                                                                                                                               |
| <span data-ttu-id="a65e0-247">id</span><span class="sxs-lookup"><span data-stu-id="a65e0-247">id</span></span>          | <span data-ttu-id="a65e0-248">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-248">Required.</span></span> <span data-ttu-id="a65e0-249">O índice numérico do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a65e0-249">The numerical index of the file.</span></span>                                                                                                                                   |
| <span data-ttu-id="a65e0-250">tamanho</span><span class="sxs-lookup"><span data-stu-id="a65e0-250">size</span></span>        | <span data-ttu-id="a65e0-251">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a65e0-251">Optional.</span></span> <span data-ttu-id="a65e0-252">O tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="a65e0-252">The size of the file, in bytes.</span></span>                                                                                                                                    |
| <span data-ttu-id="a65e0-253">source</span><span class="sxs-lookup"><span data-stu-id="a65e0-253">source</span></span>      | <span data-ttu-id="a65e0-254">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-254">Required.</span></span> <span data-ttu-id="a65e0-255">O caminho completo do sistema de arquivos para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="a65e0-255">The full file system path for the file.</span></span>                                                                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-256">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-256">Element Information</span></span>



| <span data-ttu-id="a65e0-257">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-257">Parent Element</span></span>      | <span data-ttu-id="a65e0-258">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-258">Child Elements</span></span>                                          |
|---------------------|---------------------------------------------------------|
| [<span data-ttu-id="a65e0-259">File</span><span class="sxs-lookup"><span data-stu-id="a65e0-259">filelist</span></span>](#syntax) | <span data-ttu-id="a65e0-260">[metadados](#syntax), [post](#syntax), [redimensionamento](#syntax)</span><span class="sxs-lookup"><span data-stu-id="a65e0-260">[metadata](#syntax), [post](#syntax), [resize](#syntax)</span></span> |



 

## <a name="filelist"></a><span data-ttu-id="a65e0-261">File</span><span class="sxs-lookup"><span data-stu-id="a65e0-261">filelist</span></span>

<span data-ttu-id="a65e0-262">Um contêiner para elementos que descrevem os arquivos a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="a65e0-262">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="a65e0-263">Vários elementos de [FileList](#syntax) podem estar contidos em um único nó [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-263">Multiple [filelist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-264">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-264">Syntax</span></span>


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-265">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-265">Attributes</span></span>



| <span data-ttu-id="a65e0-266">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-266">Attribute</span></span>   | <span data-ttu-id="a65e0-267">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-267">Description</span></span>      |
|-------------|------------------|
| <span data-ttu-id="a65e0-268">usesfolders</span><span class="sxs-lookup"><span data-stu-id="a65e0-268">usesfolders</span></span> | <span data-ttu-id="a65e0-269">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-269">Not implemented.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-270">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-270">Element Information</span></span>



| <span data-ttu-id="a65e0-271">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-271">Parent Element</span></span>              | <span data-ttu-id="a65e0-272">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-272">Child Elements</span></span>  |
|-----------------------------|-----------------|
| [<span data-ttu-id="a65e0-273">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="a65e0-273">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="a65e0-274">file</span><span class="sxs-lookup"><span data-stu-id="a65e0-274">file</span></span>](#syntax) |



 

## <a name="folder"></a><span data-ttu-id="a65e0-275">folder</span><span class="sxs-lookup"><span data-stu-id="a65e0-275">folder</span></span>

<span data-ttu-id="a65e0-276">Descreve uma pasta na qual os arquivos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="a65e0-276">Describes a folder in which files are stored.</span></span> <span data-ttu-id="a65e0-277">Vários elementos de [pasta](#syntax) podem estar contidos em um único nó [folderList](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-277">Multiple [folder](#syntax) elements may be contained under a single [folderlist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-278">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-278">Syntax</span></span>


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-279">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-279">Attributes</span></span>



| <span data-ttu-id="a65e0-280">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-280">Attribute</span></span>   | <span data-ttu-id="a65e0-281">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-281">Description</span></span>                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-282">destino</span><span class="sxs-lookup"><span data-stu-id="a65e0-282">destination</span></span> | <span data-ttu-id="a65e0-283">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-283">Required.</span></span> <span data-ttu-id="a65e0-284">Um caminho sugerido para a pasta assim que ela é carregada.</span><span class="sxs-lookup"><span data-stu-id="a65e0-284">A suggested path for the folder once it is uploaded.</span></span> <span data-ttu-id="a65e0-285">Esse caminho é relativo à URL de destino do site de carregamento.</span><span class="sxs-lookup"><span data-stu-id="a65e0-285">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="a65e0-286">O site de upload pode modificar esse valor conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="a65e0-286">The upload site can modify this value as necessary.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-287">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-287">Element Information</span></span>



| <span data-ttu-id="a65e0-288">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-288">Parent Element</span></span>        | <span data-ttu-id="a65e0-289">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-289">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="a65e0-290">pastalist</span><span class="sxs-lookup"><span data-stu-id="a65e0-290">folderlist</span></span>](#syntax) | <span data-ttu-id="a65e0-291">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a65e0-291">None</span></span>           |



 

## <a name="folderlist"></a><span data-ttu-id="a65e0-292">pastalist</span><span class="sxs-lookup"><span data-stu-id="a65e0-292">folderlist</span></span>

<span data-ttu-id="a65e0-293">Um contêiner para elementos que descrevem os arquivos a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="a65e0-293">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="a65e0-294">Vários elementos [folderList](#syntax) podem estar contidos em um único nó [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-294">Multiple [folderlist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-295">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-295">Syntax</span></span>


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-296">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-296">Attributes</span></span>

<span data-ttu-id="a65e0-297">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-297">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="a65e0-298">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-298">Element Information</span></span>



| <span data-ttu-id="a65e0-299">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-299">Parent Element</span></span>              | <span data-ttu-id="a65e0-300">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-300">Child Elements</span></span>    |
|-----------------------------|-------------------|
| [<span data-ttu-id="a65e0-301">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="a65e0-301">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="a65e0-302">pasta</span><span class="sxs-lookup"><span data-stu-id="a65e0-302">folder</span></span>](#syntax) |



 

## <a name="formdata"></a><span data-ttu-id="a65e0-303">formdata</span><span class="sxs-lookup"><span data-stu-id="a65e0-303">formdata</span></span>

<span data-ttu-id="a65e0-304">Descreve dados de formulário codificados em HTML opcionais que podem ser transferidos com os arquivos.</span><span class="sxs-lookup"><span data-stu-id="a65e0-304">Describes optional HTML encoded form data that may be transferred with the files.</span></span> <span data-ttu-id="a65e0-305">Esse elemento é adicionado pelo serviço se optar por carregar os arquivos como uma postagem de várias partes.</span><span class="sxs-lookup"><span data-stu-id="a65e0-305">This element is added by the service if it elects to upload the files as a multi-part post.</span></span> <span data-ttu-id="a65e0-306">Os dados do formulário, juntamente com as informações do elemento [post](#syntax) , são usados para criar o cabeçalho post.</span><span class="sxs-lookup"><span data-stu-id="a65e0-306">The form data, together with information from the [post](#syntax) element, is used to create the post header.</span></span>

<span data-ttu-id="a65e0-307">Vários elementos [FormData](#syntax) podem estar contidos em um único nó [uploadinfo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-307">Multiple [formdata](#syntax) elements may be contained under a single [uploadinfo](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-308">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-308">Syntax</span></span>


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-309">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-309">Attributes</span></span>



| <span data-ttu-id="a65e0-310">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-310">Attribute</span></span> | <span data-ttu-id="a65e0-311">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-311">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-312">name</span><span class="sxs-lookup"><span data-stu-id="a65e0-312">name</span></span>      | <span data-ttu-id="a65e0-313">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-313">Required.</span></span> <span data-ttu-id="a65e0-314">Define o nome de dados do formulário associado a esta seção do carregamento.</span><span class="sxs-lookup"><span data-stu-id="a65e0-314">Defines the form data name associated with this section of the upload.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-315">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-315">Element Information</span></span>



| <span data-ttu-id="a65e0-316">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-316">Parent Element</span></span>        | <span data-ttu-id="a65e0-317">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-317">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="a65e0-318">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-318">uploadinfo</span></span>](#syntax) | <span data-ttu-id="a65e0-319">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a65e0-319">None</span></span>           |



 

## <a name="htmlui"></a><span data-ttu-id="a65e0-320">htmlui</span><span class="sxs-lookup"><span data-stu-id="a65e0-320">htmlui</span></span>

<span data-ttu-id="a65e0-321">A URL da página HTML do lado do servidor a ser exibida quando o assistente é fechado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-321">The URL of the server-side HTML page to display when the wizard is closed.</span></span> <span data-ttu-id="a65e0-322">Esse elemento cria uma entrada de página da Web favorita no menu **favoritos** se o elemento [favorito](#syntax) estiver ausente e o nome amigável do site de carregamento for especificado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-322">This element creates a favorite webpage entry in the **Favorites** menu if the [favorite](#syntax) element is absent and the upload site's friendly name is specified.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-323">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-323">Syntax</span></span>


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-324">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-324">Attributes</span></span>



| <span data-ttu-id="a65e0-325">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-325">Attribute</span></span> | <span data-ttu-id="a65e0-326">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-326">Description</span></span>                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-327">href</span><span class="sxs-lookup"><span data-stu-id="a65e0-327">href</span></span>      | <span data-ttu-id="a65e0-328">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-328">Required.</span></span> <span data-ttu-id="a65e0-329">A URL da página HTML do lado do servidor a ser exibida quando o assistente é fechado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-329">The URL of the server-side HTML page to display when the wizard is closed.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-330">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-330">Element Information</span></span>



| <span data-ttu-id="a65e0-331">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-331">Parent Element</span></span>        | <span data-ttu-id="a65e0-332">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-332">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="a65e0-333">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-333">uploadinfo</span></span>](#syntax) | <span data-ttu-id="a65e0-334">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-334">None.</span></span> <span data-ttu-id="a65e0-335">O texto é permitido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-335">Text is allowed.</span></span> |



 

## <a name="imageproperty"></a><span data-ttu-id="a65e0-336">ImageProperty</span><span class="sxs-lookup"><span data-stu-id="a65e0-336">imageproperty</span></span>

<span data-ttu-id="a65e0-337">Especifica uma propriedade de imagem relacionada ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="a65e0-337">Specifies an image property relating to the file.</span></span> <span data-ttu-id="a65e0-338">Vários elementos [ImageProperty](#syntax) podem estar contidos em um único nó de [metadados](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-338">Multiple [imageproperty](#syntax) elements may be contained under a single [metadata](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-339">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-339">Syntax</span></span>


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-340">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-340">Attributes</span></span>



| <span data-ttu-id="a65e0-341">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-341">Attribute</span></span> | <span data-ttu-id="a65e0-342">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-342">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="a65e0-343">id</span><span class="sxs-lookup"><span data-stu-id="a65e0-343">id</span></span>        | <span data-ttu-id="a65e0-344">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-344">Required.</span></span> <span data-ttu-id="a65e0-345">A ID da propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="a65e0-345">The ID of the particular property.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-346">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-346">Element Information</span></span>



| <span data-ttu-id="a65e0-347">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-347">Parent Element</span></span>      | <span data-ttu-id="a65e0-348">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-348">Child Elements</span></span>         |
|---------------------|------------------------|
| [<span data-ttu-id="a65e0-349">los</span><span class="sxs-lookup"><span data-stu-id="a65e0-349">metadata</span></span>](#syntax) | <span data-ttu-id="a65e0-350">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-350">None.</span></span> <span data-ttu-id="a65e0-351">O texto é permitido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-351">Text is allowed.</span></span> |



 

## <a name="metadata"></a><span data-ttu-id="a65e0-352">metadata</span><span class="sxs-lookup"><span data-stu-id="a65e0-352">metadata</span></span>

<span data-ttu-id="a65e0-353">Um contêiner para elementos e texto que definem metadados para o arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="a65e0-353">A container for elements and text defining metadata for the particular file.</span></span> <span data-ttu-id="a65e0-354">Vários elementos de [metadados](#syntax) podem estar contidos em um único nó de [arquivo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-354">Multiple [metadata](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-355">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-355">Syntax</span></span>


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-356">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-356">Attributes</span></span>

<span data-ttu-id="a65e0-357">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-357">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="a65e0-358">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-358">Element Information</span></span>



| <span data-ttu-id="a65e0-359">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-359">Parent Element</span></span>  | <span data-ttu-id="a65e0-360">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-360">Child Elements</span></span>           |
|-----------------|--------------------------|
| [<span data-ttu-id="a65e0-361">file</span><span class="sxs-lookup"><span data-stu-id="a65e0-361">file</span></span>](#syntax) | [<span data-ttu-id="a65e0-362">ImageProperty</span><span class="sxs-lookup"><span data-stu-id="a65e0-362">imageproperty</span></span>](#syntax) |



 

## <a name="netplace"></a><span data-ttu-id="a65e0-363">netplace</span><span class="sxs-lookup"><span data-stu-id="a65e0-363">netplace</span></span>

<span data-ttu-id="a65e0-364">Define o destino para um local de rede que é criado em **meus locais de rede** quando o carregamento é concluído.</span><span class="sxs-lookup"><span data-stu-id="a65e0-364">Defines the target for a network place that is created in **My Network Places** when the upload is complete.</span></span> <span data-ttu-id="a65e0-365">A criação de um local de rede pode ser evitada por meio do método [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-365">Creation of a network place can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-366">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-366">Syntax</span></span>


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-367">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-367">Attributes</span></span>



| <span data-ttu-id="a65e0-368">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-368">Attribute</span></span> | <span data-ttu-id="a65e0-369">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-369">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-370">comentário</span><span class="sxs-lookup"><span data-stu-id="a65e0-370">comment</span></span>   | <span data-ttu-id="a65e0-371">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-371">Required.</span></span> <span data-ttu-id="a65e0-372">O comentário exibido para o ícone de local de rede quando o cursor é colocado nele.</span><span class="sxs-lookup"><span data-stu-id="a65e0-372">The comment displayed for the network place icon when the cursor rests on it.</span></span>         |
| <span data-ttu-id="a65e0-373">href</span><span class="sxs-lookup"><span data-stu-id="a65e0-373">href</span></span>      | <span data-ttu-id="a65e0-374">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-374">Required.</span></span> <span data-ttu-id="a65e0-375">A URL da entrada do local de rede.</span><span class="sxs-lookup"><span data-stu-id="a65e0-375">The URL of the network place entry.</span></span>                                                   |
| <span data-ttu-id="a65e0-376">name</span><span class="sxs-lookup"><span data-stu-id="a65e0-376">name</span></span>      | <span data-ttu-id="a65e0-377">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-377">Required.</span></span> <span data-ttu-id="a65e0-378">O nome do ícone de local de rede que aparece na pasta **meus locais de rede** .</span><span class="sxs-lookup"><span data-stu-id="a65e0-378">The name for the network place icon that appears in the **My Network Places** folder.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-379">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-379">Element Information</span></span>



| <span data-ttu-id="a65e0-380">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-380">Parent Element</span></span>        | <span data-ttu-id="a65e0-381">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-381">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="a65e0-382">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-382">uploadinfo</span></span>](#syntax) | <span data-ttu-id="a65e0-383">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-383">None.</span></span> <span data-ttu-id="a65e0-384">O texto é permitido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-384">Text is allowed.</span></span> |



 

## <a name="post"></a><span data-ttu-id="a65e0-385">post</span><span class="sxs-lookup"><span data-stu-id="a65e0-385">post</span></span>

<span data-ttu-id="a65e0-386">URL para a qual o arquivo deve ser postado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-386">URL to which the file should be posted.</span></span> <span data-ttu-id="a65e0-387">Esse elemento é adicionado pelo serviço quando a transferência é feita como uma postagem de várias partes e, com [FormData](#syntax), é usado para criar o cabeçalho de postagem.</span><span class="sxs-lookup"><span data-stu-id="a65e0-387">This element is added by the service when the transfer is done as a multi-part post and, with [formdata](#syntax), is used to build the post header.</span></span> <span data-ttu-id="a65e0-388">Se o serviço optar por executar a transferência de arquivo World Wide Web usando o WebDAV (criação distribuída e controle de versão), ele não deverá adicionar esse elemento.</span><span class="sxs-lookup"><span data-stu-id="a65e0-388">If the service chooses to perform the file transfer using World Wide Web Distributed Authoring and Versioning (WebDAV), it should not add this element.</span></span> <span data-ttu-id="a65e0-389">Vários elementos [post](#syntax) podem estar contidos em um único nó de [arquivo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-389">Multiple [post](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-390">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-390">Syntax</span></span>


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-391">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-391">Attributes</span></span>



| <span data-ttu-id="a65e0-392">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-392">Attribute</span></span> | <span data-ttu-id="a65e0-393">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-393">Description</span></span>                                                                    |
|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-394">filename</span><span class="sxs-lookup"><span data-stu-id="a65e0-394">filename</span></span>  | <span data-ttu-id="a65e0-395">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a65e0-395">Optional.</span></span> <span data-ttu-id="a65e0-396">O nome do arquivo Postado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-396">The file name for the posted file.</span></span>                                   |
| <span data-ttu-id="a65e0-397">href</span><span class="sxs-lookup"><span data-stu-id="a65e0-397">href</span></span>      | <span data-ttu-id="a65e0-398">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-398">Required.</span></span> <span data-ttu-id="a65e0-399">A URL da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="a65e0-399">The URL of the destination folder.</span></span>                                   |
| <span data-ttu-id="a65e0-400">name</span><span class="sxs-lookup"><span data-stu-id="a65e0-400">name</span></span>      | <span data-ttu-id="a65e0-401">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-401">Required.</span></span> <span data-ttu-id="a65e0-402">Define o nome de dados do formulário associado a esta seção da postagem.</span><span class="sxs-lookup"><span data-stu-id="a65e0-402">Defines the form data name associated with this section of the post.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-403">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-403">Element Information</span></span>



| <span data-ttu-id="a65e0-404">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-404">Parent Element</span></span>  | <span data-ttu-id="a65e0-405">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-405">Child Elements</span></span>      |
|-----------------|---------------------|
| [<span data-ttu-id="a65e0-406">file</span><span class="sxs-lookup"><span data-stu-id="a65e0-406">file</span></span>](#syntax) | [<span data-ttu-id="a65e0-407">formdata</span><span class="sxs-lookup"><span data-stu-id="a65e0-407">formdata</span></span>](#syntax) |



 

## <a name="resize"></a><span data-ttu-id="a65e0-408">redimensionar</span><span class="sxs-lookup"><span data-stu-id="a65e0-408">resize</span></span>

<span data-ttu-id="a65e0-409">Define o dimensionamento e a recompactação de um arquivo de imagem no formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="a65e0-409">Defines the scaling and recompression of an image file into JPEG format.</span></span> <span data-ttu-id="a65e0-410">Se o arquivo de origem já estiver no formato JPEG e for menor ou igual à largura e altura especificadas, ele não será dimensionado.</span><span class="sxs-lookup"><span data-stu-id="a65e0-410">If the source file is already in JPEG format and is less than or equal to the specified width and height, it is not sized.</span></span> <span data-ttu-id="a65e0-411">Se o arquivo de origem não for um arquivo JPEG, ele será convertido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-411">If the source file is not a JPEG file, it is converted.</span></span> <span data-ttu-id="a65e0-412">O dimensionamento, a recompactação e a conversão do arquivo podem ser evitados por meio do método [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-412">Scaling, recompression, and conversion of the file can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span> <span data-ttu-id="a65e0-413">Vários elementos de [redimensionamento](#syntax) podem estar contidos em um único nó de [arquivo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-413">Multiple [resize](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-414">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-414">Syntax</span></span>


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-415">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-415">Attributes</span></span>



| <span data-ttu-id="a65e0-416">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-416">Attribute</span></span> | <span data-ttu-id="a65e0-417">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-417">Description</span></span>                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-418">CX</span><span class="sxs-lookup"><span data-stu-id="a65e0-418">cx</span></span>        | <span data-ttu-id="a65e0-419">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-419">Required.</span></span> <span data-ttu-id="a65e0-420">A largura da imagem, em pixels, após o carregamento.</span><span class="sxs-lookup"><span data-stu-id="a65e0-420">The width of the image, in pixels, after uploading.</span></span> <span data-ttu-id="a65e0-421">Se esse valor for 0, o **CX** será calculado a partir do valor **CY** para preservar as dimensões relativas.</span><span class="sxs-lookup"><span data-stu-id="a65e0-421">If this value is 0, then **cx** is calculated from the **cy** value to preserve relative dimensions.</span></span>  |
| <span data-ttu-id="a65e0-422">cy</span><span class="sxs-lookup"><span data-stu-id="a65e0-422">cy</span></span>        | <span data-ttu-id="a65e0-423">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-423">Required.</span></span> <span data-ttu-id="a65e0-424">A altura da imagem, em pixels, após o carregamento.</span><span class="sxs-lookup"><span data-stu-id="a65e0-424">The height of the image, in pixels, after uploading.</span></span> <span data-ttu-id="a65e0-425">Se esse valor for 0, **CY** será calculado a partir do valor **CX** para preservar as dimensões relativas.</span><span class="sxs-lookup"><span data-stu-id="a65e0-425">If this value is 0, then **cy** is calculated from the **cx** value to preserve relative dimensions.</span></span> |
| <span data-ttu-id="a65e0-426">qualidade</span><span class="sxs-lookup"><span data-stu-id="a65e0-426">quality</span></span>   | <span data-ttu-id="a65e0-427">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-427">Required.</span></span> <span data-ttu-id="a65e0-428">O valor de qualidade JPEG, entre 0 e 100, com 100 sendo a qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="a65e0-428">The JPEG quality value, between 0 and 100, with 100 being the highest quality.</span></span>                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-429">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-429">Element Information</span></span>



| <span data-ttu-id="a65e0-430">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-430">Parent Element</span></span>  | <span data-ttu-id="a65e0-431">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-431">Child Elements</span></span> |
|-----------------|----------------|
| [<span data-ttu-id="a65e0-432">file</span><span class="sxs-lookup"><span data-stu-id="a65e0-432">file</span></span>](#syntax) | <span data-ttu-id="a65e0-433">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-433">None.</span></span>          |



 

## <a name="successpage"></a><span data-ttu-id="a65e0-434">successpage</span><span class="sxs-lookup"><span data-stu-id="a65e0-434">successpage</span></span>

<span data-ttu-id="a65e0-435">Especifica a página HTML do lado do servidor a ser exibida se o upload for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-435">Specifies the server-side HTML page to display if the upload is successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-436">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-436">Syntax</span></span>


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-437">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-437">Attributes</span></span>



| <span data-ttu-id="a65e0-438">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-438">Attribute</span></span> | <span data-ttu-id="a65e0-439">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-439">Description</span></span>                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-440">href</span><span class="sxs-lookup"><span data-stu-id="a65e0-440">href</span></span>      | <span data-ttu-id="a65e0-441">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-441">Required.</span></span> <span data-ttu-id="a65e0-442">A URL da página HTML do lado do servidor a ser exibida se o upload for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-442">The URL of the server-side HTML page to display if the upload is successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-443">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-443">Element Information</span></span>



| <span data-ttu-id="a65e0-444">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-444">Parent Element</span></span>        | <span data-ttu-id="a65e0-445">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-445">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="a65e0-446">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-446">uploadinfo</span></span>](#syntax) | <span data-ttu-id="a65e0-447">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-447">None.</span></span> <span data-ttu-id="a65e0-448">O texto é permitido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-448">Text is allowed.</span></span> |



 

## <a name="target"></a><span data-ttu-id="a65e0-449">destino</span><span class="sxs-lookup"><span data-stu-id="a65e0-449">target</span></span>

<span data-ttu-id="a65e0-450">Uma pasta de destino especificada no formato UNC (Convenção de nomenclatura universal) ou como um servidor WebDAV.</span><span class="sxs-lookup"><span data-stu-id="a65e0-450">A destination folder specified in Universal Naming Convention (UNC) format or as a WebDAV server.</span></span> <span data-ttu-id="a65e0-451">O serviço adicionará esse destino para especificar uma pasta de destino se a transferência usar um protocolo WebDAV ou de sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a65e0-451">The service adds this target to specify a destination folder if the transfer uses a WebDAV or file system protocol.</span></span> <span data-ttu-id="a65e0-452">Se o serviço optar por executar a transferência de arquivo como uma postagem de várias partes, ele não deverá adicionar esse elemento.</span><span class="sxs-lookup"><span data-stu-id="a65e0-452">If the service chooses to perform the file transfer as a multi-part post, it should not add this element.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-453">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-453">Syntax</span></span>


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-454">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-454">Attributes</span></span>



| <span data-ttu-id="a65e0-455">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-455">Attribute</span></span> | <span data-ttu-id="a65e0-456">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-456">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-457">href</span><span class="sxs-lookup"><span data-stu-id="a65e0-457">href</span></span>      | <span data-ttu-id="a65e0-458">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-458">Required.</span></span> <span data-ttu-id="a65e0-459">A URL da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="a65e0-459">The URL of the destination folder.</span></span> <span data-ttu-id="a65e0-460">Use o formulário **https://** para WebDAV ou o formulário de **\\ \\ \\ compartilhamento do servidor** para UNC.</span><span class="sxs-lookup"><span data-stu-id="a65e0-460">Use the **https://** form for WebDAV or the **\\\\server\\share** form for UNC.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-461">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-461">Element Information</span></span>



| <span data-ttu-id="a65e0-462">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-462">Parent Element</span></span>        | <span data-ttu-id="a65e0-463">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-463">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="a65e0-464">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-464">uploadinfo</span></span>](#syntax) | <span data-ttu-id="a65e0-465">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-465">None.</span></span> <span data-ttu-id="a65e0-466">O texto é permitido.</span><span class="sxs-lookup"><span data-stu-id="a65e0-466">Text is allowed.</span></span> |



 

## <a name="transfermanifest"></a><span data-ttu-id="a65e0-467">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="a65e0-467">transfermanifest</span></span>

<span data-ttu-id="a65e0-468">O nó pai do arquivo de manifesto de transferência.</span><span class="sxs-lookup"><span data-stu-id="a65e0-468">The parent node of the transfer manifest file.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-469">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-469">Syntax</span></span>


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-470">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-470">Attributes</span></span>

<span data-ttu-id="a65e0-471">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a65e0-471">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="a65e0-472">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-472">Element Information</span></span>



| <span data-ttu-id="a65e0-473">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-473">Parent Element</span></span> | <span data-ttu-id="a65e0-474">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-474">Child Elements</span></span>                                                    |
|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="a65e0-475">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a65e0-475">None</span></span>           | <span data-ttu-id="a65e0-476">[FileList](#syntax), [pastalist](#syntax), [uploadinfo](#syntax)</span><span class="sxs-lookup"><span data-stu-id="a65e0-476">[filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax)</span></span> |



 

## <a name="uploadinfo"></a><span data-ttu-id="a65e0-477">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="a65e0-477">uploadinfo</span></span>

<span data-ttu-id="a65e0-478">Um contêiner para elementos que fornecem informações do site de carregamento usado na transação.</span><span class="sxs-lookup"><span data-stu-id="a65e0-478">A container for elements providing information from the upload site used in the transaction.</span></span> <span data-ttu-id="a65e0-479">Vários elementos [uploadinfo](#syntax) podem estar contidos em um único nó [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="a65e0-479">Multiple [uploadinfo](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="a65e0-480">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65e0-480">Syntax</span></span>


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="a65e0-481">Atributos</span><span class="sxs-lookup"><span data-stu-id="a65e0-481">Attributes</span></span>



| <span data-ttu-id="a65e0-482">Atributo</span><span class="sxs-lookup"><span data-stu-id="a65e0-482">Attribute</span></span>    | <span data-ttu-id="a65e0-483">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65e0-483">Description</span></span>                                                                 |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-484">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a65e0-484">friendlyname</span></span> | <span data-ttu-id="a65e0-485">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a65e0-485">Required.</span></span> <span data-ttu-id="a65e0-486">Um nome amigável para o site que é exibido no assistente.</span><span class="sxs-lookup"><span data-stu-id="a65e0-486">A friendly name for the website which is displayed in the wizard.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="a65e0-487">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a65e0-487">Element Information</span></span>



| <span data-ttu-id="a65e0-488">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a65e0-488">Parent Element</span></span>              | <span data-ttu-id="a65e0-489">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a65e0-489">Child Elements</span></span>                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a65e0-490">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="a65e0-490">transfermanifest</span></span>](#syntax) | <span data-ttu-id="a65e0-491">[cancelledpage](#syntax), [failurepage](#syntax), [favorito](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [destino](#syntax)</span><span class="sxs-lookup"><span data-stu-id="a65e0-491">[cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span></span> |



 

 

 



