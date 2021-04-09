---
description: No Windows Vista, o painel de entrada do Tablet PC integra novos recursos de preenchimento automático que permitem que a lista de preenchimento automático de um aplicativo seja atualizada em tempo real à medida que a tinta de um usuário é reconhecida no painel de entrada.
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: Usando o preenchimento automático do painel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e7f108631eb2723b71bf8ed919c17a0eabff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090293"
---
# <a name="using-input-panel-autocomplete"></a>Usando o preenchimento automático do painel de entrada

No Windows Vista, o painel de entrada do Tablet PC integra novos recursos de preenchimento automático que permitem que a lista de preenchimento automático de um aplicativo seja atualizada em tempo real à medida que a tinta de um usuário é reconhecida no painel de entrada. Além disso, a lista de preenchimento automático do aplicativo é posicionada em um local conveniente para usuários do painel de entrada. Sem o preenchimento automático do painel de entrada, o uso de recursos de preenchimento automático com o painel de entrada é um processo difícil, exigindo que os usuários insiram um caractere por vez e movam o painel de entrada para acessar sugestões de preenchimento automático. Com a integração, o preenchimento automático é uma ferramenta poderosa para usuários de Tablet PC que aceleram e aumentam a facilidade de inserir texto com o painel de entrada.

![painel de entrada com a lista de preenchimento automático do IE](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

Há três opções de como um aplicativo pode tirar proveito da integração de preenchimento automático do painel de entrada. Os aplicativos que contêm a funcionalidade Autocompleta criada usando o preenchimento automático do Shell (por meio da interface [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) ) ou .NET Framework preenchimento automático (por meio da enumeração [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) ) recebem a integração de preenchimento automático do painel de entrada sem a necessidade de alterações de código. Os aplicativos que incluem campos personalizados de texto de preenchimento automático podem usar a API de preenchimento automático do painel de entrada para obter a mesma funcionalidade.

Em todos os casos, você pode fazer essas modificações na lista de preenchimento automático do aplicativo sem duplicar ou modificar a interface do usuário ou a lógica de previsão usada por um aplicativo para gerar uma lista de preenchimento automático. A lista de preenchimento automático continua sendo o proprietário desenhado pelo aplicativo e o conteúdo da lista de preenchimento automático é o mesmo que o texto foi digitado diretamente no campo de edição.

A integração de preenchimento automático do painel de entrada tem suporte no sistema operacional Windows Vista ou versões posteriores. A integração de preenchimento automático do painel de entrada é incorporada ao preenchimento automático do Shell, começando com o Windows Vista e em Windows Forms desenvolvimento, começando com .NET Framework versão 3,0. Embora o [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) e o [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) sejam executados em versões anteriores do Windows, a integração de preenchimento automático do painel de entrada não tem suporte no Microsoft Windows XP Tablet PC Edition ou em sistemas operacionais anteriores. Se você executar o preenchimento automático do painel de entrada em versões anteriores do Tablet PC, os aplicativos voltarão para o comportamento de pré-atualização.

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>Motivos para integrar listas de preenchimento automático do aplicativo com o painel de entrada

A integração da lista de preenchimento automático de um aplicativo permite o máximo de facilidade e velocidade de entrada para os usuários que estão inserindo texto em um campo de texto que inclui a funcionalidade de preenchimento automático. Além disso, um aplicativo que inclui a integração de preenchimento automático do painel de entrada aparece imediatamente como se fosse desenvolvido com o Tablet PC em mente, tornando o aplicativo mais atraente para os usuários do Tablet PC.

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>Como o painel de entrada e a lista de preenchimento automático interagem sem integração

Usando o painel de entrada para inserir texto em um campo de texto que inclui uma lista de preenchimento automático, mas que não está integrado ao painel de entrada:

1.  O usuário coloca o foco no campo de texto e abre o painel de entrada.
2.  O usuário grava um ou dois caracteres.
3.  O usuário toca em **Inserir**. O painel de entrada insere o texto no campo de texto do aplicativo. A lista de preenchimento automático do aplicativo é exibida e provavelmente é parcialmente ou completamente obscurecida pelo painel de entrada.
4.  O usuário arrasta o painel de entrada para descobrir a lista de preenchimento automático do aplicativo.
5.  Supondo que a entrada correta esteja incluída na lista de preenchimento automático, o usuário agora pode selecionar essa entrada; caso contrário, o usuário deverá repetir as etapas 2 e 3.

Isso é claramente um processo complicado. As expectativas do usuário de como uma lista de preenchimento automático devem funcionar são tracejadas e sua capacidade de executar tarefas é prejudicada.

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>Como o painel de entrada e a interação de lista de preenchimento automático aprimoram com a integração

Usando o painel de entrada para inserir texto em um campo de texto que inclui uma lista de preenchimento automático que é integrada com o painel de entrada:

1.  O usuário coloca o foco no campo de texto e abre o painel de entrada.
2.  O usuário grava um ou dois caracteres. A lista de preenchimento automático do aplicativo aparece diretamente acima ou diretamente abaixo do painel de entrada enquanto o usuário grava o texto.
3.  O usuário seleciona a entrada na lista AutoCompletar; a entrada é inserida diretamente no campo de texto do aplicativo ou o usuário repete a etapa 2 até que a entrada correta seja exibida.

Devido à integração, a lista de preenchimento automático aparece e é atualizada enquanto o usuário está gravando no painel de entrada. Além disso, a lista é posicionada de forma que seja conveniente para o usuário acessar durante a gravação e não obscurecida pelo painel de entrada. Por fim, quando o usuário seleciona um item de uma lista de preenchimento automático, o item é inserido diretamente no campo de entrada de texto do aplicativo, permitindo assim que o usuário ignore a etapa de inserção de texto do painel de entrada.

![painel de entrada com a lista de preenchimento automático do Outlook Express](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>Componentes de preenchimento automático padrão que incluem integração de preenchimento automático do painel de entrada

[**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) e [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) incluem integração interna do painel de entrada preenchimento automático. Os aplicativos que usam qualquer um desses componentes padrão de preenchimento automático podem aproveitar a funcionalidade de preenchimento automático do painel de entrada com pouco ou nenhum trabalho adicional. Além disso, embora o preenchimento automático do painel de entrada só tenha suporte no Windows Vista ou em novas versões do sistema operacional Windows, os aplicativos que foram criados usando o **IAutoComplete** antes do lançamento do Windows Vista obtêm a integração de preenchimento automático do painel de entrada automaticamente quando executados no Windows Vista. As seções a seguir contêm mais informações sobre os elementos **IAutoComplete** e AutoCompleteMode específicos que incluem a integração de preenchimento automático do painel de entrada.

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>Preenchimento automático do shell com integração de preenchimento automático do painel de entrada

Os aplicativos que usam o [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) obtêm integração de preenchimento automático do painel de entrada gratuitamente. Embora as APIs de preenchimento automático do Shell estejam incluídas no Windows 2000 em diante, a integração de preenchimento automático do painel de entrada só é compatível com o Windows Vista e versões mais recentes. No entanto, os aplicativos criados antes do lançamento do Windows Vista que usam o **IAutoComplete** automaticamente obtêm a integração de preenchimento automático do painel de entrada quando executados no Windows Vista.

Para tirar proveito do preenchimento automático do Tablet dessa forma, você deve usar o objeto de preenchimento automático (**\_ AutoCompletar CLSID**). Se você quiser fornecer a funcionalidade de preenchimento automático para URLs ou nomes de arquivo, use a função [**SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) para criar o objeto de preenchimento automático.

Além de [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete), você pode implementar [**IAutoComplete2**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) ou [**IAutoCompleteDropDown**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)s diretamente e ainda obter automaticamente a integração de preenchimento automático do painel de entrada.

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>Integração de preenchimento automático do painel de entrada com aplicativos .NET Framework

A partir do .NET Framework 3,0, Windows Forms TextBoxes incluem AutoCompletar. A Windows Forms AutoCompletar caixa de texto é criada sobre o preenchimento automático do Shell, o que significa que a integração de preenchimento automático do painel de entrada também é interna. .NET Framework 3,0 é compatível com o nível inferior das edições do Windows lançadas antes do Windows Vista. No entanto, como a integração de preenchimento automático do painel de entrada só tem suporte no Windows Vista ou em versões posteriores, a integração de preenchimento automático do painel de entrada funciona apenas em um aplicativo .NET Framework 3,0 quando ele é instalado no Windows Vista ou em versões posteriores.

Os aplicativos que desejam aproveitar a integração de preenchimento automático do painel de entrada no .NET Framework 3,0 devem usar uma [caixa de texto](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) Windows Forms com a propriedade [AutoCompleteMode](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1) habilitada. Você não precisa fazer nenhum trabalho adicional além de obter Windows Forms preenchimento automático para trabalhar para tirar proveito da integração de preenchimento automático do painel de entrada.

## <a name="using-input-panel-autocomplete-apis-directly"></a>Usando as APIs de preenchimento automático do painel de entrada diretamente

Os desenvolvedores de caixas de texto de preenchimento automático personalizados precisam trabalhar diretamente com as APIs de preenchimento automático do painel de entrada para obter a experiência de entrada de texto aprimorada que a integração de preenchimento automático do painel de entrada permite em seus aplicativos. As APIs de preenchimento automático do painel de entrada são incluídas como parte do sistema operacional Windows Vista e como parte do SDK da plataforma Tablet versão 1,9 ou posterior. As interfaces de preenchimento automático do painel de entrada são interfaces baseadas em COM.

A seção a seguir descreve como trabalhar essas interfaces em detalhes para um aplicativo C++. No entanto, essas interfaces COM podem ser implementadas na maioria das linguagens, incluindo C \# , por meio do uso de interoperabilidade com.

Para implementar a integração de preenchimento automático do painel de entrada em uma caixa de texto de preenchimento automático personalizado, as duas interfaces necessárias são a [**interface ITipAutocompleteProvider**](itipautocompleteprovider.md) e a [**interface ITipAutocompleteClient**](itipautocompleteclient.md). As definições para essas interfaces são encontradas em TipAutoComplete. h e TipAutoComplete \_ i.c.

Primeiro, um aplicativo deve definir e criar uma instância de uma classe de provedor de preenchimento automático, que implementa [**ITipAutocompleteProvider**](itipautocompleteprovider.md) para cada campo de entrada de texto que inclui uma lista de preenchimento automático. Essa classe gerencia o lado do aplicativo da integração de preenchimento automático. Todas as solicitações de preenchimento automático do painel de entrada são feitas do cliente de preenchimento automático para o aplicativo por meio do provedor de preenchimento automático do aplicativo. O provedor de preenchimento automático do aplicativo deve ter acesso ao HWND para a lista de preenchimento automático do aplicativo e o HWIND para o campo de entrada de texto associado. Além disso, os seguintes métodos de **ITipAutocompleteProvider** devem ser implementados:

-   [**Método ITipAutocompleteProvider:: UpdatePendingText**](itipautocompleteprovider-updatependingtext.md): esse método é usado pelo cliente de preenchimento automático para notificar o aplicativo sobre o texto que um usuário gravou no painel de entrada. Após receber essa notificação, o provedor é responsável por gerar uma lista de preenchimento automático como se o texto tivesse sido digitado no campo de entrada de texto do aplicativo. A cadeia de caracteres passa para o provedor de preenchimento automático por meio do **método ITipAutocompleteProvider:: UpdatePendingText** apenas inclui o texto atualmente no painel de entrada. Portanto, se houver texto adicional no campo de entrada de texto, é responsabilidade do provedor acrescentá-lo corretamente ao texto enviado pelo cliente. A cadeia de caracteres passada pelo **método ITipAutocompleteProvider:: UpdatePendingText** deve ser tratada como uma substituição para a seleção atual no campo. Se não houver nenhuma seleção atual, ela deverá ser colocada na posição do ponto de inserção atual. Quando a lista de preenchimento automático é gerada, o provedor deve chamar o [**método ITipAutocompleteProvider:: show**](itipautocompleteprovider-show.md) transmitindo **true** para exibir a lista de preenchimento automático. O aplicativo não deve armazenar em cache chamadas para **UpdatePendingText** , mas tratar cada chamada adicional para **UpdatePendingText** como cancelamento da chamada anterior para evitar a intermitência de uma interface do usuário de lista de preenchimento automático desatualizada. O código de exemplo a seguir ilustra essas práticas.

    ```C++
    HRESULT SampleProvider::UpdatePendingText(BSTR bstrPendingText)
    {
       //Discard previously cached pending text from Input Panel
       m_bstrPending.Empty();
        //Store the new pending text from Input Panel as m_bstrPending
    m_bstrPending = bstrPendingText;

        //Get the text from the field in two chunks. The characters to
    //the left of the selection and the characters to the right.
    CComBSTR bstrLeftContext = //Text to the left of the selection
            CComBSTR bstrRightContext = //Text to the right of the selection

    //Discard previously cached complete text
        m_bstrCompleteText.Empty();
        //Append to the field text from the left of the selection
        //the text from Input Panel and then append to that
        //the field text to the right of the selection
        m_bstrCompleteText.Append(bstrLeftContext);
        m_bstrCompleteText.Append(m_bstrPending);
        m_bstrCompleteText.Append(bstrRigtContext);

        //Update the app's AC list based on m_bstrCompleteText
        //...

        //Show the updated AC list by calling the provider's Show method
       Show(true);
       return S_OK;
    }
    ```

    

-   [**Método ITipAutocompleteProvider:: show**](itipautocompleteprovider-show.md): esse método é chamado de [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md), mas também pode ser chamado pelo cliente de preenchimento automático a qualquer momento. Após receber essa chamada, o provedor de preenchimento automático deve ocultar ou mostrar o provedor de preenchimento automático, conforme indicado pelo parâmetro. Antes de mostrar a lista de preenchimento automático, o provedor de preenchimento automático deve consultar o cliente de preenchimento automático sobre onde posicionar a lista de preenchimento automático. Mais informações sobre como posicionar a lista de preenchimento automático aparecem mais adiante neste artigo.

Em seguida, o aplicativo deve usar a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) de Active Template Library (ATL) para produzir uma instância da [**interface ITipAutocompleteClient**](itipautocompleteclient.md) com a ID de classe **CLSID \_ TipAutoCompleteClient** como um servidor em processo e, em seguida, registrar o provedor com o cliente. O [**método ITipAutocompleteClient:: aconselheprovider**](itipautocompleteclient-adviseprovider.md) do cliente de preenchimento automático registra o provedor com o cliente para permitir que o cliente chame o objeto de provedor de preenchimento automático do aplicativo. Se tiptsf.dll não estiver presente no sistema, a função **CoCreateInstance** falhará e retornará **REGDB \_ e \_ CLASSNOTREG**. Neste ponto, o aplicativo pode descartar seu objeto [**ITipAutocompleteProvider**](itipautocompleteprovider.md) e prosseguir como se o painel de entrada não existir, pois ele não é um sistema desse tipo.

O aplicativo pode optar por criar uma instância de [**ITipAutocompleteClient**](itipautocompleteclient.md) ou uma instância por campo de texto. A primeira opção exige que o provedor tenha o registro cancelado e registrado toda vez que o foco for alterado. Mais informações sobre o cancelamento do registro do provedor de preenchimento automático aparecem mais adiante neste tópico.

Há várias etapas envolvidas no posicionamento da lista de preenchimento automático que deve ser coordenada entre o provedor de preenchimento automático (aplicativo) e o cliente de preenchimento automático (painel de entrada). Antes de a lista de preenchimento automático ser mostrada, como resultado de uma chamada para o método [**show**](itipautocompleteprovider-show.md) do provedor de preenchimento automático ou devido ao usuário que está inserindo o texto usando o teclado, o provedor é solicitado a consultar o cliente sobre onde posicionar a lista de preenchimento automático. O provedor deve executar as seguintes etapas:

-   Use o [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) do cliente de preenchimento automático para determinar se o painel de entrada está pronto para que a lista de preenchimento automático seja mostrada. **RequestShowUI** usa o parâmetro *HWND* que é o HWND para a janela de lista de preenchimento automático e o método retorna **true** ou **false** para indicar se é o estado no qual a lista de preenchimento automático pode ser mostrada. Se o cliente retornar **false**, o provedor não deverá tentar mostrar a lista de preenchimento automático.
-   Chame [**RequestShowUI**](itipautocompleteclient-requestshowui.md) para definir o identificador da janela de lista de AutoCompletar pop-up antes de chamar o [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md). A falha em fazer isso causará um erro **E \_ INVALIDARG** ao chamar **PreferredRects**.
-   Se [**RequestShowUI**](itipautocompleteclient-requestshowui.md) retornar **true**, o provedor deverá calcular o retângulo de coordenadas de tela padrão da lista de preenchimento automático com base no local do campo de entrada de texto e, em seguida, chamar o [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md)do cliente de preenchimento automático. Isso permite que o cliente de preenchimento automático ajuste o retângulo para evitar que a lista de preenchimento automático se sobreponha com o painel de entrada. O método **PreferredRects** usa quatro parâmetros:

    -   RECT *rcACList*: o retângulo de coordenadas de tela padrão da lista de preenchimento automático.
    -   RECT *rcField*: o retângulo de coordenadas de tela do campo de entrada de texto correspondente.
    -   RECT *\* prcModifiedACList*: o retângulo de coordenadas de tela ajustado para o preenchimento automático
    -   BOOL *\* pfShowAbove*: esse parâmetro indica ao provedor se o retângulo *prcModifiedACList* posiciona a lista de preenchimento automático acima ou abaixo do painel de entrada. O aplicativo pode usar essas informações para desenhar corretamente elementos da interface do usuário, como alças de redimensionamento e barras de rolagem. O provedor deve inicialmente passar na direção em que a lista de preenchimento automático seria posicionada em relação ao campo de entrada de texto por *rcACList*. O cliente não alterará *pfShowAbove* se definir *PrcModifiedACList* igual a *rcACList*.

    Use os valores de retorno dos argumentos *prcModifiedACList* e *pfShowAbove* out para posicionar e mostrar a janela de lista de preenchimento automático. Se o painel de entrada não estiver em uso, [**RequestShowUI**](itipautocompleteclient-requestshowui.md) sempre retornará **true** e *prcModifiedACList* será sempre o mesmo que *rcACList*. *pfShowAbove* também é inalterado, o resultado é que as chamadas não afetam o comportamento do aplicativo. O código de exemplo a seguir ilustra essas práticas.


```C++
HRESULT SampleProvider::Show(BOOL fShow)
{
    //Ask the AC client if it is OK to show the Autocomplete list.
    BOOL fAllowShowing = FALSE;
    m_spACClient->RequestShowUI(m_hWndList, &fAllowShowing);

    if (fShow && fAllowingShowing)
        {
            // Create the parameters required to call PreferredRects
            RECT rcField = //Rectangle for app's text field
            RECT rcACList = //Default rectangle for app's AC list
            RECT rcModifiedACList = {0, 0, 0, 0};
            BOOL fShowAbove = TRUE;

//Ask the AC client to modify the position of the AC list
m_spACClient->PreferredRects(&rcACList, &rcField,
&rcModifiedACList, &fShowAbove);

            //Show the Autocomplete UI at the modified preferred rectangle
            //from rcModifiedACList and the directional info provide by
//fShowAbove
            //...
        }
    else
        {
        //Hide the Autocomplete list and clean up
        //...
        }
    return S_OK;
}
```



Quando o usuário seleciona um item na lista de preenchimento automático, o provedor precisa chamar o [**método ITipAutocompleteClient:: Userselecionar**](itipautocompleteclient-userselection.md) do cliente, além de inserir o texto do item selecionado no campo de entrada de texto. O painel de entrada usa essa notificação para descartar todo o texto restante que ainda não foi inserido no painel de entrada.

Por fim, quando o provedor não for mais necessário, o provedor deverá ser desvinculado do cliente de preenchimento automático chamando o [**método ITipAutocompleteClient:: unaconselheprovider**](itipautocompleteclient-unadviseprovider.md) do cliente de preenchimento automático para cancelar o registro do provedor. Talvez seja necessário cancelar o registro do provedor por um destes dois motivos: como o campo de entrada de texto ao qual o provedor está associado foi destruído, ou porque o aplicativo escolhe criar apenas um cliente de preenchimento automático, em vez de um campo de entrada por texto. Nessa instância, o provedor deve ter o registro cancelado toda vez que o foco for desativado do campo de texto.

## <a name="conclusion"></a>Conclusão

A integração de preenchimento automático do painel de entrada é uma ferramenta poderosa para melhorar a experiência do usuário em aplicativos do Windows que incluem listas de preenchimento automático em Tablet PCs. Sem integração, os usuários do painel de entrada precisam passar por um processo entediante de inserir texto um caractere por vez e reposicionar o painel de entrada para usar o preenchimento automático. Com a integração, as listas de preenchimento automático aparecem em um local conveniente como tinta dos usuários no painel de entrada, aumentando a velocidade e a facilidade de entrada de texto. Em aplicativos que incluem a funcionalidade de preenchimento automático criada com base no preenchimento automático do Shell ou .NET Framework 3,0 AutoCompletar, a integração de preenchimento automático do painel de entrada é um recurso gratuito e atraente. Além disso, um conjunto simples de interfaces baseadas em COM é fornecido para habilitar a mesma experiência integrada para aplicativos que optam por usar controles de preenchimento automático personalizados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 
