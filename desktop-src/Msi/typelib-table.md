---
description: A tabela TypeLib contém as informações que precisam ser colocadas no registro do registro de bibliotecas de tipos.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Tabela TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747317"
---
# <a name="typelib-table"></a><span data-ttu-id="62486-103">Tabela TypeLib</span><span class="sxs-lookup"><span data-stu-id="62486-103">TypeLib Table</span></span>

<span data-ttu-id="62486-104">A tabela TypeLib contém as informações que precisam ser colocadas no registro do registro de bibliotecas de tipos.</span><span class="sxs-lookup"><span data-stu-id="62486-104">The TypeLib table contains the information that needs to be placed in the registry registration of type libraries.</span></span>

<span data-ttu-id="62486-105">A tabela TypeLib tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="62486-105">The TypeLib table has the following columns.</span></span>



| <span data-ttu-id="62486-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="62486-106">Column</span></span>      | <span data-ttu-id="62486-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="62486-107">Type</span></span>                               | <span data-ttu-id="62486-108">Chave</span><span class="sxs-lookup"><span data-stu-id="62486-108">Key</span></span> | <span data-ttu-id="62486-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="62486-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="62486-110">LibID</span><span class="sxs-lookup"><span data-stu-id="62486-110">LibID</span></span>       | [<span data-ttu-id="62486-111">GUID</span><span class="sxs-lookup"><span data-stu-id="62486-111">GUID</span></span>](guid.md)                   | <span data-ttu-id="62486-112">S</span><span class="sxs-lookup"><span data-stu-id="62486-112">Y</span></span>   | <span data-ttu-id="62486-113">N</span><span class="sxs-lookup"><span data-stu-id="62486-113">N</span></span>        |
| <span data-ttu-id="62486-114">Idioma</span><span class="sxs-lookup"><span data-stu-id="62486-114">Language</span></span>    | [<span data-ttu-id="62486-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="62486-115">Integer</span></span>](integer.md)             | <span data-ttu-id="62486-116">S</span><span class="sxs-lookup"><span data-stu-id="62486-116">Y</span></span>   | <span data-ttu-id="62486-117">N</span><span class="sxs-lookup"><span data-stu-id="62486-117">N</span></span>        |
| <span data-ttu-id="62486-118">Componente\_</span><span class="sxs-lookup"><span data-stu-id="62486-118">Component\_</span></span> | [<span data-ttu-id="62486-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="62486-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="62486-120">S</span><span class="sxs-lookup"><span data-stu-id="62486-120">Y</span></span>   | <span data-ttu-id="62486-121">N</span><span class="sxs-lookup"><span data-stu-id="62486-121">N</span></span>        |
| <span data-ttu-id="62486-122">Versão</span><span class="sxs-lookup"><span data-stu-id="62486-122">Version</span></span>     | [<span data-ttu-id="62486-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="62486-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="62486-124">N</span><span class="sxs-lookup"><span data-stu-id="62486-124">N</span></span>   | <span data-ttu-id="62486-125">S</span><span class="sxs-lookup"><span data-stu-id="62486-125">Y</span></span>        |
| <span data-ttu-id="62486-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="62486-126">Description</span></span> | [<span data-ttu-id="62486-127">Text</span><span class="sxs-lookup"><span data-stu-id="62486-127">Text</span></span>](text.md)                   | <span data-ttu-id="62486-128">N</span><span class="sxs-lookup"><span data-stu-id="62486-128">N</span></span>   | <span data-ttu-id="62486-129">S</span><span class="sxs-lookup"><span data-stu-id="62486-129">Y</span></span>        |
| <span data-ttu-id="62486-130">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="62486-130">Directory\_</span></span> | [<span data-ttu-id="62486-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="62486-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="62486-132">N</span><span class="sxs-lookup"><span data-stu-id="62486-132">N</span></span>   | <span data-ttu-id="62486-133">S</span><span class="sxs-lookup"><span data-stu-id="62486-133">Y</span></span>        |
| <span data-ttu-id="62486-134">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="62486-134">Feature\_</span></span>   | [<span data-ttu-id="62486-135">Identificador</span><span class="sxs-lookup"><span data-stu-id="62486-135">Identifier</span></span>](identifier.md)       | <span data-ttu-id="62486-136">N</span><span class="sxs-lookup"><span data-stu-id="62486-136">N</span></span>   | <span data-ttu-id="62486-137">N</span><span class="sxs-lookup"><span data-stu-id="62486-137">N</span></span>        |
| <span data-ttu-id="62486-138">Custo</span><span class="sxs-lookup"><span data-stu-id="62486-138">Cost</span></span>        | [<span data-ttu-id="62486-139">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="62486-139">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="62486-140">N</span><span class="sxs-lookup"><span data-stu-id="62486-140">N</span></span>   | <span data-ttu-id="62486-141">S</span><span class="sxs-lookup"><span data-stu-id="62486-141">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="62486-142">Colunas</span><span class="sxs-lookup"><span data-stu-id="62486-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="62486-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span><span class="sxs-lookup"><span data-stu-id="62486-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span></span>
</dt> <dd>

<span data-ttu-id="62486-144">O GUID que identifica a biblioteca.</span><span class="sxs-lookup"><span data-stu-id="62486-144">The GUID that identifies the library.</span></span>

</dd> <dt>

<span data-ttu-id="62486-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma</span><span class="sxs-lookup"><span data-stu-id="62486-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="62486-146">O idioma da biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="62486-146">The language of the type library.</span></span> <span data-ttu-id="62486-147">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="62486-147">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="62486-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="62486-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="62486-149">Chave externa na primeira coluna da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="62486-149">External key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="62486-150">Esta coluna identifica o componente pertencente ao recurso \_ cujo arquivo de chave é a biblioteca de tipos que está sendo registrada.</span><span class="sxs-lookup"><span data-stu-id="62486-150">This column identifies the component belonging to Feature\_ whose key file is the type library being registered.</span></span>

</dd> <dt>

<span data-ttu-id="62486-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versão</span><span class="sxs-lookup"><span data-stu-id="62486-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="62486-152">Esta é a versão da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="62486-152">This is the version of the library.</span></span> <span data-ttu-id="62486-153">As versões principal e secundária são codificadas no valor inteiro de quatro bytes.</span><span class="sxs-lookup"><span data-stu-id="62486-153">The major and minor versions are encoded in the four byte integer value.</span></span> <span data-ttu-id="62486-154">A versão secundária está nos oito bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="62486-154">The minor version is in the lower eight bits.</span></span> <span data-ttu-id="62486-155">A versão principal está no meio dos dezesseis bits.</span><span class="sxs-lookup"><span data-stu-id="62486-155">The major version is in the middle sixteen bits.</span></span>

</dd> <dt>

<span data-ttu-id="62486-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="62486-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="62486-157">Uma descrição localizável da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="62486-157">A localizable description of the library.</span></span>

</dd> <dt>

<span data-ttu-id="62486-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_</span><span class="sxs-lookup"><span data-stu-id="62486-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="62486-159">Chave externa na primeira coluna da tabela de [diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="62486-159">External key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="62486-160">Esta coluna identifica o caminho de ajuda para a biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="62486-160">This column identifies the Help path for the type library.</span></span> <span data-ttu-id="62486-161">Esta coluna é ignorada durante o anúncio.</span><span class="sxs-lookup"><span data-stu-id="62486-161">This column is ignored during advertising.</span></span>

</dd> <dt>

<span data-ttu-id="62486-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_</span><span class="sxs-lookup"><span data-stu-id="62486-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="62486-163">Chave externa na primeira coluna da tabela de [recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="62486-163">External key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="62486-164">Esta coluna especifica o recurso que deve ser instalado para que a biblioteca de tipos esteja operacional.</span><span class="sxs-lookup"><span data-stu-id="62486-164">This column specifies the feature that must be installed for the type library to be operational.</span></span>

</dd> <dt>

<span data-ttu-id="62486-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Custo</span><span class="sxs-lookup"><span data-stu-id="62486-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="62486-166">O custo associado ao registro da biblioteca de tipos em bytes.</span><span class="sxs-lookup"><span data-stu-id="62486-166">The cost associated with the registration of the type library in bytes.</span></span> <span data-ttu-id="62486-167">Este deve ser um número não negativo ou nulo.</span><span class="sxs-lookup"><span data-stu-id="62486-167">This must be a non-negative number or null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62486-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="62486-168">Remarks</span></span>

<span data-ttu-id="62486-169">Essa tabela é referida quando a ação [RegisterTypeLibraries](registertypelibraries-action.md) ou a [ação UnregisterTypeLibraries](unregistertypelibraries-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="62486-169">This table is referred to when the [RegisterTypeLibraries action](registertypelibraries-action.md) or the [UnregisterTypeLibraries action](unregistertypelibraries-action.md) is executed.</span></span>

<span data-ttu-id="62486-170">O instalador grava todas as informações de registro da biblioteca de tipos no \_ \_ local do registro da máquina local hKey (HKLM).</span><span class="sxs-lookup"><span data-stu-id="62486-170">The installer writes all type library registration information into the HKEY\_LOCAL\_MACHINE (HKLM) registry location.</span></span> <span data-ttu-id="62486-171">Esse é o caso até mesmo para instalações por usuário.</span><span class="sxs-lookup"><span data-stu-id="62486-171">This is the case even for per-user installations.</span></span> <span data-ttu-id="62486-172">Bibliotecas de tipos não podem ser registradas em locais por usuário (HKCU).</span><span class="sxs-lookup"><span data-stu-id="62486-172">Type libraries cannot be registered in per-user locations (HKCU).</span></span>

<span data-ttu-id="62486-173">Os autores do pacote de instalação são altamente aconselhados em relação ao uso da tabela TypeLib.</span><span class="sxs-lookup"><span data-stu-id="62486-173">Installation package authors are strongly advised against using the TypeLib table.</span></span> <span data-ttu-id="62486-174">Em vez disso, eles devem registrar bibliotecas de tipos usando a tabela de [registro](registry-table.md) .</span><span class="sxs-lookup"><span data-stu-id="62486-174">Instead, they should register type libraries by using the [Registry](registry-table.md) table.</span></span> <span data-ttu-id="62486-175">Os motivos para evitar o auto-registro incluem:</span><span class="sxs-lookup"><span data-stu-id="62486-175">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="62486-176">Se uma instalação que usa a tabela TypeLib falhar e precisar ser revertida, a reversão poderá não restaurar o computador para o mesmo estado que existia antes da reversão.</span><span class="sxs-lookup"><span data-stu-id="62486-176">If an installation using the TypeLib table fails and must be rolled back, the rollback may not restore the computer to the same state that existed prior to the rollback.</span></span> <span data-ttu-id="62486-177">Bibliotecas de tipos registradas antes da reversão não podem ser registradas após a reversão.</span><span class="sxs-lookup"><span data-stu-id="62486-177">Type libraries registered prior to rollback may not be registered after rollback.</span></span>

## <a name="validation"></a><span data-ttu-id="62486-178">Validação</span><span class="sxs-lookup"><span data-stu-id="62486-178">Validation</span></span>

<dl>

[<span data-ttu-id="62486-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="62486-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="62486-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="62486-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="62486-181">ICE19</span><span class="sxs-lookup"><span data-stu-id="62486-181">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="62486-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="62486-182">ICE32</span></span>](ice32.md)  
</dl>

 

 



