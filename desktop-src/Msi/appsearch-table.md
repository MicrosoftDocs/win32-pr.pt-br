---
description: A tabela AppSearch contém as propriedades necessárias para pesquisar um arquivo que tenha uma assinatura de arquivo específica. A tabela AppSearch também pode ser usada para definir uma propriedade para o valor existente de um registro ou de uma entrada de arquivo. ini.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Tabela AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169205"
---
# <a name="appsearch-table"></a><span data-ttu-id="5c50f-104">Tabela AppSearch</span><span class="sxs-lookup"><span data-stu-id="5c50f-104">AppSearch Table</span></span>

<span data-ttu-id="5c50f-105">A tabela AppSearch contém as propriedades necessárias para pesquisar um arquivo que tenha uma assinatura de arquivo específica.</span><span class="sxs-lookup"><span data-stu-id="5c50f-105">The AppSearch table contains properties needed to search for a file having a particular file signature.</span></span> <span data-ttu-id="5c50f-106">A tabela AppSearch também pode ser usada para definir uma propriedade para o valor existente de um registro ou de uma entrada de arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="5c50f-106">The AppSearch table can also be used to set a property to the existing value of a registry or .ini file entry.</span></span>

<span data-ttu-id="5c50f-107">A tabela AppSearch tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c50f-107">The AppSearch table has the following columns.</span></span>



| <span data-ttu-id="5c50f-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="5c50f-108">Column</span></span>      | <span data-ttu-id="5c50f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c50f-109">Type</span></span>                         | <span data-ttu-id="5c50f-110">Chave</span><span class="sxs-lookup"><span data-stu-id="5c50f-110">Key</span></span> | <span data-ttu-id="5c50f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="5c50f-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="5c50f-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5c50f-112">Property</span></span>    | [<span data-ttu-id="5c50f-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="5c50f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="5c50f-114">S</span><span class="sxs-lookup"><span data-stu-id="5c50f-114">Y</span></span>   | <span data-ttu-id="5c50f-115">N</span><span class="sxs-lookup"><span data-stu-id="5c50f-115">N</span></span>        |
| <span data-ttu-id="5c50f-116">Signature\_</span><span class="sxs-lookup"><span data-stu-id="5c50f-116">Signature\_</span></span> | [<span data-ttu-id="5c50f-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="5c50f-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="5c50f-118">S</span><span class="sxs-lookup"><span data-stu-id="5c50f-118">Y</span></span>   | <span data-ttu-id="5c50f-119">N</span><span class="sxs-lookup"><span data-stu-id="5c50f-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5c50f-120">Colunas</span><span class="sxs-lookup"><span data-stu-id="5c50f-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5c50f-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade</span><span class="sxs-lookup"><span data-stu-id="5c50f-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="5c50f-122">A execução da ação [AppSearch](appsearch-action.md) define essa propriedade como o local do arquivo indicado pela coluna de assinatura \_ .</span><span class="sxs-lookup"><span data-stu-id="5c50f-122">Running the [AppSearch](appsearch-action.md) action sets this property to the location of the file indicated by the Signature\_ column.</span></span> <span data-ttu-id="5c50f-123">Essa propriedade será definida se a assinatura de arquivo existir no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c50f-123">This property is set if the file signature exists on the user's computer.</span></span> <span data-ttu-id="5c50f-124">As propriedades usadas nesta coluna devem ser propriedades [públicas](public-properties.md) e ter um identificador que não contenha letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5c50f-124">The properties used in this column must be [public](public-properties.md) properties and have an identifier that contains no lowercase letters.</span></span>

<span data-ttu-id="5c50f-125">A propriedade listada no campo de propriedade pode ser inicializada na tabela de [Propriedades](property-table.md) ou em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5c50f-125">The property listed in the Property field may be initialized in the [Property](property-table.md) table or from a command line.</span></span> <span data-ttu-id="5c50f-126">Se a ação [AppSearch](appsearch-action.md) localizar a assinatura, o instalador substituirá o valor da propriedade Initialized pelo valor encontrado.</span><span class="sxs-lookup"><span data-stu-id="5c50f-126">If the [AppSearch](appsearch-action.md) action locates the signature, the installer overrides the initialized property value with the found value.</span></span> <span data-ttu-id="5c50f-127">Se a assinatura não for encontrada, o valor da propriedade inicial será usado.</span><span class="sxs-lookup"><span data-stu-id="5c50f-127">If the signature is not found, then the initial property value is used.</span></span> <span data-ttu-id="5c50f-128">Se a propriedade nunca foi inicializada, a propriedade só será definida se a assinatura for encontrada.</span><span class="sxs-lookup"><span data-stu-id="5c50f-128">If the property was never initialized, then the property will only be set if the signature is found.</span></span> <span data-ttu-id="5c50f-129">Caso contrário, a propriedade será indefinida.</span><span class="sxs-lookup"><span data-stu-id="5c50f-129">Otherwise, the property is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="5c50f-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="5c50f-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="5c50f-131">A \_ coluna assinatura contém um identificador exclusivo chamado assinatura e também uma chave externa nas tabelas [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)e [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5c50f-131">The Signature\_ column contains a unique identifier called a signature and is also an external key into the [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span> <span data-ttu-id="5c50f-132">Ao pesquisar um arquivo, o valor nessa coluna também deve ser uma chave estrangeira na tabela de [assinatura](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5c50f-132">When searching for a file, the value in this column must also be a foreign key into the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="5c50f-133">Se o valor nessa coluna não estiver listado na tabela de assinatura, o instalador determinará que a pesquisa é para um diretório.</span><span class="sxs-lookup"><span data-stu-id="5c50f-133">If the value in this column is not listed in the Signature table, the installer determines that the search is for a directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c50f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c50f-134">Remarks</span></span>

<span data-ttu-id="5c50f-135">A ação [AppSearch](appsearch-action.md) em [*tabelas de sequência*](s-gly.md) processa as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="5c50f-135">The [AppSearch](appsearch-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="5c50f-136">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="5c50f-136">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="5c50f-137">A ação [AppSearch](appsearch-action.md) pesquisa assinaturas usando a tabela [CompLocator](complocator-table.md) primeiro, a tabela [RegLocator](reglocator-table.md) segundo, a tabela [IniLocator](inilocator-table.md) terceira e, por fim, a tabela [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5c50f-137">The [AppSearch](appsearch-action.md) action searches for signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table second, the [IniLocator](inilocator-table.md) table third, and finally the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="5c50f-138">As assinaturas de arquivo são listadas na tabela de [assinatura](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5c50f-138">File signatures are listed in the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="5c50f-139">Uma assinatura que não está na tabela de assinatura denota um diretório e a ação define a propriedade como o caminho do diretório para essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c50f-139">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="5c50f-140">Consulte [pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="5c50f-140">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="5c50f-141">Validação</span><span class="sxs-lookup"><span data-stu-id="5c50f-141">Validation</span></span>

<dl>

[<span data-ttu-id="5c50f-142">ICE03</span><span class="sxs-lookup"><span data-stu-id="5c50f-142">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5c50f-143">ICE06</span><span class="sxs-lookup"><span data-stu-id="5c50f-143">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5c50f-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="5c50f-144">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="5c50f-145">ICE52</span><span class="sxs-lookup"><span data-stu-id="5c50f-145">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="5c50f-146">ICE88</span><span class="sxs-lookup"><span data-stu-id="5c50f-146">ICE88</span></span>](ice88.md)  
</dl>

 

 



