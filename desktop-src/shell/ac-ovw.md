---
description: O preenchimento automático expande as cadeias de caracteres que foram inseridas parcialmente em um controle de edição em cadeias de caracteres completas.
title: Usando o preenchimento automático
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967368"
---
# <a name="using-autocomplete"></a><span data-ttu-id="bcbcc-103">Usando o preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="bcbcc-103">Using Autocomplete</span></span>

<span data-ttu-id="bcbcc-104">O preenchimento automático expande as cadeias de caracteres que foram inseridas parcialmente em um [controle de edição](/windows/desktop/Controls/edit-controls) em cadeias de caracteres completas.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-104">Autocompletion expands strings that have been partially entered in an [edit control](/windows/desktop/Controls/edit-controls) into complete strings.</span></span> <span data-ttu-id="bcbcc-105">Por exemplo, quando um usuário começa a inserir uma URL no controle de edição de endereço inserido na barra de ferramentas do Windows Internet Explorer, o preenchimento automático expande a cadeia de caracteres em uma ou mais opções de URL completas que são consistentes com a cadeia de caracteres parcial existente.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-105">For example, when a user starts to enter a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URL options that are consistent with the existing partial string.</span></span> <span data-ttu-id="bcbcc-106">Uma cadeia de caracteres de URL parcial, como "MIC", pode ser expandida para " https://www.microsoft.com " ou " https://www.microsoft.com/windows ".</span><span class="sxs-lookup"><span data-stu-id="bcbcc-106">A partial URL string such as "mic" might be expanded to "https://www.microsoft.com" or "https://www.microsoft.com/windows".</span></span> <span data-ttu-id="bcbcc-107">O preenchimento automático normalmente é usado com controles de edição ou com controles que têm um controle de edição inserido, como o controle [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .</span><span class="sxs-lookup"><span data-stu-id="bcbcc-107">Autocompletion is typically used with edit controls or with controls that have an embedded edit control, such as the [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) control.</span></span>

## <a name="adding-autocomplete-functionality-to-your-application"></a><span data-ttu-id="bcbcc-108">Adicionando a funcionalidade de preenchimento automático ao seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="bcbcc-108">Adding Autocomplete Functionality to Your Application</span></span>

<span data-ttu-id="bcbcc-109">Um aplicativo pode adicionar funcionalidade de preenchimento automático a um controle de edição de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="bcbcc-109">An application can add autocomplete functionality to an edit control in two ways:</span></span>

-   <span data-ttu-id="bcbcc-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) é uma função simples que pode preencher um caminho de arquivo ou uma URL.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) is a simple function that can autocomplete a file path or URL.</span></span>
-   <span data-ttu-id="bcbcc-111">A interface [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) é exposta pelo objeto de preenchimento automático ( \_ AutoCompletar CLSID).</span><span class="sxs-lookup"><span data-stu-id="bcbcc-111">[**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) interface is exposed by the autocomplete object (CLSID\_AutoComplete).</span></span> <span data-ttu-id="bcbcc-112">Ele permite que os aplicativos inicializem, habilitem e desabilitem o objeto.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-112">It allows applications to initialize, enable, and disable the object.</span></span> <span data-ttu-id="bcbcc-113">O **IAutoComplete** permite mais controle sobre as fontes de preenchimento automático, incluindo a capacidade de adicionar uma fonte personalizada.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-113">**IAutoComplete** allows more control over autocomplete sources, including the ability to add a custom source.</span></span> <span data-ttu-id="bcbcc-114">O restante deste tópico discute o uso de **IAutoComplete**.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-114">The remainder of this topic discusses the use of **IAutoComplete**.</span></span> <span data-ttu-id="bcbcc-115">Consulte [como habilitar o preenchimento automático manualmente](how-to-enable-autocomplete-manually.md) para obter exemplos de uso específicos.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-115">See [How To Enable Autocomplete Manually](how-to-enable-autocomplete-manually.md) for specific usage examples.</span></span>

## <a name="autocomplete-modes"></a><span data-ttu-id="bcbcc-116">Modos de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="bcbcc-116">Autocomplete Modes</span></span>

<span data-ttu-id="bcbcc-117">Ao usar [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), o preenchimento automático pode exibir a cadeia de caracteres completa em dois modos: acréscimo automático e sugestão automática.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-117">When using [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), autocompletion can display the completed string in two modes: autoappend and autosuggest.</span></span> <span data-ttu-id="bcbcc-118">Os modos são independentes; Você pode habilitar um ou ambos.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-118">The modes are independent; you can enable either or both.</span></span> <span data-ttu-id="bcbcc-119">Para especificar o modo, chame [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="bcbcc-119">To specify the mode, call [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span></span>

<dl> <dt>

<span data-ttu-id="bcbcc-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Acréscimo</span><span class="sxs-lookup"><span data-stu-id="bcbcc-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend</span></span>
</dt> <dd>

<span data-ttu-id="bcbcc-121">No modo de acréscimo automático, a conclusão automática acrescenta o restante da cadeia de caracteres candidatas mais provável aos caracteres existentes, destacando os caracteres acrescentados.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-121">In autoappend mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters.</span></span> <span data-ttu-id="bcbcc-122">Se o usuário continuar a inserir caracteres, eles serão adicionados à cadeia de caracteres parcial existente.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-122">If the user continues to enter characters, they are added to the existing partial string.</span></span> <span data-ttu-id="bcbcc-123">Se o usuário adicionar um caractere idêntico ao próximo caractere realçado, o realce desse caractere será desativado.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-123">If the user adds a character that is identical to the next highlighted character, the highlighting for that character is turned off.</span></span> <span data-ttu-id="bcbcc-124">Os caracteres restantes ainda serão realçados.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-124">The remaining characters will still be highlighted.</span></span> <span data-ttu-id="bcbcc-125">Se o usuário adicionar um caractere que não corresponde ao próximo caractere realçado, o preenchimento automático tentará gerar uma nova cadeia de caracteres candidatas com base na cadeia de caracteres parcial maior e acrescentará o restante da nova cadeia de caracteres candidatas à cadeia de caracteres parcial atual.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-125">If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string and appends the remainder of the new candidate string to the current partial string.</span></span> <span data-ttu-id="bcbcc-126">Se nenhuma cadeia de caracteres candidata puder ser encontrada, somente os caracteres digitados serão exibidos e a caixa de edição se comformará como faria sem preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-126">If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion.</span></span> <span data-ttu-id="bcbcc-127">Esse processo continua até que o usuário aceite uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-127">This process continues until the user accepts a string.</span></span>

</dd> <dt>

<span data-ttu-id="bcbcc-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Sugestão automática</span><span class="sxs-lookup"><span data-stu-id="bcbcc-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest</span></span>
</dt> <dd>

<span data-ttu-id="bcbcc-129">No modo de sugestão automática, o preenchimento automático exibe uma lista suspensa, com uma ou mais cadeias de caracteres completas sugeridas, abaixo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-129">In autosuggest mode, autocompletion displays a drop-down list, with one or more suggested complete strings, beneath the edit control.</span></span> <span data-ttu-id="bcbcc-130">O usuário pode selecionar uma das cadeias de caracteres sugeridas ou continuar digitando.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-130">The user can select one of the suggested strings or continue typing.</span></span> <span data-ttu-id="bcbcc-131">À medida que a digitação progride, a lista suspensa pode ser modificada com base na cadeia de caracteres parcial atual.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-131">As typing progresses, the drop-down list might be modified based on the current partial string.</span></span> <span data-ttu-id="bcbcc-132">Se você definir o \_ sinalizador de pesquisa aco em [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), o preenchimento automático fornecerá uma opção, na parte inferior da lista suspensa, para pesquisar a cadeia de caracteres parcial atual.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-132">If you set the ACO\_SEARCH flag in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), autocomplete provides an option, at the bottom of the drop-down list, to search for the current partial string.</span></span> <span data-ttu-id="bcbcc-133">Essa opção é exibida mesmo se não houver cadeias de caracteres sugeridas.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-133">This option is displayed even if there are no suggested strings.</span></span> <span data-ttu-id="bcbcc-134">Se o usuário selecionar a opção de pesquisa, seu aplicativo deverá iniciar um mecanismo de pesquisa para auxiliar o usuário.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-134">If the user selects the search option, your application should launch a search engine to assist the user.</span></span>

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a><span data-ttu-id="bcbcc-135">Usando fontes de preenchimento automático predefinidas</span><span class="sxs-lookup"><span data-stu-id="bcbcc-135">Using Predefined Autocomplete Sources</span></span>

<span data-ttu-id="bcbcc-136">O preenchimento automático depende de ter uma fonte que forneça cadeias de caracteres para corresponder à cadeia parcial do usuário.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-136">Autocompletion depends on having a source that provides it with strings to match against the user's partial string.</span></span> <span data-ttu-id="bcbcc-137">Você tem a opção de fornecer uma fonte de preenchimento automático personalizada, mas várias das fontes mais comuns são fornecidas pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-137">You have the option of providing a custom autocomplete source, but several of the most common sources are provided by the system.</span></span>

<dl> <dt>

<span data-ttu-id="bcbcc-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>\_ACLHISTORY CLSID</span><span class="sxs-lookup"><span data-stu-id="bcbcc-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID\_ACLHistory</span></span>
</dt> <dd>

<span data-ttu-id="bcbcc-139">Uma fonte de preenchimento automático que corresponde à lista de URLs na lista de histórico do usuário.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-139">An autocomplete source that matches against the URL list in the user's History list.</span></span>

</dd> <dt>

<span data-ttu-id="bcbcc-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>\_ACLMRU CLSID</span><span class="sxs-lookup"><span data-stu-id="bcbcc-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID\_ACLMRU</span></span>
</dt> <dd>

<span data-ttu-id="bcbcc-141">Uma fonte de preenchimento automático que corresponde à lista de URLs na lista de usuários usados recentemente.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-141">An autocomplete source that matches against the URL list in the user's Recently Used list.</span></span>

</dd> <dt>

<span data-ttu-id="bcbcc-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>\_ACLISTISF CLSID</span><span class="sxs-lookup"><span data-stu-id="bcbcc-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID\_ACListISF</span></span>
</dt> <dd>

<span data-ttu-id="bcbcc-143">Uma fonte de preenchimento automático que corresponde a itens no namespace do Shell: arquivos no computador do usuário, bem como itens em pastas virtuais, como o painel de controle.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-143">An autocomplete source that matches against items in the Shell namespace: files on the user's computer as well as items in virtual folders such as Control Panel.</span></span>

</dd> </dl>

<span data-ttu-id="bcbcc-144">Há ocasiões em que, em vez de liberar imediatamente os recursos, talvez você queira manter os ponteiros de interface para os vários objetos envolvidos no preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-144">There are occasions when, rather than immediately freeing the resources, you might want to retain the interface pointers to the various objects involved in autocomplete.</span></span> <span data-ttu-id="bcbcc-145">Em particular, isso é feito quando você deseja ajustar dinamicamente o comportamento de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-145">In particular, this is done when you want to adjust the autocomplete behavior dynamically.</span></span> <span data-ttu-id="bcbcc-146">A instância mais comum disso ocorre ao usar o objeto CLSID \_ ACListISF, que é concluído de forma completa do namespace do Shell e tem a opção [**(ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) de enumeração do diretório atual também.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-146">The most common instance of this occurs when using the CLSID\_ACListISF object, which autocompletes from the Shell namespace and has the option ([**ACLO\_CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) of enumerating from the current directory as well.</span></span> <span data-ttu-id="bcbcc-147">Por exemplo, quando você navega para uma nova pasta, o Internet Explorer altera o diretório atual da barra de endereços e, portanto, as configurações precisam ser alteradas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-147">For example, when you navigate to a new folder, Internet Explorer changes the Address bar's current directory and therefore the settings need to be changed dynamically.</span></span> <span data-ttu-id="bcbcc-148">Há duas maneiras de especificar o diretório que o objeto CLSID \_ ACListISF deve tratar como o diretório atual:</span><span class="sxs-lookup"><span data-stu-id="bcbcc-148">There are two ways to specify the directory that the CLSID\_ACListISF object should treat as the current directory:</span></span>

-   <span data-ttu-id="bcbcc-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) especifica o diretório por meio de uma [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span><span class="sxs-lookup"><span data-stu-id="bcbcc-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifies the directory through an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span></span>
-   <span data-ttu-id="bcbcc-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) especifica o diretório por meio de uma cadeia de caracteres de caminho.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifies the directory through a path string.</span></span>

<span data-ttu-id="bcbcc-151">No seguinte, suponha que **PAL** seja um ponteiro para a interface [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) de um objeto CLSID \_ ACListISF:</span><span class="sxs-lookup"><span data-stu-id="bcbcc-151">In the following, assume that **pal** is a pointer to the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) interface of a CLSID\_ACListISF object:</span></span>

-   <span data-ttu-id="bcbcc-152">Usando [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span><span class="sxs-lookup"><span data-stu-id="bcbcc-152">Using [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span></span>

    <span data-ttu-id="bcbcc-153">Para informar ao \_ objeto CLSID ACListISF que uma [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) específica deve ser tratada como o diretório atual, você pode usar a interface [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) do objeto.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-153">To tell the CLSID\_ACListISF object that a particular [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) should be treated as the current directory, you can use the object's [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) interface.</span></span> <span data-ttu-id="bcbcc-154">Como uma **ITEMIDLIST** pode se referir a uma pasta virtual, esse método é mais flexível do que o uso de [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span><span class="sxs-lookup"><span data-stu-id="bcbcc-154">Since an **ITEMIDLIST** can refer to a virtual folder, this method is more flexible than using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span></span>

    <span data-ttu-id="bcbcc-155">Observe que os exemplos a seguir usam o modelos QueryInterface, que permite uma lista de parâmetros simplificada.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-155">Note that the following examples use the templatized QueryInterface, which allows for a simplified parameter list.</span></span>

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   <span data-ttu-id="bcbcc-156">Usando [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span><span class="sxs-lookup"><span data-stu-id="bcbcc-156">Using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span></span>

    <span data-ttu-id="bcbcc-157">Para dar ao \_ objeto CLSID ACListISF um caminho como o diretório atual, você pode usar a interface [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) do objeto.</span><span class="sxs-lookup"><span data-stu-id="bcbcc-157">To give the CLSID\_ACListISF object a path as the current directory, you can use the object's [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) interface.</span></span>

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 
