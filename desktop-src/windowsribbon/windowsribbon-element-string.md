---
title: Elemento String
description: Representa um recurso de cadeia de caracteres.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Faixa de Opções do Windows do elemento String
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b0dab5d7ce1485aad5fe1e15442069c488933aa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443897"
---
# <a name="string-element"></a><span data-ttu-id="e725b-104">Elemento String</span><span class="sxs-lookup"><span data-stu-id="e725b-104">String element</span></span>

<span data-ttu-id="e725b-105">Representa um recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e725b-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="e725b-106">Uso</span><span class="sxs-lookup"><span data-stu-id="e725b-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="e725b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="e725b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e725b-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="e725b-108">Attribute</span></span></th>
<th><span data-ttu-id="e725b-109">Type</span><span class="sxs-lookup"><span data-stu-id="e725b-109">Type</span></span></th>
<th><span data-ttu-id="e725b-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e725b-110">Required</span></span></th>
<th><span data-ttu-id="e725b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e725b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e725b-112"><strong>Conteúdo</strong></span><span class="sxs-lookup"><span data-stu-id="e725b-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="e725b-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="e725b-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="e725b-114">Não</span><span class="sxs-lookup"><span data-stu-id="e725b-114">No</span></span><br/></td>
<td><span data-ttu-id="e725b-115"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="e725b-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e725b-116">Uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="e725b-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e725b-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="e725b-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="e725b-118">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="e725b-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="e725b-119">Não</span><span class="sxs-lookup"><span data-stu-id="e725b-119">No</span></span><br/></td>
<td><span data-ttu-id="e725b-120">A ID de recurso exclusiva.</span><span class="sxs-lookup"><span data-stu-id="e725b-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="e725b-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="e725b-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e725b-122">Um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="e725b-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="e725b-123">O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais.</span><span class="sxs-lookup"><span data-stu-id="e725b-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e725b-124"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="e725b-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="e725b-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="e725b-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="e725b-126">Não</span><span class="sxs-lookup"><span data-stu-id="e725b-126">No</span></span><br/></td>
<td><span data-ttu-id="e725b-127">O símbolo de recurso para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e725b-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="e725b-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="e725b-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e725b-129">Uma letra ou sublinhado seguido por qualquer sequência de letras, dígitos ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="e725b-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="e725b-130">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e725b-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e725b-131">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e725b-131">Child elements</span></span>



| <span data-ttu-id="e725b-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="e725b-132">Element</span></span>                                                                   | <span data-ttu-id="e725b-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="e725b-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="e725b-134">**String.Content**</span><span class="sxs-lookup"><span data-stu-id="e725b-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="e725b-135">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="e725b-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e725b-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="e725b-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="e725b-137">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="e725b-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="e725b-138">**String.Symbol**</span><span class="sxs-lookup"><span data-stu-id="e725b-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="e725b-139">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="e725b-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e725b-140">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e725b-140">Parent elements</span></span>



| <span data-ttu-id="e725b-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="e725b-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e725b-142">**Command.Keytip**</span><span class="sxs-lookup"><span data-stu-id="e725b-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="e725b-143">**Command.LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="e725b-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="e725b-144">**Command.LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="e725b-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="e725b-145">**Command.TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="e725b-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="e725b-146">**Command.TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="e725b-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="e725b-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="e725b-147">Remarks</span></span>

<span data-ttu-id="e725b-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e725b-148">Optional.</span></span>

<span data-ttu-id="e725b-149">Pode ocorrer no máximo uma vez para cada [**elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)ou [**Command.TooltipDescription.**](windowsribbon-element-command-tooltipdescription.md)</span><span class="sxs-lookup"><span data-stu-id="e725b-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="e725b-150">A definição de cadeia de caracteres é adicionada ao arquivo de header da Faixa de Opções, por exemplo, `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="e725b-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="e725b-151">A cadeia de caracteres é adicionada a uma tabela de cadeia de caracteres no arquivo de recurso faixa de opções em que um nome e uma ID são gerados pela estrutura de Faixa de Opções se nenhum for declarado.</span><span class="sxs-lookup"><span data-stu-id="e725b-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="e725b-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e725b-152">Examples</span></span>

<span data-ttu-id="e725b-153">O exemplo a seguir demonstra a marcação para um [**elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração **String.**</span><span class="sxs-lookup"><span data-stu-id="e725b-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="e725b-154">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e725b-154">Element information</span></span>

- <span data-ttu-id="e725b-155">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="e725b-155">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="e725b-156">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="e725b-156">**Can be empty**: No</span></span>



 

 





