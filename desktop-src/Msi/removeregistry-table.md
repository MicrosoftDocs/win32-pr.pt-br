---
description: A tabela RemoveRegistry contém as informações de registro que o aplicativo precisa excluir do registro do sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Tabela RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921965"
---
# <a name="removeregistry-table"></a><span data-ttu-id="bd0d8-103">Tabela RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="bd0d8-103">RemoveRegistry Table</span></span>

<span data-ttu-id="bd0d8-104">A tabela RemoveRegistry contém as informações de registro que o aplicativo precisa excluir do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-104">The RemoveRegistry table contains the registry information the application needs to delete from the system registry.</span></span>

<span data-ttu-id="bd0d8-105">A tabela RemoveRegistry tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-105">The RemoveRegistry table has the following columns.</span></span>



| <span data-ttu-id="bd0d8-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="bd0d8-106">Column</span></span>         | <span data-ttu-id="bd0d8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd0d8-107">Type</span></span>                         | <span data-ttu-id="bd0d8-108">Chave</span><span class="sxs-lookup"><span data-stu-id="bd0d8-108">Key</span></span> | <span data-ttu-id="bd0d8-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="bd0d8-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="bd0d8-110">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="bd0d8-110">RemoveRegistry</span></span> | [<span data-ttu-id="bd0d8-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="bd0d8-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="bd0d8-112">S</span><span class="sxs-lookup"><span data-stu-id="bd0d8-112">Y</span></span>   | <span data-ttu-id="bd0d8-113">N</span><span class="sxs-lookup"><span data-stu-id="bd0d8-113">N</span></span>        |
| <span data-ttu-id="bd0d8-114">Root</span><span class="sxs-lookup"><span data-stu-id="bd0d8-114">Root</span></span>           | [<span data-ttu-id="bd0d8-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="bd0d8-115">Integer</span></span>](integer.md)       | <span data-ttu-id="bd0d8-116">N</span><span class="sxs-lookup"><span data-stu-id="bd0d8-116">N</span></span>   | <span data-ttu-id="bd0d8-117">N</span><span class="sxs-lookup"><span data-stu-id="bd0d8-117">N</span></span>        |
| <span data-ttu-id="bd0d8-118">Chave</span><span class="sxs-lookup"><span data-stu-id="bd0d8-118">Key</span></span>            | [<span data-ttu-id="bd0d8-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="bd0d8-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="bd0d8-120">N</span><span class="sxs-lookup"><span data-stu-id="bd0d8-120">N</span></span>   | <span data-ttu-id="bd0d8-121">N</span><span class="sxs-lookup"><span data-stu-id="bd0d8-121">N</span></span>        |
| <span data-ttu-id="bd0d8-122">Nome</span><span class="sxs-lookup"><span data-stu-id="bd0d8-122">Name</span></span>           | [<span data-ttu-id="bd0d8-123">Binário</span><span class="sxs-lookup"><span data-stu-id="bd0d8-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="bd0d8-124">N</span><span class="sxs-lookup"><span data-stu-id="bd0d8-124">N</span></span>   | <span data-ttu-id="bd0d8-125">S</span><span class="sxs-lookup"><span data-stu-id="bd0d8-125">Y</span></span>        |
| <span data-ttu-id="bd0d8-126">Componente\_</span><span class="sxs-lookup"><span data-stu-id="bd0d8-126">Component\_</span></span>    | [<span data-ttu-id="bd0d8-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="bd0d8-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="bd0d8-128">N</span><span class="sxs-lookup"><span data-stu-id="bd0d8-128">N</span></span>   | <span data-ttu-id="bd0d8-129">N</span><span class="sxs-lookup"><span data-stu-id="bd0d8-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bd0d8-130">Colunas</span><span class="sxs-lookup"><span data-stu-id="bd0d8-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bd0d8-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="bd0d8-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span></span>
</dt> <dd>

<span data-ttu-id="bd0d8-132">A chave para esta tabela.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-132">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="bd0d8-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Básica</span><span class="sxs-lookup"><span data-stu-id="bd0d8-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="bd0d8-134">A chave raiz predefinida para o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-134">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="bd0d8-135">Constante</span><span class="sxs-lookup"><span data-stu-id="bd0d8-135">Constant</span></span>                          | <span data-ttu-id="bd0d8-136">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="bd0d8-136">Hexadecimal</span></span> | <span data-ttu-id="bd0d8-137">Decimal</span><span class="sxs-lookup"><span data-stu-id="bd0d8-137">Decimal</span></span> | <span data-ttu-id="bd0d8-138">Chave raiz</span><span class="sxs-lookup"><span data-stu-id="bd0d8-138">Root key</span></span>                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0d8-139">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="bd0d8-139">(none)</span></span>                            | <span data-ttu-id="bd0d8-140">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="bd0d8-140">\- 0x001</span></span>    | <span data-ttu-id="bd0d8-141">-1</span><span class="sxs-lookup"><span data-stu-id="bd0d8-141">-1</span></span>      | <span data-ttu-id="bd0d8-142">**HKEY \_ O instalador do \_ usuário atual** define essa chave enquanto faz uma instalação por usuário.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-142">**HKEY\_CURRENT\_USER** Installer sets this key while doing a per-user installation.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="bd0d8-143">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="bd0d8-143">(none)</span></span>                            | <span data-ttu-id="bd0d8-144">-0x001</span><span class="sxs-lookup"><span data-stu-id="bd0d8-144">-0x001</span></span>      | <span data-ttu-id="bd0d8-145">-1</span><span class="sxs-lookup"><span data-stu-id="bd0d8-145">-1</span></span>      | <span data-ttu-id="bd0d8-146">**HKEY \_ O instalador do \_ computador local** define essa chave enquanto faz uma instalação de todos os usuários com [**AllUsers**](allusers.md) definido como 1.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-146">**HKEY\_LOCAL\_MACHINE** Installer sets this key while doing an all-users installation with [**ALLUSERS**](allusers.md) set to 1.</span></span><br/>                                                                       |
| <span data-ttu-id="bd0d8-147">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="bd0d8-147">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="bd0d8-148">0x000</span><span class="sxs-lookup"><span data-stu-id="bd0d8-148">0x000</span></span>       | <span data-ttu-id="bd0d8-149">0</span><span class="sxs-lookup"><span data-stu-id="bd0d8-149">0</span></span>       | <span data-ttu-id="bd0d8-150">**HKEY \_ \_Raiz de classes** o instalador remove o valor do hive de **\\ \\ classes de software HKCU** durante instalações no [contexto de instalação](installation-context.md)por usuário e por máquina.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-150">**HKEY\_CLASSES\_ROOT** The installer removes the value from the **HKCU\\Software\\Classes** hive during installations in the per-user and per-machine [installation context](installation-context.md).</span></span><br/> |
| <span data-ttu-id="bd0d8-151">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="bd0d8-151">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="bd0d8-152">0x001</span><span class="sxs-lookup"><span data-stu-id="bd0d8-152">0x001</span></span>       | <span data-ttu-id="bd0d8-153">1</span><span class="sxs-lookup"><span data-stu-id="bd0d8-153">1</span></span>       | <span data-ttu-id="bd0d8-154">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="bd0d8-154">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="bd0d8-155">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="bd0d8-155">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="bd0d8-156">0x002</span><span class="sxs-lookup"><span data-stu-id="bd0d8-156">0x002</span></span>       | <span data-ttu-id="bd0d8-157">2</span><span class="sxs-lookup"><span data-stu-id="bd0d8-157">2</span></span>       | <span data-ttu-id="bd0d8-158">**\_máquina local \_ HKEY**</span><span class="sxs-lookup"><span data-stu-id="bd0d8-158">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="bd0d8-159">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="bd0d8-159">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="bd0d8-160">0x003</span><span class="sxs-lookup"><span data-stu-id="bd0d8-160">0x003</span></span>       | <span data-ttu-id="bd0d8-161">3</span><span class="sxs-lookup"><span data-stu-id="bd0d8-161">3</span></span>       | <span data-ttu-id="bd0d8-162">**usuários de HKEY \_**</span><span class="sxs-lookup"><span data-stu-id="bd0d8-162">**HKEY\_USERS**</span></span>                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="bd0d8-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves</span><span class="sxs-lookup"><span data-stu-id="bd0d8-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="bd0d8-164">A chave localizável para o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-164">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="bd0d8-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="bd0d8-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="bd0d8-166">O nome do valor do registro localizável.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-166">The localizable registry value name.</span></span>

<span data-ttu-id="bd0d8-167">A cadeia de caracteres a seguir na coluna Name tem um significado especial.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-167">The following string in the Name column has special significance.</span></span>



| <span data-ttu-id="bd0d8-168">String</span><span class="sxs-lookup"><span data-stu-id="bd0d8-168">String</span></span> | <span data-ttu-id="bd0d8-169">Significado</span><span class="sxs-lookup"><span data-stu-id="bd0d8-169">Meaning</span></span>                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0d8-170">"-"</span><span class="sxs-lookup"><span data-stu-id="bd0d8-170">"-"</span></span>    | <span data-ttu-id="bd0d8-171">A chave deve ser excluída, se presente, com todos os seus valores e subchaves, quando o componente é instalado.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-171">The key is to be deleted, if present, with all of its values and subkeys, when the component is installed.</span></span> |



 

<span data-ttu-id="bd0d8-172">Observe que a [tabela de registro](registry-table.md) deve ser usada para criar ou remover uma chave do registro quando o componente é removido.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-172">Note that the [Registry table](registry-table.md) should be used to create or remove a registry key when the component is removed.</span></span>

</dd> <dt>

<span data-ttu-id="bd0d8-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="bd0d8-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="bd0d8-174">Chave externa na primeira coluna da tabela de [componentes](component-table.md) que faz referência ao componente que controla a exclusão do valor do registro.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-174">External key into the first column of the [Component table](component-table.md) referencing the component that controls the deletion of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd0d8-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd0d8-175">Remarks</span></span>

<span data-ttu-id="bd0d8-176">As informações do registro são excluídas do registro do sistema quando o componente correspondente foi selecionado para ser instalado localmente ou executado da origem.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-176">The registry information is deleted from the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="bd0d8-177">Essa tabela é referida quando a [ação RemoveRegistryValues](removeregistryvalues-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="bd0d8-177">This table is referred to when the [RemoveRegistryValues action](removeregistryvalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="bd0d8-178">Validação</span><span class="sxs-lookup"><span data-stu-id="bd0d8-178">Validation</span></span>

<dl>

[<span data-ttu-id="bd0d8-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="bd0d8-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="bd0d8-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="bd0d8-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="bd0d8-181">ICE32</span><span class="sxs-lookup"><span data-stu-id="bd0d8-181">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="bd0d8-182">ICE46</span><span class="sxs-lookup"><span data-stu-id="bd0d8-182">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="bd0d8-183">ICE69</span><span class="sxs-lookup"><span data-stu-id="bd0d8-183">ICE69</span></span>](ice69.md)  
</dl>

 

 




