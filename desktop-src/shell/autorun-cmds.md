---
description: Este tópico é uma referência para as entradas que podem ser usadas em um arquivo autorun. inf. Uma entrada consiste em uma chave e um valor.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Entradas autorun. inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164319"
---
# <a name="autoruninf-entries"></a><span data-ttu-id="e2edb-104">Entradas autorun. inf</span><span class="sxs-lookup"><span data-stu-id="e2edb-104">Autorun.inf Entries</span></span>

<span data-ttu-id="e2edb-105">Este tópico é uma referência para as entradas que podem ser usadas em um arquivo autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="e2edb-105">This topic is a reference for the entries that can be used in an Autorun.inf file.</span></span> <span data-ttu-id="e2edb-106">Uma entrada consiste em uma chave e um valor.</span><span class="sxs-lookup"><span data-stu-id="e2edb-106">An entry consists of a key and a value.</span></span>

-   <span data-ttu-id="e2edb-107">[\[Chaves de AutoRun \]](#autorun-keys)</span><span class="sxs-lookup"><span data-stu-id="e2edb-107">[\[AutoRun\] Keys](#autorun-keys)</span></span>
    -   [<span data-ttu-id="e2edb-108">action</span><span class="sxs-lookup"><span data-stu-id="e2edb-108">action</span></span>](#parameters)
    -   [<span data-ttu-id="e2edb-109">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="e2edb-109">CustomEvent</span></span>](#customevent)
    -   [<span data-ttu-id="e2edb-110">cone</span><span class="sxs-lookup"><span data-stu-id="e2edb-110">icon</span></span>](#parameters)
    -   [<span data-ttu-id="e2edb-111">label</span><span class="sxs-lookup"><span data-stu-id="e2edb-111">label</span></span>](#parameters)
    -   [<span data-ttu-id="e2edb-112">open</span><span class="sxs-lookup"><span data-stu-id="e2edb-112">open</span></span>](#parameters)
    -   [<span data-ttu-id="e2edb-113">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="e2edb-113">UseAutoPlay</span></span>](#parameters)
    -   [<span data-ttu-id="e2edb-114">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="e2edb-114">shellexecute</span></span>](#shellexecute)
    -   [<span data-ttu-id="e2edb-115">Shell</span><span class="sxs-lookup"><span data-stu-id="e2edb-115">shell</span></span>](#autoruninf-entries)
    -   [<span data-ttu-id="e2edb-116">verbo do Shell \\</span><span class="sxs-lookup"><span data-stu-id="e2edb-116">shell\\verb</span></span>](#shellverb)
-   <span data-ttu-id="e2edb-117">[\[Chaves de conteúdo \]](#content-keys)</span><span class="sxs-lookup"><span data-stu-id="e2edb-117">[\[Content\] Keys](#content-keys)</span></span>
-   <span data-ttu-id="e2edb-118">[\[\]Chaves ExclusiveContentPaths](#exclusivecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="e2edb-118">[\[ExclusiveContentPaths\] Keys](#exclusivecontentpaths-keys)</span></span>
-   <span data-ttu-id="e2edb-119">[\[\]Chaves IgnoreContentPaths](#ignorecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="e2edb-119">[\[IgnoreContentPaths\] Keys](#ignorecontentpaths-keys)</span></span>
-   <span data-ttu-id="e2edb-120">[\[\]Chaves DeviceInstall](#deviceinstall-keys)</span><span class="sxs-lookup"><span data-stu-id="e2edb-120">[\[DeviceInstall\] Keys](#deviceinstall-keys)</span></span>
    -   [<span data-ttu-id="e2edb-121">DriverPath</span><span class="sxs-lookup"><span data-stu-id="e2edb-121">DriverPath</span></span>](#driverpath)

## <a name="autorun-keys"></a><span data-ttu-id="e2edb-122">\[Chaves de AutoRun \]</span><span class="sxs-lookup"><span data-stu-id="e2edb-122">\[AutoRun\] Keys</span></span>

-   [<span data-ttu-id="e2edb-123">action</span><span class="sxs-lookup"><span data-stu-id="e2edb-123">action</span></span>](#parameters)
-   [<span data-ttu-id="e2edb-124">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="e2edb-124">CustomEvent</span></span>](#customevent)
-   [<span data-ttu-id="e2edb-125">cone</span><span class="sxs-lookup"><span data-stu-id="e2edb-125">icon</span></span>](#parameters)
-   [<span data-ttu-id="e2edb-126">label</span><span class="sxs-lookup"><span data-stu-id="e2edb-126">label</span></span>](#parameters)
-   [<span data-ttu-id="e2edb-127">open</span><span class="sxs-lookup"><span data-stu-id="e2edb-127">open</span></span>](#parameters)
-   [<span data-ttu-id="e2edb-128">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="e2edb-128">UseAutoPlay</span></span>](#parameters)
-   [<span data-ttu-id="e2edb-129">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="e2edb-129">shellexecute</span></span>](#shellexecute)
-   [<span data-ttu-id="e2edb-130">Shell</span><span class="sxs-lookup"><span data-stu-id="e2edb-130">shell</span></span>](#autoruninf-entries)
-   [<span data-ttu-id="e2edb-131">verbo do Shell \\</span><span class="sxs-lookup"><span data-stu-id="e2edb-131">shell\\verb</span></span>](#shellverb)

### <a name="action"></a><span data-ttu-id="e2edb-132">ação</span><span class="sxs-lookup"><span data-stu-id="e2edb-132">action</span></span>

<span data-ttu-id="e2edb-133">A entrada de **ação** especifica o texto que é usado na caixa de diálogo de reprodução automática para o manipulador que representa o programa especificado na entrada [Open](#parameters) ou [ShellExecute](#shellexecute) no arquivo autorun. inf da mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-133">The **action** entry specifies the text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span> <span data-ttu-id="e2edb-134">O valor pode ser expresso como texto ou como um recurso armazenado em um binário.</span><span class="sxs-lookup"><span data-stu-id="e2edb-134">The value can be expressed as either text or as a resource stored in a binary.</span></span>


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a><span data-ttu-id="e2edb-135">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-135">Parameters</span></span>

-   <span data-ttu-id="e2edb-136">*ActionText*</span><span class="sxs-lookup"><span data-stu-id="e2edb-136">*ActionText*</span></span>

    <span data-ttu-id="e2edb-137">Texto usado na caixa de diálogo de reprodução automática para o manipulador que representa o programa especificado na entrada de [Open](#parameters) ou [ShellExecute](#shellexecute) no arquivo autorun. inf da mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-137">Text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span>

-   <span data-ttu-id="e2edb-138">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="e2edb-138">*filepath*</span></span>

    <span data-ttu-id="e2edb-139">Uma cadeia de caracteres que contém o caminho totalmente qualificado do diretório que contém o arquivo binário que contém a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e2edb-139">A string that contains the fully qualified path of the directory that contains the binary file containing the string.</span></span> <span data-ttu-id="e2edb-140">Se nenhum caminho for especificado, o arquivo deverá estar no diretório raiz da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2edb-140">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="e2edb-141">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="e2edb-141">*filename*</span></span>

    <span data-ttu-id="e2edb-142">Uma cadeia de caracteres que contém o nome do arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="e2edb-142">A string that contains the binary file's name.</span></span>

-   <span data-ttu-id="e2edb-143">*Identificação*</span><span class="sxs-lookup"><span data-stu-id="e2edb-143">*resourceID*</span></span>

    <span data-ttu-id="e2edb-144">A ID da cadeia de caracteres no arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="e2edb-144">The ID of the string within the binary file.</span></span>

### <a name="remarks"></a><span data-ttu-id="e2edb-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-145">Remarks</span></span>

<span data-ttu-id="e2edb-146">A chave de **ação** só é usada no Windows XP Service Pack 2 (SP2) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2edb-146">The **action** key is only used in Windows XP Service Pack 2 (SP2) or later.</span></span> <span data-ttu-id="e2edb-147">Só há suporte para unidades do tipo unidade \_ removível e unidade \_ corrigida.</span><span class="sxs-lookup"><span data-stu-id="e2edb-147">It is only supported for drives of type DRIVE\_REMOVABLE and DRIVE\_FIXED.</span></span> <span data-ttu-id="e2edb-148">No caso da unidade \_ removível, a chave de **ação** é necessária.</span><span class="sxs-lookup"><span data-stu-id="e2edb-148">In the case of DRIVE\_REMOVABLE, the **action** key is required.</span></span> <span data-ttu-id="e2edb-149">Um comando de **ação** no arquivo autorun. inf de um CD de áudio ou DVD de filme é ignorado e essas mídias continuam a se comportar como no Windows XP Service Pack 1 (SP1) e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="e2edb-149">An **action** command in the Autorun.inf file of an audio CD or movie DVD is ignored, and these media continue to behave as in Windows XP Service Pack 1 (SP1) and earlier.</span></span>

<span data-ttu-id="e2edb-150">A cadeia de caracteres exibida na caixa de diálogo de reprodução automática é construída combinando o texto especificado na entrada de **ação** com o texto embutido em código que nomeia o provedor, fornecido pelo shell.</span><span class="sxs-lookup"><span data-stu-id="e2edb-150">The string displayed in the Autoplay dialog is constructed by combining the text specified in the **action** entry with hard-coded text naming the provider, provided by the Shell.</span></span> <span data-ttu-id="e2edb-151">O [ícone](#parameters) é exibido ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="e2edb-151">The [icon](#parameters) is displayed next to it.</span></span> <span data-ttu-id="e2edb-152">Essa entrada sempre aparece como a primeira opção na caixa de diálogo de reprodução automática e é selecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e2edb-152">This entry always appears as the first option in the Autoplay dialog and is selected by default.</span></span> <span data-ttu-id="e2edb-153">Se o usuário aceitar a opção, o aplicativo especificado pela entrada [Open](#parameters) ou [ShellExecute](#shellexecute) no arquivo autorun. inf da mídia será iniciado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-153">If the user accepts the option, the application specified by the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file is launched.</span></span> <span data-ttu-id="e2edb-154">A opção **sempre fazer a ação selecionada** não está disponível nessa situação.</span><span class="sxs-lookup"><span data-stu-id="e2edb-154">The **Always do the selected action** option is not available in this situation.</span></span>

<span data-ttu-id="e2edb-155">As teclas de [ação](#parameters) e [ícone](#parameters) juntas definem a representação do aplicativo que é visto pelo usuário final na caixa de diálogo de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="e2edb-155">The [action](#parameters) and [icon](#parameters) keys together define the representation of the application that is seen by the end user in the Autoplay dialog.</span></span> <span data-ttu-id="e2edb-156">Eles devem ser compostos de forma que os usuários possam identificá-los facilmente.</span><span class="sxs-lookup"><span data-stu-id="e2edb-156">They should be composed in such a way that users can easily identify them.</span></span> <span data-ttu-id="e2edb-157">Eles devem indicar o aplicativo a ser executado, a empresa que o criou e qualquer identidade visual associada.</span><span class="sxs-lookup"><span data-stu-id="e2edb-157">They should indicate the application to be run, the company that created it, and any associated branding.</span></span>

<span data-ttu-id="e2edb-158">Para compatibilidade com versões anteriores, a entrada de **ação** é opcional para dispositivos do tipo unidade \_ fixa.</span><span class="sxs-lookup"><span data-stu-id="e2edb-158">For backward compatibility, the **action** entry is optional for devices of type DRIVE\_FIXED.</span></span> <span data-ttu-id="e2edb-159">Para esse tipo, uma entrada padrão será usada na caixa de diálogo de reprodução automática se nenhuma entrada de **ação** estiver presente no arquivo autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="e2edb-159">For this type, a default entry is used in the Autoplay dialog if no **action** entry is present in the Autorun.inf file.</span></span>

<span data-ttu-id="e2edb-160">A entrada de **ação** é obrigatória para dispositivos do tipo unidade \_ removível, que até agora não tinha suporte a autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="e2edb-160">The **action** entry is mandatory for devices of type DRIVE\_REMOVABLE, which until now did not have Autorun.inf support.</span></span> <span data-ttu-id="e2edb-161">Se nenhuma entrada de **ação** estiver presente, a caixa de diálogo de reprodução automática será exibida, mas sem a opção de iniciar o conteúdo adicional.</span><span class="sxs-lookup"><span data-stu-id="e2edb-161">If no **action** entry is present, the Autoplay dialog is displayed but with no option to launch the additional content.</span></span>

### <a name="customevent"></a><span data-ttu-id="e2edb-162">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="e2edb-162">CustomEvent</span></span>

<span data-ttu-id="e2edb-163">A entrada **CustomEvent** especifica um evento de conteúdo de reprodução automática personalizado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-163">The **CustomEvent** entry specifies a custom AutoPlay content event.</span></span>


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a><span data-ttu-id="e2edb-164">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-164">Parameters</span></span>

-   <span data-ttu-id="e2edb-165">*CustomEventName*</span><span class="sxs-lookup"><span data-stu-id="e2edb-165">*CustomEventName*</span></span>

    <span data-ttu-id="e2edb-166">Uma cadeia de texto que contém o nome do evento de conteúdo de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="e2edb-166">A text string containing the name of the AutoPlay content event.</span></span> <span data-ttu-id="e2edb-167">O nome não deve ter mais de 100 caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="e2edb-167">The name must be no more than 100 alphanumeric characters.</span></span>

### <a name="remarks"></a><span data-ttu-id="e2edb-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-168">Remarks</span></span>

<span data-ttu-id="e2edb-169">Você pode incluir um nome de evento personalizado no arquivo autorun. inf de um volume.</span><span class="sxs-lookup"><span data-stu-id="e2edb-169">You can include a custom event name in the Autorun.inf file of a volume.</span></span> <span data-ttu-id="e2edb-170">Quando o AutoPlay solicita ao usuário que um aplicativo use com o volume, ele exibe somente os aplicativos que se registraram para o nome do evento personalizado especificado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-170">When AutoPlay prompts the user for an application to use with the volume, it displays only applications that have registered for the specified custom event name.</span></span> <span data-ttu-id="e2edb-171">Para obter informações sobre como você pode registrar um aplicativo como um manipulador para seu evento personalizado de conteúdo de reprodução automática, consulte [inicialização automática com reprodução](/previous-versions/windows/apps/hh452731(v=win.10)) automática ou [como registrar um manipulador de eventos](how-to-register-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="e2edb-171">For information on how you can register an application as a handler for your custom AutoPlay content event, see [Auto-launching with AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) or [How to Register an Event Handler](how-to-register-an-event-handler.md).</span></span>

<span data-ttu-id="e2edb-172">O exemplo a seguir especifica o valor "MyContentOnArrival" como um novo evento de conteúdo de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="e2edb-172">The following example specifies the value "MyContentOnArrival" as a new AutoPlay content event.</span></span>


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a><span data-ttu-id="e2edb-173">ícone</span><span class="sxs-lookup"><span data-stu-id="e2edb-173">icon</span></span>

<span data-ttu-id="e2edb-174">A entrada de **ícone** especifica um ícone que representa a unidade habilitada para autorun na interface do usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="e2edb-174">The **icon** entry specifies an icon which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
icon=iconfilename[,index]
```



### <a name="parameters"></a><span data-ttu-id="e2edb-175">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-175">Parameters</span></span>

-   <span data-ttu-id="e2edb-176">*IconFilename*</span><span class="sxs-lookup"><span data-stu-id="e2edb-176">*iconfilename*</span></span>

    <span data-ttu-id="e2edb-177">Nome de um arquivo. ico,. bmp,. exe ou. dll que contém as informações do ícone.</span><span class="sxs-lookup"><span data-stu-id="e2edb-177">Name of an .ico, .bmp, .exe, or .dll file containing the icon information.</span></span> <span data-ttu-id="e2edb-178">Se um arquivo contiver mais de um ícone, você também deverá especificar o índice de base zero do ícone.</span><span class="sxs-lookup"><span data-stu-id="e2edb-178">If a file contains more than one icon, you must also specify zero-based index of the icon.</span></span>

### <a name="remarks"></a><span data-ttu-id="e2edb-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-179">Remarks</span></span>

<span data-ttu-id="e2edb-180">O ícone, junto com o rótulo, representa a unidade habilitada para AutoRun na interface do usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="e2edb-180">The icon, together with the label, represents the AutoRun-enabled drive in the Windows user interface.</span></span> <span data-ttu-id="e2edb-181">Por exemplo, no Windows Explorer, a unidade é representada por esse ícone em vez do ícone de unidade padrão.</span><span class="sxs-lookup"><span data-stu-id="e2edb-181">For instance, in Windows Explorer, the drive is represented by this icon instead of the standard drive icon.</span></span> <span data-ttu-id="e2edb-182">O arquivo do ícone deve estar no mesmo diretório que o arquivo especificado pelo comando [abrir](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="e2edb-182">The icon's file must be in the same directory as the file specified by the [open](#parameters) command.</span></span>

<span data-ttu-id="e2edb-183">O exemplo a seguir especifica o segundo ícone no arquivo de MyProg.exe.</span><span class="sxs-lookup"><span data-stu-id="e2edb-183">The following example specifies the second icon in the MyProg.exe file.</span></span>


```
icon=MyProg.exe,1
```



### <a name="label"></a><span data-ttu-id="e2edb-184">label</span><span class="sxs-lookup"><span data-stu-id="e2edb-184">label</span></span>

<span data-ttu-id="e2edb-185">A entrada de **rótulo** especifica um rótulo de texto que representa a unidade habilitada para autorun na interface do usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="e2edb-185">The **label** entry specifies a text label which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
label=LabelText
```



### <a name="parameters"></a><span data-ttu-id="e2edb-186">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-186">Parameters</span></span>

-   <span data-ttu-id="e2edb-187">*LabelText*</span><span class="sxs-lookup"><span data-stu-id="e2edb-187">*LabelText*</span></span>

    <span data-ttu-id="e2edb-188">Uma cadeia de texto que contém o rótulo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-188">A text string containing the label.</span></span> <span data-ttu-id="e2edb-189">Ele pode conter espaços e não deve ter mais de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e2edb-189">It can contain spaces and should be no longer than 32 characters.</span></span>

> [!Note]  
> <span data-ttu-id="e2edb-190">É possível colocar um valor no parâmetro **LabelText** que exceda 32 caracteres e não receber nenhuma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="e2edb-190">It is possible to put a value in the **LabelText** parameter which exceeds 32 characters and receive no error message.</span></span> <span data-ttu-id="e2edb-191">No entanto, o sistema só exibe os primeiros 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e2edb-191">However, the system only displays the first 32 characters.</span></span> <span data-ttu-id="e2edb-192">Todos os caracteres após os 32 º são truncados e não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e2edb-192">Any characters after the 32nd are truncated and not displayed.</span></span> <span data-ttu-id="e2edb-193">Por exemplo, se o **LabelText** for o seguinte: label = "este CD foi projetado para ser o CD de música final".</span><span class="sxs-lookup"><span data-stu-id="e2edb-193">For example, if the **LabelText** is as follows: label="This CD is designed to be the ultimate music CD."</span></span> <span data-ttu-id="e2edb-194">será exibido o seguinte: "este CD foi projetado para ser o UL".</span><span class="sxs-lookup"><span data-stu-id="e2edb-194">the following will be displayed, "This CD is designed to be the ul".</span></span>

 

### <a name="remarks"></a><span data-ttu-id="e2edb-195">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-195">Remarks</span></span>

<span data-ttu-id="e2edb-196">O rótulo, junto com um ícone, representa a unidade habilitada para AutoRun na interface do usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="e2edb-196">The label, together with an icon, represents the AutoRun-enabled drive in the Windows user interface.</span></span>

<span data-ttu-id="e2edb-197">O exemplo a seguir especifica o valor "meu rótulo de unidade" como o rótulo da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2edb-197">The following example specifies the value "My Drive Label" as the drive's label.</span></span>


```
label=My Drive Label
```



### <a name="open"></a><span data-ttu-id="e2edb-198">Abrir</span><span class="sxs-lookup"><span data-stu-id="e2edb-198">open</span></span>

<span data-ttu-id="e2edb-199">A entrada **aberta** especifica o caminho e o nome de arquivo do aplicativo que o autorun inicia quando um usuário insere um disco na unidade.</span><span class="sxs-lookup"><span data-stu-id="e2edb-199">The **open** entry specifies the path and file name of the application that AutoRun launches when a user inserts a disc in the drive.</span></span>


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a><span data-ttu-id="e2edb-200">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-200">Parameters</span></span>

-   <span data-ttu-id="e2edb-201">*exefile*</span><span class="sxs-lookup"><span data-stu-id="e2edb-201">*exefile*</span></span>

    <span data-ttu-id="e2edb-202">Caminho totalmente qualificado de um arquivo executável que é executado quando o CD é inserido.</span><span class="sxs-lookup"><span data-stu-id="e2edb-202">Fully qualified path of an executable file that runs when the CD is inserted.</span></span> <span data-ttu-id="e2edb-203">Se apenas um nome de arquivo for especificado, ele deverá estar no diretório raiz da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2edb-203">If only a file name is specified, it must be in drive's root directory.</span></span> <span data-ttu-id="e2edb-204">Para localizar o arquivo em um subdiretório, você deve especificar um caminho.</span><span class="sxs-lookup"><span data-stu-id="e2edb-204">To locate the file in a subdirectory, you must specify a path.</span></span> <span data-ttu-id="e2edb-205">Você também pode incluir um ou mais parâmetros de linha de comando para passar para o aplicativo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e2edb-205">You can also include one or more command-line parameters to pass to the startup application.</span></span>

### <a name="useautoplay"></a><span data-ttu-id="e2edb-206">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="e2edb-206">UseAutoPlay</span></span>

<span data-ttu-id="e2edb-207">No Windows XP, a entrada **UseAutoPlay** especifica que a reprodução automática deve ser usada em vez de Autorun.</span><span class="sxs-lookup"><span data-stu-id="e2edb-207">On Windows XP, the **UseAutoPlay** entry specifies that AutoPlay should be used instead of AutoRun.</span></span>

<span data-ttu-id="e2edb-208">No Windows Vista e posterior, essa entrada faz com que todas as ações especificadas para AutoRun (usando as entradas **Open** ou **ShellExecute** ) sejam suprimidas da caixa de diálogo de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="e2edb-208">On Windows Vista and later, this entry causes any actions specified for AutoRun (by using either the **open** or **shellexecute** entries) to be suppressed from the AutoPlay dialog.</span></span> <span data-ttu-id="e2edb-209">Essa entrada não tem nenhum efeito nas versões do Windows anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2edb-209">This entry has no effect on versions of Windows earlier than Windows XP.</span></span>

<span data-ttu-id="e2edb-210">No Windows 8 e posterior, a especificação de um valor de 0 desabilitará a reprodução automática para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-210">On Windows 8 and later, specifying a value of 0 will disable autoplay for this device.</span></span>

### <a name="parameters"></a><span data-ttu-id="e2edb-211">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-211">Parameters</span></span>

<span data-ttu-id="e2edb-212">Para usar essa opção, adicione uma entrada para **UseAutoPlay** ao arquivo autorun. inf e defina a entrada igual a 1.</span><span class="sxs-lookup"><span data-stu-id="e2edb-212">To use this option, add an entry for **UseAutoPlay** to the Autorun.inf file and set the entry equal to 1.</span></span> <span data-ttu-id="e2edb-213">Nenhum outro valor tem suporte em versões do Windows anteriores ao Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e2edb-213">No other value is supported on versions of Windows earlier than Windows 8.</span></span>

<span data-ttu-id="e2edb-214">No Windows 8 e posterior, especifique um valor de 0 para desabilitar a reprodução automática para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-214">On Windows 8 and later, specify a value of 0 to disable autoplay for this device.</span></span>


```
UseAutoPlay=1
```



### <a name="remarks"></a><span data-ttu-id="e2edb-215">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-215">Remarks</span></span>

<span data-ttu-id="e2edb-216">Atualmente, o **UseAutoPlay** é aplicável somente no Windows XP ou posterior e somente em uma unidade que o [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determina para ser do tipo **unidade de \_ cdrom**.</span><span class="sxs-lookup"><span data-stu-id="e2edb-216">Currently, **UseAutoPlay** is applicable only on Windows XP or later and only on a drive that [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determines to be of type **DRIVE\_CDROM**.</span></span>

<span data-ttu-id="e2edb-217">Quando **UseAutoPlay** é usado, qualquer ação especificada pelas entradas **Open** ou **ShellExecute** em Autorun. inf é ignorada no Windows XP e omitida da caixa de diálogo de reprodução automática no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2edb-217">When **UseAutoPlay** is used, any action specified by the **open** or **shellexecute** entries in Autorun.inf is ignored on Windows XP and omitted from the AutoPlay dialog on Windows Vista.</span></span>

<span data-ttu-id="e2edb-218">A execução automática normalmente é usada para executar ou carregar automaticamente algo contido na mídia inserida, enquanto a reprodução automática apresenta uma caixa de diálogo que inclui uma lista de ações relevantes que podem ser tomadas e permite que o usuário escolha a ação a ser tomada.</span><span class="sxs-lookup"><span data-stu-id="e2edb-218">AutoRun is typically used to automatically run or load something contained on the inserted media, whereas AutoPlay presents a dialog that includes a list of relevant actions that may be taken and enables the user to choose which action to take.</span></span> <span data-ttu-id="e2edb-219">Para obter mais informações sobre a diferença entre AutoRun e AutoPlay, consulte [criando um aplicativo de CD-ROM habilitado para autorun](autoplay.md) e [usando e configurando a reprodução automática](autoplay2k-using.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e2edb-219">For more information about the difference between AutoRun and AutoPlay, see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md) and [Using and Configuring AutoPlay](autoplay2k-using.md), respectively.</span></span>

### <a name="usage-example"></a><span data-ttu-id="e2edb-220">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="e2edb-220">Usage Example</span></span>

<span data-ttu-id="e2edb-221">Um CD contém três arquivos: autorun. inf, Readme.txt e Music. WMA.</span><span class="sxs-lookup"><span data-stu-id="e2edb-221">A CD contains three files: Autorun.inf, Readme.txt, and Music.wma.</span></span> <span data-ttu-id="e2edb-222">Dependendo da versão do Windows em uso e das opções especificadas em Autorun. inf, o CD pode ser tratado por AutoRun ou reprodução automática quando é inserido (supondo que a execução de AutoRun/AutoPlay esteja habilitada para a unidade na qual o CD é inserido).</span><span class="sxs-lookup"><span data-stu-id="e2edb-222">Depending on the version of Windows in use and options specified in Autorun.inf, the CD may be handled by either AutoRun or AutoPlay when it is inserted (assuming AutoRun/AutoPlay is enabled for the drive into which the CD is inserted).</span></span>

<span data-ttu-id="e2edb-223">Primeiro, considere um arquivo autorun. inf com o conteúdo a seguir, observando que **UseAutoPlay = 1** não está especificado:</span><span class="sxs-lookup"><span data-stu-id="e2edb-223">First, consider an Autorun.inf file with the following contents, noting that **UseAutoPlay=1** is not specified:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
```



<span data-ttu-id="e2edb-224">A ação realizada pelo shell quando este CD é inserido depende da versão do Windows em uso:</span><span class="sxs-lookup"><span data-stu-id="e2edb-224">The action taken by the Shell when this CD is inserted depends on the version of Windows in use:</span></span>

-   <span data-ttu-id="e2edb-225">No Windows XP ou anterior, esse CD é tratado por AutoRun quando é inserido.</span><span class="sxs-lookup"><span data-stu-id="e2edb-225">On Windows XP or earlier, this CD is handled by AutoRun when it is inserted.</span></span> <span data-ttu-id="e2edb-226">Nesse caso, a entrada **ShellExecute** é lida e o Shell invoca o manipulador de arquivos associado a arquivos. txt; Normalmente, isso abriria Readme.txt no bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="e2edb-226">In this case, the **shellexecute** entry is read, and the Shell invokes the file handler associated with .txt files; typically this would open Readme.txt in Notepad.</span></span>
-   <span data-ttu-id="e2edb-227">No Windows Vista, a presença de um arquivo autorun. inf com uma entrada **ShellExecute** faz com que a mídia seja identificada como o tipo "software and Games" de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="e2edb-227">On Windows Vista, the presence of an Autorun.inf file with a **shellexecute** entry causes the media to be identified as AutoPlay type "Software and games".</span></span> <span data-ttu-id="e2edb-228">Nesse caso, o usuário recebe uma caixa de diálogo de reprodução automática que inclui a ação especificada pela entrada **ShellExecute** (apresentada como "carregar Readme.txt" na caixa de diálogo), juntamente com as ações padrão associadas à mídia do tipo "software e jogos".</span><span class="sxs-lookup"><span data-stu-id="e2edb-228">In this case the user is presented with an AutoPlay dialog that includes the action specified by the **shellexecute** entry (presented as "Load Readme.txt" in the dialog), along with default actions associated with media of type "Software and games".</span></span>

<span data-ttu-id="e2edb-229">Para indicar que a reprodução automática deve ser usada em vez de AutoRun no Windows XP, e que a ação especificada pela entrada de ShellExecute de execução automática deve ser suprimida da caixa de diálogo de reprodução automática no Windows Vista, insira **UseAutoPlay** no arquivo autorun. inf da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e2edb-229">To indicate that AutoPlay should be used rather than AutoRun on Windows XP, and that the action specified by the AutoRun shellexecute entry should be suppressed from the AutoPlay dialog on Windows Vista, insert **UseAutoPlay** into the Autorun.inf file as follows:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



<span data-ttu-id="e2edb-230">Mais uma vez, a ação realizada pelo shell quando este CD é inserido depende da versão do Windows em uso.</span><span class="sxs-lookup"><span data-stu-id="e2edb-230">Once again, the action taken by the Shell when this CD is inserted depends on the version of Windows in use.</span></span>

-   <span data-ttu-id="e2edb-231">Nas versões do Windows anteriores ao Windows XP, o AutoRun ainda é usado e a ação especificada por **ShellExecute** é executada, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e2edb-231">On versions of Windows earlier than Windows XP, AutoRun is still used and the action specified by **shellexecute** is performed, as described previously.</span></span> <span data-ttu-id="e2edb-232">(Observe que apenas o AutoRun está disponível em versões do Windows anteriores ao Windows XP.)</span><span class="sxs-lookup"><span data-stu-id="e2edb-232">(Note that only AutoRun is available on versions of Windows earlier than Windows XP.)</span></span>
-   <span data-ttu-id="e2edb-233">No Windows XP, a entrada **UseAutoPlay** faz com que a reprodução automática seja usada no lugar do autorun.</span><span class="sxs-lookup"><span data-stu-id="e2edb-233">On Windows XP, the **UseAutoPlay** entry causes AutoPlay to be used in place of AutoRun.</span></span> <span data-ttu-id="e2edb-234">Nesse caso, a reprodução automática determina que a mídia contém um arquivo de áudio do Windows Media (. WMA) e categoriza o conteúdo como "arquivos de música".</span><span class="sxs-lookup"><span data-stu-id="e2edb-234">In this case, AutoPlay determines that the media contains a Windows Media Audio (.wma) file and categorizes the content as "Music files".</span></span> <span data-ttu-id="e2edb-235">O usuário recebe uma caixa de diálogo de reprodução automática que contém manipuladores registrados para o tipo de mídia de reprodução automática "arquivos de música"; a entrada de ShellExecute de execução automática é ignorada.</span><span class="sxs-lookup"><span data-stu-id="e2edb-235">The user is presented with an AutoPlay dialog containing registered handlers for the "Music files" AutoPlay media type; the AutoRun shellexecute entry is ignored.</span></span>

### <a name="shellexecute"></a><span data-ttu-id="e2edb-236">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="e2edb-236">shellexecute</span></span>

[<span data-ttu-id="e2edb-237">Versão 5,0.</span><span class="sxs-lookup"><span data-stu-id="e2edb-237">Version 5.0.</span></span>](versions.md) <span data-ttu-id="e2edb-238">A entrada **ShellExecute** especifica um aplicativo ou arquivo de dados que o autorun usará para chamar [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="e2edb-238">The **shellexecute** entry specifies an application or data file that AutoRun will use to call [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a><span data-ttu-id="e2edb-239">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-239">Parameters</span></span>

-   <span data-ttu-id="e2edb-240">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="e2edb-240">*filepath*</span></span>

    <span data-ttu-id="e2edb-241">Uma cadeia de caracteres que contém o caminho totalmente qualificado do diretório que contém os dados ou o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="e2edb-241">A string that contains the fully qualified path of the directory that contains the data or executable file.</span></span> <span data-ttu-id="e2edb-242">Se nenhum caminho for especificado, o arquivo deverá estar no diretório raiz da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2edb-242">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="e2edb-243">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="e2edb-243">*filename*</span></span>

    <span data-ttu-id="e2edb-244">Uma cadeia de caracteres que contém o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-244">A string that contains the file's name.</span></span> <span data-ttu-id="e2edb-245">Se for um arquivo executável, ele será iniciado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-245">If it is an executable file, it is launched.</span></span> <span data-ttu-id="e2edb-246">Se for um arquivo de dados, ele deverá ser um membro de um [tipo de arquivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e2edb-246">If it is a data file, it must be a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="e2edb-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) inicia o comando padrão associado ao tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) launches the default command associated with the file type.</span></span>

-   <span data-ttu-id="e2edb-248">*paramx*</span><span class="sxs-lookup"><span data-stu-id="e2edb-248">*paramx*</span></span>

    <span data-ttu-id="e2edb-249">Contém parâmetros adicionais que devem ser passados para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="e2edb-249">Contains any additional parameters that should be passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

### <a name="remarks"></a><span data-ttu-id="e2edb-250">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-250">Remarks</span></span>

<span data-ttu-id="e2edb-251">Essa entrada é semelhante à [aberta](#parameters), mas permite que você use informações de [Associação de arquivo](fa-intro.md) para executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-251">This entry is similar to [open](#parameters), but it allows you to use [file association](fa-intro.md) information to run the application.</span></span>

### <a name="shell"></a><span data-ttu-id="e2edb-252">shell</span><span class="sxs-lookup"><span data-stu-id="e2edb-252">shell</span></span>

<span data-ttu-id="e2edb-253">A entrada do **shell** especifica um comando padrão para o menu de atalho da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2edb-253">The **shell** entry specifies a default command for the drive's shortcut menu.</span></span>


```
shell=verb
```



### <a name="parameters"></a><span data-ttu-id="e2edb-254">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-254">Parameters</span></span>

-   <span data-ttu-id="e2edb-255">*verbo*</span><span class="sxs-lookup"><span data-stu-id="e2edb-255">*verb*</span></span>

    <span data-ttu-id="e2edb-256">O verbo que corresponde ao comando de menu.</span><span class="sxs-lookup"><span data-stu-id="e2edb-256">The verb that corresponds to the menu command.</span></span> <span data-ttu-id="e2edb-257">O verbo e seu comando de menu associado devem ser definidos no arquivo autorun. inf com uma entrada de [ \\ verbo de shell](#shellverb) .</span><span class="sxs-lookup"><span data-stu-id="e2edb-257">The verb and its associated menu command must be defined in the Autorun.inf file with a [shell\\verb](#shellverb) entry.</span></span>

### <a name="remarks"></a><span data-ttu-id="e2edb-258">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-258">Remarks</span></span>

<span data-ttu-id="e2edb-259">Quando um usuário clica com o botão direito do mouse no ícone da unidade, um menu de atalho é exibido.</span><span class="sxs-lookup"><span data-stu-id="e2edb-259">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="e2edb-260">Se um arquivo autorun. inf estiver presente, o comando de menu de atalho padrão será obtido dele.</span><span class="sxs-lookup"><span data-stu-id="e2edb-260">If an Autorun.inf file is present, the default shortcut menu command is taken from it.</span></span> <span data-ttu-id="e2edb-261">Esse comando também é executado quando o usuário clica duas vezes no ícone da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2edb-261">This command also executes when the user double-clicks the drive's icon.</span></span>

<span data-ttu-id="e2edb-262">Para especificar o comando de menu de atalho padrão, primeiro defina seu verbo, Cadeia de caracteres de comando e texto de menu com o [ \\ verbo do Shell](#shellverb).</span><span class="sxs-lookup"><span data-stu-id="e2edb-262">To specify the default shortcut menu command, first define its verb, command string, and menu text with [shell\\verb](#shellverb).</span></span> <span data-ttu-id="e2edb-263">Em seguida, use o Shell para transformá-lo no comando de menu de atalho padrão.</span><span class="sxs-lookup"><span data-stu-id="e2edb-263">Then use shell to make it the default shortcut menu command.</span></span> <span data-ttu-id="e2edb-264">Caso contrário, o texto do item de menu padrão será "AutoPlay", que inicia o aplicativo especificado pela entrada [aberta](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="e2edb-264">Otherwise, the default menu item text will be "AutoPlay", which launches the application specified by the [open](#parameters) entry.</span></span>

### <a name="shellverb"></a><span data-ttu-id="e2edb-265">verbo do Shell \\</span><span class="sxs-lookup"><span data-stu-id="e2edb-265">shell\\verb</span></span>

<span data-ttu-id="e2edb-266">A entrada de **\\ verbo do Shell** adiciona um comando personalizado ao menu de atalho da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2edb-266">The **shell\\verb** entry adds a custom command to the drive's shortcut menu.</span></span>


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a><span data-ttu-id="e2edb-267">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-267">Parameters</span></span>

-   <span data-ttu-id="e2edb-268">*verbo*</span><span class="sxs-lookup"><span data-stu-id="e2edb-268">*verb*</span></span>

    <span data-ttu-id="e2edb-269">O verbo do comando de menu.</span><span class="sxs-lookup"><span data-stu-id="e2edb-269">The menu command's verb.</span></span> <span data-ttu-id="e2edb-270">A entrada de *_\\ comando_* do _verbo_ do **shell \\** associa o verbo a um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="e2edb-270">The **shell\\**_verb_*_\\command_* entry associates the verb with an executable file.</span></span> <span data-ttu-id="e2edb-271">Os verbos não devem conter espaços inseridos.</span><span class="sxs-lookup"><span data-stu-id="e2edb-271">Verbs must not contain embedded spaces.</span></span> <span data-ttu-id="e2edb-272">Por padrão, *Verb* é o texto que é exibido no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="e2edb-272">By default, *verb* is the text that is displayed in the shortcut menu.</span></span>

-   <span data-ttu-id="e2edb-273">*Filename.exe*</span><span class="sxs-lookup"><span data-stu-id="e2edb-273">*Filename.exe*</span></span>

    <span data-ttu-id="e2edb-274">O caminho e o nome do arquivo do aplicativo que executa a ação.</span><span class="sxs-lookup"><span data-stu-id="e2edb-274">The path and file name of the application that performs the action.</span></span>

-   <span data-ttu-id="e2edb-275">*MenuText*</span><span class="sxs-lookup"><span data-stu-id="e2edb-275">*MenuText*</span></span>

    <span data-ttu-id="e2edb-276">Esse parâmetro especifica o texto que é exibido no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="e2edb-276">This parameter specifies the text that is displayed in the shortcut menu.</span></span> <span data-ttu-id="e2edb-277">Se for omitido, *verbo* será exibido.</span><span class="sxs-lookup"><span data-stu-id="e2edb-277">If it is omitted, *verb* is displayed.</span></span> <span data-ttu-id="e2edb-278">*MenuText* pode ser com maiúsculas e minúsculas e pode conter espaços.</span><span class="sxs-lookup"><span data-stu-id="e2edb-278">*MenuText* can be mixed-case and can contain spaces.</span></span> <span data-ttu-id="e2edb-279">Você pode definir uma tecla de atalho para o item de menu colocando um e comercial (&) na frente da letra.</span><span class="sxs-lookup"><span data-stu-id="e2edb-279">You can set a shortcut key for the menu item by putting an ampersand (&) in front of the letter.</span></span>

### <a name="remarks"></a><span data-ttu-id="e2edb-280">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-280">Remarks</span></span>

<span data-ttu-id="e2edb-281">Quando um usuário clica com o botão direito do mouse no ícone da unidade, um menu de atalho é exibido.</span><span class="sxs-lookup"><span data-stu-id="e2edb-281">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="e2edb-282">Adicionar entradas de **\\ verbo de shell** ao arquivo autorun. inf da unidade permite que você adicione comandos a esse menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="e2edb-282">Adding **shell\\verb** entries to the drive's Autorun.inf file allows you to add commands to this shortcut menu.</span></span>

<span data-ttu-id="e2edb-283">Há duas partes nessa entrada, que devem estar em linhas separadas.</span><span class="sxs-lookup"><span data-stu-id="e2edb-283">There are two parts to this entry, which must be on separate lines.</span></span> <span data-ttu-id="e2edb-284">A primeira parte é o *_\\ comando_* de _verbo_ do **shell \\**.</span><span class="sxs-lookup"><span data-stu-id="e2edb-284">The first part is **shell\\**_verb_*_\\command_*.</span></span> <span data-ttu-id="e2edb-285">É obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e2edb-285">It is required.</span></span> <span data-ttu-id="e2edb-286">Ele associa uma cadeia de caracteres, chamada de *verbo*, com o aplicativo a ser iniciado quando o comando é executado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-286">It associates a string, called a *verb*, with the application to launch when the command runs.</span></span> <span data-ttu-id="e2edb-287">A segunda parte é a entrada de _verbo_ do **shell \\**.</span><span class="sxs-lookup"><span data-stu-id="e2edb-287">The second part is the **shell\\**_verb_ entry.</span></span> <span data-ttu-id="e2edb-288">É opcional.</span><span class="sxs-lookup"><span data-stu-id="e2edb-288">It is optional.</span></span> <span data-ttu-id="e2edb-289">Você pode incluí-lo para especificar o texto que é exibido no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="e2edb-289">You can include it to specify the text that displays in the shortcut menu.</span></span>

<span data-ttu-id="e2edb-290">Para especificar um comando de menu de atalho padrão, defina o verbo com o **\\ verbo Shell** e torne-o o comando padrão com a entrada [shell](#autoruninf-entries) .</span><span class="sxs-lookup"><span data-stu-id="e2edb-290">To specify a default shortcut menu command, define the verb with **shell\\verb**, and make it the default command with the [shell](#autoruninf-entries) entry.</span></span>

<span data-ttu-id="e2edb-291">O fragmento autorun. inf de exemplo a seguir associa o verbo *readit* com a cadeia de caracteres de comando "Notepad ABC \\readme.txt".</span><span class="sxs-lookup"><span data-stu-id="e2edb-291">The following sample Autorun.inf fragment associates the *readit* verb with the command string "Notepad abc\\readme.txt".</span></span> <span data-ttu-id="e2edb-292">O texto do menu é "Read me" e ' M' ' é definido como a tecla de atalho do item.</span><span class="sxs-lookup"><span data-stu-id="e2edb-292">The menu text is "Read Me", and 'M' is defined as the item's shortcut key.</span></span> <span data-ttu-id="e2edb-293">Quando o usuário seleciona esse comando, o arquivo ABCreadme.txt da unidade \\ é aberto com o bloco de notas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e2edb-293">When the user selects this command, the drive's abc\\readme.txt file opens with Microsoft Notepad.</span></span>


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a><span data-ttu-id="e2edb-294">\[Chaves de conteúdo \]</span><span class="sxs-lookup"><span data-stu-id="e2edb-294">\[Content\] Keys</span></span>

<span data-ttu-id="e2edb-295">Há três chaves de tipo de arquivo: **MusicFiles**, **PictureFiles** e **VideoFiles**.</span><span class="sxs-lookup"><span data-stu-id="e2edb-295">There are three file type keys: **MusicFiles**, **PictureFiles**, and **VideoFiles**.</span></span>

<span data-ttu-id="e2edb-296">Se um desses conteúdos for definido como true por meio de um dos valores 1, y, Yes, t ou true, a interface de usuário da reprodução automática exibirá os manipuladores associados a esse tipo de conteúdo, independentemente de o conteúdo desse tipo existir na mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-296">If one of these contents is set to true through one the case-insensitive values 1, y, yes, t, or true, the Autoplay UI displays the handlers associated with that content type regardless of whether content of that type exists on the media.</span></span>

<span data-ttu-id="e2edb-297">Se um desses conteúdos for definido como falso por meio de um valor de não diferenciação de maiúsculas e minúsculas 0, n, não, f ou false, a interface do usuário da reprodução automática não exibirá os manipuladores associados a esse tipo de conteúdo, mesmo que o conteúdo desse tipo seja detectado na mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-297">If one of these contents is set to false through one the case-insensitive values 0, n, no, f, or false, the Autoplay UI does not display the handlers associated with that content type even if content of that type is detected on the media.</span></span>

<span data-ttu-id="e2edb-298">O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção de conteúdo à reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="e2edb-298">Use of this section is intended to allow content authors to communicate the intent of content to Autoplay.</span></span> <span data-ttu-id="e2edb-299">Por exemplo, um CD pode ser Categorizado como contendo apenas conteúdo de música, embora também tenha imagens e vídeos e, de outra forma, seria visto como tendo conteúdo misto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-299">For instance, a CD can be categorized as containing only music content even though it also has pictures and videos and would otherwise be seen as having mixed content.</span></span>

<span data-ttu-id="e2edb-300">A seção de **\[ conteúdo \]** só tem suporte no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="e2edb-300">The **\[Content\]** section is only supported under Windows Vista and later.</span></span>


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a><span data-ttu-id="e2edb-301">\[\]Chaves ExclusiveContentPaths</span><span class="sxs-lookup"><span data-stu-id="e2edb-301">\[ExclusiveContentPaths\] Keys</span></span>

<span data-ttu-id="e2edb-302">As pastas listadas nesta seção limitam a reprodução automática para pesquisar somente as pastas e suas subpastas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-302">Folders listed in this section limit Autoplay to searching only those folders and their subfolders for content.</span></span> <span data-ttu-id="e2edb-303">Eles podem ser fornecidos com ou sem uma barra invertida à esquerda ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="e2edb-303">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="e2edb-304">Em ambos os casos, eles são usados como caminhos absolutos do diretório raiz da mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-304">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="e2edb-305">No caso de pastas com espaços em seus nomes, não as coloque entre aspas à medida que as aspas são feitas literalmente como parte do caminho.</span><span class="sxs-lookup"><span data-stu-id="e2edb-305">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="e2edb-306">O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção de conteúdo à reprodução automática e reduzam o tempo de varredura limitando a verificação a determinadas áreas significativas da mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-306">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="e2edb-307">A seguir estão todos os caminhos válidos</span><span class="sxs-lookup"><span data-stu-id="e2edb-307">The following are all valid paths</span></span>


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="e2edb-308">A seção **\[ ExclusiveContentPaths \]** só tem suporte no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="e2edb-308">The **\[ExclusiveContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="ignorecontentpaths-keys"></a><span data-ttu-id="e2edb-309">\[\]Chaves IgnoreContentPaths</span><span class="sxs-lookup"><span data-stu-id="e2edb-309">\[IgnoreContentPaths\] Keys</span></span>

<span data-ttu-id="e2edb-310">As pastas listadas nesta seção e suas subpastas são ignoradas pela reprodução automática durante a pesquisa de conteúdo em uma mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-310">Folders listed in this section, and their subfolders, are ignored by Autoplay when searching a media for content.</span></span> <span data-ttu-id="e2edb-311">Eles podem ser fornecidos com ou sem uma barra invertida à esquerda ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="e2edb-311">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="e2edb-312">Em ambos os casos, eles são usados como caminhos absolutos do diretório raiz da mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-312">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="e2edb-313">No caso de pastas com espaços em seus nomes, não as coloque entre aspas à medida que as aspas são feitas literalmente como parte do caminho.</span><span class="sxs-lookup"><span data-stu-id="e2edb-313">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="e2edb-314">Os caminhos nesta seção têm precedência sobre caminhos na seção **\[ ExclusiveContentPaths \]** .</span><span class="sxs-lookup"><span data-stu-id="e2edb-314">Paths in this section take precedence over paths in the **\[ExclusiveContentPaths\]** section.</span></span> <span data-ttu-id="e2edb-315">Se um caminho fornecido em **\[ IgnoreContentPaths \]** for uma subpasta de um caminho fornecido em **\[ ExclusiveContentPaths \]**, ele ainda será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-315">If a path given in **\[IgnoreContentPaths\]** is a subfolder of a path given in **\[ExclusiveContentPaths\]**, it is still ignored.</span></span>

<span data-ttu-id="e2edb-316">O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção de conteúdo à reprodução automática e reduzam o tempo de varredura limitando a verificação a determinadas áreas significativas da mídia.</span><span class="sxs-lookup"><span data-stu-id="e2edb-316">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="e2edb-317">A seguir estão todos os caminhos válidos</span><span class="sxs-lookup"><span data-stu-id="e2edb-317">The following are all valid paths</span></span>


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="e2edb-318">A seção **\[ IgnoreContentPaths \]** só tem suporte no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="e2edb-318">The **\[IgnoreContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="deviceinstall-keys"></a><span data-ttu-id="e2edb-319">\[\]Chaves DeviceInstall</span><span class="sxs-lookup"><span data-stu-id="e2edb-319">\[DeviceInstall\] Keys</span></span>

### <a name="driverpath"></a><span data-ttu-id="e2edb-320">DriverPath</span><span class="sxs-lookup"><span data-stu-id="e2edb-320">DriverPath</span></span>

<span data-ttu-id="e2edb-321">A entrada **DriverPath** especifica um diretório a ser pesquisado recursivamente para arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="e2edb-321">The **DriverPath** entry specifies a directory to search recursively for driver files.</span></span> <span data-ttu-id="e2edb-322">Esse comando é usado durante uma instalação de driver e não faz parte de uma operação de AutoRun.</span><span class="sxs-lookup"><span data-stu-id="e2edb-322">This command is used during a driver installation and is not part of an AutoRun operation.</span></span> <span data-ttu-id="e2edb-323">A seção **\[ DeviceInstall \]** só tem suporte no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2edb-323">The **\[DeviceInstall\]** section is only supported under Windows XP.</span></span>


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a><span data-ttu-id="e2edb-324">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2edb-324">Parameters</span></span>

-   <span data-ttu-id="e2edb-325">*DirectoryPath*</span><span class="sxs-lookup"><span data-stu-id="e2edb-325">*directorypath*</span></span>

    <span data-ttu-id="e2edb-326">Um caminho para um diretório que o Windows procura por arquivos de driver, juntamente com todos os seus subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="e2edb-326">A path to a directory that Windows searches for driver files, along with all of its subdirectories.</span></span>

### <a name="remarks"></a><span data-ttu-id="e2edb-327">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-327">Remarks</span></span>

<span data-ttu-id="e2edb-328">Não use letras de unidade no *DirectoryPath* , pois elas são alteradas de um computador para o outro.</span><span class="sxs-lookup"><span data-stu-id="e2edb-328">Do not use drive letters in *directorypath* as they change from one computer to the next.</span></span>

<span data-ttu-id="e2edb-329">Para pesquisar vários diretórios, adicione uma entrada **DriverPath** para cada diretório como neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-329">To search multiple directories, add a **DriverPath** entry for each directory as in this example.</span></span>


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



<span data-ttu-id="e2edb-330">Se nenhuma entrada **DriverPath** for fornecida na seção **\[ DeviceInstall \]** ou a entrada **DriverPath** não tiver nenhum valor, essa unidade será ignorada durante uma pesquisa de arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="e2edb-330">If no **DriverPath** entry is provided in the **\[DeviceInstall\]** section or the **DriverPath** entry has no value, then that drive is skipped during a search for driver files.</span></span>

 

 
