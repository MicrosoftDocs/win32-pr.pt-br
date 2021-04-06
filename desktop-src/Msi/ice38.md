---
description: ICE38 valida que cada componente que está sendo instalado no perfil do usuário atual também especifica uma chave do registro na \_ raiz do usuário atual da hKey \_ na coluna KeyPath da tabela de componentes.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011295"
---
# <a name="ice38"></a><span data-ttu-id="025ba-103">ICE38</span><span class="sxs-lookup"><span data-stu-id="025ba-103">ICE38</span></span>

<span data-ttu-id="025ba-104">ICE38 valida que cada componente que está sendo instalado no perfil do usuário atual também especifica uma chave do registro na raiz do **\_ \_ usuário atual da hKey** na coluna KeyPath da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="025ba-104">ICE38 validates that every component being installed under the current user's profile also specifies a registry key under the **HKEY\_CURRENT\_USER** root in the KeyPath column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="025ba-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="025ba-105">Result</span></span>

<span data-ttu-id="025ba-106">ICE38 posta um erro se um componente instalado no perfil do usuário não especificar uma chave do Registro HKCU.</span><span class="sxs-lookup"><span data-stu-id="025ba-106">ICE38 posts an error if a component installed under the user's profile does not specify a HKCU registry key.</span></span>

## <a name="example"></a><span data-ttu-id="025ba-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="025ba-107">Example</span></span>

<span data-ttu-id="025ba-108">ICE38 relata os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="025ba-108">ICE38 reports the following errors for the sample shown.</span></span>



| <span data-ttu-id="025ba-109">Erro de ICE38</span><span class="sxs-lookup"><span data-stu-id="025ba-109">ICE38 error</span></span>                                                                                                                         | <span data-ttu-id="025ba-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="025ba-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="025ba-111">O componente Component1 é instalado no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="025ba-111">Component Component1 installs to user profile.</span></span> <span data-ttu-id="025ba-112">Ele deve usar uma chave do registro em HKCU como seu caminho Key, não um arquivo.</span><span class="sxs-lookup"><span data-stu-id="025ba-112">It must use a registry key under HKCU as its KeyPath, not a file.</span></span>                    | <span data-ttu-id="025ba-113">O valor da coluna Attributes de Component1 é 0, o que significa que o componente deve usar um arquivo como seu caminho KeyPath.</span><span class="sxs-lookup"><span data-stu-id="025ba-113">The value of the attributes column of Component1 is 0, meaning that the component must use a file as its KeyPath.</span></span> <span data-ttu-id="025ba-114">Isso causa dificuldades quando vários usuários instalam o componente no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="025ba-114">This causes difficulties when multiple users install the component on the same computer.</span></span> <span data-ttu-id="025ba-115">Para corrigir esse erro em Component1, defina o bit RegistryKeyPath na coluna Attributes da [tabela Component](component-table.md) e altere a entrada na coluna KeyPath para um valor listado na coluna Registry da [tabela Registry](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="025ba-115">To fix this error on Component1, set the RegistryKeyPath bit in the Attributes column of the [Component table](component-table.md) and change the entry in the KeyPath column to a value listed in the Registry column of the [Registry table](registry-table.md).</span></span><br/>                                                                                |
| <span data-ttu-id="025ba-116">O componente Component2 é instalado no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="025ba-116">Component Component2 installs to user profile.</span></span> <span data-ttu-id="025ba-117">Ele deve usar uma chave do registro em HKCU como seu caminho de chave.</span><span class="sxs-lookup"><span data-stu-id="025ba-117">It must use a registry key under HKCU as its KeyPath.</span></span> <span data-ttu-id="025ba-118">O caminho keyé nulo no momento.</span><span class="sxs-lookup"><span data-stu-id="025ba-118">The KeyPath is currently NULL.</span></span> | <span data-ttu-id="025ba-119">Component2 tem o conjunto de bits RegistryKeyPath na coluna atributos da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="025ba-119">Component2 has the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="025ba-120">O campo KeyPath deve, portanto, conter uma chave para a coluna Registry da [tabela do registro](registry-table.md) , mas a coluna KeyPath é NULL.</span><span class="sxs-lookup"><span data-stu-id="025ba-120">The KeyPath field must therefore contain a key to the Registry column of the [Registry Table](registry-table.md) but the KeyPath column is Null.</span></span> <span data-ttu-id="025ba-121">Para corrigir esse erro, altere o valor do caminho-chave para uma entrada válida na tabela do registro.</span><span class="sxs-lookup"><span data-stu-id="025ba-121">To fix this error, change the KeyPath value to a valid entry into the Registry table.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="025ba-122">O componente Component3 é instalado no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="025ba-122">Component Component3 installs to user profile.</span></span> <span data-ttu-id="025ba-123">É a chave do registro KeyPath deve estar sob HKCU.</span><span class="sxs-lookup"><span data-stu-id="025ba-123">It's KeyPath registry key must fall under HKCU.</span></span>                                      | <span data-ttu-id="025ba-124">Component3 tem o conjunto de bits RegistryKeyPath na coluna atributos da [tabela de componentes](component-table.md) , mas a raiz da entrada do Registro especificada na coluna raiz da tabela do Registro especifica **HKEY \_ \_ Machine local** em vez de **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="025ba-124">Component3 has the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md) but the root of the registry entry specified in the Root column of the Registry table specifies **HKEY\_LOCAL\_MACHINE** rather than **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="025ba-125">Para corrigir esse erro, use uma entrada de registro válida em **HKEY \_ local \_ Machine** como o caminho de chave para esse componente ou altere o valor na coluna raiz da [tabela de registro](registry-table.md) para-1 ou 1.</span><span class="sxs-lookup"><span data-stu-id="025ba-125">To fix this error, use a valid registry entry under **HKEY\_LOCAL\_MACHINE** as the KeyPath for this component or change the value in the Root column of the [Registry table](registry-table.md) to -1 or 1.</span></span><br/>                                                                  |
| <span data-ttu-id="025ba-126">A entrada do registro KeyPath para o componente Component4 não existe.</span><span class="sxs-lookup"><span data-stu-id="025ba-126">The KeyPath registry entry for component Component4 does not exist.</span></span>                                                                 | <span data-ttu-id="025ba-127">Component4 tem o conjunto de bits RegistryKeyPath na coluna atributos da [tabela de componentes](component-table.md) , mas a entrada na coluna KeyPath não existe na tabela de [registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="025ba-127">Component4 has the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md) but the entry in the KeyPath column does not exist in the [Registry Table](registry-table.md).</span></span> <span data-ttu-id="025ba-128">Para corrigir esse erro, adicione uma entrada para Reg4 à tabela de registro que seja em **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="025ba-128">To fix this error, add an entry for Reg4 to the Registry table that is a under **HKEY\_CURRENT\_USER**.</span></span><br/>                                                                                                                                                                                                                                      |
| <span data-ttu-id="025ba-129">A entrada de registro Reg5 é definida como o caminho de chave para o componente Component5, mas essa entrada de registro não pertence a Component5.</span><span class="sxs-lookup"><span data-stu-id="025ba-129">The Registry Entry Reg5 is set as the KeyPath for component Component5, but that registry entry does not belong to Component5.</span></span>      | <span data-ttu-id="025ba-130">A entrada do registro referenciada na coluna KeyPath do componente foi encontrada e está sob a árvore HKCU, mas a coluna de componente da entrada do registro \_ não se refere ao mesmo componente que a listou como o caminho-chave.</span><span class="sxs-lookup"><span data-stu-id="025ba-130">The Registry entry referenced in the KeyPath column of the component was found and lies under the HKCU tree, but the registry entry's Component\_ column does not refer back to the same component that listed it as the KeyPath.</span></span> <span data-ttu-id="025ba-131">Isso significa que a entrada do Registro usada como o caminho de chave do componente só seria criada quando algum outro componente foi instalado.</span><span class="sxs-lookup"><span data-stu-id="025ba-131">This means that the registry entry used as the KeyPath of the component would only be created when some other component was installed.</span></span> <span data-ttu-id="025ba-132">Para corrigir esse erro, altere o valor do caminho-chave para referir-se a uma entrada do registro que pertence ao componente ou altere a entrada do registro para pertencer ao componente usando-o como um caminho-chave.</span><span class="sxs-lookup"><span data-stu-id="025ba-132">To fix this error change the KeyPath value to refer to a registry entry that belongs to the component, or change the registry entry to belong to the component using it as a KeyPath.</span></span><br/> |



 

<span data-ttu-id="025ba-133">[Tabela de diretórios](directory-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="025ba-133">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="025ba-134">Diretório</span><span class="sxs-lookup"><span data-stu-id="025ba-134">Directory</span></span> | <span data-ttu-id="025ba-135">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="025ba-135">Directory\_Parent</span></span> | <span data-ttu-id="025ba-136">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="025ba-136">DefaultDir</span></span>      |
|-----------|-------------------|-----------------|
| <span data-ttu-id="025ba-137">Dir1</span><span class="sxs-lookup"><span data-stu-id="025ba-137">Dir1</span></span>      |                   | <span data-ttu-id="025ba-138">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="025ba-138">StartMenuFolder</span></span> |
| <span data-ttu-id="025ba-139">Dir2</span><span class="sxs-lookup"><span data-stu-id="025ba-139">Dir2</span></span>      |                   | <span data-ttu-id="025ba-140">DesktopFolder</span><span class="sxs-lookup"><span data-stu-id="025ba-140">DesktopFolder</span></span>   |
| <span data-ttu-id="025ba-141">Dir3</span><span class="sxs-lookup"><span data-stu-id="025ba-141">Dir3</span></span>      | <span data-ttu-id="025ba-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="025ba-142">Dir3</span></span>              | <span data-ttu-id="025ba-143">AppData</span><span class="sxs-lookup"><span data-stu-id="025ba-143">AppData</span></span>         |
| <span data-ttu-id="025ba-144">Dir4</span><span class="sxs-lookup"><span data-stu-id="025ba-144">Dir4</span></span>      | <span data-ttu-id="025ba-145">Dir3</span><span class="sxs-lookup"><span data-stu-id="025ba-145">Dir3</span></span>              | <span data-ttu-id="025ba-146">SubDir</span><span class="sxs-lookup"><span data-stu-id="025ba-146">SubDir</span></span>          |



 

<span data-ttu-id="025ba-147">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="025ba-147">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="025ba-148">Componente</span><span class="sxs-lookup"><span data-stu-id="025ba-148">Component</span></span>  | <span data-ttu-id="025ba-149">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="025ba-149">Directory\_</span></span> | <span data-ttu-id="025ba-150">Atributos</span><span class="sxs-lookup"><span data-stu-id="025ba-150">Attributes</span></span> | <span data-ttu-id="025ba-151">KeyPath</span><span class="sxs-lookup"><span data-stu-id="025ba-151">KeyPath</span></span> |
|------------|-------------|------------|---------|
| <span data-ttu-id="025ba-152">Component1</span><span class="sxs-lookup"><span data-stu-id="025ba-152">Component1</span></span> | <span data-ttu-id="025ba-153">Dir1</span><span class="sxs-lookup"><span data-stu-id="025ba-153">Dir1</span></span>        | <span data-ttu-id="025ba-154">0</span><span class="sxs-lookup"><span data-stu-id="025ba-154">0</span></span>          | <span data-ttu-id="025ba-155">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="025ba-155">File1</span></span>   |
| <span data-ttu-id="025ba-156">Component2</span><span class="sxs-lookup"><span data-stu-id="025ba-156">Component2</span></span> | <span data-ttu-id="025ba-157">Dir2</span><span class="sxs-lookup"><span data-stu-id="025ba-157">Dir2</span></span>        | <span data-ttu-id="025ba-158">4</span><span class="sxs-lookup"><span data-stu-id="025ba-158">4</span></span>          |         |
| <span data-ttu-id="025ba-159">Component3</span><span class="sxs-lookup"><span data-stu-id="025ba-159">Component3</span></span> | <span data-ttu-id="025ba-160">Dir3</span><span class="sxs-lookup"><span data-stu-id="025ba-160">Dir3</span></span>        | <span data-ttu-id="025ba-161">4</span><span class="sxs-lookup"><span data-stu-id="025ba-161">4</span></span>          | <span data-ttu-id="025ba-162">Reg3</span><span class="sxs-lookup"><span data-stu-id="025ba-162">Reg3</span></span>    |
| <span data-ttu-id="025ba-163">Component4</span><span class="sxs-lookup"><span data-stu-id="025ba-163">Component4</span></span> | <span data-ttu-id="025ba-164">Dir4</span><span class="sxs-lookup"><span data-stu-id="025ba-164">Dir4</span></span>        | <span data-ttu-id="025ba-165">4</span><span class="sxs-lookup"><span data-stu-id="025ba-165">4</span></span>          | <span data-ttu-id="025ba-166">Reg4</span><span class="sxs-lookup"><span data-stu-id="025ba-166">Reg4</span></span>    |
| <span data-ttu-id="025ba-167">Component5</span><span class="sxs-lookup"><span data-stu-id="025ba-167">Component5</span></span> | <span data-ttu-id="025ba-168">Dir5</span><span class="sxs-lookup"><span data-stu-id="025ba-168">Dir5</span></span>        | <span data-ttu-id="025ba-169">4</span><span class="sxs-lookup"><span data-stu-id="025ba-169">4</span></span>          | <span data-ttu-id="025ba-170">Reg5</span><span class="sxs-lookup"><span data-stu-id="025ba-170">Reg5</span></span>    |



 

<span data-ttu-id="025ba-171">[Tabela do registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="025ba-171">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="025ba-172">Registro</span><span class="sxs-lookup"><span data-stu-id="025ba-172">Registry</span></span> | <span data-ttu-id="025ba-173">Root</span><span class="sxs-lookup"><span data-stu-id="025ba-173">Root</span></span> | <span data-ttu-id="025ba-174">Valor</span><span class="sxs-lookup"><span data-stu-id="025ba-174">Value</span></span> | <span data-ttu-id="025ba-175">Componente\_</span><span class="sxs-lookup"><span data-stu-id="025ba-175">Component\_</span></span> |
|----------|------|-------|-------------|
| <span data-ttu-id="025ba-176">Reg3</span><span class="sxs-lookup"><span data-stu-id="025ba-176">Reg3</span></span>     | <span data-ttu-id="025ba-177">2</span><span class="sxs-lookup"><span data-stu-id="025ba-177">2</span></span>    |       | <span data-ttu-id="025ba-178">Component3</span><span class="sxs-lookup"><span data-stu-id="025ba-178">Component3</span></span>  |
| <span data-ttu-id="025ba-179">Reg5</span><span class="sxs-lookup"><span data-stu-id="025ba-179">Reg5</span></span>     | <span data-ttu-id="025ba-180">0</span><span class="sxs-lookup"><span data-stu-id="025ba-180">0</span></span>    |       | <span data-ttu-id="025ba-181">Component4</span><span class="sxs-lookup"><span data-stu-id="025ba-181">Component4</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="025ba-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="025ba-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="025ba-183">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="025ba-183">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




