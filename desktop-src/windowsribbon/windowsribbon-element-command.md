---
title: Elemento Command
description: Representa uma definição de comando.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Faixa de opções do Windows do elemento Command
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e1df5b62c7b2d7c55345ba8d6da366d04697054
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443477"
---
# <a name="command-element"></a><span data-ttu-id="39e2f-104">Elemento Command</span><span class="sxs-lookup"><span data-stu-id="39e2f-104">Command element</span></span>

<span data-ttu-id="39e2f-105">Representa uma definição de comando.</span><span class="sxs-lookup"><span data-stu-id="39e2f-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="39e2f-106">Uso</span><span class="sxs-lookup"><span data-stu-id="39e2f-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="39e2f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="39e2f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39e2f-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="39e2f-108">Attribute</span></span></th>
<th><span data-ttu-id="39e2f-109">Type</span><span class="sxs-lookup"><span data-stu-id="39e2f-109">Type</span></span></th>
<th><span data-ttu-id="39e2f-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="39e2f-110">Required</span></span></th>
<th><span data-ttu-id="39e2f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="39e2f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39e2f-112"><strong>Comentário</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-114">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-114">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-115">Usado para anotar o elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="39e2f-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="39e2f-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-117">Uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="39e2f-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="39e2f-118">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="39e2f-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39e2f-119"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-120">xs:positiveInteger union xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-121">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-121">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-122">A ID de recurso exclusiva.</span><span class="sxs-lookup"><span data-stu-id="39e2f-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="39e2f-123">
<dt><span></span><span></span><strong></strong> (A união de xs:positiveInteger e xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-124">Um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="39e2f-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="39e2f-125">O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais.</span><span class="sxs-lookup"><span data-stu-id="39e2f-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39e2f-126"><strong>Keytip</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-128">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-128">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-129">Uma cadeia de caracteres que representa o atalho de teclado de um elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="39e2f-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="39e2f-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-131">Uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="39e2f-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39e2f-132"><strong>LabelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-134">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-134">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-135">Uma cadeia de caracteres que representa o texto exibido em um elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="39e2f-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="39e2f-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-137">Uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="39e2f-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39e2f-138"><strong>LabelTitle</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-140">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-140">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-141">Uma cadeia de caracteres que representa o texto exibido em um elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="39e2f-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="39e2f-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-143">Uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="39e2f-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39e2f-144"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-146">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-146">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-147"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-148">Uma cadeia de caracteres que consiste em uma letra ou sublinhado seguida por qualquer sequência de dígitos, letras ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="39e2f-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="39e2f-149">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="39e2f-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39e2f-150"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-152">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-152">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-153"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-154">Uma cadeia de caracteres que consiste em uma letra ou sublinhado seguida por qualquer sequência de dígitos, letras ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="39e2f-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="39e2f-155">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="39e2f-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39e2f-156"><strong>TooltipDescription</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-158">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-158">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-159">Uma cadeia de caracteres que representa o texto exibido em um elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="39e2f-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="39e2f-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-161">Uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="39e2f-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39e2f-162"><strong>Tooltiptitle</strong></span><span class="sxs-lookup"><span data-stu-id="39e2f-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="39e2f-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="39e2f-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="39e2f-164">Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-164">No</span></span><br/></td>
<td><span data-ttu-id="39e2f-165">Uma cadeia de caracteres que representa o texto exibido em um elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="39e2f-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="39e2f-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="39e2f-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="39e2f-167">Uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="39e2f-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="39e2f-168">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="39e2f-168">Child elements</span></span>



| <span data-ttu-id="39e2f-169">Elemento</span><span class="sxs-lookup"><span data-stu-id="39e2f-169">Element</span></span>                                                                                                     | <span data-ttu-id="39e2f-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="39e2f-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="39e2f-171">**Command.Comment**</span><span class="sxs-lookup"><span data-stu-id="39e2f-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="39e2f-172">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="39e2f-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="39e2f-174">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-175">**Command.Keytip**</span><span class="sxs-lookup"><span data-stu-id="39e2f-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="39e2f-176">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-177">**Command.LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="39e2f-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="39e2f-178">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-179">**Command.LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="39e2f-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="39e2f-180">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-181">**Command.LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="39e2f-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="39e2f-182">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-183">**Command.LargeImages**</span><span class="sxs-lookup"><span data-stu-id="39e2f-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="39e2f-184">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="39e2f-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="39e2f-186">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-187">**Command.SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="39e2f-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="39e2f-188">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-189">**Command.SmallImages**</span><span class="sxs-lookup"><span data-stu-id="39e2f-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="39e2f-190">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-191">**Command.Symbol**</span><span class="sxs-lookup"><span data-stu-id="39e2f-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="39e2f-192">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-193">**Command.TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="39e2f-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="39e2f-194">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="39e2f-195">**Command.TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="39e2f-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="39e2f-196">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="39e2f-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="39e2f-197">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="39e2f-197">Parent elements</span></span>



| <span data-ttu-id="39e2f-198">Elemento</span><span class="sxs-lookup"><span data-stu-id="39e2f-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="39e2f-199">**Application.Commands**</span><span class="sxs-lookup"><span data-stu-id="39e2f-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="39e2f-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="39e2f-200">Remarks</span></span>

<span data-ttu-id="39e2f-201">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="39e2f-201">Required.</span></span>

<span data-ttu-id="39e2f-202">Pode ocorrer uma ou mais vezes para cada [**elemento Application.Commands.**](windowsribbon-element-application-commands.md)</span><span class="sxs-lookup"><span data-stu-id="39e2f-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="39e2f-203">Os elementos filho do elemento **Command** podem ocorrer em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="39e2f-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="39e2f-204">Normalmente, os recursos de Comando são declarados na marcação faixa de opções, mas também podem ser definidos em tempo de executar com uma chamada para [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="39e2f-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="39e2f-205">Por exemplo, é possível definir a propriedade [ \_ PKEY \_ Keytip](windowsribbon-reference-properties-uipkey-keytip.md) da interface do usuário para um Comando em vez de declarar um valor na marcação com o [**elemento Command.Keytip.**](windowsribbon-element-command-keytip.md)</span><span class="sxs-lookup"><span data-stu-id="39e2f-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="39e2f-206">Nos casos em que as propriedades Command, como rótulos e imagens, não podem ser definidas com [**SetUICommandProperty,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) elas podem ser invalidadas com uma chamada para [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="39e2f-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="39e2f-207">Após a invalidação, a estrutura consulta o aplicativo host para obter os detalhes do recurso.</span><span class="sxs-lookup"><span data-stu-id="39e2f-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="39e2f-208">Um recurso não pode ser restabelecido da tabela de recursos de marcação depois de ser invalidado.</span><span class="sxs-lookup"><span data-stu-id="39e2f-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="39e2f-209">Uma definição de comando é adicionada ao arquivo de header de marcação da Faixa de Opções para cada **Comando** declarado na marcação.</span><span class="sxs-lookup"><span data-stu-id="39e2f-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="39e2f-210">O valor de *Keytip* atua como o acelerador de teclado para um Comando, a menos que o Comando seja exposto por meio de um item de menu.</span><span class="sxs-lookup"><span data-stu-id="39e2f-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="39e2f-211">Nesse caso, a estrutura ignora o valor da *dica* de tecla e, em vez disso, usa um caractere precedido por um e comercial, conforme especificado por *LabelTitle* ou rótulo PKEY da interface do [ \_ \_ usuário.](windowsribbon-reference-properties-uipkey-label.md)</span><span class="sxs-lookup"><span data-stu-id="39e2f-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="39e2f-212">Se nenhum ampersand for especificado por *LabelTitle* ou rótulo PKEY da interface do usuário, nenhum acelerador de tecla ou \_ teclado será \_ exposto.</span><span class="sxs-lookup"><span data-stu-id="39e2f-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="39e2f-213">Exemplos</span><span class="sxs-lookup"><span data-stu-id="39e2f-213">Examples</span></span>

<span data-ttu-id="39e2f-214">O exemplo a seguir mostra um manifesto dos **elementos Command** para uma **guia** Página 1.</span><span class="sxs-lookup"><span data-stu-id="39e2f-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="39e2f-215">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="39e2f-215">Element information</span></span>

* <span data-ttu-id="39e2f-216">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="39e2f-216">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="39e2f-217">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="39e2f-217">**Can be empty**: No</span></span>



 

