---
description: A tabela ActionText contém o texto a ser exibido em uma caixa de diálogo de progresso e gravada no log para ações que levam muito tempo para serem executadas. O texto exibido consiste na descrição da ação e, opcionalmente, nos dados formatados da ação.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabela ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756746"
---
# <a name="actiontext-table"></a><span data-ttu-id="809a2-104">Tabela ActionText</span><span class="sxs-lookup"><span data-stu-id="809a2-104">ActionText Table</span></span>

<span data-ttu-id="809a2-105">A tabela ActionText contém o texto a ser exibido em uma caixa de diálogo de progresso e gravada no log para ações que levam muito tempo para serem executadas.</span><span class="sxs-lookup"><span data-stu-id="809a2-105">The ActionText Table contains text to be displayed in a progress dialog box, and written to the log for actions that take a long time to execute.</span></span> <span data-ttu-id="809a2-106">O texto exibido consiste na descrição da ação e, opcionalmente, nos dados formatados da ação.</span><span class="sxs-lookup"><span data-stu-id="809a2-106">The displayed text consists of the action description and optionally formatted data from the action.</span></span>

<span data-ttu-id="809a2-107">A tabela ActionText tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="809a2-107">The ActionText Table has the following columns.</span></span>



| <span data-ttu-id="809a2-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="809a2-108">Column</span></span>      | <span data-ttu-id="809a2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="809a2-109">Type</span></span>                         | <span data-ttu-id="809a2-110">Chave</span><span class="sxs-lookup"><span data-stu-id="809a2-110">Key</span></span> | <span data-ttu-id="809a2-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="809a2-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="809a2-112">Ação</span><span class="sxs-lookup"><span data-stu-id="809a2-112">Action</span></span>      | [<span data-ttu-id="809a2-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="809a2-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="809a2-114">S</span><span class="sxs-lookup"><span data-stu-id="809a2-114">Y</span></span>   | <span data-ttu-id="809a2-115">N</span><span class="sxs-lookup"><span data-stu-id="809a2-115">N</span></span>        |
| <span data-ttu-id="809a2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="809a2-116">Description</span></span> | [<span data-ttu-id="809a2-117">Text</span><span class="sxs-lookup"><span data-stu-id="809a2-117">Text</span></span>](text.md)             | <span data-ttu-id="809a2-118">N</span><span class="sxs-lookup"><span data-stu-id="809a2-118">N</span></span>   | <span data-ttu-id="809a2-119">S</span><span class="sxs-lookup"><span data-stu-id="809a2-119">Y</span></span>        |
| <span data-ttu-id="809a2-120">Modelo</span><span class="sxs-lookup"><span data-stu-id="809a2-120">Template</span></span>    | [<span data-ttu-id="809a2-121">Modelo</span><span class="sxs-lookup"><span data-stu-id="809a2-121">Template</span></span>](template.md)     | <span data-ttu-id="809a2-122">N</span><span class="sxs-lookup"><span data-stu-id="809a2-122">N</span></span>   | <span data-ttu-id="809a2-123">S</span><span class="sxs-lookup"><span data-stu-id="809a2-123">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="809a2-124">Colunas</span><span class="sxs-lookup"><span data-stu-id="809a2-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="809a2-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="809a2-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="809a2-126">Nome da ação.</span><span class="sxs-lookup"><span data-stu-id="809a2-126">Name of the action.</span></span>

<span data-ttu-id="809a2-127">Chave de tabela primária.</span><span class="sxs-lookup"><span data-stu-id="809a2-127">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="809a2-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="809a2-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="809a2-129">Descrição localizada que é exibida na caixa de diálogo de progresso ou gravada no log quando a ação está em execução.</span><span class="sxs-lookup"><span data-stu-id="809a2-129">Localized description that is displayed in the progress dialog box, or written to the log when the action is executing.</span></span>

</dd> <dt>

<span data-ttu-id="809a2-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Modelos</span><span class="sxs-lookup"><span data-stu-id="809a2-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Template</span></span>
</dt> <dd>

<span data-ttu-id="809a2-131">Um modelo de formato localizado que é usado para formatar registros de dados de ação a serem exibidos durante a execução da ação.</span><span class="sxs-lookup"><span data-stu-id="809a2-131">A localized format template that is used to format action data records to display during action execution.</span></span> <span data-ttu-id="809a2-132">Se um modelo não for fornecido, os dados de ação não serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="809a2-132">If a template is not supplied, then the action data is not displayed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="809a2-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="809a2-133">Remarks</span></span>

<span data-ttu-id="809a2-134">Normalmente, as entradas na tabela ActionText referem-se a ações em tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="809a2-134">Typically, the entries in the ActionText table refer to actions in sequence tables.</span></span> <span data-ttu-id="809a2-135">Há outras ações que o instalador executa que não estão listadas na tabela de sequência, mas que ainda precisam ser especificadas na tabela.</span><span class="sxs-lookup"><span data-stu-id="809a2-135">There are other actions the installer performs that are not listed in the sequence table, but still need to be specified in the table.</span></span> <span data-ttu-id="809a2-136">A tabela a seguir identifica as entradas de tabela necessárias nas quais o nome e o modelo da ação devem ser criados exatamente como mostrado, mas a descrição pode ser personalizada.</span><span class="sxs-lookup"><span data-stu-id="809a2-136">The following table identifies the required table entries where the action name and template must be authored exactly as shown, but the description can be customized.</span></span>



| <span data-ttu-id="809a2-137">Ação</span><span class="sxs-lookup"><span data-stu-id="809a2-137">Action</span></span>          | <span data-ttu-id="809a2-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="809a2-138">Description</span></span>                             | <span data-ttu-id="809a2-139">Modelo</span><span class="sxs-lookup"><span data-stu-id="809a2-139">Template</span></span> |
|-----------------|-----------------------------------------|----------|
| <span data-ttu-id="809a2-140">Reversão</span><span class="sxs-lookup"><span data-stu-id="809a2-140">Rollback</span></span>        | <span data-ttu-id="809a2-141">Desfaz ações.</span><span class="sxs-lookup"><span data-stu-id="809a2-141">Undoes actions.</span></span>                         | <span data-ttu-id="809a2-142">\[1\]</span><span class="sxs-lookup"><span data-stu-id="809a2-142">\[1\]</span></span>    |
| <span data-ttu-id="809a2-143">RollbackCleanup</span><span class="sxs-lookup"><span data-stu-id="809a2-143">RollbackCleanup</span></span> | <span data-ttu-id="809a2-144">Remove arquivos antigos.</span><span class="sxs-lookup"><span data-stu-id="809a2-144">Removes old files.</span></span>                      | <span data-ttu-id="809a2-145">\[1\]</span><span class="sxs-lookup"><span data-stu-id="809a2-145">\[1\]</span></span>    |
| <span data-ttu-id="809a2-146">GenerateScript</span><span class="sxs-lookup"><span data-stu-id="809a2-146">GenerateScript</span></span>  | <span data-ttu-id="809a2-147">Gera operações do sistema para ação.</span><span class="sxs-lookup"><span data-stu-id="809a2-147">Generates system operations for action.</span></span> | <span data-ttu-id="809a2-148">\[1\]</span><span class="sxs-lookup"><span data-stu-id="809a2-148">\[1\]</span></span>    |



 

> [!Note]  
> <span data-ttu-id="809a2-149">O texto da ação só é exibido para ações executadas dentro do script de instalação.</span><span class="sxs-lookup"><span data-stu-id="809a2-149">Action text is only displayed for actions that run within the installation script.</span></span> <span data-ttu-id="809a2-150">Portanto, o texto da ação só é exibido para ações sequenciadas entre as ações [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="809a2-150">Therefore, action text is only displayed for actions that are sequenced between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

 

<span data-ttu-id="809a2-151">Você pode importar uma tabela ActionText localizada para seu banco de dados usando Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="809a2-151">You can import a localized ActionText table into your database by using Msidb.exe or [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="809a2-152">O SDK inclui uma tabela ActionText localizada para cada um dos idiomas listados na seção [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) .</span><span class="sxs-lookup"><span data-stu-id="809a2-152">The SDK includes a localized ActionText Table for each of the languages listed in the [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) section.</span></span> <span data-ttu-id="809a2-153">Se a tabela ActionText não for populada, o instalador carregará cadeias de caracteres localizadas para o idioma especificado pela propriedade [**ProductLanguage**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="809a2-153">If the ActionText table is not populated, the installer loads localized strings for the language specified by the [**ProductLanguage**](productlanguage.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="809a2-154">Validação</span><span class="sxs-lookup"><span data-stu-id="809a2-154">Validation</span></span>

<dl>

[<span data-ttu-id="809a2-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="809a2-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="809a2-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="809a2-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="809a2-157">ICE46</span><span class="sxs-lookup"><span data-stu-id="809a2-157">ICE46</span></span>](ice46.md)  
</dl>

 

 



