---
description: Um objeto de manipulador de extensão de Shell deve ser registrado antes que o Shell possa usá-lo. Este tópico é uma discussão geral sobre como registrar um manipulador de extensão de Shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrando manipuladores de extensão do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968063"
---
# <a name="registering-shell-extension-handlers"></a><span data-ttu-id="9ee40-104">Registrando manipuladores de extensão do Shell</span><span class="sxs-lookup"><span data-stu-id="9ee40-104">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="9ee40-105">Um objeto de manipulador de extensão de Shell deve ser registrado antes que o Shell possa usá-lo.</span><span class="sxs-lookup"><span data-stu-id="9ee40-105">A Shell extension handler object must be registered before the Shell can use it.</span></span> <span data-ttu-id="9ee40-106">Este tópico é uma discussão geral sobre como registrar um manipulador de extensão de Shell.</span><span class="sxs-lookup"><span data-stu-id="9ee40-106">This topic is a general discussion of how to register a Shell extension handler.</span></span>

<span data-ttu-id="9ee40-107">Sempre que você criar ou alterar um manipulador de extensão de Shell, será importante notificar o sistema de que você fez uma alteração.</span><span class="sxs-lookup"><span data-stu-id="9ee40-107">Any time you create or change a Shell extension handler, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="9ee40-108">Faça isso chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando o evento **SHCNE \_ assocchanged** .</span><span class="sxs-lookup"><span data-stu-id="9ee40-108">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="9ee40-109">Se você não chamar **SHChangeNotify**, a alteração poderá não ser reconhecida até que o sistema seja reinicializado.</span><span class="sxs-lookup"><span data-stu-id="9ee40-109">If you do not call **SHChangeNotify**, the change might not be recognized until the system is rebooted.</span></span>

<span data-ttu-id="9ee40-110">Há alguns fatores adicionais que se aplicam aos sistemas Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9ee40-110">There are some additional factors that apply to Windows 2000 systems.</span></span> <span data-ttu-id="9ee40-111">Para obter detalhes, consulte a seção [Registrando manipuladores de extensão de Shell em sistemas Windows 2000](#registering-shell-extension-handlers) .</span><span class="sxs-lookup"><span data-stu-id="9ee40-111">For details, see the [Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) section.</span></span>

<span data-ttu-id="9ee40-112">Assim como com todos os objetos COM (Component Object Model), você deve criar um GUID para o manipulador usando uma ferramenta como Guidgen.exe, que é fornecida com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="9ee40-112">As with all Component Object Model (COM) objects, you must create a GUID for the handler using a tool such as Guidgen.exe, which is provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9ee40-113">Crie uma subchave em **HKEY \_ classes \_ raiz** \\ **CLSID** cujo nome é a forma de cadeia de caracteres desse GUID.</span><span class="sxs-lookup"><span data-stu-id="9ee40-113">Create a subkey under **HKEY\_CLASSES\_ROOT**\\**CLSID** whose name is the string form of that GUID.</span></span> <span data-ttu-id="9ee40-114">Como os manipuladores de extensão do shell são servidores em processo, você também deve criar uma subchave **InprocServer32** na subchave GUID com o valor (padrão) definido como o caminho da dll do manipulador.</span><span class="sxs-lookup"><span data-stu-id="9ee40-114">Because Shell extension handlers are in-process servers, you also must create an **InprocServer32** subkey under that GUID subkey with the (Default) value set to the path of the handler's DLL.</span></span> <span data-ttu-id="9ee40-115">Use o modelo de Threading Apartment.</span><span class="sxs-lookup"><span data-stu-id="9ee40-115">Use the apartment threading model.</span></span> <span data-ttu-id="9ee40-116">Um exemplo é mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="9ee40-116">An example is shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

<span data-ttu-id="9ee40-117">Sempre que o Shell executar uma ação que possa envolver um manipulador de extensão de Shell, ele verificará a subchave do registro apropriada.</span><span class="sxs-lookup"><span data-stu-id="9ee40-117">Any time the Shell takes an action that can involve a Shell extension handler, it checks the appropriate registry subkey.</span></span> <span data-ttu-id="9ee40-118">A subchave sob a qual um manipulador de extensão é registrado controla quando ele será chamado.</span><span class="sxs-lookup"><span data-stu-id="9ee40-118">The subkey under which an extension handler is registered controls when it will be called.</span></span> <span data-ttu-id="9ee40-119">Por exemplo, é uma prática comum ter um manipulador de menu de atalho chamado quando o Shell exibe um menu de atalho para um membro de um [tipo de arquivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="9ee40-119">For instance, it is a common practice to have a shortcut menu handler called when the Shell displays a shortcut menu for a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="9ee40-120">Nesse caso, o manipulador deve ser registrado na subchave **ProgID** do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9ee40-120">In this case, the handler must be registered under the file type's **ProgID** subkey.</span></span>

<span data-ttu-id="9ee40-121">Este tópico discute os seguintes assuntos:</span><span class="sxs-lookup"><span data-stu-id="9ee40-121">This topic discusses the following subjects:</span></span>

-   [<span data-ttu-id="9ee40-122">Nomes de manipuladores</span><span class="sxs-lookup"><span data-stu-id="9ee40-122">Handler Names</span></span>](#handler-names)
-   [<span data-ttu-id="9ee40-123">Objetos de shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="9ee40-123">Predefined Shell Objects</span></span>](#predefined-shell-objects)
-   [<span data-ttu-id="9ee40-124">Exemplo de um registro de manipulador de extensão</span><span class="sxs-lookup"><span data-stu-id="9ee40-124">Example of an Extension Handler Registration</span></span>](#example-of-an-extension-handler-registration)
    -   [<span data-ttu-id="9ee40-125">Registrando manipuladores de extensão do Shell</span><span class="sxs-lookup"><span data-stu-id="9ee40-125">Registering Shell Extension Handlers</span></span>](#registering-shell-extension-handlers)
-   [<span data-ttu-id="9ee40-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ee40-126">Related topics</span></span>](#related-topics)

## <a name="handler-names"></a><span data-ttu-id="9ee40-127">Nomes de manipuladores</span><span class="sxs-lookup"><span data-stu-id="9ee40-127">Handler Names</span></span>

<span data-ttu-id="9ee40-128">Para habilitar um manipulador de extensão de Shell, crie uma subchave com o nome da subchave do manipulador (veja abaixo) na subchave **shellex** do **ProgID** (para tipos de arquivo) ou o nome do tipo de objeto do Shell (para [ \_ \_ objetos shell predefinidos](handlers.md)).</span><span class="sxs-lookup"><span data-stu-id="9ee40-128">To enable a Shell extension handler, create a subkey with the handler subkey name (see below) under the **ShellEx** subkey of either the **ProgID** (for file types) or the Shell object type name (for [predefined\_shell\_objects](handlers.md)).</span></span>

<span data-ttu-id="9ee40-129">Por exemplo, se você quisesse registrar um manipulador de extensão de menu de atalho para myprogram. 1, comece criando a seguinte subchave:</span><span class="sxs-lookup"><span data-stu-id="9ee40-129">For example, if you wanted to register a shortcut menu extension handler for MyProgram.1, you begin by creating the following subkey:</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

<span data-ttu-id="9ee40-130">Para os seguintes manipuladores, crie uma subchave sob a subchave "nome da subchave do manipulador" denominada como a versão da cadeia de caracteres do identificador de classe (CLSID) da extensão do Shell.</span><span class="sxs-lookup"><span data-stu-id="9ee40-130">For the following handlers, create a subkey underneath the "Handler Subkey name" subkey named as the string version of the class identifier (CLSID) of the Shell extension.</span></span> <span data-ttu-id="9ee40-131">Várias extensões podem ser registradas sob o nome da subchave do manipulador criando várias subchaves.</span><span class="sxs-lookup"><span data-stu-id="9ee40-131">Multiple extensions can be registered under the handler subkey name by creating multiple subkeys.</span></span>



| <span data-ttu-id="9ee40-132">Manipulador</span><span class="sxs-lookup"><span data-stu-id="9ee40-132">Handler</span></span>                 | <span data-ttu-id="9ee40-133">Interface</span><span class="sxs-lookup"><span data-stu-id="9ee40-133">Interface</span></span>          | <span data-ttu-id="9ee40-134">Nome da subchave do manipulador</span><span class="sxs-lookup"><span data-stu-id="9ee40-134">Handler Subkey Name</span></span>       |
|-------------------------|--------------------|---------------------------|
| <span data-ttu-id="9ee40-135">Manipulador de provedor de coluna</span><span class="sxs-lookup"><span data-stu-id="9ee40-135">Column provider handler</span></span> | <span data-ttu-id="9ee40-136">IColumnProvider</span><span class="sxs-lookup"><span data-stu-id="9ee40-136">IColumnProvider</span></span>    | <span data-ttu-id="9ee40-137">**ColumnHandlers**</span><span class="sxs-lookup"><span data-stu-id="9ee40-137">**ColumnHandlers**</span></span>        |
| <span data-ttu-id="9ee40-138">Manipulador de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="9ee40-138">Shortcut menu handler</span></span>   | <span data-ttu-id="9ee40-139">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="9ee40-139">IContextMenu</span></span>       | <span data-ttu-id="9ee40-140">**ContextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="9ee40-140">**ContextMenuHandlers**</span></span>   |
| <span data-ttu-id="9ee40-141">Manipulador de Copyhook</span><span class="sxs-lookup"><span data-stu-id="9ee40-141">Copyhook handler</span></span>        | <span data-ttu-id="9ee40-142">ICopyHook</span><span class="sxs-lookup"><span data-stu-id="9ee40-142">ICopyHook</span></span>          | <span data-ttu-id="9ee40-143">**CopyHookHandlers**</span><span class="sxs-lookup"><span data-stu-id="9ee40-143">**CopyHookHandlers**</span></span>      |
| <span data-ttu-id="9ee40-144">Manipulador do tipo "arrastar e soltar"</span><span class="sxs-lookup"><span data-stu-id="9ee40-144">Drag-and-drop handler</span></span>   | <span data-ttu-id="9ee40-145">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="9ee40-145">IContextMenu</span></span>       | <span data-ttu-id="9ee40-146">**DragDropHandlers**</span><span class="sxs-lookup"><span data-stu-id="9ee40-146">**DragDropHandlers**</span></span>      |
| <span data-ttu-id="9ee40-147">Manipulador de folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="9ee40-147">Property sheet handler</span></span>  | <span data-ttu-id="9ee40-148">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="9ee40-148">IShellPropSheetExt</span></span> | <span data-ttu-id="9ee40-149">**PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="9ee40-149">**PropertySheetHandlers**</span></span> |



 

<span data-ttu-id="9ee40-150">Para os seguintes manipuladores, o valor padrão da chave "nome da subchave do manipulador" é a versão da cadeia de caracteres do CLSID da extensão do Shell.</span><span class="sxs-lookup"><span data-stu-id="9ee40-150">For the following handlers, the default value of the "Handler Subkey Name" key is the string version of the CLSID of the Shell extension.</span></span> <span data-ttu-id="9ee40-151">Somente uma extensão pode ser registrada para esses manipuladores.</span><span class="sxs-lookup"><span data-stu-id="9ee40-151">Only one extension can be registered for these handlers.</span></span>



| <span data-ttu-id="9ee40-152">Manipulador</span><span class="sxs-lookup"><span data-stu-id="9ee40-152">Handler</span></span>                 | <span data-ttu-id="9ee40-153">Interface</span><span class="sxs-lookup"><span data-stu-id="9ee40-153">Interface</span></span>            | <span data-ttu-id="9ee40-154">Nome da subchave do manipulador</span><span class="sxs-lookup"><span data-stu-id="9ee40-154">Handler Subkey Name</span></span>                        |
|-------------------------|----------------------|--------------------------------------------|
| <span data-ttu-id="9ee40-155">Manipulador de dados</span><span class="sxs-lookup"><span data-stu-id="9ee40-155">Data handler</span></span>            | <span data-ttu-id="9ee40-156">IDataObject</span><span class="sxs-lookup"><span data-stu-id="9ee40-156">IDataObject</span></span>          | <span data-ttu-id="9ee40-157">**DataHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee40-157">**DataHandler**</span></span>                            |
| <span data-ttu-id="9ee40-158">Descartar manipulador</span><span class="sxs-lookup"><span data-stu-id="9ee40-158">Drop handler</span></span>            | <span data-ttu-id="9ee40-159">IDropTarget</span><span class="sxs-lookup"><span data-stu-id="9ee40-159">IDropTarget</span></span>          | <span data-ttu-id="9ee40-160">**DropHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee40-160">**DropHandler**</span></span>                            |
| <span data-ttu-id="9ee40-161">Manipulador de ícone</span><span class="sxs-lookup"><span data-stu-id="9ee40-161">Icon handler</span></span>            | <span data-ttu-id="9ee40-162">IExtractIconA/W</span><span class="sxs-lookup"><span data-stu-id="9ee40-162">IExtractIconA/W</span></span>      | <span data-ttu-id="9ee40-163">**IconHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee40-163">**IconHandler**</span></span>                            |
| <span data-ttu-id="9ee40-164">Manipulador de imagem em miniatura</span><span class="sxs-lookup"><span data-stu-id="9ee40-164">Thumbnail image handler</span></span> | <span data-ttu-id="9ee40-165">Manipuladordeminiaturai</span><span class="sxs-lookup"><span data-stu-id="9ee40-165">IThumbnailProvider</span></span>   | <span data-ttu-id="9ee40-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span><span class="sxs-lookup"><span data-stu-id="9ee40-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span></span> |
| <span data-ttu-id="9ee40-167">Manipulador de infodicas</span><span class="sxs-lookup"><span data-stu-id="9ee40-167">Infotip handler</span></span>         | <span data-ttu-id="9ee40-168">IQueryInfo</span><span class="sxs-lookup"><span data-stu-id="9ee40-168">IQueryInfo</span></span>           | <span data-ttu-id="9ee40-169">**{00021500-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="9ee40-169">**{00021500-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="9ee40-170">Link do Shell (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9ee40-170">Shell link (ANSI)</span></span>       | <span data-ttu-id="9ee40-171">IShellLinkA</span><span class="sxs-lookup"><span data-stu-id="9ee40-171">IShellLinkA</span></span>          | <span data-ttu-id="9ee40-172">**{000214EE-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="9ee40-172">**{000214EE-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="9ee40-173">Link do Shell (UNICODE)</span><span class="sxs-lookup"><span data-stu-id="9ee40-173">Shell link (UNICODE)</span></span>    | <span data-ttu-id="9ee40-174">IShellLinkW</span><span class="sxs-lookup"><span data-stu-id="9ee40-174">IShellLinkW</span></span>          | <span data-ttu-id="9ee40-175">**{000214F9-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="9ee40-175">**{000214F9-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="9ee40-176">Armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="9ee40-176">Structured storage</span></span>      | <span data-ttu-id="9ee40-177">IStorage</span><span class="sxs-lookup"><span data-stu-id="9ee40-177">IStorage</span></span>             | <span data-ttu-id="9ee40-178">**{0000000B-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="9ee40-178">**{0000000B-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="9ee40-179">Metadados</span><span class="sxs-lookup"><span data-stu-id="9ee40-179">Metadata</span></span>                | <span data-ttu-id="9ee40-180">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="9ee40-180">IPropertySetStorage</span></span>  | <span data-ttu-id="9ee40-181">**PropertyHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee40-181">**PropertyHandler**</span></span>                        |
| <span data-ttu-id="9ee40-182">Fixar no menu iniciar</span><span class="sxs-lookup"><span data-stu-id="9ee40-182">Pin to Start Menu</span></span>       | <span data-ttu-id="9ee40-183">IStartMenuPinnedList</span><span class="sxs-lookup"><span data-stu-id="9ee40-183">IStartMenuPinnedList</span></span> | <span data-ttu-id="9ee40-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span><span class="sxs-lookup"><span data-stu-id="9ee40-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span></span> |
| <span data-ttu-id="9ee40-185">Fixar à barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="9ee40-185">Pin to Taskbar</span></span>          |                      | <span data-ttu-id="9ee40-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span><span class="sxs-lookup"><span data-stu-id="9ee40-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span></span> |



 

<span data-ttu-id="9ee40-187">As subchaves especificadas para adicionar **Pin ao menu iniciar** e **fixar à barra de tarefas** no menu de atalho de um item só são necessárias para tipos de arquivo que incluem a entrada [IsShortcut](./links.md) .</span><span class="sxs-lookup"><span data-stu-id="9ee40-187">The subkeys specified to add **Pin to Start Menu** and **Pin to Taskbar** to an item's shortcut menu are only required for file types that include the [IsShortCut](./links.md) entry.</span></span>

## <a name="predefined-shell-objects"></a><span data-ttu-id="9ee40-188">Objetos de shell predefinidos</span><span class="sxs-lookup"><span data-stu-id="9ee40-188">Predefined Shell Objects</span></span>

<span data-ttu-id="9ee40-189">O Shell define objetos adicionais na **\_ \_ raiz de classes hKey** que podem ser estendidas da mesma maneira que os tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9ee40-189">The Shell defines additional objects under **HKEY\_CLASSES\_ROOT** which can be extended in the same way as file types.</span></span> <span data-ttu-id="9ee40-190">Por exemplo, para adicionar um manipulador de folha de propriedades para todos os arquivos, você pode se registrar na subchave **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="9ee40-190">For example, to add a property sheet handler for all files, you can register under the **PropertySheetHandlers** subkey.</span></span>

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

<span data-ttu-id="9ee40-191">A tabela a seguir fornece as várias subchaves da **\_ \_ raiz de classes hKey** em que os manipuladores de extensão podem ser registrados.</span><span class="sxs-lookup"><span data-stu-id="9ee40-191">The following table gives the various subkeys of **HKEY\_CLASSES\_ROOT** under which extension handlers can be registered.</span></span> <span data-ttu-id="9ee40-192">Observe que muitos manipuladores de extensão não podem ser registrados em todas as subchaves listadas.</span><span class="sxs-lookup"><span data-stu-id="9ee40-192">Note that many extension handlers cannot be registered under all of the listed subkeys.</span></span> <span data-ttu-id="9ee40-193">Para obter mais detalhes, consulte a documentação do manipulador específico.</span><span class="sxs-lookup"><span data-stu-id="9ee40-193">For further details, see the specific handler's documentation.</span></span>



| <span data-ttu-id="9ee40-194">Subchave</span><span class="sxs-lookup"><span data-stu-id="9ee40-194">Subkey</span></span>                    | <span data-ttu-id="9ee40-195">Description</span><span class="sxs-lookup"><span data-stu-id="9ee40-195">Description</span></span>                                                          | <span data-ttu-id="9ee40-196">Possíveis manipuladores</span><span class="sxs-lookup"><span data-stu-id="9ee40-196">Possible Handlers</span></span>                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="9ee40-197">\**\** _</span><span class="sxs-lookup"><span data-stu-id="9ee40-197">\**\** _</span></span>                    | <span data-ttu-id="9ee40-198">Todos os arquivos</span><span class="sxs-lookup"><span data-stu-id="9ee40-198">All files</span></span>                                                            | <span data-ttu-id="9ee40-199">Menu de atalho, folha de propriedades, verbos (veja abaixo)</span><span class="sxs-lookup"><span data-stu-id="9ee40-199">Shortcut Menu, Property Sheet, Verbs (see below)</span></span> |
| <span data-ttu-id="9ee40-200">_ *AllFileSystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="9ee40-200">_ *AllFileSystemObjects*\*</span></span>  | <span data-ttu-id="9ee40-201">Todos os arquivos e pastas de arquivos</span><span class="sxs-lookup"><span data-stu-id="9ee40-201">All files and file folders</span></span>                                           | <span data-ttu-id="9ee40-202">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-202">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-203">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="9ee40-203">**Folder**</span></span>                | <span data-ttu-id="9ee40-204">Todas as pastas</span><span class="sxs-lookup"><span data-stu-id="9ee40-204">All folders</span></span>                                                          | <span data-ttu-id="9ee40-205">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-205">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-206">**Active**</span><span class="sxs-lookup"><span data-stu-id="9ee40-206">**Directory**</span></span>             | <span data-ttu-id="9ee40-207">Pastas de arquivos</span><span class="sxs-lookup"><span data-stu-id="9ee40-207">File folders</span></span>                                                         | <span data-ttu-id="9ee40-208">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-208">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-209">**Plano de fundo do diretório \\**</span><span class="sxs-lookup"><span data-stu-id="9ee40-209">**Directory\\Background**</span></span> | <span data-ttu-id="9ee40-210">Plano de fundo da pasta de arquivos</span><span class="sxs-lookup"><span data-stu-id="9ee40-210">File folder background</span></span>                                               | <span data-ttu-id="9ee40-211">Somente menu de atalho</span><span class="sxs-lookup"><span data-stu-id="9ee40-211">Shortcut Menu only</span></span>                               |
| <span data-ttu-id="9ee40-212">**DesktopBackground**</span><span class="sxs-lookup"><span data-stu-id="9ee40-212">**DesktopBackground**</span></span>     | <span data-ttu-id="9ee40-213">Plano de fundo da área de trabalho (Windows 7 e superior)</span><span class="sxs-lookup"><span data-stu-id="9ee40-213">Desktop background (Windows 7 and higher)</span></span>                            | <span data-ttu-id="9ee40-214">Menu de atalho, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-214">Shortcut Menu, Verbs</span></span>                             |
| <span data-ttu-id="9ee40-215">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="9ee40-215">**Drive**</span></span>                 | <span data-ttu-id="9ee40-216">Todas as unidades em MyComputer, como "C: \\ "</span><span class="sxs-lookup"><span data-stu-id="9ee40-216">All drives in MyComputer, such as "C:\\"</span></span>                             | <span data-ttu-id="9ee40-217">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-217">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-218">**Rede**</span><span class="sxs-lookup"><span data-stu-id="9ee40-218">**Network**</span></span>               | <span data-ttu-id="9ee40-219">Rede inteira (em meus locais de rede)</span><span class="sxs-lookup"><span data-stu-id="9ee40-219">Entire network (under My Network Places)</span></span>                             | <span data-ttu-id="9ee40-220">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-220">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-221">**Tipo de rede \\\\\#**</span><span class="sxs-lookup"><span data-stu-id="9ee40-221">**Network\\Type\\\#**</span></span>     | <span data-ttu-id="9ee40-222">Todos os objetos do tipo \# (veja abaixo)</span><span class="sxs-lookup"><span data-stu-id="9ee40-222">All objects of type \# (see below)</span></span>                                   | <span data-ttu-id="9ee40-223">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-223">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-224">**NetShare**</span><span class="sxs-lookup"><span data-stu-id="9ee40-224">**NetShare**</span></span>              | <span data-ttu-id="9ee40-225">Todos os compartilhamentos de rede</span><span class="sxs-lookup"><span data-stu-id="9ee40-225">All network shares</span></span>                                                   | <span data-ttu-id="9ee40-226">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-226">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-227">**NetServer**</span><span class="sxs-lookup"><span data-stu-id="9ee40-227">**NetServer**</span></span>             | <span data-ttu-id="9ee40-228">Todos os servidores de rede</span><span class="sxs-lookup"><span data-stu-id="9ee40-228">All network servers</span></span>                                                  | <span data-ttu-id="9ee40-229">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-229">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-230">*\_nome do provedor de rede \_*</span><span class="sxs-lookup"><span data-stu-id="9ee40-230">*network\_provider\_name*</span></span> | <span data-ttu-id="9ee40-231">Todos os objetos fornecidos pelo "*nome do \_ provedor \_ de rede*" do provedor de rede</span><span class="sxs-lookup"><span data-stu-id="9ee40-231">All objects provided by network provider "*network\_provider\_name*"</span></span> | <span data-ttu-id="9ee40-232">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-232">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="9ee40-233">**Impressoras**</span><span class="sxs-lookup"><span data-stu-id="9ee40-233">**Printers**</span></span>              | <span data-ttu-id="9ee40-234">Todas as impressoras</span><span class="sxs-lookup"><span data-stu-id="9ee40-234">All printers</span></span>                                                         | <span data-ttu-id="9ee40-235">Menu de atalho, folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="9ee40-235">Shortcut Menu, Property Sheet</span></span>                    |
| <span data-ttu-id="9ee40-236">**AudioCD**</span><span class="sxs-lookup"><span data-stu-id="9ee40-236">**AudioCD**</span></span>               | <span data-ttu-id="9ee40-237">CD de áudio na unidade de CD</span><span class="sxs-lookup"><span data-stu-id="9ee40-237">Audio CD in CD drive</span></span>                                                 | <span data-ttu-id="9ee40-238">Somente verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-238">Verbs only</span></span>                                       |
| <span data-ttu-id="9ee40-239">**DVD**</span><span class="sxs-lookup"><span data-stu-id="9ee40-239">**DVD**</span></span>                   | <span data-ttu-id="9ee40-240">Unidade de DVD (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="9ee40-240">DVD drive (Windows 2000)</span></span>                                             | <span data-ttu-id="9ee40-241">Menu de atalho, folha de propriedades, verbos</span><span class="sxs-lookup"><span data-stu-id="9ee40-241">Shortcut Menu, Property Sheet, Verbs</span></span>             |



 

### <a name="notes"></a><span data-ttu-id="9ee40-242">Observações</span><span class="sxs-lookup"><span data-stu-id="9ee40-242">Notes</span></span>

-   <span data-ttu-id="9ee40-243">O menu de atalho de segundo plano da pasta de arquivo é acessado clicando com o botão direito do mouse em uma pasta de arquivo, mas não em qualquer conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="9ee40-243">The file folder background shortcut menu is accessed by right-clicking within a file folder, but not over any of the folder's contents.</span></span>
-   <span data-ttu-id="9ee40-244">"Verbos" são comandos especiais registrados sob o verbo do Shell de subchave do **HKEY \_ classes \_ raiz** \\  \\  \\ .</span><span class="sxs-lookup"><span data-stu-id="9ee40-244">"Verbs" are special commands registered under **HKEY\_CLASSES\_ROOT**\\*Subkey*\\**Shell**\\**Verb**.</span></span>
-   <span data-ttu-id="9ee40-245">Para o tipo de **rede** \\  \\ **\#** , " \# " é um código de tipo de provedor de rede em decimal.</span><span class="sxs-lookup"><span data-stu-id="9ee40-245">For **Network**\\**Type**\\**\#**, "\#" is a network provider type code in decimal.</span></span> <span data-ttu-id="9ee40-246">O código do tipo de provedor de rede é a palavra alta de um tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="9ee40-246">The network provider type code is the high word of a network type.</span></span> <span data-ttu-id="9ee40-247">A lista de tipos de rede é fornecida no arquivo de cabeçalho Winnetwk. h (WNNC \_ net \_ \* Values).</span><span class="sxs-lookup"><span data-stu-id="9ee40-247">The list of network types is given in the Winnetwk.h header file (WNNC\_NET\_\* values).</span></span> <span data-ttu-id="9ee40-248">Por exemplo, WNNC \_ net \_ Shiva é 0x00330000, portanto, a subchave de tipo correspondente seria tipo de rede **\_ \_ raiz de classes hKey** \\  \\  \\ **51**.</span><span class="sxs-lookup"><span data-stu-id="9ee40-248">For example, WNNC\_NET\_SHIVA is 0x00330000, so the corresponding type subkey would be **HKEY\_CLASSES\_ROOT**\\**Network**\\**Type**\\**51**.</span></span>
-   <span data-ttu-id="9ee40-249">"*\_ \_ nome do provedor de rede*" é um nome de provedor de rede, conforme especificado por [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), com os espaços convertidos em sublinhados.</span><span class="sxs-lookup"><span data-stu-id="9ee40-249">"*network\_provider\_name*" is a network provider name as specified by [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), with the spaces converted into underscores.</span></span> <span data-ttu-id="9ee40-250">Por exemplo, se o provedor de rede de rede da Microsoft estiver instalado, o nome do provedor será "rede do Microsoft Windows" e o *\_ \_ nome do provedor de rede* correspondente será a **\_ \_ rede do Microsoft Windows**.</span><span class="sxs-lookup"><span data-stu-id="9ee40-250">For example, if the Microsoft Networking network provider is installed, its provider name is "Microsoft Windows Network", and the corresponding *network\_provider\_name* is **Microsoft\_Windows\_Network**.</span></span>

## <a name="example-of-an-extension-handler-registration"></a><span data-ttu-id="9ee40-251">Exemplo de um registro de manipulador de extensão</span><span class="sxs-lookup"><span data-stu-id="9ee40-251">Example of an Extension Handler Registration</span></span>

<span data-ttu-id="9ee40-252">Para habilitar um manipulador específico, crie uma subchave na subchave do tipo de manipulador de extensão com o nome do manipulador.</span><span class="sxs-lookup"><span data-stu-id="9ee40-252">To enable a particular handler, create a subkey under the extension handler type subkey with the name of the handler.</span></span> <span data-ttu-id="9ee40-253">O shell não usa o nome do manipulador, mas ele deve ser diferente de todos os outros nomes nessa subchave de tipo.</span><span class="sxs-lookup"><span data-stu-id="9ee40-253">The Shell does not use the handler's name, but it must be different from all other names under that type subkey.</span></span> <span data-ttu-id="9ee40-254">Defina o valor padrão da subchave Name para a forma de cadeia de caracteres do GUID do manipulador.</span><span class="sxs-lookup"><span data-stu-id="9ee40-254">Set the default value of the name subkey to the string form of the handler's GUID.</span></span>

<span data-ttu-id="9ee40-255">O exemplo a seguir ilustra as entradas do registro que habilitam manipuladores de extensão de folha de propriedades e de menu de atalho, usando um tipo de arquivo. MYP de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9ee40-255">The following example illustrates registry entries that enable shortcut menu and property sheet extension handlers, using an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a><span data-ttu-id="9ee40-256">Registrando manipuladores de extensão do Shell</span><span class="sxs-lookup"><span data-stu-id="9ee40-256">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="9ee40-257">O procedimento de registro discutido nesta seção deve ser seguido para todos os sistemas Windows.</span><span class="sxs-lookup"><span data-stu-id="9ee40-257">The registration procedure discussed in this section must be followed for all Windows systems.</span></span> <span data-ttu-id="9ee40-258">No entanto, com os sistemas posteriores, uma etapa adicional pode ser necessária.</span><span class="sxs-lookup"><span data-stu-id="9ee40-258">However, with later systems, an additional step might be necessary.</span></span> <span data-ttu-id="9ee40-259">Como essas versões posteriores do Windows são projetadas para serem usadas em um ambiente gerenciado, o acesso ao registro pode ser administrativamente restrito, exigindo uma abordagem um pouco diferente da instalação do que a descrita na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="9ee40-259">Because these later versions of Windows are designed to be used in a managed environment, access to the registry could be administratively restricted, requiring a somewhat different approach to installation than described in the previous section.</span></span>

> [!Note]  
> <span data-ttu-id="9ee40-260">Os programas de instalação geralmente não devem gravar diretamente no registro.</span><span class="sxs-lookup"><span data-stu-id="9ee40-260">Setup programs should generally not write directly to the registry.</span></span> <span data-ttu-id="9ee40-261">Em vez disso, a instalação deve ser realizada com Windows Installer pacotes.</span><span class="sxs-lookup"><span data-stu-id="9ee40-261">Instead, setup should be accomplished with Windows Installer packages.</span></span> <span data-ttu-id="9ee40-262">Essas ferramentas garantem que o software seja executado bem e fornece acesso a recursos como registro de classe por usuário.</span><span class="sxs-lookup"><span data-stu-id="9ee40-262">These tools ensure that software runs well and provides access to capabilities such as per-user class registration.</span></span>

 

<span data-ttu-id="9ee40-263">Os manipuladores de extensão do shell são executados no processo do Shell.</span><span class="sxs-lookup"><span data-stu-id="9ee40-263">Shell extension handlers run in the Shell process.</span></span> <span data-ttu-id="9ee40-264">Como é um processo do sistema, o administrador de um sistema pode limitar os manipuladores de extensão do Shell àqueles em uma lista aprovada definindo o valor de EnforceShellExtensionSecurity da chave do **Gerenciador** como 1, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="9ee40-264">Because it is a system process, the administrator of a system can limit Shell extension handlers to those on an approved list by setting the EnforceShellExtensionSecurity value of the **Explorer** key to 1 as shown here:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

<span data-ttu-id="9ee40-265">Para posicionar um manipulador de extensão de Shell na lista aprovada, crie um valor **reg \_ sz** cujo nome seja a forma de cadeia de caracteres do GUID do manipulador sob a subchave **aprovada** .</span><span class="sxs-lookup"><span data-stu-id="9ee40-265">To place a Shell extension handler on the approved list, create a **REG\_SZ** value whose name is the string form of the handler's GUID under the **Approved** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

<span data-ttu-id="9ee40-266">Por exemplo, o exemplo a seguir adiciona os manipuladores *myCommand* e *MyPropSheet* à lista aprovada.</span><span class="sxs-lookup"><span data-stu-id="9ee40-266">For example, the following example adds the *MyCommand* and *MyPropSheet* handlers to the approved list.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

<span data-ttu-id="9ee40-267">O shell não usa o valor atribuído ao GUID, mas deve ser definido para facilitar a inspeção do registro.</span><span class="sxs-lookup"><span data-stu-id="9ee40-267">The Shell does not use the value that is assigned to the GUID, but it should be set to make inspecting the registry easier.</span></span>

<span data-ttu-id="9ee40-268">Seu aplicativo de instalação poderá adicionar valores à subchave **aprovada** somente se a pessoa que está instalando o aplicativo tiver privilégios suficientes.</span><span class="sxs-lookup"><span data-stu-id="9ee40-268">Your setup application can add values to the **Approved** subkey only if the person installing the application has sufficient privileges.</span></span> <span data-ttu-id="9ee40-269">Se a tentativa de adicionar um manipulador de extensão falhar, você deverá informar ao usuário que privilégios administrativos são necessários para instalar totalmente o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9ee40-269">If the attempt to add an extension handler fails, you should inform the user that administrative privileges are required to fully install the application.</span></span> <span data-ttu-id="9ee40-270">Se o manipulador for essencial para o aplicativo, você deverá falhar a instalação e notificar o usuário para entrar em contato com um administrador.</span><span class="sxs-lookup"><span data-stu-id="9ee40-270">If the handler is essential to the application, you should fail the setup and notify the user to contact an administrator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ee40-271">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ee40-271">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ee40-272">Inicializando manipuladores de extensão do Shell</span><span class="sxs-lookup"><span data-stu-id="9ee40-272">Initializing Shell Extension Handlers</span></span>](int-shell-exts.md)
</dt> </dl>

 

 
