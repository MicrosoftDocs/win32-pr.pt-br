---
description: ICE69 verifica se todas as subcadeias de caracteres do formulário \[ $componentkey \] em uma cadeia de caracteres formatada não fazem referência cruzada de componentes.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171142"
---
# <a name="ice69"></a><span data-ttu-id="ddea4-103">ICE69</span><span class="sxs-lookup"><span data-stu-id="ddea4-103">ICE69</span></span>

<span data-ttu-id="ddea4-104">ICE69 verifica se todas as subcadeias de caracteres do formulário \[ $componentkey \] em uma cadeia de caracteres [formatada](formatted.md) não fazem referência cruzada de componentes.</span><span class="sxs-lookup"><span data-stu-id="ddea4-104">ICE69 checks that all substrings of the form \[$componentkey\] within a [formatted](formatted.md) string do not cross-reference components.</span></span> <span data-ttu-id="ddea4-105">Uma referência entre componentes ocorre quando a \[ propriedade $componentkey \] de uma cadeia de caracteres formatada refere-se a um componente que não é o componente armazenado na \_ coluna componente de suas tabelas.</span><span class="sxs-lookup"><span data-stu-id="ddea4-105">A cross-component reference occurs when the \[$componentkey\] property of a formatted string refers to a component other than the component stored in the Component\_ column of your tables.</span></span>

<span data-ttu-id="ddea4-106">Problemas com referências entre componentes surgem da maneira como as cadeias de caracteres [formatadas](formatted.md) são avaliadas.</span><span class="sxs-lookup"><span data-stu-id="ddea4-106">Problems with cross-component referencing arise from the way [formatted](formatted.md) strings are evaluated.</span></span> <span data-ttu-id="ddea4-107">Se o componente referenciado com \[ a \] Propriedade $componentkey já estiver instalado e não estiver sendo alterado durante a instalação atual (por exemplo, sendo reinstalado, movido para a origem e assim por diante), a expressão \[ $componentkey \] será avaliada como NULL, porque o estado de ação do componente em \[ $componentkey \] é nulo.</span><span class="sxs-lookup"><span data-stu-id="ddea4-107">If the component referenced with the \[$componentkey\] property is already installed and is not being changed during the current installation (for example, being reinstalled, moved to source, and so forth), the expression \[$componentkey\] evaluates to null, because the action state of the component in \[$componentkey\] is null.</span></span> <span data-ttu-id="ddea4-108">Problemas semelhantes podem ocorrer durante as operações de atualização e reparo.</span><span class="sxs-lookup"><span data-stu-id="ddea4-108">Similar problems can occur during upgrade and repair operations.</span></span>

## <a name="result"></a><span data-ttu-id="ddea4-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="ddea4-109">Result</span></span>

<span data-ttu-id="ddea4-110">ICE69 retornará um erro se uma \[ \] subcadeia de caracteres $componentkey dentro de uma cadeia de caracteres [formatada](formatted.md) cruzar referências a um componente em outro recurso.</span><span class="sxs-lookup"><span data-stu-id="ddea4-110">ICE69 returns an error if a \[$componentkey\] substring within a [formatted](formatted.md) string cross-references a component in another feature.</span></span> <span data-ttu-id="ddea4-111">ICE69 retornará um aviso se uma \[ \] subcadeia de caracteres $componentkey dentro de uma cadeia de caracteres formatada cruzar referências a um componente no mesmo recurso.</span><span class="sxs-lookup"><span data-stu-id="ddea4-111">ICE69 returns a warning if a \[$componentkey\] substring within a formatted string cross-references a component in the same feature.</span></span> <span data-ttu-id="ddea4-112">(A tabela [FeatureComponents](featurecomponents-table.md) é usada para determinar esse mapeamento.</span><span class="sxs-lookup"><span data-stu-id="ddea4-112">(The [FeatureComponents](featurecomponents-table.md) table is used to determine this mapping.</span></span> <span data-ttu-id="ddea4-113">Ele deve mapear para o mesmo recurso para o aviso.</span><span class="sxs-lookup"><span data-stu-id="ddea4-113">It must map to the same feature for the warning.</span></span> <span data-ttu-id="ddea4-114">A referência a componentes em recursos pai ou referência a componentes em recursos filho é considerada um erro.)</span><span class="sxs-lookup"><span data-stu-id="ddea4-114">Referencing components in parent features or referencing components in child features is considered to be an error.)</span></span>

<span data-ttu-id="ddea4-115">ICE69 relatará um erro se a \[ \# \] subcadeia de caracteres FileKey dentro de uma cadeia de caracteres [formatada](formatted.md) fizer referência a um arquivo que não está especificado na tabela de [arquivos](file-table.md) como pertencente ao mesmo componente.</span><span class="sxs-lookup"><span data-stu-id="ddea4-115">ICE69 reports an error if the \[\#FileKey\] substring within a [formatted](formatted.md) string references a file which is not specified in the [File](file-table.md) table as belonging to the same component.</span></span>

## <a name="example"></a><span data-ttu-id="ddea4-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ddea4-116">Example</span></span>

<span data-ttu-id="ddea4-117">ICE69 relata o seguinte para os exemplos mostrados.</span><span class="sxs-lookup"><span data-stu-id="ddea4-117">ICE69 reports the following for the examples shown.</span></span>

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

<span data-ttu-id="ddea4-118">Para corrigir esse erro, não faça referência cruzada de componentes.</span><span class="sxs-lookup"><span data-stu-id="ddea4-118">To fix this error, do not cross-reference components.</span></span> <span data-ttu-id="ddea4-119">Altere o \[ $componentkey \] para corresponder ao componente do atalho.</span><span class="sxs-lookup"><span data-stu-id="ddea4-119">Change the \[$componentkey\] to match the component of the shortcut.</span></span>

<span data-ttu-id="ddea4-120">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="ddea4-120">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="ddea4-121">Atalho</span><span class="sxs-lookup"><span data-stu-id="ddea4-121">Shortcut</span></span>  | <span data-ttu-id="ddea4-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="ddea4-122">Component\_</span></span> | <span data-ttu-id="ddea4-123">Argumento</span><span class="sxs-lookup"><span data-stu-id="ddea4-123">Argument</span></span>     |
|-----------|-------------|--------------|
| <span data-ttu-id="ddea4-124">Teste</span><span class="sxs-lookup"><span data-stu-id="ddea4-124">Test</span></span>      | <span data-ttu-id="ddea4-125">QuickTest</span><span class="sxs-lookup"><span data-stu-id="ddea4-125">QuickTest</span></span>   | <span data-ttu-id="ddea4-126">-v \[ $Test\]</span><span class="sxs-lookup"><span data-stu-id="ddea4-126">-v \[$Test\]</span></span> |
| <span data-ttu-id="ddea4-127">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="ddea4-127">Shortcut2</span></span> | <span data-ttu-id="ddea4-128">QuickTest</span><span class="sxs-lookup"><span data-stu-id="ddea4-128">QuickTest</span></span>   | <span data-ttu-id="ddea4-129">\[$Test 2\]</span><span class="sxs-lookup"><span data-stu-id="ddea4-129">\[$Test2\]</span></span>   |



 

<span data-ttu-id="ddea4-130">As tabelas de [verbo](verb-table.md) e de [extensão](extension-table.md) são casos especiais em que a tabela de verbos faz referência a uma extensão que pertence a um componente.</span><span class="sxs-lookup"><span data-stu-id="ddea4-130">The [Verb](verb-table.md) and [Extension](extension-table.md) tables are special cases in that the Verb table references an extension that belongs to a component.</span></span> <span data-ttu-id="ddea4-131">No entanto, uma extensão pode pertencer a vários componentes porque a chave primária para a tabela de extensão é composta pelas colunas de extensão e componente \_ .</span><span class="sxs-lookup"><span data-stu-id="ddea4-131">An Extension, however, can belong to multiple components because the primary key for the extension table is made up of the Extension and Component\_ columns.</span></span> <span data-ttu-id="ddea4-132">Logicamente, você pode ter a seguinte situação.</span><span class="sxs-lookup"><span data-stu-id="ddea4-132">You can logically have the following situation.</span></span>

<span data-ttu-id="ddea4-133">[Tabela de verbos](verb-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="ddea4-133">[Verb Table](verb-table.md) (partial)</span></span>



| <span data-ttu-id="ddea4-134">Extensão</span><span class="sxs-lookup"><span data-stu-id="ddea4-134">Extension</span></span> | <span data-ttu-id="ddea4-135">Verbo\_</span><span class="sxs-lookup"><span data-stu-id="ddea4-135">Verb\_</span></span> | <span data-ttu-id="ddea4-136">Argumento</span><span class="sxs-lookup"><span data-stu-id="ddea4-136">Argument</span></span>                |
|-----------|--------|-------------------------|
| <span data-ttu-id="ddea4-137">TST</span><span class="sxs-lookup"><span data-stu-id="ddea4-137">tst</span></span>       | <span data-ttu-id="ddea4-138">Abrir</span><span class="sxs-lookup"><span data-stu-id="ddea4-138">open</span></span>   | <span data-ttu-id="ddea4-139">-v \[ $comp 1 \] \[ $comp 2\]</span><span class="sxs-lookup"><span data-stu-id="ddea4-139">-v \[$comp1\]\[$comp2\]</span></span> |



 

<span data-ttu-id="ddea4-140">[Tabela de extensão](extension-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="ddea4-140">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="ddea4-141">Extensão</span><span class="sxs-lookup"><span data-stu-id="ddea4-141">Extension</span></span> | <span data-ttu-id="ddea4-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="ddea4-142">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="ddea4-143">TST</span><span class="sxs-lookup"><span data-stu-id="ddea4-143">tst</span></span>       | <span data-ttu-id="ddea4-144">comp1</span><span class="sxs-lookup"><span data-stu-id="ddea4-144">comp1</span></span>       |
| <span data-ttu-id="ddea4-145">TST</span><span class="sxs-lookup"><span data-stu-id="ddea4-145">tst</span></span>       | <span data-ttu-id="ddea4-146">COMP2</span><span class="sxs-lookup"><span data-stu-id="ddea4-146">comp2</span></span>       |



 

[<span data-ttu-id="ddea4-147">Tabela FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="ddea4-147">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="ddea4-148">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="ddea4-148">Feature\_</span></span> | <span data-ttu-id="ddea4-149">Componente\_</span><span class="sxs-lookup"><span data-stu-id="ddea4-149">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="ddea4-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="ddea4-150">Feature1</span></span>  | <span data-ttu-id="ddea4-151">QuickTest</span><span class="sxs-lookup"><span data-stu-id="ddea4-151">QuickTest</span></span>   |
| <span data-ttu-id="ddea4-152">Feature1</span><span class="sxs-lookup"><span data-stu-id="ddea4-152">Feature1</span></span>  | <span data-ttu-id="ddea4-153">Teste</span><span class="sxs-lookup"><span data-stu-id="ddea4-153">Test</span></span>        |
| <span data-ttu-id="ddea4-154">Feature2</span><span class="sxs-lookup"><span data-stu-id="ddea4-154">Feature2</span></span>  | <span data-ttu-id="ddea4-155">Test2</span><span class="sxs-lookup"><span data-stu-id="ddea4-155">Test2</span></span>       |



 

<span data-ttu-id="ddea4-156">Nesse caso, você deve garantir que pelo menos uma das propriedades de \[ $componentkey \] seja avaliada como um valor não nulo.</span><span class="sxs-lookup"><span data-stu-id="ddea4-156">In this case, you must ensure that at least one of the \[$componentkey\] properties evaluates to a non-null value.</span></span> <span data-ttu-id="ddea4-157">No entanto, cada \[ \] Propriedade $componentkey na coluna Argument da tabela Verb ( \[ $comp 1 \] e \[ $comp 2 \] no exemplo acima) deve fazer referência a um possível componente incluído com a extensão associada ao verbo.</span><span class="sxs-lookup"><span data-stu-id="ddea4-157">However, every \[$componentkey\] property in the Argument column of the Verb table (\[$comp1\] and \[$comp2\] in the above example) must reference a possible component included with the extension associated with the verb.</span></span> <span data-ttu-id="ddea4-158">Uma referência como \[ $comp 3 \] resultaria em um aviso de ICE69.</span><span class="sxs-lookup"><span data-stu-id="ddea4-158">A reference like \[$comp3\] would result in a warning from ICE69.</span></span>

<span data-ttu-id="ddea4-159">A [tabela AppID](appid-table.md) tem uma situação semelhante à tabela de verbos.</span><span class="sxs-lookup"><span data-stu-id="ddea4-159">The [AppId table](appid-table.md) has a similar situation to the Verb table.</span></span> <span data-ttu-id="ddea4-160">Ele usa a [tabela de classes](class-table.md) para sua referência de componente.</span><span class="sxs-lookup"><span data-stu-id="ddea4-160">It uses the [Class table](class-table.md) for its component reference.</span></span> <span data-ttu-id="ddea4-161">Nesse caso, a tabela AppId é validada da mesma maneira que a validação de Verb-Extension (agora, a classe AppId).</span><span class="sxs-lookup"><span data-stu-id="ddea4-161">In this case, the AppId table is validated in the same way as the Verb-Extension validation (now AppId-Class).</span></span>

<span data-ttu-id="ddea4-162">A coluna de argumento da tabela de classes é validada como o [atalho](shortcut-table.md), o [registro](registry-table.md)e as tabelas semelhantes.</span><span class="sxs-lookup"><span data-stu-id="ddea4-162">The Class table's Argument column is validated like the [Shortcut](shortcut-table.md), [Registry](registry-table.md), and similar tables.</span></span>

## <a name="table-used-during-execution-only-if-found"></a><span data-ttu-id="ddea4-163">Tabela usada durante a execução (somente se encontrada)</span><span class="sxs-lookup"><span data-stu-id="ddea4-163">Table used during execution (only if found)</span></span>

[<span data-ttu-id="ddea4-164">IniFile</span><span class="sxs-lookup"><span data-stu-id="ddea4-164">IniFile</span></span>](inifile-table.md)

[<span data-ttu-id="ddea4-165">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="ddea4-165">RemoveIniFile</span></span>](removeinifile-table.md)

[<span data-ttu-id="ddea4-166">Registro</span><span class="sxs-lookup"><span data-stu-id="ddea4-166">Registry</span></span>](registry-table.md)

[<span data-ttu-id="ddea4-167">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="ddea4-167">RemoveRegistry</span></span>](removeregistry-table.md)

[<span data-ttu-id="ddea4-168">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="ddea4-168">ServiceControl</span></span>](servicecontrol-table.md)

[<span data-ttu-id="ddea4-169">Instalar o</span><span class="sxs-lookup"><span data-stu-id="ddea4-169">ServiceInstall</span></span>](serviceinstall-table.md)

[<span data-ttu-id="ddea4-170">Atalho</span><span class="sxs-lookup"><span data-stu-id="ddea4-170">Shortcut</span></span>](shortcut-table.md)

[<span data-ttu-id="ddea4-171">Verbo</span><span class="sxs-lookup"><span data-stu-id="ddea4-171">Verb</span></span>](verb-table.md)

[<span data-ttu-id="ddea4-172">Extensão</span><span class="sxs-lookup"><span data-stu-id="ddea4-172">Extension</span></span>](extension-table.md)

[<span data-ttu-id="ddea4-173">Classe</span><span class="sxs-lookup"><span data-stu-id="ddea4-173">Class</span></span>](class-table.md)

[<span data-ttu-id="ddea4-174">AppId</span><span class="sxs-lookup"><span data-stu-id="ddea4-174">AppId</span></span>](appid-table.md)

[<span data-ttu-id="ddea4-175">Ambiente</span><span class="sxs-lookup"><span data-stu-id="ddea4-175">Environment</span></span>](environment-table.md)

## <a name="related-topics"></a><span data-ttu-id="ddea4-176">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddea4-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddea4-177">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="ddea4-177">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



