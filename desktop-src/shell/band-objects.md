---
description: A barra do Explorer foi introduzida com o Microsoft Internet Explorer 4,0 para fornecer uma área de exibição adjacente ao painel do navegador.
title: Criar Barras personalizadas do Explorer, Faixas de ferramentas e Faixas da área de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9a57cc5bc8afa3e973c6d4d99b8bcee186287a6c9278407b900f84500d7d0e51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461737"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Criando barras personalizadas do Explorer, faixas de ferramentas e faixas de escrivaninha

A barra do Explorer foi introduzida com o Microsoft Internet Explorer 4,0 para fornecer uma área de exibição adjacente ao painel do navegador. ele é basicamente uma janela filho dentro da janela Windows Internet Explorer e pode ser usado para exibir informações e interagir com o usuário praticamente da mesma forma. As barras do Explorer são exibidas com mais frequência como um painel vertical no lado esquerdo do painel do navegador. No entanto, uma barra do Explorer também pode ser exibida horizontalmente, abaixo do painel do navegador.

![Captura de tela que mostra as barras verticais e horizontais do Explorer.](images/expl1.jpg)

Há uma ampla variedade de usos possíveis para a barra do Explorer. Os usuários podem selecionar a opção que desejam ver de várias maneiras diferentes, incluindo selecioná-la no submenu **barra do Explorer** do menu **Exibir** ou clicar em um botão da barra de ferramentas. O Internet Explorer fornece várias barras padrão do Explorer, incluindo favoritos e pesquisa.

Uma das maneiras que você pode personalizar o Internet Explorer é adicionando uma barra personalizada do Explorer. Quando implementado e registrado, ele será adicionado ao submenu **barra do Explorer** do menu **Exibir** . Quando selecionado pelo usuário, a área de exibição da barra do Explorer pode ser usada para exibir informações e tomar a entrada do usuário praticamente da mesma forma que uma janela normal.

![captura de tela das barras do Gerenciador](images/expl2.jpg)

Para criar uma barra personalizada do Explorer, você deve implementar e registrar um *objeto Band*. Os objetos de banda foram introduzidos com a versão 4,71 do Shell e fornecem recursos semelhantes aos de janelas normais. No entanto, como eles são objetos de Component Object Model (COM) e contidos pelo Internet Explorer ou pelo shell, eles são implementados de maneira um pouco diferente. Objetos de banda simples foram usados para criar as barras do Gerenciador de amostras exibidas no primeiro elemento gráfico. A implementação do exemplo de barra vertical do Explorer será discutida detalhadamente em uma seção posterior.

## <a name="tool-bands"></a>Faixas de ferramentas

uma *faixa de ferramentas* é um objeto de banda que foi introduzido com o Microsoft Internet Explorer 5 para dar suporte ao recurso de barra de ferramentas de rádio Windows. A barra de ferramentas do Internet Explorer é, na verdade, um [controle rebar](../controls/rebar-controls.md) que contém vários [controles ToolBar](../controls/toolbar-control-reference.md). Ao criar uma faixa de ferramentas, você pode adicionar uma banda a esse controle rebar. No entanto, como as barras do Explorer, uma faixa de ferramenta é uma janela de uso geral.

![captura de tela de faixas de ferramentas](images/toolband1.jpg)

Os usuários exibem uma barra de ferramentas selecionando-o no submenu **barras de ferramentas** do menu **Exibir** ou no menu de atalho exibido ao clicar com o botão direito do mouse na área da barra de ferramentas.

## <a name="desk-bands"></a>Faixas de escrivaninha

Os objetos de banda também podem ser usados para criar *faixas de escrivaninha*. Embora sua implementação básica seja semelhante às barras do Explorer, as faixas de escrivaninha não estão relacionadas ao Internet Explorer. Uma banda de mesa é basicamente uma maneira de criar uma janela encaixáveis na área de trabalho. O usuário seleciona-o clicando com o botão direito do mouse na barra de tarefas e selecionando-o no submenu **barras de ferramentas** .

![Captura de tela que mostra uma faixa de exemplo de escrivaninha.](images/desk2.png)

Inicialmente, as faixas de escrivaninha são encaixadas na barra de tarefas.

![Captura de tela que mostra as faixas de escrivaninha encaixadas na barra de tarefas.](images/desk1.jpg)

Em seguida, o usuário pode arrastar a faixa de escrivaninha para a área de trabalho e ela será exibida como uma janela normal.

![captura de tela de faixas de escrivaninha](images/desk3.png)

## <a name="implementing-band-objects"></a>Implementando objetos de banda

Os tópicos a seguir são discutidos.

-   [Noções básicas do objeto Band](#band-object-basics)
-   [Registro de banda](#band-registration)
-   [Um exemplo simples de uma barra personalizada do Explorer](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Noções básicas do objeto Band

Embora eles possam ser usados de forma muito semelhante às janelas normais, os objetos de banda são objetos COM que existem dentro de um contêiner. As barras do Explorer são contidas pelo Internet Explorer, e as faixas de escrivaninha são contidas pelo shell. Embora eles atendam a funções diferentes, sua implementação básica é muito semelhante. A principal diferença é em como o objeto Band é registrado, o que, por sua vez, controla o tipo de objeto e seu contêiner. Esta seção aborda esses aspectos da implementação que são comuns a todos os objetos de banda. Consulte [um exemplo simples de uma barra personalizada do Explorer](#a-simple-example-of-a-custom-explorer-bar) para obter detalhes adicionais de implementação.

Além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), todos os objetos de banda devem implementar as interfaces a seguir.

-   [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

Além de registrar seu identificador de classe (CLSID), os objetos da barra do Gerenciador e da faixa de escrivaninha também devem ser registrados para a categoria de componente apropriada. O registro da categoria de componente determina o tipo de objeto e seu contêiner. As bandas de ferramenta usam um procedimento de registro diferente e não têm um identificador de categoria (CATID). Os CATIDs para os três objetos de banda que os exigem são:



| Tipo de banda               | Categoria do componente |
|-------------------------|--------------------|
| Barra vertical do Explorer   | InfoBand de CATID \_    |
| Barra horizontal do Gerenciador | CommBand de CATID \_    |
| Faixa de escrivaninha               | DeskBand de CATID \_    |



 

Consulte [registro de banda](#band-registration) para obter mais informações sobre como registrar objetos de banda.

Se o objeto Band for aceitar a entrada do usuário, ele também deverá implementar [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject). Para adicionar itens ao menu de atalho para as faixas de barra ou escrivaninha do Explorer, o objeto de faixa deve exportar [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). As faixas de ferramentas não dão suporte a menus de atalho.

como os objetos de banda implementam uma janela filho, eles também devem implementar um procedimento de janela para lidar com Windows mensagens.

Os objetos de banda podem enviar comandos para seu contêiner por meio da interface [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) do contêiner. Para obter o ponteiro de interface, chame o método [**IInputObjectSite:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do contêiner e solicite \_ IOleCommandTarget de IID. Em seguida, você envia comandos para o contêiner com [**IOleCommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec). O grupo de comandos é CGID \_ DeskBand. Quando o método [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) de um objeto Band é chamado, o contêiner usa o parâmetro *dwBandID* para atribuir o objeto Band um identificador que é usado para três dos comandos. Há suporte para as IDs de comando de quatro **IOleCommandTarget:: exec** .

-   \_BANDINFOCHANGED DBID

    As informações da banda foram alteradas. Defina o parâmetro *pvaIn* para o identificador de banda que foi recebido na chamada mais recente para [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). O contêiner chamará o método **IDeskBand:: GetBandInfo** do objeto Band para solicitar as informações atualizadas.

-   \_MAXIMIZEBAND DBID

    Maximize a banda. Defina o parâmetro *pvaIn* para o identificador de banda que foi recebido na chamada mais recente para [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).

-   DBID \_ somente

    Ativar ou desativar outras faixas no contêiner. Defina o parâmetro *pvaIn* para o tipo de VT \_ desconhecido com um dos seguintes valores:

    

    | Valor | Descrição                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | pUnk  | Um ponteiro para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do objeto de banda. Todas as outras faixas de escrivaninha ficarão ocultas. |
    | 0     | Ocultar todas as faixas de escrivaninha.                                                                                        |
    | 1     | Mostrar todas as faixas de escrivaninha.                                                                                        |

    

     

-   \_PUSHCHEVRON DBID

    [Versão 5](versions.md). Exiba um menu de divisa. O contêiner envia uma [**mensagem \_ PUSHCHEVRON RB**](../controls/rb-pushchevron.md) e o objeto Band recebe uma notificação [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) que solicita que ele exiba o menu de divisa. Defina o parâmetro *nCmdExecOpt* do método [**IOleCommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) como o identificador de banda recebido na chamada mais recente para [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Defina o parâmetro *pvaIn* do método **IOleCommandTarget:: exec** como o \_ tipo VT i4 com um valor definido pelo aplicativo. Ele passa de volta para o objeto Band como o valor *lAppValue* da \_ notificação RBN CHEVRONPUSHED.

### <a name="band-registration"></a>Registro de banda

Um objeto de banda deve ser registrado como um servidor em processo OLE que dá suporte ao Threading Apartment. O valor padrão para o servidor é uma cadeia de caracteres de texto de menu. Para barras do Explorer, ele aparecerá no submenu **barra do Explorer** do menu **Exibir** do Internet Explorer. Para as faixas de ferramentas, ela aparecerá no submenu **barras de ferramentas** do menu **Exibir** do Internet Explorer. Para faixas de escrivaninha, ela aparecerá no submenu **barras de ferramentas** do menu de atalho da barra de tarefas. Assim como os recursos de menu, colocar um e comercial (&) na frente de uma letra fará com que ele seja sublinhado e habilite atalhos de teclado. Por exemplo, a cadeia de menu para a barra vertical do Explorer mostrada no primeiro elemento gráfico é "exemplo &barra vertical do Explorer".

Inicialmente, o Internet Explorer recupera uma enumeração dos objetos de barra do Gerenciador registrados do registro usando as categorias de componente. Para aumentar o desempenho, ele armazena em cache essa enumeração, fazendo com que as barras do Explorer adicionadas subsequentemente sejam ignoradas. para forçar Windows Internet Explorer a recriar o cache e reconhecer uma nova barra do explorer, exclua as seguintes chaves do registro durante o registro da nova barra do explorer:

**HKEY \_ Software de \_ usuário atual** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer**, \\ **descartada** \\ , categorias de componente de instalação de **createsetup** \\  \\ **{00021493-0000-0000-C000-000000000046}** \\ **Enum**

**HKEY \_ Software de \_ usuário atual** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer**, \\ **descartada** \\ , categorias de componente de instalação de **createsetup** \\  \\ **{00021494-0000-0000-C000-000000000046}** \\ **Enum**

> [!Note]  
> Como um cache da barra do Explorer é criado para cada usuário, o aplicativo de instalação pode precisar enumerar todos os hives do registro do usuário ou adicionar um stub por usuário para ser executado quando o usuário fizer logon pela primeira vez.

 

Em geral, a entrada de registro básica para um objeto de banda será exibida da seguinte maneira.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

As faixas de ferramentas também devem ter o CLSID do seu objeto registrado no Internet Explorer. Para fazer isso, atribua um valor em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **barra de ferramentas** chamado com o GUID CLSID do objeto de faixa de ferramenta, conforme mostrado aqui. Seu valor de dados é ignorado, portanto, o tipo de valor não é importante.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

Há vários valores opcionais que também podem ser adicionados ao registro. Por exemplo, o valor a seguir será necessário se você quiser usar a barra do Explorer para exibir HTML o valor mostrado não é um exemplo, mas o valor real que deve ser usado.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

Usado em conjunto com o valor mostrado acima, o valor opcional a seguir também será necessário se você quiser usar a barra do Explorer para exibir HTML. Esse valor deve ser definido como o local do arquivo que contém o conteúdo HTML da barra do Explorer.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

Outro valor opcional define a largura ou a altura padrão da barra do Explorer, dependendo se ela é vertical ou horizontal, respectivamente.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

O valor de barras deve ser definido como a largura ou altura da barra. O valor requer oito bytes e é colocado no registro como um valor binário. Os primeiros quatro bytes especificam o tamanho em pixels, em formato hexadecimal, a partir do byte mais à esquerda. Os últimos quatro bytes são reservados e devem ser definidos como zero.

Por exemplo, as entradas de registro completas para uma barra do Explorer com capacidade para HTML com uma largura padrão de pixels de 291 (0x123) são mostradas aqui.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

Você pode manipular o registro do CATID de um objeto de banda programaticamente. Crie um objeto do Gerenciador de categorias de componente (CLSID \_ StdComponentCategoriesMgr) e solicite um ponteiro para sua interface [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) . Passe o CLSID e o CATID do objeto de banda para [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Um exemplo simples de uma barra personalizada do Explorer

Este exemplo percorre a implementação da barra vertical do Explorer de exemplo mostrada na introdução.

O procedimento básico para criar uma barra personalizada do Explorer é o seguinte.

1.  [Implemente as funções necessárias para a dll](#dll-functions).
2.  [Implemente as interfaces COM necessárias.](#required-interface-implementations)
3.  [Implemente as interfaces COM opcionais desejadas.](#optional-interface-implementations)
4.  [Registre o CLSID do objeto e, se necessário, a categoria do componente.](#clsid-registration)
5.  Crie uma janela filho do Internet Explorer, dimensionada para caber na região de exibição da barra do Explorer.
6.  [Use a janela filho para exibir informações e interagir com o usuário.](#the-window-procedure)

A implementação muito simples usada na amostra da barra do Gerenciador poderia ser realmente usada para qualquer tipo de barra do Explorer ou uma faixa de escrivaninha, simplesmente registrando-a para a categoria de componente apropriada. Implementações mais sofisticadas precisarão ser personalizadas para a região de exibição e o contêiner de cada tipo de objeto. no entanto, grande parte dessa personalização pode ser realizada com o código de exemplo e sua extensão, aplicando técnicas de programação de Windows familiares à janela filho. Por exemplo, você pode adicionar controles para interação do usuário ou gráficos para uma exibição mais rica.

### <a name="dll-functions"></a>Funções de DLL

Todos os três objetos são empacotados em uma única DLL, que expõe as funções a seguir.

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

As três primeiras funções são implementações padrão e não serão discutidas aqui. A implementação da fábrica de classes também é padrão.

### <a name="required-interface-implementations"></a>Implementações de interface necessárias

O exemplo de barra vertical do Explorer implementa as quatro interfaces necessárias: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)e [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) como parte da classe CExplorerBar. As implementações do Construtor, destruidor e **IUnknown** são simples e não serão discutidas aqui. Consulte o código de exemplo para obter detalhes.

As interfaces a seguir são discutidas em detalhes.

-   [IObjectWithSite](#iobjectwithsite)
-   [IPersistStream](#ipersiststream)
-   [IDeskBand](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

Quando o usuário seleciona uma barra do Explorer, o contêiner chama o método [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) do objeto de banda correspondente. O parâmetro *punkSite* será definido como o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do site.

Em geral, uma implementação de [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) deve executar as seguintes etapas:

1.  Libere qualquer ponteiro de site que esteja sendo mantido no momento.
2.  Se o ponteiro passado para [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) for definido como **NULL**, a banda será removida. **SetSite** pode retornar S \_ OK.
3.  Se o ponteiro passado para [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) for não **nulo**, um novo site será definido. **SetSite** deve fazer o seguinte:
    1.  Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no site para sua interface [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .
    2.  Chame [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para obter o identificador da janela pai. Salve o identificador para uso posterior. Libere [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) se não for mais necessário.
    3.  Crie a janela do objeto de banda como um filho da janela obtida na etapa anterior. Não a crie como uma janela visível.
    4.  Se o objeto Band implementar [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no site para sua interface [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) . Armazene o ponteiro para esta interface para uso posterior.
    5.  Se todas as etapas forem bem-sucedidas, retorne as S \_ OK. Caso contrário, retorne o código de erro definido por OLE indicando o que falhou.

O exemplo da barra do Explorer implementa [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) da seguinte maneira. No código m a seguir, *\_ pSite* é uma variável de membro particular que contém o ponteiro [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e *m \_ hwndParent* mantém a alça da janela pai. Neste exemplo, a criação de janela também é tratada. Se a janela não existir, esse método criará a janela da barra do Explorer como um filho de tamanho adequado da janela pai obtida por **SetSite**. O identificador da janela filho é armazenado na *\_ HWND do m*.


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



A implementação do [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) de exemplo simplesmente encapsula uma chamada para o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do site, usando o ponteiro do site salvo por [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a>IPersistStream

O Internet Explorer chamará a interface [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) da barra do Explorer para permitir que a barra do Explorer carregue ou salve dados persistentes. Se não houver dados persistentes, os métodos ainda devem retornar um código de êxito. A interface **IPersistStream** herda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), portanto, cinco métodos devem ser implementados.

-   [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream:: IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream:: Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream:: GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

A amostra da barra do Gerenciador não usa nenhum dado persistente e tem apenas uma implementação mínima de [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) retorna o CLSID do objeto (CLSID \_ SampleExplorerBar) e o resto retorna S \_ OK, s \_ false ou E \_ NOTIMPL.

### <a name="ideskband"></a>IDeskBand

A interface [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) é específica para objetos de banda. Além de seu único método, ele herda de [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), que por sua vez herda de [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).

Há dois métodos [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) : [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) e [**IOleWindow:: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp). A implementação de exemplo da barra do Explorer de **GetWindow** retorna o identificador da janela filho da barra do Explorer, *m \_ hWnd*. A ajuda contextual não está implementada, portanto **ContextSensitiveHelp** retorna **E \_ NOTIMPL**.

A interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) tem três métodos.

-   [**IDockingWindow::ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**IDockingWindow::CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**IDockingWindow::ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

O método [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) não é usado com nenhum tipo de objeto Band e sempre deve retornar e \_ NOTIMPL. O método [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) mostra ou oculta a janela da barra do Explorer, dependendo do valor de seu parâmetro.


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



O método [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) destrói a janela da barra do Gerenciador.


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



O método restante, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), é específico para **IDeskBand**. O Internet Explorer usa-o para especificar o identificador e o modo de exibição da barra do Explorer. O Internet Explorer também pode solicitar uma ou mais partes de informações da barra do Explorer preenchendo o membro **dwMask** da estrutura [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) que é passada como o terceiro parâmetro. **GetBandInfo** deve armazenar o identificador e o modo de exibição e preencher a estrutura **DESKBANDINFO** com os dados solicitados. O exemplo da barra do Explorer implementa **GetBandInfo** conforme mostrado no exemplo de código a seguir.


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a>Implementações de interface opcional

Há duas interfaces que não são necessárias, mas que podem ser úteis para implementar: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). O exemplo da barra do Gerenciador implementa **IInputObject**. Consulte a documentação para obter informações sobre como implementar o **IContextMenu**.

### <a name="iinputobject"></a>IInputObject

A interface [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) deve ser implementada se um objeto Band aceitar entrada do usuário. O Internet Explorer implementa [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e usa o **IInputObject** para manter o foco de entrada do usuário adequado quando ele tem mais de uma janela contida. Há três métodos que precisam ser implementados por uma barra do Explorer.

-   [**IInputObject::UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**IInputObject::HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**IInputObject::TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

O Internet Explorer chama [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) para informar à barra do Explorer que está sendo ativada ou desativada. Quando ativado, o exemplo da barra do Explorer chama [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) para definir o foco para sua janela.

O Internet Explorer chama [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) quando está tentando determinar qual janela tem o foco. Se a janela da barra do Explorer ou um de seus descendentes tiver foco, **HasFocusIO** deverá retornar s \_ OK. Caso contrário, ele deve retornar S \_ false.

[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) permite que o objeto processe aceleradores de teclado. A amostra da barra do Gerenciador não implementa esse método, portanto, retorna S \_ false.

A implementação da barra de exemplo do [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) é a seguinte.


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a>Registro de CLSID

Assim como acontece com todos os objetos COM, o CLSID da barra do Explorer deve ser registrado. Para que o objeto funcione corretamente com o Internet Explorer, ele também deve ser registrado para a categoria de componente apropriada (CATID \_ InfoBand). A seção de código relevante para a barra do Gerenciador é mostrada no exemplo de código a seguir.


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



O registro de objetos de banda no exemplo usa procedimentos COM normais.

Além do CLSID, o servidor de objeto de banda também deve ser registrado para uma ou mais categorias de componente. Essa é, na verdade, a principal diferença na implementação entre as amostras de barra vertical e horizontal do Explorer. Esse processo é tratado pela criação de um objeto do Gerenciador de categorias de componente (CLSID \_ StdComponentCategoriesMgr) e usando o método [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) para registrar o servidor de objeto de banda. Neste exemplo, o registro de categoria de componente é manipulado passando o CLSID de exemplo da barra do Explorer e o CATID para uma função particular —**RegisterComCat**— conforme mostrado no exemplo de código a seguir.


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a>O procedimento de janela

como um objeto band usa uma janela filho para sua exibição, ele deve implementar um procedimento de janela para manipular Windows mensagens. O exemplo de banda tem funcionalidade mínima, portanto, seu procedimento de janela manipula apenas cinco mensagens:

-   [**NCCREATE do WM \_**](../winmsg/wm-nccreate.md)
-   [**pintura do WM \_**](../gdi/wm-paint.md)
-   [**comando do WM \_**](../menurc/wm-command.md)
-   [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)
-   [**KILLFOCUS do WM \_**](../inputdev/wm-killfocus.md)

O procedimento pode ser facilmente expandido para acomodar mensagens adicionais para dar suporte a mais recursos.


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



O manipulador de comandos do WM \_ simplesmente retorna zero. O manipulador de pintura do WM \_ cria a exibição de texto simples mostrada no exemplo da barra do Explorer na introdução.


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



Os \_ manipuladores do WM SETFOCUS e do WM KILLFOCUS informam \_ o site de uma alteração de foco chamando o método [**IInputObjectSite:: OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) do site.


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



Os objetos de banda fornecem uma maneira flexível e eficiente de estender os recursos do Internet Explorer Criando barras personalizadas do Explorer. A implementação de uma banda de mesa permite que você estenda os recursos das janelas normais. Embora alguma programação COM seja necessária, ela finalmente serve para fornecer uma janela filho para a interface do usuário. a partir daí, a maior parte da implementação pode usar técnicas de programação Windows familiares. Embora o exemplo discutido aqui tenha apenas uma funcionalidade limitada, ele ilustra todos os recursos necessários de um objeto de banda e pode ser prontamente estendido para criar uma interface de usuário exclusiva e poderosa.

 

 
