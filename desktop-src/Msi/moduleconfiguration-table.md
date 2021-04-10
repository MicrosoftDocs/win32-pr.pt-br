---
description: A Tabela ModuleConfiguration identifica os atributos configuráveis do módulo. Esta tabela não é mesclada no banco de dados.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Tabela ModuleConfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170054"
---
# <a name="moduleconfiguration-table"></a><span data-ttu-id="75318-104">Tabela ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="75318-104">ModuleConfiguration Table</span></span>

<span data-ttu-id="75318-105">A Tabela ModuleConfiguration identifica os atributos configuráveis do módulo.</span><span class="sxs-lookup"><span data-stu-id="75318-105">The ModuleConfiguration table identifies the configurable attributes of the module.</span></span> <span data-ttu-id="75318-106">Esta tabela não é mesclada no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="75318-106">This table is not merged into the database.</span></span>

<span data-ttu-id="75318-107">A Tabela ModuleConfiguration tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="75318-107">The ModuleConfiguration table has the following columns.</span></span>



| <span data-ttu-id="75318-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="75318-108">Column</span></span>       | <span data-ttu-id="75318-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="75318-109">Type</span></span>                         | <span data-ttu-id="75318-110">Chave</span><span class="sxs-lookup"><span data-stu-id="75318-110">Key</span></span> | <span data-ttu-id="75318-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="75318-111">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="75318-112">Nome</span><span class="sxs-lookup"><span data-stu-id="75318-112">Name</span></span>         | [<span data-ttu-id="75318-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="75318-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="75318-114">S</span><span class="sxs-lookup"><span data-stu-id="75318-114">Y</span></span>   | <span data-ttu-id="75318-115">N</span><span class="sxs-lookup"><span data-stu-id="75318-115">N</span></span>        |
| <span data-ttu-id="75318-116">Formatar</span><span class="sxs-lookup"><span data-stu-id="75318-116">Format</span></span>       | [<span data-ttu-id="75318-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="75318-117">Integer</span></span>](integer.md)       | <span data-ttu-id="75318-118">N</span><span class="sxs-lookup"><span data-stu-id="75318-118">N</span></span>   | <span data-ttu-id="75318-119">N</span><span class="sxs-lookup"><span data-stu-id="75318-119">N</span></span>        |
| <span data-ttu-id="75318-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="75318-120">Type</span></span>         | [<span data-ttu-id="75318-121">Text</span><span class="sxs-lookup"><span data-stu-id="75318-121">Text</span></span>](text.md)             | <span data-ttu-id="75318-122">N</span><span class="sxs-lookup"><span data-stu-id="75318-122">N</span></span>   | <span data-ttu-id="75318-123">S</span><span class="sxs-lookup"><span data-stu-id="75318-123">Y</span></span>        |
| <span data-ttu-id="75318-124">ContextData</span><span class="sxs-lookup"><span data-stu-id="75318-124">ContextData</span></span>  | [<span data-ttu-id="75318-125">Text</span><span class="sxs-lookup"><span data-stu-id="75318-125">Text</span></span>](text.md)             | <span data-ttu-id="75318-126">N</span><span class="sxs-lookup"><span data-stu-id="75318-126">N</span></span>   | <span data-ttu-id="75318-127">S</span><span class="sxs-lookup"><span data-stu-id="75318-127">Y</span></span>        |
| <span data-ttu-id="75318-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="75318-128">DefaultValue</span></span> | [<span data-ttu-id="75318-129">Text</span><span class="sxs-lookup"><span data-stu-id="75318-129">Text</span></span>](text.md)             | <span data-ttu-id="75318-130">N</span><span class="sxs-lookup"><span data-stu-id="75318-130">N</span></span>   | <span data-ttu-id="75318-131">S</span><span class="sxs-lookup"><span data-stu-id="75318-131">Y</span></span>        |
| <span data-ttu-id="75318-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="75318-132">Attributes</span></span>   | [<span data-ttu-id="75318-133">Inteiro</span><span class="sxs-lookup"><span data-stu-id="75318-133">Integer</span></span>](integer.md)       | <span data-ttu-id="75318-134">N</span><span class="sxs-lookup"><span data-stu-id="75318-134">N</span></span>   | <span data-ttu-id="75318-135">S</span><span class="sxs-lookup"><span data-stu-id="75318-135">Y</span></span>        |
| <span data-ttu-id="75318-136">DisplayName</span><span class="sxs-lookup"><span data-stu-id="75318-136">DisplayName</span></span>  | [<span data-ttu-id="75318-137">Text</span><span class="sxs-lookup"><span data-stu-id="75318-137">Text</span></span>](text.md)             | <span data-ttu-id="75318-138">N</span><span class="sxs-lookup"><span data-stu-id="75318-138">N</span></span>   | <span data-ttu-id="75318-139">S</span><span class="sxs-lookup"><span data-stu-id="75318-139">Y</span></span>        |
| <span data-ttu-id="75318-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="75318-140">Description</span></span>  | [<span data-ttu-id="75318-141">Text</span><span class="sxs-lookup"><span data-stu-id="75318-141">Text</span></span>](text.md)             | <span data-ttu-id="75318-142">N</span><span class="sxs-lookup"><span data-stu-id="75318-142">N</span></span>   | <span data-ttu-id="75318-143">S</span><span class="sxs-lookup"><span data-stu-id="75318-143">Y</span></span>        |
| <span data-ttu-id="75318-144">HelpLocation</span><span class="sxs-lookup"><span data-stu-id="75318-144">HelpLocation</span></span> | [<span data-ttu-id="75318-145">Text</span><span class="sxs-lookup"><span data-stu-id="75318-145">Text</span></span>](text.md)             | <span data-ttu-id="75318-146">N</span><span class="sxs-lookup"><span data-stu-id="75318-146">N</span></span>   | <span data-ttu-id="75318-147">S</span><span class="sxs-lookup"><span data-stu-id="75318-147">Y</span></span>        |
| <span data-ttu-id="75318-148">HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="75318-148">HelpKeyword</span></span>  | [<span data-ttu-id="75318-149">Text</span><span class="sxs-lookup"><span data-stu-id="75318-149">Text</span></span>](text.md)             | <span data-ttu-id="75318-150">N</span><span class="sxs-lookup"><span data-stu-id="75318-150">N</span></span>   | <span data-ttu-id="75318-151">S</span><span class="sxs-lookup"><span data-stu-id="75318-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="75318-152">Colunas</span><span class="sxs-lookup"><span data-stu-id="75318-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="75318-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="75318-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="75318-154">Este campo define o nome do item configurável.</span><span class="sxs-lookup"><span data-stu-id="75318-154">This field defines the name of the configurable item.</span></span> <span data-ttu-id="75318-155">Esse nome é referenciado no modelo de formatação na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="75318-155">This name is referenced in the formatting template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="75318-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="75318-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format</span></span>
</dt> <dd>

<span data-ttu-id="75318-157">Esta coluna especifica o formato dos dados que estão sendo alterados.</span><span class="sxs-lookup"><span data-stu-id="75318-157">This column specifies the format of the data being changed.</span></span>



| <span data-ttu-id="75318-158">Formatar</span><span class="sxs-lookup"><span data-stu-id="75318-158">Format</span></span>                                       | <span data-ttu-id="75318-159">Valor</span><span class="sxs-lookup"><span data-stu-id="75318-159">Value</span></span> |
|----------------------------------------------|-------|
| [<span data-ttu-id="75318-160">Texto</span><span class="sxs-lookup"><span data-stu-id="75318-160">Text</span></span>](text-format-types.md)                | <span data-ttu-id="75318-161">0</span><span class="sxs-lookup"><span data-stu-id="75318-161">0</span></span>     |
| [<span data-ttu-id="75318-162">Chave</span><span class="sxs-lookup"><span data-stu-id="75318-162">Key</span></span>](key-format-types.md)                  | <span data-ttu-id="75318-163">1</span><span class="sxs-lookup"><span data-stu-id="75318-163">1</span></span>     |
| [<span data-ttu-id="75318-164">Inteiro</span><span class="sxs-lookup"><span data-stu-id="75318-164">Integer</span></span>](integer-format-types.md)          | <span data-ttu-id="75318-165">2</span><span class="sxs-lookup"><span data-stu-id="75318-165">2</span></span>     |
| [<span data-ttu-id="75318-166">Formato de campo de bits</span><span class="sxs-lookup"><span data-stu-id="75318-166">Bitfield Format</span></span>](bitfield-format-types.md) | <span data-ttu-id="75318-167">3</span><span class="sxs-lookup"><span data-stu-id="75318-167">3</span></span>     |



 

</dd> <dt>

<span data-ttu-id="75318-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva</span><span class="sxs-lookup"><span data-stu-id="75318-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="75318-169">Esta coluna especifica o tipo para os dados que estão sendo alterados.</span><span class="sxs-lookup"><span data-stu-id="75318-169">This column specifies the type for the data being changed.</span></span> <span data-ttu-id="75318-170">Esse tipo é usado para fornecer um contexto para qualquer interface do usuário e não é usado no processo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="75318-170">This type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="75318-171">Os valores válidos para essa coluna dependem do valor na coluna formato.</span><span class="sxs-lookup"><span data-stu-id="75318-171">The valid values for this column depend on the value in the Format column.</span></span>

</dd> <dt>

<span data-ttu-id="75318-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span><span class="sxs-lookup"><span data-stu-id="75318-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span></span>
</dt> <dd>

<span data-ttu-id="75318-173">Esta coluna especifica um contexto semântico para os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="75318-173">This column specifies a semantic context for the requested data.</span></span> <span data-ttu-id="75318-174">O tipo é usado para fornecer um contexto para qualquer interface do usuário e não é usado no processo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="75318-174">The type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="75318-175">Os valores válidos para essa coluna dependem dos valores nas colunas Format e Type.</span><span class="sxs-lookup"><span data-stu-id="75318-175">The valid values for this column depend on the values in the Format and Type columns.</span></span>

</dd> <dt>

<span data-ttu-id="75318-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>ValorPadrão</span><span class="sxs-lookup"><span data-stu-id="75318-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span></span>
</dt> <dd>

<span data-ttu-id="75318-177">Esta coluna especifica um valor padrão para o item nesse registro se a ferramenta de mesclagem declinar para fornecer um valor.</span><span class="sxs-lookup"><span data-stu-id="75318-177">This column specifies a default value for the item in this record if the merge tool declines to provide a value.</span></span> <span data-ttu-id="75318-178">Esse valor deve ter o formato, o tipo e o contexto do item.</span><span class="sxs-lookup"><span data-stu-id="75318-178">This value must have the format, type, and context of the item.</span></span> <span data-ttu-id="75318-179">Se esse for um item de formato "chave", a chave estrangeira deverá ser uma chave válida para as tabelas do módulo.</span><span class="sxs-lookup"><span data-stu-id="75318-179">If this is a "Key" format item, the foreign key must be a valid key into the tables of the module.</span></span> <span data-ttu-id="75318-180">NULL pode ser um valor válido para esta coluna, dependendo do item.</span><span class="sxs-lookup"><span data-stu-id="75318-180">Null may be a valid value for this column depending on the item.</span></span> <span data-ttu-id="75318-181">Para itens de formato "chave", esse valor está no [formato especial CMSM](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="75318-181">For "Key" format items, this value is in [CMSM special format](cmsm-special-format.md).</span></span> <span data-ttu-id="75318-182">Para todos os outros tipos, o valor é tratado literalmente.</span><span class="sxs-lookup"><span data-stu-id="75318-182">For all other types, the value is treated literally.</span></span>

<span data-ttu-id="75318-183">Os autores de módulo devem garantir que o módulo seja válido em seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="75318-183">Module authors must ensure that the module is valid in its default state.</span></span> <span data-ttu-id="75318-184">Isso garante que versões do Mergemod.dll anteriores à versão 2,0 ainda possam usar o módulo em seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="75318-184">This ensures that versions of Mergemod.dll earlier than version 2.0 can still use the module in its default state.</span></span>

</dd> <dt>

<span data-ttu-id="75318-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="75318-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="75318-186">Esta coluna é um campo de bits que contém atributos para este item configurável.</span><span class="sxs-lookup"><span data-stu-id="75318-186">This column is a bit field containing attributes for this configurable item.</span></span> <span data-ttu-id="75318-187">NULL é equivalente a 0.</span><span class="sxs-lookup"><span data-stu-id="75318-187">Null is equivalent to 0.</span></span> <span data-ttu-id="75318-188">Todos os outros bits desta coluna são reservados para uso futuro e devem ser 0.</span><span class="sxs-lookup"><span data-stu-id="75318-188">All other bits in this column are reserved for future use and must be 0.</span></span>



| <span data-ttu-id="75318-189">Nome</span><span class="sxs-lookup"><span data-stu-id="75318-189">Name</span></span>                             | <span data-ttu-id="75318-190">Decimal</span><span class="sxs-lookup"><span data-stu-id="75318-190">Decimal</span></span> | <span data-ttu-id="75318-191">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="75318-191">Hexadecimal</span></span> | <span data-ttu-id="75318-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="75318-192">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75318-193">msmConfigurableOptionKeyNoOrphan</span><span class="sxs-lookup"><span data-stu-id="75318-193">msmConfigurableOptionKeyNoOrphan</span></span> | <span data-ttu-id="75318-194">1</span><span class="sxs-lookup"><span data-stu-id="75318-194">1</span></span>       | <span data-ttu-id="75318-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="75318-195">0x00000001</span></span>  | <span data-ttu-id="75318-196">Esse atributo só se aplica a registros que listam uma chave estrangeira em uma tabela de módulo em seu campo DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="75318-196">This attribute only applies to records that list a foreign key to a module table in their DefaultValue field.</span></span> <span data-ttu-id="75318-197">A ferramenta de mesclagem ignora o atributo para todos os formatos que não sejam os [tipos de formato de chave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="75318-197">The merge tool ignores the attribute for any formats other than the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="75318-198">Os itens não listados na [tabela ModuleSubstitution](modulesubstitution-table.md) são excluídos da verificação a seguir.</span><span class="sxs-lookup"><span data-stu-id="75318-198">Items not listed in the [ModuleSubstitution table](modulesubstitution-table.md) are excluded from the following check.</span></span> <span data-ttu-id="75318-199">A ferramenta de mesclagem não mescla a linha referenciada pela coluna DefaultValue no banco de dados de destino se as condições a seguir forem satisfeitas após a conclusão de todas as opções de configuração.</span><span class="sxs-lookup"><span data-stu-id="75318-199">The merge tool does not merge the row referenced by the DefaultValue column into the target database if the following conditions are satisfied after completing all configuration options.</span></span><br/> <span data-ttu-id="75318-200">Cada linha na Tabela ModuleConfiguration com o mesmo DefaultValue tem o conjunto msmConfigurationItemsKeyNoOrphan.</span><span class="sxs-lookup"><span data-stu-id="75318-200">Every row in the ModuleConfiguration table with the same DefaultValue has the msmConfigurationItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="75318-201">Nenhuma linha usa o DefaultValue porque a ferramenta de criação recusou o fornecimento de um valor.</span><span class="sxs-lookup"><span data-stu-id="75318-201">No rows use the DefaultValue because the authoring tool declined to provide a value.</span></span><br/> <span data-ttu-id="75318-202">A ferramenta de mesclagem mescla a linha se qualquer uma das condições a seguir for satisfeita.</span><span class="sxs-lookup"><span data-stu-id="75318-202">The merge tool merges the row if any of the following conditions are satisfied.</span></span><br/> <span data-ttu-id="75318-203">A ferramenta de mesclagem localiza qualquer linha que não tenha msmConfigItemsKeyNoOrphan definido.</span><span class="sxs-lookup"><span data-stu-id="75318-203">The merge tool finds any row that does not have msmConfigItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="75318-204">Se a ferramenta de mesclagem localizar qualquer linha usando DefaultValue porque a ferramenta de criação recusou o fornecimento de um valor.</span><span class="sxs-lookup"><span data-stu-id="75318-204">If the merge tool finds any row using DefaultValue because the authoring tool declined to provide a value.</span></span><br/> |
| <span data-ttu-id="75318-205">msmConfigurableOptionNonNullable</span><span class="sxs-lookup"><span data-stu-id="75318-205">msmConfigurableOptionNonNullable</span></span> | <span data-ttu-id="75318-206">2</span><span class="sxs-lookup"><span data-stu-id="75318-206">2</span></span>       | <span data-ttu-id="75318-207">0x00000002</span><span class="sxs-lookup"><span data-stu-id="75318-207">0x00000002</span></span>  | <span data-ttu-id="75318-208">Quando esse atributo é definido, NULL não é uma resposta válida para este item.</span><span class="sxs-lookup"><span data-stu-id="75318-208">When this attribute is set, null is not a valid response for this item.</span></span> <span data-ttu-id="75318-209">Esse atributo não tem nenhum efeito para tipos [de formato de](bitfield-format-types.md)campo [inteiro](integer-format-types.md) ou de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="75318-209">This attribute has no effect for [Integer Format Types](integer-format-types.md) or [Bitfield Format Types](bitfield-format-types.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="75318-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span><span class="sxs-lookup"><span data-stu-id="75318-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="75318-211">Esta coluna fornece uma breve descrição desse item que a ferramenta de criação pode usar na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="75318-211">This column provides a short description of this item that the authoring tool may use in the user interface.</span></span> <span data-ttu-id="75318-212">Esta coluna não pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="75318-212">This column may not be localized.</span></span> <span data-ttu-id="75318-213">Defina esta coluna como NULL para que o módulo seja solicitado que a ferramenta de criação não exponha essa propriedade na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="75318-213">Set this column to null to have the module is request that the authoring tool not expose this property in the UI.</span></span> <span data-ttu-id="75318-214">A ferramenta pode desconsiderar o valor nesse campo.</span><span class="sxs-lookup"><span data-stu-id="75318-214">The tool may disregard the value in this field.</span></span>

</dd> <dt>

<span data-ttu-id="75318-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="75318-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="75318-216">Esta coluna fornece uma descrição desse item que a ferramenta de criação pode usar em elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="75318-216">This column provides a description of this item that the authoring tool may use in UI elements.</span></span> <span data-ttu-id="75318-217">Essa cadeia de caracteres pode ser localizada pela transformação de idioma do módulo.</span><span class="sxs-lookup"><span data-stu-id="75318-217">This string may be localized by the module's language transform.</span></span> <span data-ttu-id="75318-218">Esta coluna pode ser nula.</span><span class="sxs-lookup"><span data-stu-id="75318-218">This column may be null.</span></span>

</dd> <dt>

<span data-ttu-id="75318-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span><span class="sxs-lookup"><span data-stu-id="75318-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span></span>
</dt> <dd>

<span data-ttu-id="75318-220">Esta coluna fornece o nome de um arquivo de ajuda (sem a extensão. chm) ou uma lista delimitada por ponto e vírgula de namespaces de ajuda.</span><span class="sxs-lookup"><span data-stu-id="75318-220">This column provides either the name of a help file (without the .chm extension) or a semicolon delimited list of help namespaces.</span></span> <span data-ttu-id="75318-221">Esta coluna poderá ser nula se nenhuma ajuda estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="75318-221">This column can be null if no help is available.</span></span> <span data-ttu-id="75318-222">Essa coluna poderá ser nula somente se a coluna HelpKeyword for nula.</span><span class="sxs-lookup"><span data-stu-id="75318-222">This column can be null only if the HelpKeyword column is null.</span></span>

</dd> <dt>

<span data-ttu-id="75318-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="75318-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span></span>
</dt> <dd>

<span data-ttu-id="75318-224">Esta coluna fornece uma palavra-chave para o arquivo de ajuda ou namespace da coluna HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="75318-224">This column provides a keyword into the help file or namespace from the HelpLocation column.</span></span> <span data-ttu-id="75318-225">A interpretação dessa palavra-chave depende da coluna HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="75318-225">The interpretation of this keyword depends on the HelpLocation column.</span></span> <span data-ttu-id="75318-226">Esta coluna pode ser nula.</span><span class="sxs-lookup"><span data-stu-id="75318-226">This column may be null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75318-227">Comentários</span><span class="sxs-lookup"><span data-stu-id="75318-227">Remarks</span></span>

<span data-ttu-id="75318-228">A Tabela ModuleConfiguration é usada por [módulos de mesclagem configuráveis](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="75318-228">The ModuleConfiguration table is used by [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="75318-229">Mergemod.dll 2,0 ou posterior é necessário para criar um módulo de mesclagem configurável.</span><span class="sxs-lookup"><span data-stu-id="75318-229">Mergemod.dll 2.0 or later is required to create a configurable merge module.</span></span>

<span data-ttu-id="75318-230">Para garantir a compatibilidade com versões mais antigas do Mergemod.dll, a Tabela ModuleConfiguration e a [tabela ModuleSubstitution](modulesubstitution-table.md) devem ser adicionadas à [tabela ModuleIgnoreTable](moduleignoretable-table.md) de cada módulo.</span><span class="sxs-lookup"><span data-stu-id="75318-230">To ensure compatibility with older versions of Mergemod.dll, the ModuleConfiguration table and [ModuleSubstitution table](modulesubstitution-table.md) should be added to the [ModuleIgnoreTable table](moduleignoretable-table.md) of every module.</span></span>

## <a name="validation"></a><span data-ttu-id="75318-231">Validação</span><span class="sxs-lookup"><span data-stu-id="75318-231">Validation</span></span>

<dl>

[<span data-ttu-id="75318-232">ICE03</span><span class="sxs-lookup"><span data-stu-id="75318-232">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="75318-233">ICE06</span><span class="sxs-lookup"><span data-stu-id="75318-233">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="75318-234">ICE25</span><span class="sxs-lookup"><span data-stu-id="75318-234">ICE25</span></span>](ice25.md)  
[<span data-ttu-id="75318-235">ICE45</span><span class="sxs-lookup"><span data-stu-id="75318-235">ICE45</span></span>](ice45.md)  
</dl>

 

 




