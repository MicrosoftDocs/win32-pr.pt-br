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
# <a name="using-autocomplete"></a>Usando o preenchimento automático

O preenchimento automático expande as cadeias de caracteres que foram inseridas parcialmente em um [controle de edição](/windows/desktop/Controls/edit-controls) em cadeias de caracteres completas. Por exemplo, quando um usuário começa a inserir uma URL no controle de edição de endereço inserido na barra de ferramentas do Windows Internet Explorer, o preenchimento automático expande a cadeia de caracteres em uma ou mais opções de URL completas que são consistentes com a cadeia de caracteres parcial existente. Uma cadeia de caracteres de URL parcial, como "MIC", pode ser expandida para " https://www.microsoft.com " ou " https://www.microsoft.com/windows ". O preenchimento automático normalmente é usado com controles de edição ou com controles que têm um controle de edição inserido, como o controle [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .

## <a name="adding-autocomplete-functionality-to-your-application"></a>Adicionando a funcionalidade de preenchimento automático ao seu aplicativo

Um aplicativo pode adicionar funcionalidade de preenchimento automático a um controle de edição de duas maneiras:

-   [**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) é uma função simples que pode preencher um caminho de arquivo ou uma URL.
-   A interface [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) é exposta pelo objeto de preenchimento automático ( \_ AutoCompletar CLSID). Ele permite que os aplicativos inicializem, habilitem e desabilitem o objeto. O **IAutoComplete** permite mais controle sobre as fontes de preenchimento automático, incluindo a capacidade de adicionar uma fonte personalizada. O restante deste tópico discute o uso de **IAutoComplete**. Consulte [como habilitar o preenchimento automático manualmente](how-to-enable-autocomplete-manually.md) para obter exemplos de uso específicos.

## <a name="autocomplete-modes"></a>Modos de preenchimento automático

Ao usar [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), o preenchimento automático pode exibir a cadeia de caracteres completa em dois modos: acréscimo automático e sugestão automática. Os modos são independentes; Você pode habilitar um ou ambos. Para especificar o modo, chame [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Acréscimo
</dt> <dd>

No modo de acréscimo automático, a conclusão automática acrescenta o restante da cadeia de caracteres candidatas mais provável aos caracteres existentes, destacando os caracteres acrescentados. Se o usuário continuar a inserir caracteres, eles serão adicionados à cadeia de caracteres parcial existente. Se o usuário adicionar um caractere idêntico ao próximo caractere realçado, o realce desse caractere será desativado. Os caracteres restantes ainda serão realçados. Se o usuário adicionar um caractere que não corresponde ao próximo caractere realçado, o preenchimento automático tentará gerar uma nova cadeia de caracteres candidatas com base na cadeia de caracteres parcial maior e acrescentará o restante da nova cadeia de caracteres candidatas à cadeia de caracteres parcial atual. Se nenhuma cadeia de caracteres candidata puder ser encontrada, somente os caracteres digitados serão exibidos e a caixa de edição se comformará como faria sem preenchimento automático. Esse processo continua até que o usuário aceite uma cadeia de caracteres.

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Sugestão automática
</dt> <dd>

No modo de sugestão automática, o preenchimento automático exibe uma lista suspensa, com uma ou mais cadeias de caracteres completas sugeridas, abaixo do controle de edição. O usuário pode selecionar uma das cadeias de caracteres sugeridas ou continuar digitando. À medida que a digitação progride, a lista suspensa pode ser modificada com base na cadeia de caracteres parcial atual. Se você definir o \_ sinalizador de pesquisa aco em [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), o preenchimento automático fornecerá uma opção, na parte inferior da lista suspensa, para pesquisar a cadeia de caracteres parcial atual. Essa opção é exibida mesmo se não houver cadeias de caracteres sugeridas. Se o usuário selecionar a opção de pesquisa, seu aplicativo deverá iniciar um mecanismo de pesquisa para auxiliar o usuário.

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>Usando fontes de preenchimento automático predefinidas

O preenchimento automático depende de ter uma fonte que forneça cadeias de caracteres para corresponder à cadeia parcial do usuário. Você tem a opção de fornecer uma fonte de preenchimento automático personalizada, mas várias das fontes mais comuns são fornecidas pelo sistema.

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>\_ACLHISTORY CLSID
</dt> <dd>

Uma fonte de preenchimento automático que corresponde à lista de URLs na lista de histórico do usuário.

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>\_ACLMRU CLSID
</dt> <dd>

Uma fonte de preenchimento automático que corresponde à lista de URLs na lista de usuários usados recentemente.

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>\_ACLISTISF CLSID
</dt> <dd>

Uma fonte de preenchimento automático que corresponde a itens no namespace do Shell: arquivos no computador do usuário, bem como itens em pastas virtuais, como o painel de controle.

</dd> </dl>

Há ocasiões em que, em vez de liberar imediatamente os recursos, talvez você queira manter os ponteiros de interface para os vários objetos envolvidos no preenchimento automático. Em particular, isso é feito quando você deseja ajustar dinamicamente o comportamento de preenchimento automático. A instância mais comum disso ocorre ao usar o objeto CLSID \_ ACListISF, que é concluído de forma completa do namespace do Shell e tem a opção [**(ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) de enumeração do diretório atual também. Por exemplo, quando você navega para uma nova pasta, o Internet Explorer altera o diretório atual da barra de endereços e, portanto, as configurações precisam ser alteradas dinamicamente. Há duas maneiras de especificar o diretório que o objeto CLSID \_ ACListISF deve tratar como o diretório atual:

-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) especifica o diretório por meio de uma [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).
-   [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) especifica o diretório por meio de uma cadeia de caracteres de caminho.

No seguinte, suponha que **PAL** seja um ponteiro para a interface [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) de um objeto CLSID \_ ACListISF:

-   Usando [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):

    Para informar ao \_ objeto CLSID ACListISF que uma [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) específica deve ser tratada como o diretório atual, você pode usar a interface [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) do objeto. Como uma **ITEMIDLIST** pode se referir a uma pasta virtual, esse método é mais flexível do que o uso de [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).

    Observe que os exemplos a seguir usam o modelos QueryInterface, que permite uma lista de parâmetros simplificada.

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   Usando [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):

    Para dar ao \_ objeto CLSID ACListISF um caminho como o diretório atual, você pode usar a interface [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) do objeto.

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

    

 

 
