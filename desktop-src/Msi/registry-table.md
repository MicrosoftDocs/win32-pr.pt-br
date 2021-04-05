---
description: A tabela de registro contém as informações de registro que o aplicativo precisa definir no registro do sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabela do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921637"
---
# <a name="registry-table"></a><span data-ttu-id="bdf1b-103">Tabela do registro</span><span class="sxs-lookup"><span data-stu-id="bdf1b-103">Registry Table</span></span>

<span data-ttu-id="bdf1b-104">A tabela de registro contém as informações de registro que o aplicativo precisa definir no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-104">The Registry table holds the registry information that the application needs to set in the system registry.</span></span>

<span data-ttu-id="bdf1b-105">A tabela de registro tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-105">The Registry table has the following columns.</span></span>



| <span data-ttu-id="bdf1b-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="bdf1b-106">Column</span></span>      | <span data-ttu-id="bdf1b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="bdf1b-107">Type</span></span>                         | <span data-ttu-id="bdf1b-108">Chave</span><span class="sxs-lookup"><span data-stu-id="bdf1b-108">Key</span></span> | <span data-ttu-id="bdf1b-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="bdf1b-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="bdf1b-110">Registro</span><span class="sxs-lookup"><span data-stu-id="bdf1b-110">Registry</span></span>    | [<span data-ttu-id="bdf1b-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="bdf1b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="bdf1b-112">S</span><span class="sxs-lookup"><span data-stu-id="bdf1b-112">Y</span></span>   | <span data-ttu-id="bdf1b-113">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-113">N</span></span>        |
| <span data-ttu-id="bdf1b-114">Root</span><span class="sxs-lookup"><span data-stu-id="bdf1b-114">Root</span></span>        | [<span data-ttu-id="bdf1b-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="bdf1b-115">Integer</span></span>](integer.md)       | <span data-ttu-id="bdf1b-116">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-116">N</span></span>   | <span data-ttu-id="bdf1b-117">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-117">N</span></span>        |
| <span data-ttu-id="bdf1b-118">Chave</span><span class="sxs-lookup"><span data-stu-id="bdf1b-118">Key</span></span>         | [<span data-ttu-id="bdf1b-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="bdf1b-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="bdf1b-120">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-120">N</span></span>   | <span data-ttu-id="bdf1b-121">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-121">N</span></span>        |
| <span data-ttu-id="bdf1b-122">Nome</span><span class="sxs-lookup"><span data-stu-id="bdf1b-122">Name</span></span>        | [<span data-ttu-id="bdf1b-123">Binário</span><span class="sxs-lookup"><span data-stu-id="bdf1b-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="bdf1b-124">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-124">N</span></span>   | <span data-ttu-id="bdf1b-125">S</span><span class="sxs-lookup"><span data-stu-id="bdf1b-125">Y</span></span>        |
| <span data-ttu-id="bdf1b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bdf1b-126">Value</span></span>       | [<span data-ttu-id="bdf1b-127">Binário</span><span class="sxs-lookup"><span data-stu-id="bdf1b-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="bdf1b-128">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-128">N</span></span>   | <span data-ttu-id="bdf1b-129">S</span><span class="sxs-lookup"><span data-stu-id="bdf1b-129">Y</span></span>        |
| <span data-ttu-id="bdf1b-130">Componente\_</span><span class="sxs-lookup"><span data-stu-id="bdf1b-130">Component\_</span></span> | [<span data-ttu-id="bdf1b-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="bdf1b-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="bdf1b-132">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-132">N</span></span>   | <span data-ttu-id="bdf1b-133">N</span><span class="sxs-lookup"><span data-stu-id="bdf1b-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bdf1b-134">Colunas</span><span class="sxs-lookup"><span data-stu-id="bdf1b-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bdf1b-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry</span><span class="sxs-lookup"><span data-stu-id="bdf1b-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry</span></span>
</dt> <dd>

<span data-ttu-id="bdf1b-136">Chave primária usada para identificar um registro de registro.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-136">Primary key used to identify a registry record.</span></span>

</dd> <dt>

<span data-ttu-id="bdf1b-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Básica</span><span class="sxs-lookup"><span data-stu-id="bdf1b-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="bdf1b-138">A chave raiz predefinida para o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-138">The predefined root key for the registry value.</span></span> <span data-ttu-id="bdf1b-139">Insira um valor de-1 neste campo para tornar a chave raiz dependente do tipo de instalação.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-139">Enter a value of -1 in this field to make the root key dependent on the type of installation.</span></span> <span data-ttu-id="bdf1b-140">Insira um dos outros valores na tabela a seguir para forçar o valor do registro a ser gravado em uma chave de raiz específica.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-140">Enter one of the other values in the following table to force the registry value to be written under a particular root key.</span></span>



| <span data-ttu-id="bdf1b-141">Constante</span><span class="sxs-lookup"><span data-stu-id="bdf1b-141">Constant</span></span>                          | <span data-ttu-id="bdf1b-142">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="bdf1b-142">Hexadecimal</span></span> | <span data-ttu-id="bdf1b-143">Decimal</span><span class="sxs-lookup"><span data-stu-id="bdf1b-143">Decimal</span></span> | <span data-ttu-id="bdf1b-144">Chave raiz</span><span class="sxs-lookup"><span data-stu-id="bdf1b-144">Root key</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf1b-145">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="bdf1b-145">(none)</span></span>                            | <span data-ttu-id="bdf1b-146">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="bdf1b-146">\- 0x001</span></span>    | <span data-ttu-id="bdf1b-147">-1</span><span class="sxs-lookup"><span data-stu-id="bdf1b-147">-1</span></span>      | <span data-ttu-id="bdf1b-148">Se essa for uma instalação por usuário, o valor do registro será gravado em **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-148">If this is a per-user installation, the registry value is written under **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="bdf1b-149">Se essa for uma instalação por máquina, o valor do registro será gravado em **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-149">If this is a per-machine installation, the registry value is written under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="bdf1b-150">Observe que uma instalação por computador é especificada definindo a propriedade [**AllUsers**](allusers.md) como 1.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-150">Note that a per-machine installation is specified by setting the [**ALLUSERS**](allusers.md) property to 1.</span></span><br/>                |
| <span data-ttu-id="bdf1b-151">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="bdf1b-151">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="bdf1b-152">0x000</span><span class="sxs-lookup"><span data-stu-id="bdf1b-152">0x000</span></span>       | <span data-ttu-id="bdf1b-153">0</span><span class="sxs-lookup"><span data-stu-id="bdf1b-153">0</span></span>       | <span data-ttu-id="bdf1b-154">**HKEY \_ \_Raiz de classes** o instalador grava ou remove o valor do hive de **\\ \\ classes de software HKCU** durante a instalação no [contexto de instalação](installation-context.md)por usuário.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-154">**HKEY\_CLASSES\_ROOT** The installer writes or removes the value from the **HKCU\\Software\\Classes** hive during installation in the per-user [installation context](installation-context.md).</span></span><br/> <span data-ttu-id="bdf1b-155">O instalador grava ou remove o valor do hive **de \\ \\ classes de software HKLM** durante instalações por máquina.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-155">The installer writes or removes the value from the **HKLM\\Software\\Classes** hive during per-machine installations.</span></span><br/> |
| <span data-ttu-id="bdf1b-156">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="bdf1b-156">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="bdf1b-157">0x001</span><span class="sxs-lookup"><span data-stu-id="bdf1b-157">0x001</span></span>       | <span data-ttu-id="bdf1b-158">1</span><span class="sxs-lookup"><span data-stu-id="bdf1b-158">1</span></span>       | <span data-ttu-id="bdf1b-159">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="bdf1b-159">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="bdf1b-160">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="bdf1b-160">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="bdf1b-161">0x002</span><span class="sxs-lookup"><span data-stu-id="bdf1b-161">0x002</span></span>       | <span data-ttu-id="bdf1b-162">2</span><span class="sxs-lookup"><span data-stu-id="bdf1b-162">2</span></span>       | <span data-ttu-id="bdf1b-163">**\_máquina local \_ HKEY**</span><span class="sxs-lookup"><span data-stu-id="bdf1b-163">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="bdf1b-164">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="bdf1b-164">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="bdf1b-165">0x003</span><span class="sxs-lookup"><span data-stu-id="bdf1b-165">0x003</span></span>       | <span data-ttu-id="bdf1b-166">3</span><span class="sxs-lookup"><span data-stu-id="bdf1b-166">3</span></span>       | <span data-ttu-id="bdf1b-167">**usuários de HKEY \_**</span><span class="sxs-lookup"><span data-stu-id="bdf1b-167">**HKEY\_USERS**</span></span>                                                                                                                                                                                                                                                                                                                              |



 

<span data-ttu-id="bdf1b-168">Observe que é recomendável que as entradas do registro gravadas no hive **HKCU** façam referência a um componente com o conjunto de bits RegistryKeyPath na coluna Attributes da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-168">Note that it is recommended that registry entries written to the **HKCU** hive reference a component having the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="bdf1b-169">Isso garante que o instalador grave as entradas de Registro necessárias quando houver vários usuários no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-169">This ensures that the installer writes the necessary registry entries when there are multiple users on the same computer.</span></span>

</dd> <dt>

<span data-ttu-id="bdf1b-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves</span><span class="sxs-lookup"><span data-stu-id="bdf1b-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="bdf1b-171">A chave localizável para o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-171">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="bdf1b-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="bdf1b-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="bdf1b-173">Esta coluna contém o nome do valor do registro (localizável).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-173">This column contains the registry value name (localizable).</span></span> <span data-ttu-id="bdf1b-174">Se isso for nulo, os dados inseridos na coluna valor serão gravados na chave do registro padrão.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-174">If this is Null, then the data entered into the Value column are written to the default registry key.</span></span>

<span data-ttu-id="bdf1b-175">Se a coluna valor for nula, as cadeias de caracteres mostradas na tabela a seguir na coluna nome terão significado especial.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-175">If the Value column is Null, then the strings shown in the following table in the Name column have special significance.</span></span>



| <span data-ttu-id="bdf1b-176">String</span><span class="sxs-lookup"><span data-stu-id="bdf1b-176">String</span></span> | <span data-ttu-id="bdf1b-177">Significado</span><span class="sxs-lookup"><span data-stu-id="bdf1b-177">Meaning</span></span>                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | <span data-ttu-id="bdf1b-178">A chave deve ser criada, se ausente, quando o componente é instalado.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-178">The key is to be created, if absent, when the component is installed.</span></span>                                                                                                                            |
| \-     | <span data-ttu-id="bdf1b-179">A chave deve ser excluída, se estiver presente, com todos os seus valores e subchaves quando o componente for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-179">The key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span>                                                                                     |
| \*     | <span data-ttu-id="bdf1b-180">A chave deve ser criada, se ausente, quando o componente é instalado.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-180">The key is to be created, if absent, when the component is installed.</span></span> <span data-ttu-id="bdf1b-181">Além disso, a chave deve ser excluída, se estiver presente, com todos os seus valores e subchaves, quando o componente for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-181">Additionally, the key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span> |



 

<span data-ttu-id="bdf1b-182">Observe que a [tabela RemoveRegistry](removeregistry-table.md) deve ser usada se uma chave do registro instalada for excluída, com seus valores e subchaves, quando o componente for instalado.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-182">Note that the [RemoveRegistry table](removeregistry-table.md) must be used if an installed registry key is to be deleted, with its values and subkeys, when the component is installed.</span></span>

</dd> <dt>

<span data-ttu-id="bdf1b-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="bdf1b-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="bdf1b-184">Esta coluna é o valor de registro localizável.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-184">This column is the localizable registry value.</span></span> <span data-ttu-id="bdf1b-185">O campo está [formatado](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-185">The field is [Formatted](formatted.md).</span></span> <span data-ttu-id="bdf1b-186">Se o valor for anexado a um dos seguintes prefixos (ou seja \# % , *valor*), o valor será interpretado conforme descrito na tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-186">If the value is attached to one of the following prefixes (i.e. \#%*value*) then the value is interpreted as described in the table.</span></span> <span data-ttu-id="bdf1b-187">Observe que cada prefixo começa com um sinal numérico ( \# ).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-187">Note that each prefix begins with a number sign (\#).</span></span> <span data-ttu-id="bdf1b-188">Se o valor começar com dois ou mais sinais numéricos consecutivos ( \# ), o primeiro \# será ignorado e o valor será interpretado e armazenado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-188">If the value begins with two or more consecutive number signs (\#), the first \# is ignored and value is interpreted and stored as a string.</span></span>



| <span data-ttu-id="bdf1b-189">Prefixo</span><span class="sxs-lookup"><span data-stu-id="bdf1b-189">Prefix</span></span> | <span data-ttu-id="bdf1b-190">Significado</span><span class="sxs-lookup"><span data-stu-id="bdf1b-190">Meaning</span></span>                                                                        |
|--------|--------------------------------------------------------------------------------|
| <span data-ttu-id="bdf1b-191">\#w.x.y.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-191">\#x</span></span>    | <span data-ttu-id="bdf1b-192">O valor é interpretado e armazenado como um valor hexadecimal (REG \_ Binary).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-192">The value is interpreted and stored as a hexadecimal value (REG\_BINARY).</span></span>      |
| \#%    | <span data-ttu-id="bdf1b-193">O valor é interpretado e armazenado como uma cadeia de caracteres expansível (REG \_ Expand \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-193">The value is interpreted and stored as an expandable string (REG\_EXPAND\_SZ).</span></span> |
| \#     | <span data-ttu-id="bdf1b-194">O valor é interpretado e armazenado como um inteiro (REG \_ DWORD).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-194">The value is interpreted and stored as an integer (REG\_DWORD).</span></span>                |



 

-   <span data-ttu-id="bdf1b-195">Se o valor contiver o til da sequência \[ ~ \] , o valor será interpretado como uma lista delimitada por nulo de cadeias de caracteres (reg \_ multi \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-195">If the value contains the sequence tilde \[~\], then the value is interpreted as a Null-delimited list of strings (REG\_MULTI\_SZ).</span></span> <span data-ttu-id="bdf1b-196">Por exemplo, para especificar uma lista contendo as três cadeias de caracteres a, b e c, use "a \[ ~ \] b \[ ~ \] c".</span><span class="sxs-lookup"><span data-stu-id="bdf1b-196">For example, to specify a list containing the three strings a, b and c, use "a\[~\]b\[~\]c".</span></span>
-   <span data-ttu-id="bdf1b-197">A sequência \[ ~ \] dentro do valor separa as cadeias de caracteres individuais e é interpretada e armazenada como um caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-197">The sequence \[~\] within the value separates the individual strings and is interpreted and stored as a Null character.</span></span>
-   <span data-ttu-id="bdf1b-198">Se um \[ ~ \] precede a lista de cadeias de caracteres, as cadeias devem ser acrescentadas a qualquer cadeia de caracteres de valor de registro existente.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-198">If a \[~\] precedes the string list, the strings are to be appended to any existing registry value strings.</span></span> <span data-ttu-id="bdf1b-199">Se uma cadeia de caracteres de acréscimo já ocorrer no valor do registro, a ocorrência original da cadeia de caracteres será removida.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-199">If an appending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="bdf1b-200">Se a \[ ~ \] seguir o final da lista de cadeias de caracteres, as cadeias devem ser precedidas a quaisquer cadeias de caracteres de valor de registro existentes.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-200">If a \[~\] follows the end of the string list, the strings are to be prepended to any existing registry value strings.</span></span> <span data-ttu-id="bdf1b-201">Se uma cadeia de caracteres de prependência já ocorrer no valor do registro, a ocorrência original da cadeia de caracteres será removida.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-201">If a prepending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="bdf1b-202">Se um \[ ~ \] estiver no início e no fim ou não no início nem no final da lista de cadeias de caracteres, as cadeias serão substituídas por qualquer cadeia de caracteres de valor de registro existente.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-202">If a \[~\] is at both the beginning and the end or at neither the beginning nor the end of the string list, the strings are to replace any existing registry value strings.</span></span>
-   <span data-ttu-id="bdf1b-203">Caso contrário, o valor será interpretado e armazenado como uma cadeia de caracteres (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-203">Otherwise, the value is interpreted and stored as a string (REG\_SZ).</span></span>

</dd> <dt>

<span data-ttu-id="bdf1b-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="bdf1b-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="bdf1b-205">Chave externa na primeira coluna da tabela de [componentes](component-table.md) que faz referência ao componente que controla a instalação do valor do registro.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-205">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdf1b-206">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdf1b-206">Remarks</span></span>

<span data-ttu-id="bdf1b-207">As ações [WriteRegistryValues](writeregistryvalues-action.md) e [RemoveRegistryValues](removeregistryvalues-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-207">The [WriteRegistryValues](writeregistryvalues-action.md) and [RemoveRegistryValues](removeregistryvalues-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="bdf1b-208">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-208">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="bdf1b-209">As informações do registro são gravadas no registro do sistema quando o componente correspondente foi selecionado para ser instalado localmente ou executado da origem.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-209">The registry information is written out to the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="bdf1b-210">Observe que o instalador remove uma chave do registro depois de remover o último valor ou subchave sob a chave.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-210">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="bdf1b-211">Para impedir que uma chave de registro vazia seja removida durante a desinstalação, grave um valor fictício sob a chave que você precisa manter e digite + na coluna nome.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-211">To prevent an empty registry key from being removed when uninstalling, write a dummy value under the key you need to keep and enter + in the Name column.</span></span> <span data-ttu-id="bdf1b-212">Se \* estiver na coluna nome, a chave será excluída, com todos os seus valores e subchaves, quando o componente for removido.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-212">If \* is in the Name column, the key is deleted, with all of its values and subkeys, when the component is removed.</span></span>

<span data-ttu-id="bdf1b-213">Uma ação personalizada pode ser usada para adicionar linhas à tabela do registro durante uma instalação, desinstalação ou Repair Transaction.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-213">A custom action can be used to add rows to the Registry table during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="bdf1b-214">Essas linhas não persistem na tabela do registro e as informações só estão disponíveis durante a transação atual.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-214">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="bdf1b-215">A ação personalizada deve, portanto, ser executada em cada instalação, desinstalação ou reparo de transação que exija as informações nessas linhas adicionais.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-215">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="bdf1b-216">A ação personalizada deve vir antes das ações [RemoveRegistryValues](removeregistryvalues-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="bdf1b-216">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

<span data-ttu-id="bdf1b-217">Para obter informações sobre como proteger uma chave do registro, consulte a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md) e a [Tabela LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="bdf1b-217">For information on how to secure a registry key see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="bdf1b-218">Validação</span><span class="sxs-lookup"><span data-stu-id="bdf1b-218">Validation</span></span>

<dl>

[<span data-ttu-id="bdf1b-219">ICE02</span><span class="sxs-lookup"><span data-stu-id="bdf1b-219">ICE02</span></span>](ice02.md)  
[<span data-ttu-id="bdf1b-220">ICE03</span><span class="sxs-lookup"><span data-stu-id="bdf1b-220">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="bdf1b-221">ICE06</span><span class="sxs-lookup"><span data-stu-id="bdf1b-221">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="bdf1b-222">ICE32</span><span class="sxs-lookup"><span data-stu-id="bdf1b-222">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="bdf1b-223">ICE38</span><span class="sxs-lookup"><span data-stu-id="bdf1b-223">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="bdf1b-224">ICE43</span><span class="sxs-lookup"><span data-stu-id="bdf1b-224">ICE43</span></span>](ice43.md)  
[<span data-ttu-id="bdf1b-225">ICE46</span><span class="sxs-lookup"><span data-stu-id="bdf1b-225">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="bdf1b-226">ICE49</span><span class="sxs-lookup"><span data-stu-id="bdf1b-226">ICE49</span></span>](ice49.md)  
[<span data-ttu-id="bdf1b-227">ICE53</span><span class="sxs-lookup"><span data-stu-id="bdf1b-227">ICE53</span></span>](ice53.md)  
[<span data-ttu-id="bdf1b-228">ICE55</span><span class="sxs-lookup"><span data-stu-id="bdf1b-228">ICE55</span></span>](ice55.md)  
[<span data-ttu-id="bdf1b-229">ICE57</span><span class="sxs-lookup"><span data-stu-id="bdf1b-229">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="bdf1b-230">ICE70</span><span class="sxs-lookup"><span data-stu-id="bdf1b-230">ICE70</span></span>](ice70.md)  
[<span data-ttu-id="bdf1b-231">ICE80</span><span class="sxs-lookup"><span data-stu-id="bdf1b-231">ICE80</span></span>](ice80.md)  
</dl>

 

 




