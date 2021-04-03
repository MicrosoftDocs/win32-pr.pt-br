---
description: O ICE43 valida que os atalhos que não fazem referência a um recurso como seu destino (atalhos não anunciados) estão em componentes que têm uma entrada de Registro HKCU como seu caminho de chave.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9df4a6051557fca3e185f56ca3ad7978c2c0b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091731"
---
# <a name="ice43"></a><span data-ttu-id="a4159-103">ICE43</span><span class="sxs-lookup"><span data-stu-id="a4159-103">ICE43</span></span>

<span data-ttu-id="a4159-104">O ICE43 valida que os atalhos que não fazem referência a um recurso como seu destino (atalhos não anunciados) estão em componentes que têm uma entrada de Registro HKCU como seu caminho de chave.</span><span class="sxs-lookup"><span data-stu-id="a4159-104">ICE43 validates that shortcuts that do not reference a feature as their Target (non-advertised shortcuts) are in components having a HKCU registry entry as their key path.</span></span>

## <a name="result"></a><span data-ttu-id="a4159-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="a4159-105">Result</span></span>

<span data-ttu-id="a4159-106">ICE43 posta uma mensagem de erro se um atalho não anunciado estiver em um componente que não tem uma entrada de Registro HKCU como seu caminho de chave.</span><span class="sxs-lookup"><span data-stu-id="a4159-106">ICE43 posts an error message if a non-advertised shortcut is in a component that does not have a HKCU registry entry as its key path.</span></span>

## <a name="example"></a><span data-ttu-id="a4159-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a4159-107">Example</span></span>

<span data-ttu-id="a4159-108">ICE43 relataria os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="a4159-108">ICE43 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="a4159-109">Erro de ICE43</span><span class="sxs-lookup"><span data-stu-id="a4159-109">ICE43 error</span></span>                                                                                                                             | <span data-ttu-id="a4159-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4159-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4159-111">O componente Component1 tem atalhos não anunciados.</span><span class="sxs-lookup"><span data-stu-id="a4159-111">Component Component1 has non-advertised shortcuts.</span></span> <span data-ttu-id="a4159-112">Ele deve usar uma chave do registro em HKCU como seu caminho Key, não um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a4159-112">It must use a registry key under HKCU as its KeyPath, not a file.</span></span>                    | <span data-ttu-id="a4159-113">A coluna Attributes de Component1 é 0, o que significa que o componente usa um arquivo como seu caminho KeyPath.</span><span class="sxs-lookup"><span data-stu-id="a4159-113">The attributes column of Component1 is 0, meaning that the component uses a file as its KeyPath.</span></span> <span data-ttu-id="a4159-114">Isso faz com que atalhos não anunciados neste componente sejam instalados somente para o primeiro usuário no computador.</span><span class="sxs-lookup"><span data-stu-id="a4159-114">This causes non-advertised shortcuts in this component to be installed for the first user on the computer ONLY.</span></span> <span data-ttu-id="a4159-115">Os usuários que instalarem o componente mais tarde não verão os atalhos porque o componente aparece para o instalador já existente no computador.</span><span class="sxs-lookup"><span data-stu-id="a4159-115">Users who install the component later do not see the shortcuts because the component appear to the installer as already existing on the computer.</span></span> <span data-ttu-id="a4159-116">Para corrigir esse erro, defina o bit RegistryKeyPath dos atributos para alternar o componente para uma entrada de registro e, em seguida, altere o valor de caminho Keypara uma entrada válida na tabela do registro.</span><span class="sxs-lookup"><span data-stu-id="a4159-116">To fix this error, set the RegistryKeyPath bit of the attributes to switch the Component to a Registry entry, then change the KeyPath value to a valid entry in the Registry table.</span></span><br/> |
| <span data-ttu-id="a4159-117">O componente Component2 tem atalhos não anunciados.</span><span class="sxs-lookup"><span data-stu-id="a4159-117">Component Component2 has non-advertised shortcuts.</span></span> <span data-ttu-id="a4159-118">Ele deve usar uma chave do registro em HKCU como seu caminho de chave.</span><span class="sxs-lookup"><span data-stu-id="a4159-118">It must use a registry key under HKCU as its KeyPath.</span></span> <span data-ttu-id="a4159-119">O caminho keyé nulo no momento.</span><span class="sxs-lookup"><span data-stu-id="a4159-119">The KeyPath is currently null.</span></span> | <span data-ttu-id="a4159-120">A coluna atributos está definida para usar o registro, mas o caminho keyé nulo.</span><span class="sxs-lookup"><span data-stu-id="a4159-120">The Attributes column is set to use the registry, but the KeyPath is null.</span></span> <span data-ttu-id="a4159-121">O caminho de chave deve se referir a uma entrada na tabela do registro.</span><span class="sxs-lookup"><span data-stu-id="a4159-121">The KeyPath must refer to an entry in the Registry Table.</span></span> <span data-ttu-id="a4159-122">Para corrigir esse erro, altere o valor do caminho-chave para uma entrada válida na tabela do registro.</span><span class="sxs-lookup"><span data-stu-id="a4159-122">To fix this error, change the KeyPath value to a valid entry in the Registry table.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a4159-123">O componente Component3 tem atalhos não anunciados.</span><span class="sxs-lookup"><span data-stu-id="a4159-123">Component Component3 has non-advertised shortcuts.</span></span> <span data-ttu-id="a4159-124">Sua chave do registro KeyPath deve estar sob HKCU.</span><span class="sxs-lookup"><span data-stu-id="a4159-124">Its KeyPath registry key must fall under HKCU.</span></span>                                       | <span data-ttu-id="a4159-125">A coluna atributos é definida para usar o registro, mas a entrada de registro referenciada não está sob HKCU.</span><span class="sxs-lookup"><span data-stu-id="a4159-125">The Attributes column is set to use the registry, but the referenced registry entry is not under HKCU.</span></span> <span data-ttu-id="a4159-126">Para corrigir esse erro, alterne para uma entrada de registro diferente como o caminho de chave para esse componente ou altere o valor raiz da entrada do registro para-1 ou 1.</span><span class="sxs-lookup"><span data-stu-id="a4159-126">To fix this error, either switch to a different registry entry as the KeyPath for this component, or change the Root value of the Registry entry to either -1 or 1.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a4159-127">A entrada do registro KeyPath para o componente Component4 não existe.</span><span class="sxs-lookup"><span data-stu-id="a4159-127">The KeyPath registry entry for component Component4 does not exist.</span></span>                                                                     | <span data-ttu-id="a4159-128">A entrada do registro referenciada na coluna KeyPath do componente não está na tabela do registro.</span><span class="sxs-lookup"><span data-stu-id="a4159-128">The Registry entry referenced in the KeyPath column of the component is not in the Registry Table.</span></span> <span data-ttu-id="a4159-129">Para corrigir esse erro, crie uma entrada.</span><span class="sxs-lookup"><span data-stu-id="a4159-129">To fix this error, create an entry.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a4159-130">A entrada de registro Reg5 é definida como o caminho de chave para o componente Component5, mas essa entrada de registro não pertence a Component5.</span><span class="sxs-lookup"><span data-stu-id="a4159-130">The Registry Entry Reg5 is set as the KeyPath for component Component5, but that registry entry does not belong to Component5.</span></span>          | <span data-ttu-id="a4159-131">Há uma entrada de registro referenciada na coluna KeyPath do componente que está sob a árvore HKCU, mas a coluna de componente da entrada do registro \_ não se refere ao mesmo componente que a listou como o caminho-chave.</span><span class="sxs-lookup"><span data-stu-id="a4159-131">There is a Registry entry referenced in the KeyPath column of the component that lies under the HKCU tree, but the registry entry's Component\_ column does not refer back to the same component that listed it as the KeyPath.</span></span> <span data-ttu-id="a4159-132">Isso significa que a entrada do Registro usada como o caminho de chave do componente só será criada se algum outro componente tiver sido instalado.</span><span class="sxs-lookup"><span data-stu-id="a4159-132">This means that the registry entry used as the KeyPath of the component is only created if some other component was installed.</span></span> <span data-ttu-id="a4159-133">Para corrigir esse erro, altere o valor do caminho-chave para referir-se a uma entrada do registro que pertence ao componente ou altere a entrada do registro para pertencer ao componente usando-o como um caminho-chave.</span><span class="sxs-lookup"><span data-stu-id="a4159-133">To fix this error, change the KeyPath value to refer to a registry entry that belongs to the component or change the registry entry to belong to the component using it as a KeyPath.</span></span><br/>   |



 

<span data-ttu-id="a4159-134">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="a4159-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a4159-135">Componente</span><span class="sxs-lookup"><span data-stu-id="a4159-135">Component</span></span>  | <span data-ttu-id="a4159-136">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4159-136">Attributes</span></span> | <span data-ttu-id="a4159-137">KeyPath</span><span class="sxs-lookup"><span data-stu-id="a4159-137">KeyPath</span></span> |
|------------|------------|---------|
| <span data-ttu-id="a4159-138">Component1</span><span class="sxs-lookup"><span data-stu-id="a4159-138">Component1</span></span> | <span data-ttu-id="a4159-139">0</span><span class="sxs-lookup"><span data-stu-id="a4159-139">0</span></span>          | <span data-ttu-id="a4159-140">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="a4159-140">File1</span></span>   |
| <span data-ttu-id="a4159-141">Component2</span><span class="sxs-lookup"><span data-stu-id="a4159-141">Component2</span></span> | <span data-ttu-id="a4159-142">4</span><span class="sxs-lookup"><span data-stu-id="a4159-142">4</span></span>          |         |
| <span data-ttu-id="a4159-143">Component3</span><span class="sxs-lookup"><span data-stu-id="a4159-143">Component3</span></span> | <span data-ttu-id="a4159-144">4</span><span class="sxs-lookup"><span data-stu-id="a4159-144">4</span></span>          | <span data-ttu-id="a4159-145">Reg3</span><span class="sxs-lookup"><span data-stu-id="a4159-145">Reg3</span></span>    |
| <span data-ttu-id="a4159-146">Component4</span><span class="sxs-lookup"><span data-stu-id="a4159-146">Component4</span></span> | <span data-ttu-id="a4159-147">4</span><span class="sxs-lookup"><span data-stu-id="a4159-147">4</span></span>          | <span data-ttu-id="a4159-148">Reg4</span><span class="sxs-lookup"><span data-stu-id="a4159-148">Reg4</span></span>    |
| <span data-ttu-id="a4159-149">Component5</span><span class="sxs-lookup"><span data-stu-id="a4159-149">Component5</span></span> | <span data-ttu-id="a4159-150">4</span><span class="sxs-lookup"><span data-stu-id="a4159-150">4</span></span>          | <span data-ttu-id="a4159-151">Reg5</span><span class="sxs-lookup"><span data-stu-id="a4159-151">Reg5</span></span>    |



 

<span data-ttu-id="a4159-152">[Tabela do registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="a4159-152">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="a4159-153">Registro</span><span class="sxs-lookup"><span data-stu-id="a4159-153">Registry</span></span> | <span data-ttu-id="a4159-154">Root</span><span class="sxs-lookup"><span data-stu-id="a4159-154">Root</span></span> | <span data-ttu-id="a4159-155">Valor</span><span class="sxs-lookup"><span data-stu-id="a4159-155">Value</span></span> | <span data-ttu-id="a4159-156">Componente\_</span><span class="sxs-lookup"><span data-stu-id="a4159-156">Component\_</span></span> |
|----------|------|-------|-------------|
| <span data-ttu-id="a4159-157">Reg3</span><span class="sxs-lookup"><span data-stu-id="a4159-157">Reg3</span></span>     | <span data-ttu-id="a4159-158">2</span><span class="sxs-lookup"><span data-stu-id="a4159-158">2</span></span>    |       | <span data-ttu-id="a4159-159">Component3</span><span class="sxs-lookup"><span data-stu-id="a4159-159">Component3</span></span>  |
| <span data-ttu-id="a4159-160">Reg5</span><span class="sxs-lookup"><span data-stu-id="a4159-160">Reg5</span></span>     | <span data-ttu-id="a4159-161">0</span><span class="sxs-lookup"><span data-stu-id="a4159-161">0</span></span>    |       | <span data-ttu-id="a4159-162">Component4</span><span class="sxs-lookup"><span data-stu-id="a4159-162">Component4</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="a4159-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4159-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4159-164">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="a4159-164">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




