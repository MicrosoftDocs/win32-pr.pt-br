---
title: Elemento Command
description: Representa uma definição de comando.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Faixa de das janelas do elemento de comando
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b684b361927180a4bb87d2d7814d2f26d4fdcd91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294394"
---
# <a name="command-element"></a><span data-ttu-id="fde11-104">Elemento Command</span><span class="sxs-lookup"><span data-stu-id="fde11-104">Command element</span></span>

<span data-ttu-id="fde11-105">Representa uma definição de comando.</span><span class="sxs-lookup"><span data-stu-id="fde11-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="fde11-106">Uso</span><span class="sxs-lookup"><span data-stu-id="fde11-106">Usage</span></span>

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a><span data-ttu-id="fde11-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="fde11-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fde11-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="fde11-108">Attribute</span></span></th>
<th><span data-ttu-id="fde11-109">Type</span><span class="sxs-lookup"><span data-stu-id="fde11-109">Type</span></span></th>
<th><span data-ttu-id="fde11-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fde11-110">Required</span></span></th>
<th><span data-ttu-id="fde11-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fde11-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fde11-112"><strong>Comentário</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="fde11-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-114">No</span><span class="sxs-lookup"><span data-stu-id="fde11-114">No</span></span><br/></td>
<td><span data-ttu-id="fde11-115">Usado para anotar o elemento Command.</span><span class="sxs-lookup"><span data-stu-id="fde11-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="fde11-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-117">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="fde11-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="fde11-118">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="fde11-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fde11-119"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-120">xs: positiveInteger Union xs: String</span><span class="sxs-lookup"><span data-stu-id="fde11-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-121">No</span><span class="sxs-lookup"><span data-stu-id="fde11-121">No</span></span><br/></td>
<td><span data-ttu-id="fde11-122">A ID de recurso exclusiva.</span><span class="sxs-lookup"><span data-stu-id="fde11-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="fde11-123">
<dt><span></span><span></span><strong></strong> (A União de xs: positiveInteger e xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-124">Um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="fde11-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="fde11-125">O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais.</span><span class="sxs-lookup"><span data-stu-id="fde11-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fde11-126"><strong>KeyTip</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="fde11-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-128">No</span><span class="sxs-lookup"><span data-stu-id="fde11-128">No</span></span><br/></td>
<td><span data-ttu-id="fde11-129">Uma cadeia de caracteres que representa o atalho de teclado de um elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="fde11-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="fde11-130">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-131">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo o espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="fde11-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fde11-132"><strong>LabelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="fde11-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-134">No</span><span class="sxs-lookup"><span data-stu-id="fde11-134">No</span></span><br/></td>
<td><span data-ttu-id="fde11-135">Uma cadeia de caracteres que representa o texto exibido em um elemento Command.</span><span class="sxs-lookup"><span data-stu-id="fde11-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="fde11-136">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-137">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="fde11-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fde11-138"><strong>LabelTitle</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="fde11-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-140">No</span><span class="sxs-lookup"><span data-stu-id="fde11-140">No</span></span><br/></td>
<td><span data-ttu-id="fde11-141">Uma cadeia de caracteres que representa o texto exibido em um elemento Command.</span><span class="sxs-lookup"><span data-stu-id="fde11-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="fde11-142">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-143">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="fde11-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fde11-144"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="fde11-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-146">No</span><span class="sxs-lookup"><span data-stu-id="fde11-146">No</span></span><br/></td>
<td><span data-ttu-id="fde11-147"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-148">Uma cadeia de caracteres que consiste em uma letra ou sublinhado seguido por qualquer sequência de dígitos, letras ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="fde11-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="fde11-149">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="fde11-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fde11-150"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="fde11-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-152">No</span><span class="sxs-lookup"><span data-stu-id="fde11-152">No</span></span><br/></td>
<td><span data-ttu-id="fde11-153"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-154">Uma cadeia de caracteres que consiste em uma letra ou sublinhado seguido por qualquer sequência de dígitos, letras ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="fde11-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="fde11-155">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="fde11-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fde11-156"><strong>TooltipDescription</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="fde11-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-158">No</span><span class="sxs-lookup"><span data-stu-id="fde11-158">No</span></span><br/></td>
<td><span data-ttu-id="fde11-159">Uma cadeia de caracteres que representa o texto exibido em um elemento Command.</span><span class="sxs-lookup"><span data-stu-id="fde11-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="fde11-160">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-161">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="fde11-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fde11-162"><strong>TooltipTitle</strong></span><span class="sxs-lookup"><span data-stu-id="fde11-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="fde11-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="fde11-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="fde11-164">No</span><span class="sxs-lookup"><span data-stu-id="fde11-164">No</span></span><br/></td>
<td><span data-ttu-id="fde11-165">Uma cadeia de caracteres que representa o texto exibido em um elemento Command.</span><span class="sxs-lookup"><span data-stu-id="fde11-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="fde11-166">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fde11-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fde11-167">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="fde11-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fde11-168">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fde11-168">Child elements</span></span>



| <span data-ttu-id="fde11-169">Elemento</span><span class="sxs-lookup"><span data-stu-id="fde11-169">Element</span></span>                                                                                                     | <span data-ttu-id="fde11-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="fde11-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="fde11-171">**Comando. Comment**</span><span class="sxs-lookup"><span data-stu-id="fde11-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="fde11-172">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="fde11-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="fde11-174">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-175">**Comando. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="fde11-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="fde11-176">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-177">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="fde11-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="fde11-178">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-179">**Comando. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="fde11-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="fde11-180">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-181">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="fde11-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="fde11-182">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-183">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="fde11-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="fde11-184">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="fde11-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="fde11-186">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-187">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="fde11-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="fde11-188">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-189">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="fde11-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="fde11-190">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-191">**Comando. Symbol**</span><span class="sxs-lookup"><span data-stu-id="fde11-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="fde11-192">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-193">**Comando. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="fde11-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="fde11-194">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="fde11-195">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="fde11-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="fde11-196">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="fde11-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fde11-197">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fde11-197">Parent elements</span></span>



| <span data-ttu-id="fde11-198">Elemento</span><span class="sxs-lookup"><span data-stu-id="fde11-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="fde11-199">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="fde11-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fde11-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="fde11-200">Remarks</span></span>

<span data-ttu-id="fde11-201">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="fde11-201">Required.</span></span>

<span data-ttu-id="fde11-202">Pode ocorrer uma ou mais vezes para cada elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="fde11-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="fde11-203">Os elementos filho do elemento **Command** podem ocorrer em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="fde11-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="fde11-204">Normalmente, os recursos de comando são declarados na marcação da faixa de medida, mas também podem ser definidos em tempo de execução com uma chamada para [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="fde11-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="fde11-205">Por exemplo, é possível definir a propriedade [ \_ PKEY \_ KeyTip da interface do usuário](windowsribbon-reference-properties-uipkey-keytip.md) para um comando em vez de declarar um valor na marcação com o elemento [**Command. KeyTip**](windowsribbon-element-command-keytip.md) .</span><span class="sxs-lookup"><span data-stu-id="fde11-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="fde11-206">Nos casos em que as propriedades de comando, como rótulos e imagens, não podem ser definidas com [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , elas podem ser invalidadas com uma chamada para [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="fde11-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="fde11-207">Após a invalidação, a estrutura consulta o aplicativo host para obter os detalhes do recurso.</span><span class="sxs-lookup"><span data-stu-id="fde11-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="fde11-208">Um recurso não pode ser restabelecido da tabela de recursos de marcação depois de ser invalidado.</span><span class="sxs-lookup"><span data-stu-id="fde11-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="fde11-209">Uma definição de comando é adicionada ao arquivo de cabeçalho de marcação da faixa de medida para cada **comando** declarado na marcação.</span><span class="sxs-lookup"><span data-stu-id="fde11-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="fde11-210">O valor de *KeyTip* atua como o acelerador de teclado para um comando, a menos que esse comando seja exposto por meio de um item de menu.</span><span class="sxs-lookup"><span data-stu-id="fde11-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="fde11-211">Nesse caso, a estrutura ignora o valor de *KeyTip* e, em vez disso, usa um caractere precedido por um e comercial como especificado por *LabelTitle* ou [rótulo de \_ PKEY \_ de interface do usuário](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="fde11-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="fde11-212">Se nenhum e comercial for especificado por *LabelTitle* ou rótulo de PKEY da interface do usuário \_ \_ , nenhum KeyTip ou acelerador de teclado será exposto.</span><span class="sxs-lookup"><span data-stu-id="fde11-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="fde11-213">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fde11-213">Examples</span></span>

<span data-ttu-id="fde11-214">O exemplo a seguir mostra um manifesto dos elementos **Command** para uma guia **Home** .</span><span class="sxs-lookup"><span data-stu-id="fde11-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a><span data-ttu-id="fde11-215">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="fde11-215">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="fde11-216">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fde11-216">Minimum supported system</span></span><br/> | <span data-ttu-id="fde11-217">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fde11-217">Windows 7</span></span> |
| <span data-ttu-id="fde11-218">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="fde11-218">Can be empty</span></span>                        | <span data-ttu-id="fde11-219">Não</span><span class="sxs-lookup"><span data-stu-id="fde11-219">No</span></span>        |



 

