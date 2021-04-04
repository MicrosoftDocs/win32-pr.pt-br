---
title: Elemento String
description: Representa um recurso de cadeia de caracteres.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Faixa de sequência do elemento string do Windows
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006604"
---
# <a name="string-element"></a><span data-ttu-id="3be78-104">Elemento String</span><span class="sxs-lookup"><span data-stu-id="3be78-104">String element</span></span>

<span data-ttu-id="3be78-105">Representa um recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3be78-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="3be78-106">Uso</span><span class="sxs-lookup"><span data-stu-id="3be78-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="3be78-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="3be78-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3be78-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="3be78-108">Attribute</span></span></th>
<th><span data-ttu-id="3be78-109">Type</span><span class="sxs-lookup"><span data-stu-id="3be78-109">Type</span></span></th>
<th><span data-ttu-id="3be78-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3be78-110">Required</span></span></th>
<th><span data-ttu-id="3be78-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3be78-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3be78-112"><strong>Conteúdo</strong></span><span class="sxs-lookup"><span data-stu-id="3be78-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="3be78-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="3be78-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="3be78-114">No</span><span class="sxs-lookup"><span data-stu-id="3be78-114">No</span></span><br/></td>
<td><span data-ttu-id="3be78-115"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="3be78-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3be78-116">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="3be78-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be78-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="3be78-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="3be78-118">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="3be78-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3be78-119">No</span><span class="sxs-lookup"><span data-stu-id="3be78-119">No</span></span><br/></td>
<td><span data-ttu-id="3be78-120">A ID de recurso exclusiva.</span><span class="sxs-lookup"><span data-stu-id="3be78-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="3be78-121">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="3be78-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3be78-122">Um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="3be78-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="3be78-123">O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais.</span><span class="sxs-lookup"><span data-stu-id="3be78-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be78-124"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="3be78-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="3be78-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="3be78-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="3be78-126">No</span><span class="sxs-lookup"><span data-stu-id="3be78-126">No</span></span><br/></td>
<td><span data-ttu-id="3be78-127">O símbolo de recurso para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3be78-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="3be78-128">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="3be78-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3be78-129">Uma letra ou sublinhado seguido por qualquer sequência de letras, dígitos ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="3be78-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="3be78-130">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3be78-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3be78-131">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3be78-131">Child elements</span></span>



| <span data-ttu-id="3be78-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="3be78-132">Element</span></span>                                                                   | <span data-ttu-id="3be78-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="3be78-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="3be78-134">**String. Content**</span><span class="sxs-lookup"><span data-stu-id="3be78-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="3be78-135">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="3be78-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3be78-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="3be78-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="3be78-137">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="3be78-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3be78-138">**String. Symbol**</span><span class="sxs-lookup"><span data-stu-id="3be78-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="3be78-139">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="3be78-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3be78-140">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3be78-140">Parent elements</span></span>



| <span data-ttu-id="3be78-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="3be78-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3be78-142">**Comando. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="3be78-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="3be78-143">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="3be78-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="3be78-144">**Comando. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="3be78-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="3be78-145">**Comando. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="3be78-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="3be78-146">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="3be78-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="3be78-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="3be78-147">Remarks</span></span>

<span data-ttu-id="3be78-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3be78-148">Optional.</span></span>

<span data-ttu-id="3be78-149">Pode ocorrer no máximo uma vez para cada [**comando. LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)ou [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) elemento.</span><span class="sxs-lookup"><span data-stu-id="3be78-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="3be78-150">A definição da cadeia de caracteres é adicionada ao arquivo de cabeçalho da faixa de faixas, por exemplo, `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="3be78-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="3be78-151">A cadeia de caracteres é adicionada a uma tabela de cadeia de caracteres no arquivo de recurso da faixa de lista, em que um nome e uma ID são gerados pela estrutura da faixa de faixas, se nenhum for declarado.</span><span class="sxs-lookup"><span data-stu-id="3be78-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="3be78-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3be78-152">Examples</span></span>

<span data-ttu-id="3be78-153">O exemplo a seguir demonstra a marcação para um elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração de **cadeia de caracteres** .</span><span class="sxs-lookup"><span data-stu-id="3be78-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="3be78-154">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3be78-154">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="3be78-155">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3be78-155">Minimum supported system</span></span><br/> | <span data-ttu-id="3be78-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3be78-156">Windows 7</span></span> |
| <span data-ttu-id="3be78-157">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="3be78-157">Can be empty</span></span>                        | <span data-ttu-id="3be78-158">Não</span><span class="sxs-lookup"><span data-stu-id="3be78-158">No</span></span>        |



 

 





