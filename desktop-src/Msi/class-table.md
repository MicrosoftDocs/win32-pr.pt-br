---
description: A tabela de classes contém informações relacionadas ao servidor COM que devem ser geradas como parte do anúncio do produto. Cada linha pode gerar um conjunto de valores e chaves do registro. As informações de ProgId associadas estão incluídas nesta tabela.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabela de classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758968"
---
# <a name="class-table"></a><span data-ttu-id="c8faf-105">Tabela de classes</span><span class="sxs-lookup"><span data-stu-id="c8faf-105">Class Table</span></span>

<span data-ttu-id="c8faf-106">A tabela de classes contém informações relacionadas ao servidor COM que devem ser geradas como parte do anúncio do produto.</span><span class="sxs-lookup"><span data-stu-id="c8faf-106">The Class table contains COM server-related information that must be generated as a part of the product advertisement.</span></span> <span data-ttu-id="c8faf-107">Cada linha pode gerar um conjunto de valores e chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="c8faf-107">Each row may generate a set of registry keys and values.</span></span> <span data-ttu-id="c8faf-108">As informações de ProgId associadas estão incluídas nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="c8faf-108">The associated ProgId information is included in this table.</span></span>

<span data-ttu-id="c8faf-109">A tabela de classes tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8faf-109">The Class table has the following columns.</span></span>



| <span data-ttu-id="c8faf-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="c8faf-110">Column</span></span>           | <span data-ttu-id="c8faf-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8faf-111">Type</span></span>                         | <span data-ttu-id="c8faf-112">Chave</span><span class="sxs-lookup"><span data-stu-id="c8faf-112">Key</span></span> | <span data-ttu-id="c8faf-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="c8faf-113">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="c8faf-114">CLSID</span><span class="sxs-lookup"><span data-stu-id="c8faf-114">CLSID</span></span>            | [<span data-ttu-id="c8faf-115">GUID</span><span class="sxs-lookup"><span data-stu-id="c8faf-115">GUID</span></span>](guid.md)             | <span data-ttu-id="c8faf-116">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-116">Y</span></span>   | <span data-ttu-id="c8faf-117">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-117">N</span></span>        |
| <span data-ttu-id="c8faf-118">Contexto</span><span class="sxs-lookup"><span data-stu-id="c8faf-118">Context</span></span>          | [<span data-ttu-id="c8faf-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="c8faf-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="c8faf-120">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-120">Y</span></span>   | <span data-ttu-id="c8faf-121">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-121">N</span></span>        |
| <span data-ttu-id="c8faf-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c8faf-122">Component\_</span></span>      | [<span data-ttu-id="c8faf-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="c8faf-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="c8faf-124">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-124">Y</span></span>   | <span data-ttu-id="c8faf-125">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-125">N</span></span>        |
| <span data-ttu-id="c8faf-126">ProgId \_ padrão</span><span class="sxs-lookup"><span data-stu-id="c8faf-126">ProgId\_Default</span></span>  | [<span data-ttu-id="c8faf-127">Text</span><span class="sxs-lookup"><span data-stu-id="c8faf-127">Text</span></span>](text.md)             | <span data-ttu-id="c8faf-128">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-128">N</span></span>   | <span data-ttu-id="c8faf-129">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-129">Y</span></span>        |
| <span data-ttu-id="c8faf-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8faf-130">Description</span></span>      | [<span data-ttu-id="c8faf-131">Text</span><span class="sxs-lookup"><span data-stu-id="c8faf-131">Text</span></span>](text.md)             | <span data-ttu-id="c8faf-132">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-132">N</span></span>   | <span data-ttu-id="c8faf-133">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-133">Y</span></span>        |
| <span data-ttu-id="c8faf-134">AppId\_</span><span class="sxs-lookup"><span data-stu-id="c8faf-134">AppId\_</span></span>          | [<span data-ttu-id="c8faf-135">GUID</span><span class="sxs-lookup"><span data-stu-id="c8faf-135">GUID</span></span>](guid.md)             | <span data-ttu-id="c8faf-136">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-136">N</span></span>   | <span data-ttu-id="c8faf-137">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-137">Y</span></span>        |
| <span data-ttu-id="c8faf-138">FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="c8faf-138">FileTypeMask</span></span>     | [<span data-ttu-id="c8faf-139">Text</span><span class="sxs-lookup"><span data-stu-id="c8faf-139">Text</span></span>](text.md)             | <span data-ttu-id="c8faf-140">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-140">N</span></span>   | <span data-ttu-id="c8faf-141">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-141">Y</span></span>        |
| <span data-ttu-id="c8faf-142">ícone\_</span><span class="sxs-lookup"><span data-stu-id="c8faf-142">Icon\_</span></span>           | [<span data-ttu-id="c8faf-143">Identificador</span><span class="sxs-lookup"><span data-stu-id="c8faf-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="c8faf-144">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-144">N</span></span>   | <span data-ttu-id="c8faf-145">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-145">Y</span></span>        |
| <span data-ttu-id="c8faf-146">IconIndex</span><span class="sxs-lookup"><span data-stu-id="c8faf-146">IconIndex</span></span>        | [<span data-ttu-id="c8faf-147">Inteiro</span><span class="sxs-lookup"><span data-stu-id="c8faf-147">Integer</span></span>](integer.md)       | <span data-ttu-id="c8faf-148">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-148">N</span></span>   | <span data-ttu-id="c8faf-149">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-149">Y</span></span>        |
| <span data-ttu-id="c8faf-150">DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="c8faf-150">DefInprocHandler</span></span> | [<span data-ttu-id="c8faf-151">Filename</span><span class="sxs-lookup"><span data-stu-id="c8faf-151">Filename</span></span>](filename.md)     | <span data-ttu-id="c8faf-152">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-152">N</span></span>   | <span data-ttu-id="c8faf-153">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-153">Y</span></span>        |
| <span data-ttu-id="c8faf-154">Argumento</span><span class="sxs-lookup"><span data-stu-id="c8faf-154">Argument</span></span>         | [<span data-ttu-id="c8faf-155">Binário</span><span class="sxs-lookup"><span data-stu-id="c8faf-155">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c8faf-156">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-156">N</span></span>   | <span data-ttu-id="c8faf-157">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-157">Y</span></span>        |
| <span data-ttu-id="c8faf-158">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="c8faf-158">Feature\_</span></span>        | [<span data-ttu-id="c8faf-159">Identificador</span><span class="sxs-lookup"><span data-stu-id="c8faf-159">Identifier</span></span>](identifier.md) | <span data-ttu-id="c8faf-160">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-160">N</span></span>   | <span data-ttu-id="c8faf-161">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-161">N</span></span>        |
| <span data-ttu-id="c8faf-162">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8faf-162">Attributes</span></span>       | [<span data-ttu-id="c8faf-163">Inteiro</span><span class="sxs-lookup"><span data-stu-id="c8faf-163">Integer</span></span>](integer.md)       | <span data-ttu-id="c8faf-164">N</span><span class="sxs-lookup"><span data-stu-id="c8faf-164">N</span></span>   | <span data-ttu-id="c8faf-165">S</span><span class="sxs-lookup"><span data-stu-id="c8faf-165">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="c8faf-166">Informações da coluna</span><span class="sxs-lookup"><span data-stu-id="c8faf-166">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="c8faf-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span><span class="sxs-lookup"><span data-stu-id="c8faf-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-168">O identificador de classe (ID) de um servidor COM.</span><span class="sxs-lookup"><span data-stu-id="c8faf-168">The Class identifier (ID) of a COM server.</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Noticioso</span><span class="sxs-lookup"><span data-stu-id="c8faf-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Context</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-170">O contexto do servidor para este servidor.</span><span class="sxs-lookup"><span data-stu-id="c8faf-170">The server context for this server.</span></span> <span data-ttu-id="c8faf-171">Insira um dos valores a seguir para a chave CLSID.</span><span class="sxs-lookup"><span data-stu-id="c8faf-171">Enter one of the following values for the CLSID Key.</span></span>



| <span data-ttu-id="c8faf-172">CHAVE CLSID</span><span class="sxs-lookup"><span data-stu-id="c8faf-172">CLSID KEY</span></span>                             | <span data-ttu-id="c8faf-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8faf-173">Description</span></span>                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="c8faf-174">LocalServer</span><span class="sxs-lookup"><span data-stu-id="c8faf-174">LocalServer</span></span>](../com/localserver.md)       | <span data-ttu-id="c8faf-175">Especifica o caminho completo para um aplicativo de servidor local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c8faf-175">Specifies the full path to a 16-bit local server application.</span></span>             |
| [<span data-ttu-id="c8faf-176">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="c8faf-176">LocalServer32</span></span>](../com/localserver32.md)   | <span data-ttu-id="c8faf-177">Especifica o caminho completo para um aplicativo de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c8faf-177">Specifies the full path to a 32-bit local server application.</span></span>             |
| [<span data-ttu-id="c8faf-178">InprocServer</span><span class="sxs-lookup"><span data-stu-id="c8faf-178">InprocServer</span></span>](../com/inprocserver.md)     | <span data-ttu-id="c8faf-179">Especifica o caminho para uma DLL de servidor em processo.</span><span class="sxs-lookup"><span data-stu-id="c8faf-179">Specifies the path to an in-process server DLL.</span></span>                           |
| [<span data-ttu-id="c8faf-180">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="c8faf-180">InprocServer32</span></span>](../com/inprocserver32.md) | <span data-ttu-id="c8faf-181">Especifica o caminho para um servidor em processo de 32 bits e o modelo de Threading.</span><span class="sxs-lookup"><span data-stu-id="c8faf-181">Specifies the path to a 32-bit in-process server and the threading model.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c8faf-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="c8faf-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-183">Chave externa na [tabela de componentes](component-table.md) especificando o componente cujo arquivo de chave fornece o servidor com.</span><span class="sxs-lookup"><span data-stu-id="c8faf-183">External key into the [Component table](component-table.md) specifying the component whose key file provides the COM server.</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId \_ padrão</span><span class="sxs-lookup"><span data-stu-id="c8faf-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId\_Default</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-185">A ID de programa padrão associada a essa ID de classe.</span><span class="sxs-lookup"><span data-stu-id="c8faf-185">The default Program ID associated with this Class ID.</span></span> <span data-ttu-id="c8faf-186">Esta coluna é uma chave estrangeira na [tabela ProgID](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8faf-186">This column is a foreign key into the [ProgID table](progid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="c8faf-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-188">Descrição localizada associada à ID da classe e à ID do programa.</span><span class="sxs-lookup"><span data-stu-id="c8faf-188">Localized description associated with the Class ID and Program ID.</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span><span class="sxs-lookup"><span data-stu-id="c8faf-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-190">ID do aplicativo que contém informações de DCOM para o aplicativo associado ( [GUID](guid.md)da cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="c8faf-190">Application ID containing DCOM information for the associated application (string [GUID](guid.md)).</span></span> <span data-ttu-id="c8faf-191">Esta coluna é uma chave estrangeira na [tabela AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8faf-191">This column is a foreign key into the [AppId table](appid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="c8faf-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-193">Contém informações para a chave HKCR (esta CLSID).</span><span class="sxs-lookup"><span data-stu-id="c8faf-193">Contains information for the HKCR (this CLSID) key.</span></span>

<span data-ttu-id="c8faf-194">Se existirem vários padrões, eles deverão ser delimitados por ponto e vírgula, e subchaves numéricas serão geradas: 0, 1, 2... Para obter mais informações sobre essa funcionalidade, consulte [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span><span class="sxs-lookup"><span data-stu-id="c8faf-194">If multiple patterns exist, they must be delimited by a semicolon, and numeric subkeys are generated: 0, 1, 2... For more information about this functionality, see [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Cone\_</span><span class="sxs-lookup"><span data-stu-id="c8faf-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-196">O arquivo que fornece o ícone associado a este CLSID.</span><span class="sxs-lookup"><span data-stu-id="c8faf-196">The file providing the icon associated with this CLSID.</span></span> <span data-ttu-id="c8faf-197">O instalador grava a entrada nesta coluna sob a chave DefaultIcon associada ao ProgId.</span><span class="sxs-lookup"><span data-stu-id="c8faf-197">The installer writes the entry in this column under the DefaultIcon key associated with the ProgId.</span></span> <span data-ttu-id="c8faf-198">Se não for NULL, a coluna será uma chave estrangeira na tabela de [ícones](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8faf-198">If it is not null, the column is a foreign key into the [Icon table](icon-table.md).</span></span> <span data-ttu-id="c8faf-199">Se for NULL, o servidor COM fornecerá o recurso de ícone.</span><span class="sxs-lookup"><span data-stu-id="c8faf-199">If it is null, the COM server provides the icon resource.</span></span> <span data-ttu-id="c8faf-200">Associações de arquivo anunciadas e atalhos exigem um valor não nulo nesta coluna para serem exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="c8faf-200">Advertised file associations and shortcuts require a non-null value in this column to display properly.</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="c8faf-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-202">Índice de ícone no arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="c8faf-202">Icon index into the icon file.</span></span> <span data-ttu-id="c8faf-203">Isso pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="c8faf-203">This can be null.</span></span>

<span data-ttu-id="c8faf-204">Somente números não negativos.</span><span class="sxs-lookup"><span data-stu-id="c8faf-204">Non-negative numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="c8faf-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-206">Este campo especifica o manipulador em processo padrão para o contexto de servidor especificado no campo de contexto.</span><span class="sxs-lookup"><span data-stu-id="c8faf-206">This field specifies the default in-process handler for the server context specified in the Context field.</span></span>

<span data-ttu-id="c8faf-207">Esse campo deverá ser nulo se uma chave CLSID InprocServer ou InprocServer aparecer no campo de contexto.</span><span class="sxs-lookup"><span data-stu-id="c8faf-207">This field must be Null if an InprocServer or InprocServer CLSID key appears in the Context field.</span></span>

<span data-ttu-id="c8faf-208">Se uma chave de CLSID LocalServer ou LocalServer32 aparecer no campo de contexto, o valor no campo DefInprocHandler identificará o manipulador em processo padrão.</span><span class="sxs-lookup"><span data-stu-id="c8faf-208">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the value in the DefInprocHandler field identifies the default in-process handler.</span></span>



| <span data-ttu-id="c8faf-209">Valor</span><span class="sxs-lookup"><span data-stu-id="c8faf-209">Value</span></span>                | <span data-ttu-id="c8faf-210">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8faf-210">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8faf-211">valor não numérico</span><span class="sxs-lookup"><span data-stu-id="c8faf-211">non-numeric value</span></span>    | <span data-ttu-id="c8faf-212">O instalador trata um valor não numérico no campo DefInprocHandler como um arquivo do sistema que serve como o manipulador de 32 bits no processo especificado pela chave InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="c8faf-212">The installer treats a non-numeric value in the DefInprocHandler field as a system file serving as the 32-bit in-process handler specified by the InprocHandler32 key.</span></span>                                                                                                            |
| <span data-ttu-id="c8faf-213">Nulo</span><span class="sxs-lookup"><span data-stu-id="c8faf-213">Null</span></span>                 | <span data-ttu-id="c8faf-214">Os campos DefInprocHandler e Argument podem ser nulos para uma chave CLSID LocalServer ou LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="c8faf-214">The DefInprocHandler and Argument fields can both be Null for a LocalServer or LocalServer32 CLSID key.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="c8faf-215">1 = padrão (sistema)</span><span class="sxs-lookup"><span data-stu-id="c8faf-215">1 = default (system)</span></span> | <span data-ttu-id="c8faf-216">O padrão é o manipulador no processo de 16 bits especificado por InprocHandler.</span><span class="sxs-lookup"><span data-stu-id="c8faf-216">The default is the 16-bit in-process handler specified by InprocHandler.</span></span> <span data-ttu-id="c8faf-217">Nesse caso, o valor de InprocHandler é o nome no registro sob o qual o valor do manipulador in-Process padrão é armazenado.</span><span class="sxs-lookup"><span data-stu-id="c8faf-217">In this case, the value of InprocHandler is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="c8faf-218">Por exemplo, HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="c8faf-218">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span>     |
| <span data-ttu-id="c8faf-219">2 = padrão (sistema)</span><span class="sxs-lookup"><span data-stu-id="c8faf-219">2 = default (system)</span></span> | <span data-ttu-id="c8faf-220">O padrão é o manipulador no processo de 32 bits especificado por InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="c8faf-220">The default is the 32-bit in-process handler specified by InprocHandler32.</span></span> <span data-ttu-id="c8faf-221">Nesse caso, o valor de InprocHandler32 é o nome no registro sob o qual o valor do manipulador in-Process padrão é armazenado.</span><span class="sxs-lookup"><span data-stu-id="c8faf-221">In this case, the value of InprocHandler32 is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="c8faf-222">Por exemplo, HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="c8faf-222">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span> |
| <span data-ttu-id="c8faf-223">3 = padrão (sistema)</span><span class="sxs-lookup"><span data-stu-id="c8faf-223">3 = default (system)</span></span> | <span data-ttu-id="c8faf-224">O padrão é um manipulador no processo de 16 bits ou 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c8faf-224">The default is a 16-bit or 32-bit in-process handler.</span></span>                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="c8faf-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento</span><span class="sxs-lookup"><span data-stu-id="c8faf-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-226">Se uma chave de CLSID de LocalServer ou LocalServer32 aparecer no campo de contexto, o texto nesse campo será registrado como o argumento no servidor e será usado pelo COM para invocar o servidor.</span><span class="sxs-lookup"><span data-stu-id="c8faf-226">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the text in this field is registered as the argument against the server and is used by COM to invoke the server.</span></span> <span data-ttu-id="c8faf-227">Os campos DefInprocHandler e Argument poderão ser nulos se LocalServer ou LocalServer32 aparecerem no campo de contexto.</span><span class="sxs-lookup"><span data-stu-id="c8faf-227">The DefInprocHandler and Argument fields can both be Null if LocalServer or LocalServer32 appears in the Context field.</span></span>

<span data-ttu-id="c8faf-228">Observe que a resolução das propriedades no campo argumento é limitada.</span><span class="sxs-lookup"><span data-stu-id="c8faf-228">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="c8faf-229">Uma propriedade formatada como \[ propriedade \] nesse campo só poderá ser resolvida se a propriedade já tiver o valor pretendido quando o componente proprietário da classe for instalado.</span><span class="sxs-lookup"><span data-stu-id="c8faf-229">A property formatted as \[Property\] in this field can only be resolved if the property already has the intended value when the component owning the class is installed.</span></span> <span data-ttu-id="c8faf-230">Por exemplo, para o argumento " \[ \#MyDoc.doc\] " para resolver o valor correto, o mesmo processo deve estar instalando o arquivo MyDoc.doc e o componente que possui a classe.</span><span class="sxs-lookup"><span data-stu-id="c8faf-230">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the class.</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_</span><span class="sxs-lookup"><span data-stu-id="c8faf-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-232">Chave externa na [tabela de recursos](feature-table.md) que especifica o recurso que fornece o servidor com.</span><span class="sxs-lookup"><span data-stu-id="c8faf-232">External key into the [Feature table](feature-table.md) specifying the feature that provides the COM server.</span></span>

<span data-ttu-id="c8faf-233">Chave externa para a coluna um da tabela de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8faf-233">External key to column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="c8faf-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="c8faf-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="c8faf-235">Se **msidbClassAttributesRelativePath** for definido nesta coluna, o nome de arquivo simples poderá ser usado para servidores com.</span><span class="sxs-lookup"><span data-stu-id="c8faf-235">If **msidbClassAttributesRelativePath** is set in this column, the bare file name can be used for COM servers.</span></span> <span data-ttu-id="c8faf-236">O instalador registra o nome do arquivo somente em vez do caminho completo.</span><span class="sxs-lookup"><span data-stu-id="c8faf-236">The installer registers the file name only instead of the complete path.</span></span> <span data-ttu-id="c8faf-237">Isso permite que o servidor no diretório atual tenha precedência e permita várias cópias do mesmo componente.</span><span class="sxs-lookup"><span data-stu-id="c8faf-237">This enables the server in the current directory to take precedence and allows multiple copies of the same component.</span></span>



| <span data-ttu-id="c8faf-238">Atributo</span><span class="sxs-lookup"><span data-stu-id="c8faf-238">Attribute</span></span>                            | <span data-ttu-id="c8faf-239">Decimal</span><span class="sxs-lookup"><span data-stu-id="c8faf-239">Decimal</span></span> | <span data-ttu-id="c8faf-240">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="c8faf-240">Hexadecimal</span></span> |
|--------------------------------------|---------|-------------|
| <span data-ttu-id="c8faf-241">**msidbClassAttributesRelativePath**</span><span class="sxs-lookup"><span data-stu-id="c8faf-241">**msidbClassAttributesRelativePath**</span></span> | <span data-ttu-id="c8faf-242">1</span><span class="sxs-lookup"><span data-stu-id="c8faf-242">1</span></span>       | <span data-ttu-id="c8faf-243">0x001</span><span class="sxs-lookup"><span data-stu-id="c8faf-243">0x001</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8faf-244">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8faf-244">Remarks</span></span>

<span data-ttu-id="c8faf-245">Essa tabela é referida quando a [ação RegisterClassInfo](registerclassinfo-action.md) ou a [ação UnregisterClassInfo](unregisterclassinfo-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="c8faf-245">This table is referred to when the [RegisterClassInfo action](registerclassinfo-action.md) or the [UnregisterClassInfo action](unregisterclassinfo-action.md) are executed.</span></span>

## <a name="validation"></a><span data-ttu-id="c8faf-246">Validação</span><span class="sxs-lookup"><span data-stu-id="c8faf-246">Validation</span></span>

<dl>

[<span data-ttu-id="c8faf-247">ICE03</span><span class="sxs-lookup"><span data-stu-id="c8faf-247">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c8faf-248">ICE06</span><span class="sxs-lookup"><span data-stu-id="c8faf-248">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c8faf-249">ICE19</span><span class="sxs-lookup"><span data-stu-id="c8faf-249">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="c8faf-250">ICE32</span><span class="sxs-lookup"><span data-stu-id="c8faf-250">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c8faf-251">ICE36</span><span class="sxs-lookup"><span data-stu-id="c8faf-251">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="c8faf-252">ICE41</span><span class="sxs-lookup"><span data-stu-id="c8faf-252">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="c8faf-253">ICE42</span><span class="sxs-lookup"><span data-stu-id="c8faf-253">ICE42</span></span>](ice42.md)  
[<span data-ttu-id="c8faf-254">ICE46</span><span class="sxs-lookup"><span data-stu-id="c8faf-254">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c8faf-255">ICE66</span><span class="sxs-lookup"><span data-stu-id="c8faf-255">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="c8faf-256">ICE69</span><span class="sxs-lookup"><span data-stu-id="c8faf-256">ICE69</span></span>](ice69.md)  
</dl>

 

 
