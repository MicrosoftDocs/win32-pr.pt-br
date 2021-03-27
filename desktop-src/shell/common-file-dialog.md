---
description: A partir do Windows Vista, a caixa de diálogo de item comum substitui a caixa de diálogo de arquivo comum mais antiga quando usada para abrir ou salvar um arquivo.
title: Caixa de diálogo de item comum
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296218"
---
# <a name="common-item-dialog"></a><span data-ttu-id="7691a-103">Caixa de diálogo de item comum</span><span class="sxs-lookup"><span data-stu-id="7691a-103">Common Item Dialog</span></span>

<span data-ttu-id="7691a-104">A partir do Windows Vista, a caixa de diálogo de item comum substitui a caixa de diálogo de arquivo comum mais antiga quando usada para abrir ou salvar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7691a-104">Starting with Windows Vista, the Common Item Dialog supersedes the older Common File Dialog when used to open or save a file.</span></span> <span data-ttu-id="7691a-105">A caixa de diálogo de item comum é usada em duas variações: a caixa de diálogo **abrir** e **salvar** .</span><span class="sxs-lookup"><span data-stu-id="7691a-105">The Common Item Dialog is used in two variations: the **Open** dialog and the **Save** dialog.</span></span> <span data-ttu-id="7691a-106">Essas duas caixas de diálogo compartilham a maior parte de sua funcionalidade, mas cada uma tem seus próprios métodos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="7691a-106">These two dialogs share most of their functionality, but each has its own unique methods.</span></span>

<span data-ttu-id="7691a-107">Embora essa versão mais recente seja chamada de caixa de diálogo de item comum, ela continua a ser chamada de caixa de diálogo de arquivo comum na maioria das documentações.</span><span class="sxs-lookup"><span data-stu-id="7691a-107">While this newer version is named the Common Item Dialog, it continues to be called the Common File Dialog in most documentation.</span></span> <span data-ttu-id="7691a-108">A menos que esteja lidando especificamente com uma versão mais antiga do Windows, você deve supor que qualquer menção da caixa de diálogo arquivo comum se refere a essa caixa de diálogo de item comum.</span><span class="sxs-lookup"><span data-stu-id="7691a-108">Unless you are dealing specifically with an older version of Windows, you should assume that any mention of the Common File Dialog refers to this Common Item Dialog.</span></span>

<span data-ttu-id="7691a-109">Os tópicos a seguir são discutidos aqui:</span><span class="sxs-lookup"><span data-stu-id="7691a-109">The following topics are discussed here:</span></span>

-   [<span data-ttu-id="7691a-110">IFileDialog, IFileOpenDialog e IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="7691a-110">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [<span data-ttu-id="7691a-111">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="7691a-111">Sample Usage</span></span>](#sample-usage)
-   [<span data-ttu-id="7691a-112">Ouvindo eventos a partir da caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="7691a-112">Listening to Events from the Dialog</span></span>](#listening-to-events-from-the-dialog)
    -   [<span data-ttu-id="7691a-113">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="7691a-113">OnFileOk</span></span>](#onfileok)
    -   [<span data-ttu-id="7691a-114">OnShareViolation e onoverwrite</span><span class="sxs-lookup"><span data-stu-id="7691a-114">OnShareViolation and OnOverwrite</span></span>](#onshareviolation-and-onoverwrite)
-   [<span data-ttu-id="7691a-115">Personalizando a caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="7691a-115">Customizing the Dialog</span></span>](#customizing-the-dialog)
    -   [<span data-ttu-id="7691a-116">Adicionando opções ao botão OK</span><span class="sxs-lookup"><span data-stu-id="7691a-116">Adding Options to the OK Button</span></span>](#adding-options-to-the-ok-button)
    -   [<span data-ttu-id="7691a-117">Respondendo a eventos em controles adicionados</span><span class="sxs-lookup"><span data-stu-id="7691a-117">Responding to Events in Added Controls</span></span>](#responding-to-events-in-added-controls)
-   [<span data-ttu-id="7691a-118">Exemplos completos</span><span class="sxs-lookup"><span data-stu-id="7691a-118">Full Samples</span></span>](#full-samples)
-   [<span data-ttu-id="7691a-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7691a-119">Related topics</span></span>](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a><span data-ttu-id="7691a-120">IFileDialog, IFileOpenDialog e IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="7691a-120">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>

<span data-ttu-id="7691a-121">O Windows Vista fornece implementações das caixas de diálogo **abrir** e **salvar** : CLSID \_ FileOpenDialog e CLSID \_ FileSaveDialog.</span><span class="sxs-lookup"><span data-stu-id="7691a-121">Windows Vista provides implementations of the **Open** and **Save** dialogs: CLSID\_FileOpenDialog and CLSID\_FileSaveDialog.</span></span> <span data-ttu-id="7691a-122">Essas caixas de diálogo são mostradas aqui.</span><span class="sxs-lookup"><span data-stu-id="7691a-122">Those dialog boxes are shown here.</span></span>

![captura de tela da caixa de diálogo abrir](images/cid/openfiledialog.png)

![captura de tela da caixa de diálogo Salvar como](images/cid/savefiledialog.png)

<span data-ttu-id="7691a-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) e [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) herdam de [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) e compartilham grande parte de sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="7691a-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) and [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) inherit from [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and share much of their functionality.</span></span> <span data-ttu-id="7691a-126">Além disso, a caixa de diálogo **abrir** dá suporte a **IFileOpenDialog** e a caixa de diálogo **salvar** dá suporte a **IFileSaveDialog**.</span><span class="sxs-lookup"><span data-stu-id="7691a-126">In addition, the **Open** dialog supports **IFileOpenDialog**, and the **Save** dialog supports **IFileSaveDialog**.</span></span>

<span data-ttu-id="7691a-127">A implementação de caixa de diálogo de item comum encontrada no Windows Vista fornece várias vantagens em relação à implementação fornecida em versões anteriores:</span><span class="sxs-lookup"><span data-stu-id="7691a-127">The Common Item Dialog implementation found in Windows Vista provides several advantages over the implementation provided in earlier versions:</span></span>

-   <span data-ttu-id="7691a-128">Dá suporte ao uso direto do namespace do Shell por meio de [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) em vez de usar caminhos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7691a-128">Supports direct use of the Shell namespace through [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) instead of using file system paths.</span></span>
-   <span data-ttu-id="7691a-129">Permite a personalização simples da caixa de diálogo, como a definição do rótulo no botão **OK** , sem a necessidade de um procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="7691a-129">Enables simple customization of the dialog, such as setting the label on the **OK** button, without requiring a hook procedure.</span></span>
-   <span data-ttu-id="7691a-130">Dá suporte à personalização mais ampla da caixa de diálogo pela adição de um conjunto de controles controlados por dados que operam sem um modelo de caixa de diálogo do Win32.</span><span class="sxs-lookup"><span data-stu-id="7691a-130">Supports more extensive customization of the dialog by the addition of a set of data-driven controls that operate without a Win32 dialog template.</span></span> <span data-ttu-id="7691a-131">Esse esquema de personalização libera o processo de chamada do layout da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7691a-131">This customization scheme frees the calling process from UI layout.</span></span> <span data-ttu-id="7691a-132">Como as alterações no design da caixa de diálogo continuam a usar esse modelo de dados, a implementação da caixa de diálogo não está vinculada à versão atual específica da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-132">Since any changes to the dialog design continue to use this data model, the dialog implementation is not tied to the specific current version of the dialog.</span></span>
-   <span data-ttu-id="7691a-133">Dá suporte à notificação do chamador de eventos na caixa de diálogo, como alteração de seleção ou alteração de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7691a-133">Supports caller notification of events within the dialog, such as selection change or file type change.</span></span> <span data-ttu-id="7691a-134">Também permite que o processo de chamada Conecte determinados eventos na caixa de diálogo, como a análise.</span><span class="sxs-lookup"><span data-stu-id="7691a-134">Also enables the calling process to hook certain events in the dialog, such as the parsing.</span></span>
-   <span data-ttu-id="7691a-135">Apresenta novos recursos de caixa de diálogo, como adicionar locais especificados pelo chamador à barra de **locais** .</span><span class="sxs-lookup"><span data-stu-id="7691a-135">Introduces new dialog features such as adding caller-specified places to the **Places** bar.</span></span>
-   <span data-ttu-id="7691a-136">Na caixa de diálogo **salvar** , os desenvolvedores podem aproveitar os novos recursos de metadados do shell do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7691a-136">In the **Save** dialog, developers can take advantage of new metadata features of the Windows Vista Shell.</span></span>

<span data-ttu-id="7691a-137">Além disso, os desenvolvedores podem optar por implementar as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="7691a-137">Additionally, developers can choose to implement the following interfaces:</span></span>

-   <span data-ttu-id="7691a-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) para receber notificações de eventos dentro da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) to receive notifications of events within the dialog.</span></span>
-   <span data-ttu-id="7691a-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) para adicionar controles à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) to add controls to the dialog.</span></span>
-   <span data-ttu-id="7691a-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) a ser notificado sobre eventos nesses controles adicionados.</span><span class="sxs-lookup"><span data-stu-id="7691a-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) to be notified of events in those added controls.</span></span>

<span data-ttu-id="7691a-141">A caixa de diálogo **abrir** ou **salvar** retorna um objeto [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) ou [**IShellitemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) para o processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="7691a-141">The **Open** or **Save** dialog returns an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) or [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) object to the calling process.</span></span> <span data-ttu-id="7691a-142">O chamador pode então usar um objeto **IShellItem** individual para obter um caminho do sistema de arquivos ou abrir um fluxo no item para ler ou gravar informações.</span><span class="sxs-lookup"><span data-stu-id="7691a-142">The caller can then use an individual **IShellItem** object to get a file system path or to open a stream on the item to read or write information.</span></span>

<span data-ttu-id="7691a-143">Os sinalizadores e as opções disponíveis para os novos métodos de diálogo são muito semelhantes aos sinalizadores **OFN** mais antigos encontrados na estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e usados em [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="7691a-143">Flags and options available to the new dialog methods are very similar to the older **OFN** flags found in the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure and used in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="7691a-144">Muitos deles são exatamente iguais, exceto que começam com um prefixo de FOS.</span><span class="sxs-lookup"><span data-stu-id="7691a-144">Many of them are exactly the same, except that they begin with an FOS prefix.</span></span> <span data-ttu-id="7691a-145">A lista completa pode ser encontrada nos tópicos [**IFileDialog:: getoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) e [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) .</span><span class="sxs-lookup"><span data-stu-id="7691a-145">The complete list can be found in the [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) and [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) topics.</span></span> <span data-ttu-id="7691a-146">As caixas de diálogo **abrir** e **salvar** são criadas por padrão com os sinalizadores mais comuns.</span><span class="sxs-lookup"><span data-stu-id="7691a-146">**Open** and **Save** dialogs are created by default with the most common flags.</span></span> <span data-ttu-id="7691a-147">Para a caixa de diálogo **aberta** , isso é (FOS \_ PATHMUSTEXIST \| FOS \_ FILEMUSTEXIST \| FOS \_ NOCHANGEDIR) e, para a caixa de diálogo **salvar** , isso é (FOS \_ OVERWRITEPROMPT FOS NOREADONLYRETURN \| \_ \| FOS \_ PATHMUSTEXIST \| FOS \_ NOCHANGEDIR).</span><span class="sxs-lookup"><span data-stu-id="7691a-147">For the **Open** dialog, this is (FOS\_PATHMUSTEXIST \| FOS\_FILEMUSTEXIST \| FOS\_NOCHANGEDIR) and for the **Save** dialog this is (FOS\_OVERWRITEPROMPT \| FOS\_NOREADONLYRETURN \| FOS\_PATHMUSTEXIST \| FOS\_NOCHANGEDIR).</span></span>

<span data-ttu-id="7691a-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) e suas interfaces descendentes herdam de e estendem [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span><span class="sxs-lookup"><span data-stu-id="7691a-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and its descendant interfaces inherit from and extend [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="7691a-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) usa como seu único parâmetro o identificador da janela pai.</span><span class="sxs-lookup"><span data-stu-id="7691a-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) takes as its only parameter the handle of the parent window.</span></span> <span data-ttu-id="7691a-150">Se **Mostrar** retornar com êxito, haverá um resultado válido.</span><span class="sxs-lookup"><span data-stu-id="7691a-150">If **Show** returns successfully, there is a valid result.</span></span> <span data-ttu-id="7691a-151">Se ele retornar `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , significa que o usuário cancelou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-151">If it returns `HRESULT_FROM_WIN32(ERROR_CANCELLED)`, it means the user canceled the dialog.</span></span> <span data-ttu-id="7691a-152">Ele também pode retornar, legitimamente, outro código de erro, como **E \_ OUTOFMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="7691a-152">It might also legitimately return another error code such as **E\_OUTOFMEMORY**.</span></span>

### <a name="sample-usage"></a><span data-ttu-id="7691a-153">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="7691a-153">Sample Usage</span></span>

<span data-ttu-id="7691a-154">As seções a seguir mostram o código de exemplo para uma variedade de tarefas de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-154">The following sections show example code for a variety of dialog tasks.</span></span>

-   [<span data-ttu-id="7691a-155">Uso básico</span><span class="sxs-lookup"><span data-stu-id="7691a-155">Basic Usage</span></span>](#basic-usage)
-   [<span data-ttu-id="7691a-156">Limitando resultados a itens do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="7691a-156">Limiting Results to File System Items</span></span>](#limiting-results-to-file-system-items)
-   [<span data-ttu-id="7691a-157">Especificando tipos de arquivo para uma caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="7691a-157">Specifying File Types for a Dialog</span></span>](#specifying-file-types-for-a-dialog)
-   [<span data-ttu-id="7691a-158">Controlando a pasta padrão</span><span class="sxs-lookup"><span data-stu-id="7691a-158">Controlling the Default Folder</span></span>](#controlling-the-default-folder)
-   [<span data-ttu-id="7691a-159">Adicionando itens à barra de locais</span><span class="sxs-lookup"><span data-stu-id="7691a-159">Adding Items to the Places Bar</span></span>](#adding-items-to-the-places-bar)
-   [<span data-ttu-id="7691a-160">Persistência de estado</span><span class="sxs-lookup"><span data-stu-id="7691a-160">State Persistence</span></span>](#state-persistence)
-   [<span data-ttu-id="7691a-161">Recursos de seleção ascada</span><span class="sxs-lookup"><span data-stu-id="7691a-161">Multiselect Capabilities</span></span>](#multiselect-capabilities)

<span data-ttu-id="7691a-162">A maior parte do código de exemplo pode ser encontrada no [exemplo de caixa de diálogo SDK do Windows arquivo comum](samples-commonfiledialog.md).</span><span class="sxs-lookup"><span data-stu-id="7691a-162">Most of the sample code can be found in the Windows SDK [Common File Dialog Sample](samples-commonfiledialog.md).</span></span>

### <a name="basic-usage"></a><span data-ttu-id="7691a-163">Uso básico</span><span class="sxs-lookup"><span data-stu-id="7691a-163">Basic Usage</span></span>

<span data-ttu-id="7691a-164">O exemplo a seguir ilustra como iniciar uma caixa de diálogo **aberta** .</span><span class="sxs-lookup"><span data-stu-id="7691a-164">The following example illustrates how to launch an **Open** dialog.</span></span> <span data-ttu-id="7691a-165">Neste exemplo, ele é restrito aos documentos do Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="7691a-165">In this example, it is restricted to Microsoft Word documents.</span></span>

> [!Note]  
> <span data-ttu-id="7691a-166">Vários exemplos neste tópico usam a `CDialogEventHandler_CreateInstance` função auxiliar para criar uma instância da implementação [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) .</span><span class="sxs-lookup"><span data-stu-id="7691a-166">Several examples in this topic use the `CDialogEventHandler_CreateInstance` helper function to create an instance of the [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) implementation.</span></span> <span data-ttu-id="7691a-167">Para usar essa função em seu próprio código, copie o código-fonte da `CDialogEventHandler_CreateInstance` função do [exemplo de caixa de diálogo de arquivo comum](samples-commonfiledialog.md), do qual todos os exemplos neste tópico são tirados.</span><span class="sxs-lookup"><span data-stu-id="7691a-167">To use this function in your own code, copy the source code for the `CDialogEventHandler_CreateInstance` function from the [Common File Dialog Sample](samples-commonfiledialog.md), from which all of the examples in this topic are taken.</span></span>

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a><span data-ttu-id="7691a-168">Limitando resultados a itens do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="7691a-168">Limiting Results to File System Items</span></span>

<span data-ttu-id="7691a-169">O exemplo a seguir, extraído acima, demonstra como restringir os resultados em itens do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7691a-169">The following example, taken from above, demonstrates how to restrict results to file system items.</span></span> <span data-ttu-id="7691a-170">Observe que [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adiciona o novo sinalizador a um valor obtido por meio de [**IFileDialog:: getoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span><span class="sxs-lookup"><span data-stu-id="7691a-170">Note that [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adds the new flag to a value obtained through [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span></span> <span data-ttu-id="7691a-171">Esse é o método recomendado.</span><span class="sxs-lookup"><span data-stu-id="7691a-171">This is the recommended method.</span></span>


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a><span data-ttu-id="7691a-172">Especificando tipos de arquivo para uma caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="7691a-172">Specifying File Types for a Dialog</span></span>

<span data-ttu-id="7691a-173">Para definir tipos de arquivo específicos que a caixa de diálogo pode manipular, use o método [**IFileDialog:: SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) .</span><span class="sxs-lookup"><span data-stu-id="7691a-173">To set specific file types that the dialog can handle, use the [**IFileDialog::SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) method.</span></span> <span data-ttu-id="7691a-174">Esse método aceita uma matriz de estruturas [**COMDLG \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , cada uma representando um tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7691a-174">That method accepts an array of [**COMDLG\_FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) structures, each of which represents a file type.</span></span>

<span data-ttu-id="7691a-175">O mecanismo de extensão padrão em uma caixa de diálogo não é alterado em [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="7691a-175">The default extension mechanism in a dialog is unchanged from [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="7691a-176">A extensão de nome de arquivo que é anexada ao texto que o usuário digita na caixa de edição de nome de arquivo é inicializada quando o diálogo é aberto.</span><span class="sxs-lookup"><span data-stu-id="7691a-176">The file name extension that is appended to the text the user types in the file name edit box is initialized when the dialog opens.</span></span> <span data-ttu-id="7691a-177">Ele deve corresponder ao tipo de arquivo padrão (selecionado conforme a caixa de diálogo é aberta).</span><span class="sxs-lookup"><span data-stu-id="7691a-177">It should match the default file type (that selected as the dialog opens).</span></span> <span data-ttu-id="7691a-178">Se o tipo de arquivo padrão for " \* . \* " (todos os arquivos), o arquivo pode ser uma extensão de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="7691a-178">If the default file type is "\*.\*" (all files), the file can be an extension of your choice.</span></span> <span data-ttu-id="7691a-179">Se o usuário escolher um tipo de arquivo diferente, a extensão será atualizada automaticamente para a primeira extensão de nome de arquivo associada a esse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7691a-179">If the user chooses a different file type, the extension automatically updates to the first file name extension associated with that file type.</span></span> <span data-ttu-id="7691a-180">Se o usuário escolher " \* . \* " (todos os arquivos), a extensão é revertida para seu valor original.</span><span class="sxs-lookup"><span data-stu-id="7691a-180">If the user chooses "\*.\*" (all files), then the extension reverts to its original value.</span></span>

<span data-ttu-id="7691a-181">O exemplo a seguir ilustra como isso foi feito acima.</span><span class="sxs-lookup"><span data-stu-id="7691a-181">The following example illustrates how this was done above.</span></span>


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a><span data-ttu-id="7691a-182">Controlando a pasta padrão</span><span class="sxs-lookup"><span data-stu-id="7691a-182">Controlling the Default Folder</span></span>

<span data-ttu-id="7691a-183">Quase todas as pastas no namespace do Shell podem ser usadas como a pasta padrão para a caixa de diálogo (a pasta apresentada quando o usuário opta por abrir ou salvar um arquivo).</span><span class="sxs-lookup"><span data-stu-id="7691a-183">Almost any folder in the Shell namespace can be used as the default folder for the dialog (the folder presented when the user chooses to open or save a file).</span></span> <span data-ttu-id="7691a-184">Chame [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) antes de chamar [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="7691a-184">Call [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) to do so.</span></span>

<span data-ttu-id="7691a-185">A pasta padrão é a pasta na qual a caixa de diálogo é iniciada na primeira vez que um usuário a abre do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7691a-185">The default folder is the folder in which the dialog starts the first time a user opens it from your application.</span></span> <span data-ttu-id="7691a-186">Depois disso, a caixa de diálogo será aberta na última pasta que um usuário abriu ou na última pasta usada para salvar um item.</span><span class="sxs-lookup"><span data-stu-id="7691a-186">After that, the dialog will open in the last folder a user opened or the last folder they used to save an item.</span></span> <span data-ttu-id="7691a-187">Consulte [persistência de estado](#state-persistence) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="7691a-187">See [State Persistence](#state-persistence) for more details.</span></span>

<span data-ttu-id="7691a-188">Você pode forçar a caixa de diálogo a sempre mostrar a mesma pasta quando ela é aberta, independentemente da ação anterior do usuário, chamando [**IFileDialog:: SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span><span class="sxs-lookup"><span data-stu-id="7691a-188">You can force the dialog to always show the same folder when it opens, regardless of previous user action, by calling [**IFileDialog::SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span></span> <span data-ttu-id="7691a-189">No entanto, não recomendamos fazer isso.</span><span class="sxs-lookup"><span data-stu-id="7691a-189">However, we do not recommended doing this.</span></span> <span data-ttu-id="7691a-190">Se você chamar **SetFolder** antes de exibir a caixa de diálogo, o local mais recente no qual o usuário salvou ou abrir não será mostrado.</span><span class="sxs-lookup"><span data-stu-id="7691a-190">If you call **SetFolder** before you display the dialog box, the most recent location that the user saved to or opened from is not shown.</span></span> <span data-ttu-id="7691a-191">A menos que haja um motivo muito específico para esse comportamento, não é uma experiência de usuário boa ou esperada e deve ser evitada.</span><span class="sxs-lookup"><span data-stu-id="7691a-191">Unless there is a very specific reason for this behavior, it is not a good or expected user experience and should be avoided.</span></span> <span data-ttu-id="7691a-192">Em quase todas as instâncias, [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) é o melhor método.</span><span class="sxs-lookup"><span data-stu-id="7691a-192">In almost all instances, [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) is the better method.</span></span>

<span data-ttu-id="7691a-193">Ao salvar um documento pela primeira vez na caixa de diálogo **salvar** , você deve seguir as mesmas diretrizes para determinar a pasta inicial como fez na caixa de diálogo **abrir** .</span><span class="sxs-lookup"><span data-stu-id="7691a-193">When saving a document for the first time in the **Save** dialog, you should follow the same guidelines in determining the initial folder as you did in the **Open** dialog.</span></span> <span data-ttu-id="7691a-194">Se o usuário estiver editando um documento existente anteriormente, abra a caixa de diálogo na pasta em que o documento está armazenado e preencha o quadro de edição com o nome desse documento.</span><span class="sxs-lookup"><span data-stu-id="7691a-194">If the user is editing a previously existing document, open the dialog in the folder where that document is stored, and populate the edit box with that document's name.</span></span> <span data-ttu-id="7691a-195">Chame [**IFileSaveDialog:: SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) com o item atual antes de chamar [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span><span class="sxs-lookup"><span data-stu-id="7691a-195">Call [**IFileSaveDialog::SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) with the current item prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span></span>

### <a name="adding-items-to-the-places-bar"></a><span data-ttu-id="7691a-196">Adicionando itens à barra de locais</span><span class="sxs-lookup"><span data-stu-id="7691a-196">Adding Items to the Places Bar</span></span>

<span data-ttu-id="7691a-197">O exemplo a seguir demonstra a adição de itens à barra de **locais** :</span><span class="sxs-lookup"><span data-stu-id="7691a-197">The following example demonstrates the addition of items to the **Places** bar:</span></span>


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a><span data-ttu-id="7691a-198">Persistência de estado</span><span class="sxs-lookup"><span data-stu-id="7691a-198">State Persistence</span></span>

<span data-ttu-id="7691a-199">Antes do Windows Vista, um estado, como a última pasta visitada, foi salvo em uma base por processo.</span><span class="sxs-lookup"><span data-stu-id="7691a-199">Prior to Windows Vista, a state, such as the last visited folder, was saved on a per-process basis.</span></span> <span data-ttu-id="7691a-200">No entanto, essas informações foram usadas independentemente da ação em particular.</span><span class="sxs-lookup"><span data-stu-id="7691a-200">However, that information was used regardless of the particular action.</span></span> <span data-ttu-id="7691a-201">Por exemplo, um aplicativo de edição de vídeo apresentaria a mesma pasta na caixa de diálogo **renderizar como** na caixa de diálogo **importar mídia** .</span><span class="sxs-lookup"><span data-stu-id="7691a-201">For example, a video editing application would present the same folder in the **Render As** dialog as is would in the **Import Media** dialog.</span></span> <span data-ttu-id="7691a-202">No Windows Vista, você pode ser mais específico por meio do uso de GUIDs.</span><span class="sxs-lookup"><span data-stu-id="7691a-202">In Windows Vista you can be more specific through the use of GUIDs.</span></span> <span data-ttu-id="7691a-203">Para atribuir um **GUID** à caixa de diálogo, chame [**IFileDialog:: SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span><span class="sxs-lookup"><span data-stu-id="7691a-203">To assign a **GUID** to the dialog, call [**iFileDialog::SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span></span>

### <a name="multiselect-capabilities"></a><span data-ttu-id="7691a-204">Recursos de seleção ascada</span><span class="sxs-lookup"><span data-stu-id="7691a-204">Multiselect Capabilities</span></span>

<span data-ttu-id="7691a-205">A funcionalidade multiseleção está disponível na caixa de diálogo **abrir** usando o método [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) , como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="7691a-205">Multiselect functionality is available in the **Open** dialog using the [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) method as shown here.</span></span>


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a><span data-ttu-id="7691a-206">Ouvindo eventos a partir da caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="7691a-206">Listening to Events from the Dialog</span></span>

<span data-ttu-id="7691a-207">Um processo de chamada pode registrar uma interface [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) com a caixa de diálogo usando os métodos [**IFileDialog:: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) e [**IFileDialog:: Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) , conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="7691a-207">A calling process can register an [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) interface with the dialog by using the [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) and [**IFileDialog::Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) methods as shown here.</span></span>

<span data-ttu-id="7691a-208">Isso é obtido do exemplo de [uso básico](#basic-usage) .</span><span class="sxs-lookup"><span data-stu-id="7691a-208">This is taken from the [Basic Usage](#basic-usage) sample.</span></span>


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



<span data-ttu-id="7691a-209">A maior parte do processamento da caixa de diálogo seria colocada aqui.</span><span class="sxs-lookup"><span data-stu-id="7691a-209">The bulk of the dialog processing would be placed here.</span></span>


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



<span data-ttu-id="7691a-210">O processo de chamada pode usar eventos para notificação quando o usuário altera a pasta, o tipo de arquivo ou a seleção.</span><span class="sxs-lookup"><span data-stu-id="7691a-210">The calling process can use events for notification when the user changes the folder, file type, or selection.</span></span> <span data-ttu-id="7691a-211">Esses eventos são particularmente úteis quando o processo de chamada tem controles adicionados à caixa de diálogo (consulte [Personalizando a caixa de diálogo](#customizing-the-dialog)) e deve alterar o estado desses controles em reação a esses eventos.</span><span class="sxs-lookup"><span data-stu-id="7691a-211">These events are particularly useful when the calling process has added controls to the dialog (see [Customizing the Dialog](#customizing-the-dialog)) and must change the state of those controls in reaction to these events.</span></span> <span data-ttu-id="7691a-212">O útil em todos os casos é a capacidade do processo de chamada de fornecer código personalizado para lidar com situações como violações de compartilhamento, substituição de arquivos ou determinação de se um arquivo é válido antes de fechar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-212">Useful in all cases is the ability of the calling process to provide custom code to deal with situations such as sharing violations, overwriting files, or determining if a file is valid before the dialog closes.</span></span> <span data-ttu-id="7691a-213">Alguns desses casos são descritos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="7691a-213">Some of those cases are described in this section.</span></span>

### <a name="onfileok"></a><span data-ttu-id="7691a-214">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="7691a-214">OnFileOk</span></span>

<span data-ttu-id="7691a-215">Esse método é chamado depois que o usuário escolhe um item, logo antes da caixa de diálogo fechar.</span><span class="sxs-lookup"><span data-stu-id="7691a-215">This method is called after the user chooses an item, just before the dialog closes.</span></span> <span data-ttu-id="7691a-216">Em seguida, o aplicativo pode chamar [**IFileDialog:: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) ou [**IFileOpenDialog:: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) como seria feito depois que a caixa de diálogo tivesse sido fechada.</span><span class="sxs-lookup"><span data-stu-id="7691a-216">The application can then call [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) or [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) as would be done once the dialog had closed.</span></span> <span data-ttu-id="7691a-217">Se o item escolhido for aceitável, ele poderá retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7691a-217">If the item chosen is acceptable, they can return S\_OK.</span></span> <span data-ttu-id="7691a-218">Caso contrário, eles retornam S \_ false e exibem a interface do usuário que informa ao usuários por que o item escolhido não é válido.</span><span class="sxs-lookup"><span data-stu-id="7691a-218">Otherwise, they return S\_FALSE and display UI that tells the user why the chosen item is not valid.</span></span> <span data-ttu-id="7691a-219">Se S \_ false for retornado, a caixa de diálogo não será fechada.</span><span class="sxs-lookup"><span data-stu-id="7691a-219">If S\_FALSE is returned, the dialog does not close.</span></span>

<span data-ttu-id="7691a-220">O processo de chamada pode usar o identificador de janela da própria caixa de diálogo como o pai da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7691a-220">The calling process can use the window handle of the dialog itself as the parent of the UI.</span></span> <span data-ttu-id="7691a-221">Esse identificador pode ser obtido primeiro chamando [**IOleWindow:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) e, em seguida, chamando [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) com o identificador, conforme mostrado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="7691a-221">That handle can be obtained by first calling [**IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) and then calling [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) with the handle as shown in this example.</span></span>


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a><span data-ttu-id="7691a-222">OnShareViolation e onoverwrite</span><span class="sxs-lookup"><span data-stu-id="7691a-222">OnShareViolation and OnOverwrite</span></span>

<span data-ttu-id="7691a-223">Se o usuário optar por substituir um arquivo na caixa de diálogo **salvar** ou se um arquivo que está sendo salvo ou substituído estiver em uso e não puder ser gravado (uma violação de compartilhamento), o aplicativo poderá fornecer uma funcionalidade personalizada para substituir o comportamento padrão da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-223">If the user chooses to overwrite a file in the **Save** dialog, or if a file being saved or replaced is in use and cannot be written to (a sharing violation), the application can provide custom functionality to override the default behavior of the dialog.</span></span> <span data-ttu-id="7691a-224">Por padrão, ao substituir um arquivo, a caixa de diálogo exibe um prompt que permite ao usuário verificar essa ação.</span><span class="sxs-lookup"><span data-stu-id="7691a-224">By default, when overwriting a file, the dialog displays a prompt allowing the user to verify this action.</span></span> <span data-ttu-id="7691a-225">Para violações de compartilhamento, por padrão, a caixa de diálogo exibe uma mensagem de erro, ela não fecha e o usuário precisa fazer outra escolha.</span><span class="sxs-lookup"><span data-stu-id="7691a-225">For sharing violations, by default the dialog displays an error message, it does not close, and the user is required to make another choice.</span></span> <span data-ttu-id="7691a-226">O processo de chamada pode substituir esses padrões e exibir sua própria interface do usuário, se desejado.</span><span class="sxs-lookup"><span data-stu-id="7691a-226">The calling process can override these defaults and display its own UI if desired.</span></span> <span data-ttu-id="7691a-227">A caixa de diálogo pode ser instruída para recusar o arquivo e permanecer aberta ou aceitar o arquivo e fechar com êxito.</span><span class="sxs-lookup"><span data-stu-id="7691a-227">The dialog can be instructed to refuse the file and remain open or accept the file and close successfully.</span></span>

## <a name="customizing-the-dialog"></a><span data-ttu-id="7691a-228">Personalizando a caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="7691a-228">Customizing the Dialog</span></span>

<span data-ttu-id="7691a-229">Uma variedade de controles pode ser adicionada à caixa de diálogo sem fornecer um modelo de caixa de diálogo do Win32.</span><span class="sxs-lookup"><span data-stu-id="7691a-229">A variety of controls can be added to the dialog without supplying a Win32 dialog template.</span></span> <span data-ttu-id="7691a-230">Esses controles incluem botão de pressão, ComboBox, adCheckButton, listas de botões de opção, grupos, separadores e controles de texto estáticos.</span><span class="sxs-lookup"><span data-stu-id="7691a-230">These controls include PushButton, ComboBox, EditBox, CheckButton, RadioButton lists, Groups, Separators, and Static Text controls.</span></span> <span data-ttu-id="7691a-231">Chame **QueryInterface** no objeto Dialog ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)ou [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) para obter um ponteiro [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) .</span><span class="sxs-lookup"><span data-stu-id="7691a-231">Call **QueryInterface** on the dialog object ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), or [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) to obtain an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer.</span></span> <span data-ttu-id="7691a-232">Use essa interface para adicionar controles.</span><span class="sxs-lookup"><span data-stu-id="7691a-232">Use that interface to add controls.</span></span> <span data-ttu-id="7691a-233">Cada controle tem uma ID fornecida pelo chamador associada, bem como um estado *visível* e *habilitado* que pode ser definido pelo processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="7691a-233">Each control has an associated caller-supplied ID as well as a *visible* and *enabled* state that can be set by the calling process.</span></span> <span data-ttu-id="7691a-234">Alguns controles, como a "pressão", também têm texto associado a eles.</span><span class="sxs-lookup"><span data-stu-id="7691a-234">Some controls, such as PushButton, also have text associated with them.</span></span>

<span data-ttu-id="7691a-235">Vários controles podem ser adicionados a um "grupo Visual" que se move como uma única unidade no layout da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-235">Multiple controls can be added into a "visual group" that moves as a single unit in the layout of the dialog.</span></span> <span data-ttu-id="7691a-236">Os grupos podem ter um rótulo associado a eles.</span><span class="sxs-lookup"><span data-stu-id="7691a-236">Groups can have a label associated with them.</span></span>

<span data-ttu-id="7691a-237">Os controles podem ser adicionados somente antes da exibição da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-237">Controls can be added only before the dialog is shown.</span></span> <span data-ttu-id="7691a-238">No entanto, quando a caixa de diálogo é exibida, os controles podem ser ocultados ou mostrados como desejado, talvez em resposta à ação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7691a-238">However, once the dialog is displayed, controls can be hidden or shown as desired, perhaps in response to user action.</span></span> <span data-ttu-id="7691a-239">Os exemplos a seguir mostram como adicionar uma lista de botões de opção à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-239">The following examples show how to add a radio button list to the dialog.</span></span>


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a><span data-ttu-id="7691a-240">Adicionando opções ao botão OK</span><span class="sxs-lookup"><span data-stu-id="7691a-240">Adding Options to the OK Button</span></span>

<span data-ttu-id="7691a-241">Da mesma forma, as opções podem ser adicionadas aos botões **abrir** ou **salvar** , que são o botão **OK** para seus respectivos tipos de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7691a-241">Similarly, choices can be added to the **Open** or **Save** buttons, which are the **OK** button for their respective dialog types.</span></span> <span data-ttu-id="7691a-242">As opções podem ser acessadas por meio de uma caixa de listagem suspensa anexada ao botão.</span><span class="sxs-lookup"><span data-stu-id="7691a-242">The options are accessible through a drop-down list box attached to the button.</span></span> <span data-ttu-id="7691a-243">O primeiro item na lista se torna o texto do botão.</span><span class="sxs-lookup"><span data-stu-id="7691a-243">The first item in the list becomes the text for the button.</span></span> <span data-ttu-id="7691a-244">O exemplo a seguir mostra como fornecer um botão **Open** com duas possibilidades: "Open" e "Open as Read-Only".</span><span class="sxs-lookup"><span data-stu-id="7691a-244">The following example shows how to provide an **Open** button with two possibilities: "Open" and "Open as read-only".</span></span>


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





<span data-ttu-id="7691a-245">A escolha do usuário pode ser verificada após a caixa de diálogo retornar do método [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) como você faria para uma ComboBox ou pode ser verificada como parte da manipulação por [**IFileDialogEvents:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span><span class="sxs-lookup"><span data-stu-id="7691a-245">The user's choice can be verified after the dialog returns from the [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) method as you would for a ComboBox, or it can verified as part of the handling by [**IFileDialogEvents::OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span></span>

### <a name="responding-to-events-in-added-controls"></a><span data-ttu-id="7691a-246">Respondendo a eventos em controles adicionados</span><span class="sxs-lookup"><span data-stu-id="7691a-246">Responding to Events in Added Controls</span></span>

<span data-ttu-id="7691a-247">O manipulador de eventos fornecido pelo processo de chamada pode implementar [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) além de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span><span class="sxs-lookup"><span data-stu-id="7691a-247">The events handler provided by the calling process can implement [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) in addition to [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span></span> <span data-ttu-id="7691a-248">O **IFileDialogControlEvents** permite que o processo de chamada reaja a esses eventos:</span><span class="sxs-lookup"><span data-stu-id="7691a-248">**IFileDialogControlEvents** enables the calling process to react to these events:</span></span>

-   <span data-ttu-id="7691a-249">Botão de pressão clicado</span><span class="sxs-lookup"><span data-stu-id="7691a-249">PushButton clicked</span></span>
-   <span data-ttu-id="7691a-250">Estado de CheckButton alterado</span><span class="sxs-lookup"><span data-stu-id="7691a-250">CheckButton state changed</span></span>
-   <span data-ttu-id="7691a-251">Item selecionado em uma lista de menus, caixas de combinação ou botões de opção</span><span class="sxs-lookup"><span data-stu-id="7691a-251">Item selected from a menu, ComboBox, or RadioButton list</span></span>
-   <span data-ttu-id="7691a-252">Ativação de controle.</span><span class="sxs-lookup"><span data-stu-id="7691a-252">Control activating.</span></span> <span data-ttu-id="7691a-253">Isso é enviado quando um menu está prestes a exibir uma lista suspensa, caso o processo de chamada queira alterar os itens na lista.</span><span class="sxs-lookup"><span data-stu-id="7691a-253">This is sent when a menu is about to display a drop-down list, in case the calling process wants to change the items in the list.</span></span>

## <a name="full-samples"></a><span data-ttu-id="7691a-254">Exemplos completos</span><span class="sxs-lookup"><span data-stu-id="7691a-254">Full Samples</span></span>

<span data-ttu-id="7691a-255">Veja a seguir exemplos de C++ completos e baixáveis do SDK (Software Development Kit) do Windows que demonstram o uso e a interação com a caixa de diálogo de item comum.</span><span class="sxs-lookup"><span data-stu-id="7691a-255">The following are complete, downloadable C++ samples from the Windows Software Development Kit (SDK) which demonstrate the use of and interaction with the Common Item Dialog.</span></span>

-   [<span data-ttu-id="7691a-256">Exemplo de caixa de diálogo de arquivo comum</span><span class="sxs-lookup"><span data-stu-id="7691a-256">Common File Dialog Sample</span></span>](samples-commonfiledialog.md)
-   [<span data-ttu-id="7691a-257">Exemplo de modos de diálogo de arquivo comum</span><span class="sxs-lookup"><span data-stu-id="7691a-257">Common File Dialog Modes Sample</span></span>](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a><span data-ttu-id="7691a-258">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7691a-258">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7691a-259">**\_argumentos de PPV de IID \_**</span><span class="sxs-lookup"><span data-stu-id="7691a-259">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
