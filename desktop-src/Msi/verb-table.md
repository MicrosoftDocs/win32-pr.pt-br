---
description: A tabela de verbos contém informações de verbo de comando associadas a extensões de nome de arquivo que devem ser geradas como parte do anúncio do produto. Cada linha gera um conjunto de valores e chaves do registro.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Tabela de verbo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787057"
---
# <a name="verb-table"></a><span data-ttu-id="ff362-104">Tabela de verbo</span><span class="sxs-lookup"><span data-stu-id="ff362-104">Verb Table</span></span>

<span data-ttu-id="ff362-105">A tabela de verbos contém informações de verbo de comando associadas a extensões de nome de arquivo que devem ser geradas como parte do anúncio do produto.</span><span class="sxs-lookup"><span data-stu-id="ff362-105">The Verb table contains command-verb information associated with file name extensions that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="ff362-106">Cada linha gera um conjunto de valores e chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="ff362-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="ff362-107">A tabela de verbos tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff362-107">The Verb table has the following columns.</span></span>



| <span data-ttu-id="ff362-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="ff362-108">Column</span></span>      | <span data-ttu-id="ff362-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff362-109">Type</span></span>                       | <span data-ttu-id="ff362-110">Chave</span><span class="sxs-lookup"><span data-stu-id="ff362-110">Key</span></span> | <span data-ttu-id="ff362-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="ff362-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="ff362-112">Extensão\_</span><span class="sxs-lookup"><span data-stu-id="ff362-112">Extension\_</span></span> | [<span data-ttu-id="ff362-113">Text</span><span class="sxs-lookup"><span data-stu-id="ff362-113">Text</span></span>](text.md)           | <span data-ttu-id="ff362-114">S</span><span class="sxs-lookup"><span data-stu-id="ff362-114">Y</span></span>   | <span data-ttu-id="ff362-115">N</span><span class="sxs-lookup"><span data-stu-id="ff362-115">N</span></span>        |
| <span data-ttu-id="ff362-116">Verbo</span><span class="sxs-lookup"><span data-stu-id="ff362-116">Verb</span></span>        | [<span data-ttu-id="ff362-117">Text</span><span class="sxs-lookup"><span data-stu-id="ff362-117">Text</span></span>](text.md)           | <span data-ttu-id="ff362-118">S</span><span class="sxs-lookup"><span data-stu-id="ff362-118">Y</span></span>   | <span data-ttu-id="ff362-119">N</span><span class="sxs-lookup"><span data-stu-id="ff362-119">N</span></span>        |
| <span data-ttu-id="ff362-120">Sequência</span><span class="sxs-lookup"><span data-stu-id="ff362-120">Sequence</span></span>    | [<span data-ttu-id="ff362-121">Inteiro</span><span class="sxs-lookup"><span data-stu-id="ff362-121">Integer</span></span>](integer.md)     | <span data-ttu-id="ff362-122">N</span><span class="sxs-lookup"><span data-stu-id="ff362-122">N</span></span>   | <span data-ttu-id="ff362-123">Y</span><span class="sxs-lookup"><span data-stu-id="ff362-123">Y</span></span>        |
| <span data-ttu-id="ff362-124">Comando</span><span class="sxs-lookup"><span data-stu-id="ff362-124">Command</span></span>     | [<span data-ttu-id="ff362-125">Binário</span><span class="sxs-lookup"><span data-stu-id="ff362-125">Formatted</span></span>](formatted.md) | <span data-ttu-id="ff362-126">N</span><span class="sxs-lookup"><span data-stu-id="ff362-126">N</span></span>   | <span data-ttu-id="ff362-127">S</span><span class="sxs-lookup"><span data-stu-id="ff362-127">Y</span></span>        |
| <span data-ttu-id="ff362-128">Argumento</span><span class="sxs-lookup"><span data-stu-id="ff362-128">Argument</span></span>    | [<span data-ttu-id="ff362-129">Binário</span><span class="sxs-lookup"><span data-stu-id="ff362-129">Formatted</span></span>](formatted.md) | <span data-ttu-id="ff362-130">N</span><span class="sxs-lookup"><span data-stu-id="ff362-130">N</span></span>   | <span data-ttu-id="ff362-131">S</span><span class="sxs-lookup"><span data-stu-id="ff362-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ff362-132">Colunas</span><span class="sxs-lookup"><span data-stu-id="ff362-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ff362-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extensão\_</span><span class="sxs-lookup"><span data-stu-id="ff362-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="ff362-134">A extensão associada à linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="ff362-134">The extension associated with the table row.</span></span> <span data-ttu-id="ff362-135">Esta coluna é uma chave externa para a primeira coluna da [tabela de extensão](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff362-135">This column is an external key to the first column of the [Extension table](extension-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff362-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo</span><span class="sxs-lookup"><span data-stu-id="ff362-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span>
</dt> <dd>

<span data-ttu-id="ff362-137">O verbo para o comando.</span><span class="sxs-lookup"><span data-stu-id="ff362-137">The verb for the command.</span></span>

</dd> <dt>

<span data-ttu-id="ff362-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="ff362-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="ff362-139">A sequência dos comandos.</span><span class="sxs-lookup"><span data-stu-id="ff362-139">The sequence of the commands.</span></span> <span data-ttu-id="ff362-140">Somente os verbos para os quais a coluna de sequência é não nula são usados para preparar uma lista ordenada para o valor padrão da chave do Shell.</span><span class="sxs-lookup"><span data-stu-id="ff362-140">Only verbs for which the Sequence column is non-Null are used to prepare an ordered list for the default value of the shell key.</span></span> <span data-ttu-id="ff362-141">O verbo com o menor valor nessa coluna torna-se o verbo padrão.</span><span class="sxs-lookup"><span data-stu-id="ff362-141">The Verb with the lowest value in this column becomes the default verb.</span></span>

</dd> <dt>

<span data-ttu-id="ff362-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Linha</span><span class="sxs-lookup"><span data-stu-id="ff362-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="ff362-143">O texto localizável exibido no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="ff362-143">The localizable text displayed on the context menu.</span></span>

</dd> <dt>

<span data-ttu-id="ff362-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento</span><span class="sxs-lookup"><span data-stu-id="ff362-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="ff362-145">Valor para os argumentos do comando.</span><span class="sxs-lookup"><span data-stu-id="ff362-145">Value for the command arguments.</span></span>

<span data-ttu-id="ff362-146">Observe que a resolução das propriedades no campo argumento é limitada.</span><span class="sxs-lookup"><span data-stu-id="ff362-146">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="ff362-147">Uma propriedade formatada como \[ *Propriedade* \] nesse campo só poderá ser resolvida se a propriedade já tiver o valor pretendido quando o componente proprietário do verbo for instalado.</span><span class="sxs-lookup"><span data-stu-id="ff362-147">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component owning the verb is installed.</span></span> <span data-ttu-id="ff362-148">Por exemplo, para o argumento " \[ \#MyDoc.doc\] " para resolver o valor correto, o mesmo processo deve estar instalando o arquivo MyDoc.doc e o componente que possui o verbo.</span><span class="sxs-lookup"><span data-stu-id="ff362-148">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff362-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff362-149">Remarks</span></span>

<span data-ttu-id="ff362-150">Essa tabela é referida quando a ação [RegisterExtensionInfo](registerextensioninfo-action.md) ou a [ação UnregisterExtensionInfo](unregisterextensioninfo-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="ff362-150">This table is referred to when the [RegisterExtensionInfo action](registerextensioninfo-action.md) or the [UnregisterExtensionInfo action](unregisterextensioninfo-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="ff362-151">Validação</span><span class="sxs-lookup"><span data-stu-id="ff362-151">Validation</span></span>

<dl>

[<span data-ttu-id="ff362-152">ICE03</span><span class="sxs-lookup"><span data-stu-id="ff362-152">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ff362-153">ICE06</span><span class="sxs-lookup"><span data-stu-id="ff362-153">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ff362-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="ff362-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ff362-155">ICE46</span><span class="sxs-lookup"><span data-stu-id="ff362-155">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="ff362-156">ICE69</span><span class="sxs-lookup"><span data-stu-id="ff362-156">ICE69</span></span>](ice69.md)  
</dl>

 

 



