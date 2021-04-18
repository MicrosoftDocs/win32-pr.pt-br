---
description: Msitran.exe usa MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo e MsiDatabaseApplyTransform para gerar ou aplicar um arquivo de transformação. Essa ferramenta só está disponível nos componentes SDK do Windows para desenvolvedores de Windows Installer.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759211"
---
# <a name="msitranexe"></a><span data-ttu-id="5d432-103">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="5d432-103">Msitran.exe</span></span>

<span data-ttu-id="5d432-104">Msitran.exe usa [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)e [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) para gerar ou aplicar um arquivo de transformação.</span><span class="sxs-lookup"><span data-stu-id="5d432-104">Msitran.exe uses [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa), and [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) to generate or apply a transform file.</span></span>

<span data-ttu-id="5d432-105">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="5d432-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d432-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d432-106">Syntax</span></span>

<span data-ttu-id="5d432-107">Use a sintaxe a seguir para gerar uma transformação.</span><span class="sxs-lookup"><span data-stu-id="5d432-107">Use the following syntax to generate a transform.</span></span>

<span data-ttu-id="5d432-108">**msitran-g** *{banco de dados base} {REF DB} {nome do arquivo de transformação} \[ {condições de \] erro/condições de validação}*</span><span class="sxs-lookup"><span data-stu-id="5d432-108">**msitran -g** *{base db}{ref db}{transform file name}\[{error conditions / validation conditions}\]*</span></span>

<span data-ttu-id="5d432-109">Use a sintaxe a seguir para aplicar uma transformação</span><span class="sxs-lookup"><span data-stu-id="5d432-109">Use the following syntax to apply a transform</span></span>

<span data-ttu-id="5d432-110">**msitran-a** *{Transform} {banco de dados} \[ {condições \] de erro}*</span><span class="sxs-lookup"><span data-stu-id="5d432-110">**msitran -a** *{transform}{database}\[{error conditions}\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="5d432-111">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="5d432-111">Command Line Options</span></span>

<span data-ttu-id="5d432-112">Msitran.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5d432-112">Msitran.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="5d432-113">Um delimitador de barra também pode ser usado no lugar de um traço.</span><span class="sxs-lookup"><span data-stu-id="5d432-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="5d432-114">Opção</span><span class="sxs-lookup"><span data-stu-id="5d432-114">Option</span></span> | <span data-ttu-id="5d432-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d432-115">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="5d432-116">-g</span><span class="sxs-lookup"><span data-stu-id="5d432-116">-g</span></span>     | <span data-ttu-id="5d432-117">Geração de transformação.</span><span class="sxs-lookup"><span data-stu-id="5d432-117">Transform generation.</span></span>  |
| <span data-ttu-id="5d432-118">-a</span><span class="sxs-lookup"><span data-stu-id="5d432-118">-a</span></span>     | <span data-ttu-id="5d432-119">Aplicativo de transformação.</span><span class="sxs-lookup"><span data-stu-id="5d432-119">Transform application.</span></span> |



 

<span data-ttu-id="5d432-120">Os erros a seguir podem ser suprimidos ao aplicar uma transformação.</span><span class="sxs-lookup"><span data-stu-id="5d432-120">The following errors may be suppressed when applying a transform.</span></span> <span data-ttu-id="5d432-121">Para suprimir um erro, inclua o caractere apropriado no argumento {Error Conditions}.</span><span class="sxs-lookup"><span data-stu-id="5d432-121">To suppress an error, include the appropriate character in the {error conditions} argument.</span></span> <span data-ttu-id="5d432-122">As condições especificadas com-g são colocadas nas informações resumidas da transformação, mas não são usadas ao aplicar uma transformação com-a.</span><span class="sxs-lookup"><span data-stu-id="5d432-122">Conditions specified with -g are placed in the summary information of the transform, but are not used when applying a transform with -a.</span></span> <span data-ttu-id="5d432-123">Para obter informações, consulte [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span><span class="sxs-lookup"><span data-stu-id="5d432-123">For information, see [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span></span>



| <span data-ttu-id="5d432-124">Opção</span><span class="sxs-lookup"><span data-stu-id="5d432-124">Option</span></span> | <span data-ttu-id="5d432-125">Erro suprimido</span><span class="sxs-lookup"><span data-stu-id="5d432-125">Suppressed error</span></span>           |
|--------|----------------------------|
| <span data-ttu-id="5d432-126">um</span><span class="sxs-lookup"><span data-stu-id="5d432-126">a</span></span>      | <span data-ttu-id="5d432-127">Adicionar linha existente.</span><span class="sxs-lookup"><span data-stu-id="5d432-127">Add existing row.</span></span>          |
| <span data-ttu-id="5d432-128">b</span><span class="sxs-lookup"><span data-stu-id="5d432-128">b</span></span>      | <span data-ttu-id="5d432-129">Excluir linha inexistente.</span><span class="sxs-lookup"><span data-stu-id="5d432-129">Delete non-existing row.</span></span>   |
| <span data-ttu-id="5d432-130">c</span><span class="sxs-lookup"><span data-stu-id="5d432-130">c</span></span>      | <span data-ttu-id="5d432-131">Adicionar tabela existente.</span><span class="sxs-lookup"><span data-stu-id="5d432-131">Add existing table.</span></span>        |
| <span data-ttu-id="5d432-132">d</span><span class="sxs-lookup"><span data-stu-id="5d432-132">d</span></span>      | <span data-ttu-id="5d432-133">Excluir tabela não existente.</span><span class="sxs-lookup"><span data-stu-id="5d432-133">Delete non-existing table.</span></span> |
| <span data-ttu-id="5d432-134">e</span><span class="sxs-lookup"><span data-stu-id="5d432-134">e</span></span>      | <span data-ttu-id="5d432-135">Modificar a linha existente.</span><span class="sxs-lookup"><span data-stu-id="5d432-135">Modify existing row.</span></span>       |
| <span data-ttu-id="5d432-136">f</span><span class="sxs-lookup"><span data-stu-id="5d432-136">f</span></span>      | <span data-ttu-id="5d432-137">Altere a página de código.</span><span class="sxs-lookup"><span data-stu-id="5d432-137">Change codepage.</span></span>           |



 

<span data-ttu-id="5d432-138">As condições de validação a seguir podem ser usadas para indicar quando uma transformação pode ser aplicada a um pacote.</span><span class="sxs-lookup"><span data-stu-id="5d432-138">The following validation conditions may be used to indicate when a transform may be applied to a package.</span></span> <span data-ttu-id="5d432-139">Essas condições podem ser especificadas com-g, mas não-a.</span><span class="sxs-lookup"><span data-stu-id="5d432-139">These conditions may be specified with -g, but not -a.</span></span>



| <span data-ttu-id="5d432-140">Opção</span><span class="sxs-lookup"><span data-stu-id="5d432-140">Option</span></span> | <span data-ttu-id="5d432-141">Condição de validação</span><span class="sxs-lookup"><span data-stu-id="5d432-141">Validation condition</span></span>                                  |
|--------|-------------------------------------------------------|
| <span data-ttu-id="5d432-142">g</span><span class="sxs-lookup"><span data-stu-id="5d432-142">g</span></span>      | <span data-ttu-id="5d432-143">Verifique o código de atualização.</span><span class="sxs-lookup"><span data-stu-id="5d432-143">Check upgrade code.</span></span>                                   |
| <span data-ttu-id="5d432-144">l</span><span class="sxs-lookup"><span data-stu-id="5d432-144">l</span></span>      | <span data-ttu-id="5d432-145">Verificar idioma.</span><span class="sxs-lookup"><span data-stu-id="5d432-145">Check language.</span></span>                                       |
| <span data-ttu-id="5d432-146">p</span><span class="sxs-lookup"><span data-stu-id="5d432-146">p</span></span>      | <span data-ttu-id="5d432-147">Verifique a plataforma.</span><span class="sxs-lookup"><span data-stu-id="5d432-147">Check platform.</span></span>                                       |
| <span data-ttu-id="5d432-148">r</span><span class="sxs-lookup"><span data-stu-id="5d432-148">r</span></span>      | <span data-ttu-id="5d432-149">Verifique o produto.</span><span class="sxs-lookup"><span data-stu-id="5d432-149">Check product.</span></span>                                        |
| <span data-ttu-id="5d432-150">s</span><span class="sxs-lookup"><span data-stu-id="5d432-150">s</span></span>      | <span data-ttu-id="5d432-151">Verifique somente a versão principal.</span><span class="sxs-lookup"><span data-stu-id="5d432-151">Check major version only.</span></span>                             |
| <span data-ttu-id="5d432-152">t</span><span class="sxs-lookup"><span data-stu-id="5d432-152">t</span></span>      | <span data-ttu-id="5d432-153">Verifique apenas as versões principal e secundária.</span><span class="sxs-lookup"><span data-stu-id="5d432-153">Check major and minor versions only.</span></span>                  |
| <span data-ttu-id="5d432-154">u</span><span class="sxs-lookup"><span data-stu-id="5d432-154">u</span></span>      | <span data-ttu-id="5d432-155">Verifique as versões principal, secundária e de atualização.</span><span class="sxs-lookup"><span data-stu-id="5d432-155">Check major, minor, and upgrade versions.</span></span>             |
| <span data-ttu-id="5d432-156">v</span><span class="sxs-lookup"><span data-stu-id="5d432-156">v</span></span>      | <span data-ttu-id="5d432-157">Versão do banco de dados aplicada < versão do banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="5d432-157">Applied database version < Base database version.</span></span>  |
| <span data-ttu-id="5d432-158">w</span><span class="sxs-lookup"><span data-stu-id="5d432-158">w</span></span>      | <span data-ttu-id="5d432-159">Versão do banco de dados aplicada <= versão do banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="5d432-159">Applied database version <= Base database version.</span></span> |
| <span data-ttu-id="5d432-160">x</span><span class="sxs-lookup"><span data-stu-id="5d432-160">x</span></span>      | <span data-ttu-id="5d432-161">Versão do banco de dados aplicada = versão do banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="5d432-161">Applied database version = Base database version.</span></span>     |
| <span data-ttu-id="5d432-162">a</span><span class="sxs-lookup"><span data-stu-id="5d432-162">y</span></span>      | <span data-ttu-id="5d432-163">Versão do banco de dados aplicada >= versão do banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="5d432-163">Applied database version >= Base database version.</span></span> |
| <span data-ttu-id="5d432-164">z</span><span class="sxs-lookup"><span data-stu-id="5d432-164">z</span></span>      | <span data-ttu-id="5d432-165">Versão do banco de dados aplicada > versão do banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="5d432-165">Applied database version > Base database version.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="5d432-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d432-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d432-167">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5d432-167">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="5d432-168">Transformações de banco de dados</span><span class="sxs-lookup"><span data-stu-id="5d432-168">Database Transforms</span></span>](database-transforms.md)
</dt> <dt>

[<span data-ttu-id="5d432-169">Um exemplo de transformação de personalização</span><span class="sxs-lookup"><span data-stu-id="5d432-169">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> <dt>

[<span data-ttu-id="5d432-170">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="5d432-170">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



