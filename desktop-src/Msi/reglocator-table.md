---
description: A tabela RegLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando o registro ou para procurar uma própria entrada de registro em si. Esta tabela tem as seguintes colunas.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Tabela RegLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756894"
---
# <a name="reglocator-table"></a><span data-ttu-id="14cd6-104">Tabela RegLocator</span><span class="sxs-lookup"><span data-stu-id="14cd6-104">RegLocator Table</span></span>

<span data-ttu-id="14cd6-105">A tabela RegLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando o registro ou para procurar uma própria entrada de registro em si.</span><span class="sxs-lookup"><span data-stu-id="14cd6-105">The RegLocator table holds the information needed to search for a file or directory using the registry, or to search for a particular registry entry itself.</span></span> <span data-ttu-id="14cd6-106">Esta tabela tem as seguintes colunas.</span><span class="sxs-lookup"><span data-stu-id="14cd6-106">This table has the following columns.</span></span>



| <span data-ttu-id="14cd6-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="14cd6-107">Column</span></span>      | <span data-ttu-id="14cd6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="14cd6-108">Type</span></span>                         | <span data-ttu-id="14cd6-109">Chave</span><span class="sxs-lookup"><span data-stu-id="14cd6-109">Key</span></span> | <span data-ttu-id="14cd6-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="14cd6-110">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="14cd6-111">Signature\_</span><span class="sxs-lookup"><span data-stu-id="14cd6-111">Signature\_</span></span> | [<span data-ttu-id="14cd6-112">Identificador</span><span class="sxs-lookup"><span data-stu-id="14cd6-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="14cd6-113">S</span><span class="sxs-lookup"><span data-stu-id="14cd6-113">Y</span></span>   | <span data-ttu-id="14cd6-114">N</span><span class="sxs-lookup"><span data-stu-id="14cd6-114">N</span></span>        |
| <span data-ttu-id="14cd6-115">Root</span><span class="sxs-lookup"><span data-stu-id="14cd6-115">Root</span></span>        | [<span data-ttu-id="14cd6-116">Inteiro</span><span class="sxs-lookup"><span data-stu-id="14cd6-116">Integer</span></span>](integer.md)       | <span data-ttu-id="14cd6-117">N</span><span class="sxs-lookup"><span data-stu-id="14cd6-117">N</span></span>   | <span data-ttu-id="14cd6-118">N</span><span class="sxs-lookup"><span data-stu-id="14cd6-118">N</span></span>        |
| <span data-ttu-id="14cd6-119">Chave</span><span class="sxs-lookup"><span data-stu-id="14cd6-119">Key</span></span>         | [<span data-ttu-id="14cd6-120">RegPath</span><span class="sxs-lookup"><span data-stu-id="14cd6-120">RegPath</span></span>](regpath.md)       | <span data-ttu-id="14cd6-121">N</span><span class="sxs-lookup"><span data-stu-id="14cd6-121">N</span></span>   | <span data-ttu-id="14cd6-122">N</span><span class="sxs-lookup"><span data-stu-id="14cd6-122">N</span></span>        |
| <span data-ttu-id="14cd6-123">Nome</span><span class="sxs-lookup"><span data-stu-id="14cd6-123">Name</span></span>        | [<span data-ttu-id="14cd6-124">Binário</span><span class="sxs-lookup"><span data-stu-id="14cd6-124">Formatted</span></span>](formatted.md)   | <span data-ttu-id="14cd6-125">N</span><span class="sxs-lookup"><span data-stu-id="14cd6-125">N</span></span>   | <span data-ttu-id="14cd6-126">Y</span><span class="sxs-lookup"><span data-stu-id="14cd6-126">Y</span></span>        |
| <span data-ttu-id="14cd6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="14cd6-127">Type</span></span>        | [<span data-ttu-id="14cd6-128">Inteiro</span><span class="sxs-lookup"><span data-stu-id="14cd6-128">Integer</span></span>](integer.md)       | <span data-ttu-id="14cd6-129">N</span><span class="sxs-lookup"><span data-stu-id="14cd6-129">N</span></span>   | <span data-ttu-id="14cd6-130">S</span><span class="sxs-lookup"><span data-stu-id="14cd6-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="14cd6-131">Colunas</span><span class="sxs-lookup"><span data-stu-id="14cd6-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="14cd6-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="14cd6-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="14cd6-133">O valor no campo assinatura \_ representa uma assinatura exclusiva que é uma chave externa na coluna um da tabela de [assinatura](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="14cd6-133">The value in the Signature\_ field represents a unique signature that is an external key into column one of the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="14cd6-134">Se essa assinatura estiver presente na tabela de assinatura, a pesquisa será para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="14cd6-134">If this signature is present in the Signature table, the search is for a file.</span></span> <span data-ttu-id="14cd6-135">Se essa assinatura estiver ausente da tabela de assinatura e o valor da coluna de tipo for **msidbLocatorTypeRawValue**, a pesquisa será para o nome da chave do registro apontado pela tabela RegLocator.</span><span class="sxs-lookup"><span data-stu-id="14cd6-135">If this signature is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the registry key name pointed to by the RegLocator table.</span></span> <span data-ttu-id="14cd6-136">Caso contrário, a pesquisa será para um diretório apontado pela tabela RegLocator.</span><span class="sxs-lookup"><span data-stu-id="14cd6-136">Otherwise the search is for a directory pointed to by the RegLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="14cd6-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Básica</span><span class="sxs-lookup"><span data-stu-id="14cd6-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="14cd6-138">A chave raiz predefinida para o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="14cd6-138">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="14cd6-139">Constante</span><span class="sxs-lookup"><span data-stu-id="14cd6-139">Constant</span></span>                          | <span data-ttu-id="14cd6-140">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="14cd6-140">Hexadecimal</span></span> | <span data-ttu-id="14cd6-141">Decimal</span><span class="sxs-lookup"><span data-stu-id="14cd6-141">Decimal</span></span> | <span data-ttu-id="14cd6-142">Chave raiz</span><span class="sxs-lookup"><span data-stu-id="14cd6-142">Root key</span></span>             |
|-----------------------------------|-------------|---------|----------------------|
| <span data-ttu-id="14cd6-143">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="14cd6-143">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="14cd6-144">0x000</span><span class="sxs-lookup"><span data-stu-id="14cd6-144">0x000</span></span>       | <span data-ttu-id="14cd6-145">0</span><span class="sxs-lookup"><span data-stu-id="14cd6-145">0</span></span>       | <span data-ttu-id="14cd6-146">\_raiz de classes hKey \_</span><span class="sxs-lookup"><span data-stu-id="14cd6-146">HKEY\_CLASSES\_ROOT</span></span>  |
| <span data-ttu-id="14cd6-147">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="14cd6-147">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="14cd6-148">0x001</span><span class="sxs-lookup"><span data-stu-id="14cd6-148">0x001</span></span>       | <span data-ttu-id="14cd6-149">1</span><span class="sxs-lookup"><span data-stu-id="14cd6-149">1</span></span>       | <span data-ttu-id="14cd6-150">HKEY \_ Current \_ User</span><span class="sxs-lookup"><span data-stu-id="14cd6-150">HKEY\_CURRENT\_USER</span></span>  |
| <span data-ttu-id="14cd6-151">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="14cd6-151">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="14cd6-152">0x002</span><span class="sxs-lookup"><span data-stu-id="14cd6-152">0x002</span></span>       | <span data-ttu-id="14cd6-153">2</span><span class="sxs-lookup"><span data-stu-id="14cd6-153">2</span></span>       | <span data-ttu-id="14cd6-154">\_máquina local \_ HKEY</span><span class="sxs-lookup"><span data-stu-id="14cd6-154">HKEY\_LOCAL\_MACHINE</span></span> |
| <span data-ttu-id="14cd6-155">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="14cd6-155">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="14cd6-156">0x003</span><span class="sxs-lookup"><span data-stu-id="14cd6-156">0x003</span></span>       | <span data-ttu-id="14cd6-157">3</span><span class="sxs-lookup"><span data-stu-id="14cd6-157">3</span></span>       | <span data-ttu-id="14cd6-158">usuários de HKEY \_</span><span class="sxs-lookup"><span data-stu-id="14cd6-158">HKEY\_USERS</span></span>          |



 

</dd> <dt>

<span data-ttu-id="14cd6-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves</span><span class="sxs-lookup"><span data-stu-id="14cd6-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="14cd6-160">A chave para o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="14cd6-160">The key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="14cd6-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="14cd6-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="14cd6-162">O nome do valor do registro.</span><span class="sxs-lookup"><span data-stu-id="14cd6-162">The registry value name.</span></span> <span data-ttu-id="14cd6-163">Se esse valor for NULL, o valor do valor padrão ou não nomeado da chave, se houver, será recuperado.</span><span class="sxs-lookup"><span data-stu-id="14cd6-163">If this value is null, then the value from the key's unnamed or default value, if any, is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="14cd6-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva</span><span class="sxs-lookup"><span data-stu-id="14cd6-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="14cd6-165">Um valor que determina se o valor do registro é um nome de arquivo, um local de diretório ou um valor de registro bruto.</span><span class="sxs-lookup"><span data-stu-id="14cd6-165">A value that determines if the registry value is a file name, a directory location, or raw registry value.</span></span>

<span data-ttu-id="14cd6-166">A tabela a seguir lista os valores válidos.</span><span class="sxs-lookup"><span data-stu-id="14cd6-166">The following table lists valid values.</span></span> <span data-ttu-id="14cd6-167">Defina um dos três primeiros valores e **msidbLocatorType64bit** , se necessário.</span><span class="sxs-lookup"><span data-stu-id="14cd6-167">Set one of the first three values and **msidbLocatorType64bit** if necessary.</span></span> <span data-ttu-id="14cd6-168">Se a entrada nesse campo estiver ausente, o tipo será definido como 1.</span><span class="sxs-lookup"><span data-stu-id="14cd6-168">If the entry in this field is absent, Type is set to be 1.</span></span>



| <span data-ttu-id="14cd6-169">Constante</span><span class="sxs-lookup"><span data-stu-id="14cd6-169">Constant</span></span>                      | <span data-ttu-id="14cd6-170">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="14cd6-170">Hexadecimal</span></span> | <span data-ttu-id="14cd6-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="14cd6-171">Decimal</span></span> | <span data-ttu-id="14cd6-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="14cd6-172">Description</span></span>                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14cd6-173">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="14cd6-173">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="14cd6-174">0x000</span><span class="sxs-lookup"><span data-stu-id="14cd6-174">0x000</span></span>       | <span data-ttu-id="14cd6-175">0</span><span class="sxs-lookup"><span data-stu-id="14cd6-175">0</span></span>       | <span data-ttu-id="14cd6-176">O caminho da chave é um diretório.</span><span class="sxs-lookup"><span data-stu-id="14cd6-176">Key path is a directory.</span></span>                                                                                                                                           |
| <span data-ttu-id="14cd6-177">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="14cd6-177">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="14cd6-178">0x001</span><span class="sxs-lookup"><span data-stu-id="14cd6-178">0x001</span></span>       | <span data-ttu-id="14cd6-179">1</span><span class="sxs-lookup"><span data-stu-id="14cd6-179">1</span></span>       | <span data-ttu-id="14cd6-180">O caminho da chave é um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="14cd6-180">Key path is a file name.</span></span>                                                                                                                                           |
| <span data-ttu-id="14cd6-181">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="14cd6-181">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="14cd6-182">0x002</span><span class="sxs-lookup"><span data-stu-id="14cd6-182">0x002</span></span>       | <span data-ttu-id="14cd6-183">2</span><span class="sxs-lookup"><span data-stu-id="14cd6-183">2</span></span>       | <span data-ttu-id="14cd6-184">O caminho da chave é um valor do registro.</span><span class="sxs-lookup"><span data-stu-id="14cd6-184">Key path is a registry value.</span></span>                                                                                                                                      |
| <span data-ttu-id="14cd6-185">**msidbLocatorType64bit**</span><span class="sxs-lookup"><span data-stu-id="14cd6-185">**msidbLocatorType64bit**</span></span>     | <span data-ttu-id="14cd6-186">0x010</span><span class="sxs-lookup"><span data-stu-id="14cd6-186">0x010</span></span>       | <span data-ttu-id="14cd6-187">16</span><span class="sxs-lookup"><span data-stu-id="14cd6-187">16</span></span>      | <span data-ttu-id="14cd6-188">Defina este bit para que o instalador pesquise a parte de 64 bits do registro.</span><span class="sxs-lookup"><span data-stu-id="14cd6-188">Set this bit to have the installer search the 64-bit portion of the registry.</span></span> <span data-ttu-id="14cd6-189">Não defina esse bit para que o instalador pesquise a parte de 32 bits do registro.</span><span class="sxs-lookup"><span data-stu-id="14cd6-189">Do not set this bit to have the installer search the 32-bit portion of the registry.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14cd6-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="14cd6-190">Remarks</span></span>

<span data-ttu-id="14cd6-191">Observe que, se o valor no campo Type for **msidbLocatorTypeRawValue**, o instalador definirá o valor da propriedade especificada no campo de propriedade da tabela [AppSearch](appsearch-table.md) como o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="14cd6-191">Note that if the value in the Type field is **msidbLocatorTypeRawValue**, the installer sets the value of the property specified in the Property field of the [AppSearch](appsearch-table.md) table to the registry value.</span></span> <span data-ttu-id="14cd6-192">O instalador adiciona um prefixo ao valor do registro que identifica o tipo de valor do registro.</span><span class="sxs-lookup"><span data-stu-id="14cd6-192">The installer adds a prefix to the registry value that identifies the type of registry value.</span></span> <span data-ttu-id="14cd6-193">Para obter mais informações sobre tipos de valores de registro, consulte [tipos de valor do registro](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="14cd6-193">For more information about types of registry values, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>



| <span data-ttu-id="14cd6-194">Tipo de Registro</span><span class="sxs-lookup"><span data-stu-id="14cd6-194">Registry type</span></span>   | <span data-ttu-id="14cd6-195">Prefixo adicionado pelo instalador</span><span class="sxs-lookup"><span data-stu-id="14cd6-195">Prefix added by Installer</span></span>                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14cd6-196">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="14cd6-196">REG\_SZ</span></span>         | <span data-ttu-id="14cd6-197">Nenhum, mas se o primeiro caractere do valor do registro for \# , o instalador escapará o caractere prefixando um outro \# .</span><span class="sxs-lookup"><span data-stu-id="14cd6-197">None, but if the first character of the registry value is \#, the installer escapes the character by prefixing a another \#.</span></span>            |
| <span data-ttu-id="14cd6-198">DWORD</span><span class="sxs-lookup"><span data-stu-id="14cd6-198">DWORD</span></span>           | <span data-ttu-id="14cd6-199">" \# ", opcionalmente seguido por ' + ' ou '-'</span><span class="sxs-lookup"><span data-stu-id="14cd6-199">"\#" optionally followed by '+' or '-'</span></span>                                                                                                  |
| <span data-ttu-id="14cd6-200">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="14cd6-200">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="14cd6-201">"\#%"</span><span class="sxs-lookup"><span data-stu-id="14cd6-201">"\#%"</span></span>                                                                                                                                   |
| <span data-ttu-id="14cd6-202">REG \_ multi \_ sz</span><span class="sxs-lookup"><span data-stu-id="14cd6-202">REG\_MULTI\_SZ</span></span>  | <span data-ttu-id="14cd6-203">Nulo.</span><span class="sxs-lookup"><span data-stu-id="14cd6-203">Null.</span></span> <span data-ttu-id="14cd6-204">O instalador define a propriedade com um valor que começa com um NULL e termina com NULL.</span><span class="sxs-lookup"><span data-stu-id="14cd6-204">The installer sets the property to a value beginning with a null and ending with a null.</span></span>                                          |
| <span data-ttu-id="14cd6-205">\_binário reg</span><span class="sxs-lookup"><span data-stu-id="14cd6-205">REG\_BINARY</span></span>     | <span data-ttu-id="14cd6-206">" \# x" no caso de reg \_ Binary, o instalador converte e salva cada dígito hexadecimal (Nibble) como um caractere ASCII prefixado por " \# x".</span><span class="sxs-lookup"><span data-stu-id="14cd6-206">"\#x" In case of REG\_BINARY, the installer converts and saves each hexadecimal digit (nibble) as an ASCII character prefixed by "\#x".</span></span> |



 

<span data-ttu-id="14cd6-207">Normalmente, as colunas nesta tabela não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="14cd6-207">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="14cd6-208">Se um autor decidir procurar produtos em vários idiomas, deverá haver uma entrada separada incluída na tabela para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="14cd6-208">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="14cd6-209">Observe que não é possível usar a tabela RegLocator para verificar apenas a presença da chave.</span><span class="sxs-lookup"><span data-stu-id="14cd6-209">Note that it is not possible to use the RegLocator table to check only for the presence of the key.</span></span> <span data-ttu-id="14cd6-210">No entanto, você pode pesquisar o valor padrão de uma chave e recuperar seu valor se ele não estiver vazio.</span><span class="sxs-lookup"><span data-stu-id="14cd6-210">However, you can search for the default value of a key and retrieve its value if it is not empty.</span></span>

<span data-ttu-id="14cd6-211">Para obter mais informações, consulte [pesquisando aplicativos existentes, arquivos, entradas de registro ou entradas de arquivo. ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="14cd6-211">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="14cd6-212">Validação</span><span class="sxs-lookup"><span data-stu-id="14cd6-212">Validation</span></span>

<dl>

[<span data-ttu-id="14cd6-213">ICE03</span><span class="sxs-lookup"><span data-stu-id="14cd6-213">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="14cd6-214">ICE06</span><span class="sxs-lookup"><span data-stu-id="14cd6-214">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="14cd6-215">ICE46</span><span class="sxs-lookup"><span data-stu-id="14cd6-215">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="14cd6-216">ICE80</span><span class="sxs-lookup"><span data-stu-id="14cd6-216">ICE80</span></span>](ice80.md)  
</dl>

 

 
