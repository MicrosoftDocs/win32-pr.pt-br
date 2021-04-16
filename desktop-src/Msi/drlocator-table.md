---
description: A tabela DrLocator contém as informações necessárias para localizar um arquivo ou diretório pesquisando a árvore de diretórios.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabela DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752459"
---
# <a name="drlocator-table"></a><span data-ttu-id="11141-103">Tabela DrLocator</span><span class="sxs-lookup"><span data-stu-id="11141-103">DrLocator Table</span></span>

<span data-ttu-id="11141-104">A tabela DrLocator contém as informações necessárias para localizar um arquivo ou diretório pesquisando a árvore de diretórios.</span><span class="sxs-lookup"><span data-stu-id="11141-104">The DrLocator table holds the information needed to find a file or directory by searching the directory tree.</span></span>

<span data-ttu-id="11141-105">A tabela DrLocator tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="11141-105">The DrLocator table has the following columns.</span></span>



| <span data-ttu-id="11141-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="11141-106">Column</span></span>      | <span data-ttu-id="11141-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="11141-107">Type</span></span>                         | <span data-ttu-id="11141-108">Chave</span><span class="sxs-lookup"><span data-stu-id="11141-108">Key</span></span> | <span data-ttu-id="11141-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="11141-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="11141-110">Signature\_</span><span class="sxs-lookup"><span data-stu-id="11141-110">Signature\_</span></span> | [<span data-ttu-id="11141-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="11141-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="11141-112">S</span><span class="sxs-lookup"><span data-stu-id="11141-112">Y</span></span>   | <span data-ttu-id="11141-113">N</span><span class="sxs-lookup"><span data-stu-id="11141-113">N</span></span>        |
| <span data-ttu-id="11141-114">Pai</span><span class="sxs-lookup"><span data-stu-id="11141-114">Parent</span></span>      | [<span data-ttu-id="11141-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="11141-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="11141-116">S</span><span class="sxs-lookup"><span data-stu-id="11141-116">Y</span></span>   | <span data-ttu-id="11141-117">S</span><span class="sxs-lookup"><span data-stu-id="11141-117">Y</span></span>        |
| <span data-ttu-id="11141-118">Caminho</span><span class="sxs-lookup"><span data-stu-id="11141-118">Path</span></span>        | [<span data-ttu-id="11141-119">AnyPath</span><span class="sxs-lookup"><span data-stu-id="11141-119">AnyPath</span></span>](anypath.md)       | <span data-ttu-id="11141-120">S</span><span class="sxs-lookup"><span data-stu-id="11141-120">Y</span></span>   | <span data-ttu-id="11141-121">S</span><span class="sxs-lookup"><span data-stu-id="11141-121">Y</span></span>        |
| <span data-ttu-id="11141-122">Profundidade</span><span class="sxs-lookup"><span data-stu-id="11141-122">Depth</span></span>       | [<span data-ttu-id="11141-123">Inteiro</span><span class="sxs-lookup"><span data-stu-id="11141-123">Integer</span></span>](integer.md)       | <span data-ttu-id="11141-124">N</span><span class="sxs-lookup"><span data-stu-id="11141-124">N</span></span>   | <span data-ttu-id="11141-125">S</span><span class="sxs-lookup"><span data-stu-id="11141-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="11141-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="11141-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="11141-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="11141-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="11141-128">A \_ coluna de assinatura é uma chave externa para a primeira coluna da [tabela de assinatura](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="11141-128">The Signature\_ column is an external key to the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="11141-129">Esse campo pode representar uma assinatura de arquivo exclusiva listada na tabela de assinatura.</span><span class="sxs-lookup"><span data-stu-id="11141-129">This field may represent a unique file signature listed in the Signature table.</span></span> <span data-ttu-id="11141-130">Se o valor nessa coluna estiver ausente da tabela de assinatura, a pesquisa será considerada para um diretório apontado pela tabela DrLocator.</span><span class="sxs-lookup"><span data-stu-id="11141-130">If the value in this column is absent from the Signature table, then the search is assumed to be for a directory pointed to by the DrLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="11141-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Primária</span><span class="sxs-lookup"><span data-stu-id="11141-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent</span></span>
</dt> <dd>

<span data-ttu-id="11141-132">Essa coluna é a assinatura do diretório pai do arquivo ou diretório na coluna de assinatura \_ .</span><span class="sxs-lookup"><span data-stu-id="11141-132">This column is the signature of the parent directory of the file or directory in the Signature\_ column.</span></span> <span data-ttu-id="11141-133">Se esse campo for nulo e a coluna de caminho não expandir para um caminho completo, todas as unidades fixas do sistema do usuário serão pesquisadas usando o caminho.</span><span class="sxs-lookup"><span data-stu-id="11141-133">If this field is null, and the Path column does not expand to a full path, then all the fixed drives of the user's system are searched by using the Path.</span></span>

<span data-ttu-id="11141-134">Esse campo é uma chave em uma das tabelas a seguir: as tabelas [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)ou DrLocator.</span><span class="sxs-lookup"><span data-stu-id="11141-134">This field is a key into one of the following tables: the [RegLocator](reglocator-table.md), the [IniLocator](inilocator-table.md), the [CompLocator](complocator-table.md), or the DrLocator tables.</span></span>

</dd> <dt>

<span data-ttu-id="11141-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Multi-Path</span><span class="sxs-lookup"><span data-stu-id="11141-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="11141-136">A coluna Path contém o caminho no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="11141-136">The Path column contains the path on the user's system.</span></span> <span data-ttu-id="11141-137">Este é um caminho completo ou um subcaminho relativo abaixo do diretório especificado na coluna pai.</span><span class="sxs-lookup"><span data-stu-id="11141-137">This is a either a full path or a relative subpath below the directory specified in the Parent column.</span></span> <span data-ttu-id="11141-138">Consulte as restrições no tipo de dados [AnyPath](anypath.md) .</span><span class="sxs-lookup"><span data-stu-id="11141-138">See the restrictions on the [AnyPath](anypath.md) data type.</span></span>

</dd> <dt>

<span data-ttu-id="11141-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Detalhado</span><span class="sxs-lookup"><span data-stu-id="11141-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Depth</span></span>
</dt> <dd>

<span data-ttu-id="11141-140">A profundidade abaixo do caminho que o instalador pesquisa pelo arquivo ou diretório especificado na \_ coluna assinatura.</span><span class="sxs-lookup"><span data-stu-id="11141-140">The depth below the path that the installer searches for the file or directory specified in the Signature\_ column.</span></span> <span data-ttu-id="11141-141">O valor usado no campo profundidade baseia-se em zero.</span><span class="sxs-lookup"><span data-stu-id="11141-141">The value used in the Depth field is based on zero.</span></span> <span data-ttu-id="11141-142">Por exemplo, se o campo caminho for c:/Arquivos de programas/bin, a coluna profundidade deverá ser definida como 0 ou maior para detectar um arquivo localizado dentro da pasta bin.</span><span class="sxs-lookup"><span data-stu-id="11141-142">For example, if the Path field is c:/Program Files/bin, the Depth column must be set to 0 or greater, to detect a file located inside the folder bin.</span></span> <span data-ttu-id="11141-143">Se o campo de profundidade estiver vazio, presume-se que a profundidade seja zero.</span><span class="sxs-lookup"><span data-stu-id="11141-143">If the Depth field is empty, the depth is assumed to be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11141-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="11141-144">Remarks</span></span>

<span data-ttu-id="11141-145">Essa tabela é usada com a [tabela AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="11141-145">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="11141-146">As colunas desta tabela geralmente não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="11141-146">This table's columns are generally not localized.</span></span> <span data-ttu-id="11141-147">Se um autor decidir procurar produtos em vários idiomas, deverá haver uma entrada separada incluída na tabela para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="11141-147">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="11141-148">Consulte [pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="11141-148">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="11141-149">Validação</span><span class="sxs-lookup"><span data-stu-id="11141-149">Validation</span></span>

<dl>

[<span data-ttu-id="11141-150">ICE03</span><span class="sxs-lookup"><span data-stu-id="11141-150">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="11141-151">ICE06</span><span class="sxs-lookup"><span data-stu-id="11141-151">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="11141-152">ICE46</span><span class="sxs-lookup"><span data-stu-id="11141-152">ICE46</span></span>](ice46.md)  
</dl>

 

 



