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
# <a name="common-item-dialog"></a>Caixa de diálogo de item comum

A partir do Windows Vista, a caixa de diálogo de item comum substitui a caixa de diálogo de arquivo comum mais antiga quando usada para abrir ou salvar um arquivo. A caixa de diálogo de item comum é usada em duas variações: a caixa de diálogo **abrir** e **salvar** . Essas duas caixas de diálogo compartilham a maior parte de sua funcionalidade, mas cada uma tem seus próprios métodos exclusivos.

Embora essa versão mais recente seja chamada de caixa de diálogo de item comum, ela continua a ser chamada de caixa de diálogo de arquivo comum na maioria das documentações. A menos que esteja lidando especificamente com uma versão mais antiga do Windows, você deve supor que qualquer menção da caixa de diálogo arquivo comum se refere a essa caixa de diálogo de item comum.

Os tópicos a seguir são discutidos aqui:

-   [IFileDialog, IFileOpenDialog e IFileSaveDialog](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [Exemplo de uso](#sample-usage)
-   [Ouvindo eventos a partir da caixa de diálogo](#listening-to-events-from-the-dialog)
    -   [OnFileOk](#onfileok)
    -   [OnShareViolation e onoverwrite](#onshareviolation-and-onoverwrite)
-   [Personalizando a caixa de diálogo](#customizing-the-dialog)
    -   [Adicionando opções ao botão OK](#adding-options-to-the-ok-button)
    -   [Respondendo a eventos em controles adicionados](#responding-to-events-in-added-controls)
-   [Exemplos completos](#full-samples)
-   [Tópicos relacionados](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>IFileDialog, IFileOpenDialog e IFileSaveDialog

O Windows Vista fornece implementações das caixas de diálogo **abrir** e **salvar** : CLSID \_ FileOpenDialog e CLSID \_ FileSaveDialog. Essas caixas de diálogo são mostradas aqui.

![captura de tela da caixa de diálogo abrir](images/cid/openfiledialog.png)

![captura de tela da caixa de diálogo Salvar como](images/cid/savefiledialog.png)

[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) e [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) herdam de [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) e compartilham grande parte de sua funcionalidade. Além disso, a caixa de diálogo **abrir** dá suporte a **IFileOpenDialog** e a caixa de diálogo **salvar** dá suporte a **IFileSaveDialog**.

A implementação de caixa de diálogo de item comum encontrada no Windows Vista fornece várias vantagens em relação à implementação fornecida em versões anteriores:

-   Dá suporte ao uso direto do namespace do Shell por meio de [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) em vez de usar caminhos do sistema de arquivos.
-   Permite a personalização simples da caixa de diálogo, como a definição do rótulo no botão **OK** , sem a necessidade de um procedimento de gancho.
-   Dá suporte à personalização mais ampla da caixa de diálogo pela adição de um conjunto de controles controlados por dados que operam sem um modelo de caixa de diálogo do Win32. Esse esquema de personalização libera o processo de chamada do layout da interface do usuário. Como as alterações no design da caixa de diálogo continuam a usar esse modelo de dados, a implementação da caixa de diálogo não está vinculada à versão atual específica da caixa de diálogo.
-   Dá suporte à notificação do chamador de eventos na caixa de diálogo, como alteração de seleção ou alteração de tipo de arquivo. Também permite que o processo de chamada Conecte determinados eventos na caixa de diálogo, como a análise.
-   Apresenta novos recursos de caixa de diálogo, como adicionar locais especificados pelo chamador à barra de **locais** .
-   Na caixa de diálogo **salvar** , os desenvolvedores podem aproveitar os novos recursos de metadados do shell do Windows Vista.

Além disso, os desenvolvedores podem optar por implementar as seguintes interfaces:

-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) para receber notificações de eventos dentro da caixa de diálogo.
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) para adicionar controles à caixa de diálogo.
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) a ser notificado sobre eventos nesses controles adicionados.

A caixa de diálogo **abrir** ou **salvar** retorna um objeto [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) ou [**IShellitemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) para o processo de chamada. O chamador pode então usar um objeto **IShellItem** individual para obter um caminho do sistema de arquivos ou abrir um fluxo no item para ler ou gravar informações.

Os sinalizadores e as opções disponíveis para os novos métodos de diálogo são muito semelhantes aos sinalizadores **OFN** mais antigos encontrados na estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e usados em [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). Muitos deles são exatamente iguais, exceto que começam com um prefixo de FOS. A lista completa pode ser encontrada nos tópicos [**IFileDialog:: getoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) e [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) . As caixas de diálogo **abrir** e **salvar** são criadas por padrão com os sinalizadores mais comuns. Para a caixa de diálogo **aberta** , isso é (FOS \_ PATHMUSTEXIST \| FOS \_ FILEMUSTEXIST \| FOS \_ NOCHANGEDIR) e, para a caixa de diálogo **salvar** , isso é (FOS \_ OVERWRITEPROMPT FOS NOREADONLYRETURN \| \_ \| FOS \_ PATHMUSTEXIST \| FOS \_ NOCHANGEDIR).

[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) e suas interfaces descendentes herdam de e estendem [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) usa como seu único parâmetro o identificador da janela pai. Se **Mostrar** retornar com êxito, haverá um resultado válido. Se ele retornar `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , significa que o usuário cancelou a caixa de diálogo. Ele também pode retornar, legitimamente, outro código de erro, como **E \_ OUTOFMEMORY**.

### <a name="sample-usage"></a>Exemplo de uso

As seções a seguir mostram o código de exemplo para uma variedade de tarefas de caixa de diálogo.

-   [Uso básico](#basic-usage)
-   [Limitando resultados a itens do sistema de arquivos](#limiting-results-to-file-system-items)
-   [Especificando tipos de arquivo para uma caixa de diálogo](#specifying-file-types-for-a-dialog)
-   [Controlando a pasta padrão](#controlling-the-default-folder)
-   [Adicionando itens à barra de locais](#adding-items-to-the-places-bar)
-   [Persistência de estado](#state-persistence)
-   [Recursos de seleção ascada](#multiselect-capabilities)

A maior parte do código de exemplo pode ser encontrada no [exemplo de caixa de diálogo SDK do Windows arquivo comum](samples-commonfiledialog.md).

### <a name="basic-usage"></a>Uso básico

O exemplo a seguir ilustra como iniciar uma caixa de diálogo **aberta** . Neste exemplo, ele é restrito aos documentos do Microsoft Word.

> [!Note]  
> Vários exemplos neste tópico usam a `CDialogEventHandler_CreateInstance` função auxiliar para criar uma instância da implementação [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) . Para usar essa função em seu próprio código, copie o código-fonte da `CDialogEventHandler_CreateInstance` função do [exemplo de caixa de diálogo de arquivo comum](samples-commonfiledialog.md), do qual todos os exemplos neste tópico são tirados.

 


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



### <a name="limiting-results-to-file-system-items"></a>Limitando resultados a itens do sistema de arquivos

O exemplo a seguir, extraído acima, demonstra como restringir os resultados em itens do sistema de arquivos. Observe que [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adiciona o novo sinalizador a um valor obtido por meio de [**IFileDialog:: getoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions). Esse é o método recomendado.


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



### <a name="specifying-file-types-for-a-dialog"></a>Especificando tipos de arquivo para uma caixa de diálogo

Para definir tipos de arquivo específicos que a caixa de diálogo pode manipular, use o método [**IFileDialog:: SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) . Esse método aceita uma matriz de estruturas [**COMDLG \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , cada uma representando um tipo de arquivo.

O mecanismo de extensão padrão em uma caixa de diálogo não é alterado em [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). A extensão de nome de arquivo que é anexada ao texto que o usuário digita na caixa de edição de nome de arquivo é inicializada quando o diálogo é aberto. Ele deve corresponder ao tipo de arquivo padrão (selecionado conforme a caixa de diálogo é aberta). Se o tipo de arquivo padrão for " \* . \* " (todos os arquivos), o arquivo pode ser uma extensão de sua escolha. Se o usuário escolher um tipo de arquivo diferente, a extensão será atualizada automaticamente para a primeira extensão de nome de arquivo associada a esse tipo de arquivo. Se o usuário escolher " \* . \* " (todos os arquivos), a extensão é revertida para seu valor original.

O exemplo a seguir ilustra como isso foi feito acima.


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



### <a name="controlling-the-default-folder"></a>Controlando a pasta padrão

Quase todas as pastas no namespace do Shell podem ser usadas como a pasta padrão para a caixa de diálogo (a pasta apresentada quando o usuário opta por abrir ou salvar um arquivo). Chame [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) antes de chamar [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) para fazer isso.

A pasta padrão é a pasta na qual a caixa de diálogo é iniciada na primeira vez que um usuário a abre do seu aplicativo. Depois disso, a caixa de diálogo será aberta na última pasta que um usuário abriu ou na última pasta usada para salvar um item. Consulte [persistência de estado](#state-persistence) para obter mais detalhes.

Você pode forçar a caixa de diálogo a sempre mostrar a mesma pasta quando ela é aberta, independentemente da ação anterior do usuário, chamando [**IFileDialog:: SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder). No entanto, não recomendamos fazer isso. Se você chamar **SetFolder** antes de exibir a caixa de diálogo, o local mais recente no qual o usuário salvou ou abrir não será mostrado. A menos que haja um motivo muito específico para esse comportamento, não é uma experiência de usuário boa ou esperada e deve ser evitada. Em quase todas as instâncias, [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) é o melhor método.

Ao salvar um documento pela primeira vez na caixa de diálogo **salvar** , você deve seguir as mesmas diretrizes para determinar a pasta inicial como fez na caixa de diálogo **abrir** . Se o usuário estiver editando um documento existente anteriormente, abra a caixa de diálogo na pasta em que o documento está armazenado e preencha o quadro de edição com o nome desse documento. Chame [**IFileSaveDialog:: SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) com o item atual antes de chamar [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).

### <a name="adding-items-to-the-places-bar"></a>Adicionando itens à barra de locais

O exemplo a seguir demonstra a adição de itens à barra de **locais** :


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



### <a name="state-persistence"></a>Persistência de estado

Antes do Windows Vista, um estado, como a última pasta visitada, foi salvo em uma base por processo. No entanto, essas informações foram usadas independentemente da ação em particular. Por exemplo, um aplicativo de edição de vídeo apresentaria a mesma pasta na caixa de diálogo **renderizar como** na caixa de diálogo **importar mídia** . No Windows Vista, você pode ser mais específico por meio do uso de GUIDs. Para atribuir um **GUID** à caixa de diálogo, chame [**IFileDialog:: SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).

### <a name="multiselect-capabilities"></a>Recursos de seleção ascada

A funcionalidade multiseleção está disponível na caixa de diálogo **abrir** usando o método [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) , como mostrado aqui.


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



## <a name="listening-to-events-from-the-dialog"></a>Ouvindo eventos a partir da caixa de diálogo

Um processo de chamada pode registrar uma interface [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) com a caixa de diálogo usando os métodos [**IFileDialog:: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) e [**IFileDialog:: Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) , conforme mostrado aqui.

Isso é obtido do exemplo de [uso básico](#basic-usage) .


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



A maior parte do processamento da caixa de diálogo seria colocada aqui.


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



O processo de chamada pode usar eventos para notificação quando o usuário altera a pasta, o tipo de arquivo ou a seleção. Esses eventos são particularmente úteis quando o processo de chamada tem controles adicionados à caixa de diálogo (consulte [Personalizando a caixa de diálogo](#customizing-the-dialog)) e deve alterar o estado desses controles em reação a esses eventos. O útil em todos os casos é a capacidade do processo de chamada de fornecer código personalizado para lidar com situações como violações de compartilhamento, substituição de arquivos ou determinação de se um arquivo é válido antes de fechar a caixa de diálogo. Alguns desses casos são descritos nesta seção.

### <a name="onfileok"></a>OnFileOk

Esse método é chamado depois que o usuário escolhe um item, logo antes da caixa de diálogo fechar. Em seguida, o aplicativo pode chamar [**IFileDialog:: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) ou [**IFileOpenDialog:: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) como seria feito depois que a caixa de diálogo tivesse sido fechada. Se o item escolhido for aceitável, ele poderá retornar S \_ OK. Caso contrário, eles retornam S \_ false e exibem a interface do usuário que informa ao usuários por que o item escolhido não é válido. Se S \_ false for retornado, a caixa de diálogo não será fechada.

O processo de chamada pode usar o identificador de janela da própria caixa de diálogo como o pai da interface do usuário. Esse identificador pode ser obtido primeiro chamando [**IOleWindow:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) e, em seguida, chamando [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) com o identificador, conforme mostrado neste exemplo.


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



### <a name="onshareviolation-and-onoverwrite"></a>OnShareViolation e onoverwrite

Se o usuário optar por substituir um arquivo na caixa de diálogo **salvar** ou se um arquivo que está sendo salvo ou substituído estiver em uso e não puder ser gravado (uma violação de compartilhamento), o aplicativo poderá fornecer uma funcionalidade personalizada para substituir o comportamento padrão da caixa de diálogo. Por padrão, ao substituir um arquivo, a caixa de diálogo exibe um prompt que permite ao usuário verificar essa ação. Para violações de compartilhamento, por padrão, a caixa de diálogo exibe uma mensagem de erro, ela não fecha e o usuário precisa fazer outra escolha. O processo de chamada pode substituir esses padrões e exibir sua própria interface do usuário, se desejado. A caixa de diálogo pode ser instruída para recusar o arquivo e permanecer aberta ou aceitar o arquivo e fechar com êxito.

## <a name="customizing-the-dialog"></a>Personalizando a caixa de diálogo

Uma variedade de controles pode ser adicionada à caixa de diálogo sem fornecer um modelo de caixa de diálogo do Win32. Esses controles incluem botão de pressão, ComboBox, adCheckButton, listas de botões de opção, grupos, separadores e controles de texto estáticos. Chame **QueryInterface** no objeto Dialog ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)ou [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) para obter um ponteiro [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) . Use essa interface para adicionar controles. Cada controle tem uma ID fornecida pelo chamador associada, bem como um estado *visível* e *habilitado* que pode ser definido pelo processo de chamada. Alguns controles, como a "pressão", também têm texto associado a eles.

Vários controles podem ser adicionados a um "grupo Visual" que se move como uma única unidade no layout da caixa de diálogo. Os grupos podem ter um rótulo associado a eles.

Os controles podem ser adicionados somente antes da exibição da caixa de diálogo. No entanto, quando a caixa de diálogo é exibida, os controles podem ser ocultados ou mostrados como desejado, talvez em resposta à ação do usuário. Os exemplos a seguir mostram como adicionar uma lista de botões de opção à caixa de diálogo.


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





### <a name="adding-options-to-the-ok-button"></a>Adicionando opções ao botão OK

Da mesma forma, as opções podem ser adicionadas aos botões **abrir** ou **salvar** , que são o botão **OK** para seus respectivos tipos de diálogo. As opções podem ser acessadas por meio de uma caixa de listagem suspensa anexada ao botão. O primeiro item na lista se torna o texto do botão. O exemplo a seguir mostra como fornecer um botão **Open** com duas possibilidades: "Open" e "Open as Read-Only".


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





A escolha do usuário pode ser verificada após a caixa de diálogo retornar do método [**show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) como você faria para uma ComboBox ou pode ser verificada como parte da manipulação por [**IFileDialogEvents:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).

### <a name="responding-to-events-in-added-controls"></a>Respondendo a eventos em controles adicionados

O manipulador de eventos fornecido pelo processo de chamada pode implementar [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) além de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents). O **IFileDialogControlEvents** permite que o processo de chamada reaja a esses eventos:

-   Botão de pressão clicado
-   Estado de CheckButton alterado
-   Item selecionado em uma lista de menus, caixas de combinação ou botões de opção
-   Ativação de controle. Isso é enviado quando um menu está prestes a exibir uma lista suspensa, caso o processo de chamada queira alterar os itens na lista.

## <a name="full-samples"></a>Exemplos completos

Veja a seguir exemplos de C++ completos e baixáveis do SDK (Software Development Kit) do Windows que demonstram o uso e a interação com a caixa de diálogo de item comum.

-   [Exemplo de caixa de diálogo de arquivo comum](samples-commonfiledialog.md)
-   [Exemplo de modos de diálogo de arquivo comum](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_argumentos de PPV de IID \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
