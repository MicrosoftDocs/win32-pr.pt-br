---
description: A tabela CompLocator contém as informações necessárias para localizar um arquivo ou diretório que está usando os dados de configuração do instalador.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Tabela CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506256"
---
# <a name="complocator-table"></a><span data-ttu-id="857da-103">Tabela CompLocator</span><span class="sxs-lookup"><span data-stu-id="857da-103">CompLocator Table</span></span>

<span data-ttu-id="857da-104">A tabela CompLocator contém as informações necessárias para localizar um arquivo ou diretório que está usando os dados de configuração do instalador.</span><span class="sxs-lookup"><span data-stu-id="857da-104">The CompLocator Table contains the information needed to find a file or directory that is using the installer configuration data.</span></span>

<span data-ttu-id="857da-105">A tabela CompLocator contém as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="857da-105">The CompLocator table contains the following information.</span></span>



| <span data-ttu-id="857da-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="857da-106">Column</span></span>      | <span data-ttu-id="857da-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="857da-107">Type</span></span>                         | <span data-ttu-id="857da-108">Chave</span><span class="sxs-lookup"><span data-stu-id="857da-108">Key</span></span> | <span data-ttu-id="857da-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="857da-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="857da-110">Signature\_</span><span class="sxs-lookup"><span data-stu-id="857da-110">Signature\_</span></span> | [<span data-ttu-id="857da-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="857da-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="857da-112">S</span><span class="sxs-lookup"><span data-stu-id="857da-112">Y</span></span>   | <span data-ttu-id="857da-113">N</span><span class="sxs-lookup"><span data-stu-id="857da-113">N</span></span>        |
| <span data-ttu-id="857da-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="857da-114">ComponentId</span></span> | [<span data-ttu-id="857da-115">GUID</span><span class="sxs-lookup"><span data-stu-id="857da-115">GUID</span></span>](guid.md)             | <span data-ttu-id="857da-116">N</span><span class="sxs-lookup"><span data-stu-id="857da-116">N</span></span>   | <span data-ttu-id="857da-117">N</span><span class="sxs-lookup"><span data-stu-id="857da-117">N</span></span>        |
| <span data-ttu-id="857da-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="857da-118">Type</span></span>        | [<span data-ttu-id="857da-119">Inteiro</span><span class="sxs-lookup"><span data-stu-id="857da-119">Integer</span></span>](integer.md)       | <span data-ttu-id="857da-120">N</span><span class="sxs-lookup"><span data-stu-id="857da-120">N</span></span>   | <span data-ttu-id="857da-121">S</span><span class="sxs-lookup"><span data-stu-id="857da-121">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="857da-122">Informações da coluna</span><span class="sxs-lookup"><span data-stu-id="857da-122">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="857da-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="857da-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="857da-124">Essa coluna representa uma assinatura de arquivo exclusiva e também a chave externa na [tabela de assinatura](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="857da-124">This column represents a unique file signature and is also the external key into the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="857da-125">Se a chave estiver ausente da tabela de assinatura, a pesquisa será considerada para a presença de um diretório apontado pela tabela CompLocator.</span><span class="sxs-lookup"><span data-stu-id="857da-125">If the key is absent from the Signature Table, the search is assumed to be for the presence of a directory pointed to by the CompLocator Table.</span></span>

</dd> <dt>

<span data-ttu-id="857da-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="857da-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="857da-127">A ID do componente cujo caminho de chave deve ser usado para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="857da-127">The component ID of the component whose key path is to be used for the search.</span></span> <span data-ttu-id="857da-128">Deve ser o GUID de um componente que aparece no campo ComponentID da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="857da-128">This should be the GUID of a component that appears in the ComponentId field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="857da-129">Pode ser a ID do componente de um componente pertencente a outro produto instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="857da-129">It may be the component ID of a component belonging to another product installed on the computer.</span></span> <span data-ttu-id="857da-130">Ele não deve ser o GUID de um componente publicado que aparece no campo ComponentID da [tabela PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="857da-130">It should not be the GUID of a published component appearing in the ComponentId field of the [PublishComponent Table](publishcomponent-table.md).</span></span>

<span data-ttu-id="857da-131">Para localizar o valor de GUID de ID de componente para um arquivo instalado por outro produto, vá para o pacote de instalação do produto.</span><span class="sxs-lookup"><span data-stu-id="857da-131">To find the component ID GUID value for a file installed by another product, go to the installation package of the product.</span></span> <span data-ttu-id="857da-132">Vá para a [tabela de arquivos](file-table.md) e localize a linha que contém o identificador de arquivo para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="857da-132">Go to the [File Table](file-table.md) and find the row that contains the file identifier for the file.</span></span> <span data-ttu-id="857da-133">A \_ coluna Component dessa linha contém o identificador de componente para o componente que controla o arquivo.</span><span class="sxs-lookup"><span data-stu-id="857da-133">The Component\_ column of this row contains the component identifier for the component that controls the file.</span></span> <span data-ttu-id="857da-134">Vá para a [tabela de componentes](component-table.md) e localize a linha que contém esse identificador de componente na coluna componente.</span><span class="sxs-lookup"><span data-stu-id="857da-134">Go to the [Component table](component-table.md) and find the row that contains this component identifier in the Component column.</span></span> <span data-ttu-id="857da-135">A coluna ComponentID desta linha contém o GUID da ID do componente.</span><span class="sxs-lookup"><span data-stu-id="857da-135">The ComponentId column of this row contains the component ID GUID.</span></span>

</dd> <dt>

<span data-ttu-id="857da-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva</span><span class="sxs-lookup"><span data-stu-id="857da-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="857da-137">Um valor booliano que determina se o caminho de chave do componente é um nome de arquivo ou um local de diretório.</span><span class="sxs-lookup"><span data-stu-id="857da-137">A Boolean value that determines if the key path of the component is a file name or a directory location.</span></span>

<span data-ttu-id="857da-138">A tabela a seguir lista os valores válidos.</span><span class="sxs-lookup"><span data-stu-id="857da-138">The following table lists valid values.</span></span> <span data-ttu-id="857da-139">Se estiver ausente, o tipo será definido como 1 (um).</span><span class="sxs-lookup"><span data-stu-id="857da-139">If absent, Type is set to be 1 (one).</span></span>



| <span data-ttu-id="857da-140">Constante</span><span class="sxs-lookup"><span data-stu-id="857da-140">Constant</span></span>                      | <span data-ttu-id="857da-141">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="857da-141">Hexadecimal</span></span> | <span data-ttu-id="857da-142">Decimal</span><span class="sxs-lookup"><span data-stu-id="857da-142">Decimal</span></span> | <span data-ttu-id="857da-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="857da-143">Description</span></span>              |
|-------------------------------|-------------|---------|--------------------------|
| <span data-ttu-id="857da-144">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="857da-144">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="857da-145">0x000</span><span class="sxs-lookup"><span data-stu-id="857da-145">0x000</span></span>       | <span data-ttu-id="857da-146">0</span><span class="sxs-lookup"><span data-stu-id="857da-146">0</span></span>       | <span data-ttu-id="857da-147">O caminho da chave é um diretório.</span><span class="sxs-lookup"><span data-stu-id="857da-147">Key path is a directory.</span></span> |
| <span data-ttu-id="857da-148">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="857da-148">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="857da-149">0x001</span><span class="sxs-lookup"><span data-stu-id="857da-149">0x001</span></span>       | <span data-ttu-id="857da-150">1</span><span class="sxs-lookup"><span data-stu-id="857da-150">1</span></span>       | <span data-ttu-id="857da-151">O caminho da chave é um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="857da-151">Key path is a file name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="857da-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="857da-152">Remarks</span></span>

<span data-ttu-id="857da-153">Essa tabela é usada com a [tabela AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="857da-153">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="857da-154">Normalmente, as colunas nesta tabela não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="857da-154">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="857da-155">Se um autor decidir procurar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="857da-155">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="857da-156">Para obter mais informações, consulte [pesquisando aplicativos existentes, arquivos, entradas de registro ou entradas de arquivo. ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="857da-156">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="857da-157">Validação</span><span class="sxs-lookup"><span data-stu-id="857da-157">Validation</span></span>

<dl>

[<span data-ttu-id="857da-158">ICE03</span><span class="sxs-lookup"><span data-stu-id="857da-158">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="857da-159">ICE06</span><span class="sxs-lookup"><span data-stu-id="857da-159">ICE06</span></span>](ice06.md)  
</dl>

 

 



