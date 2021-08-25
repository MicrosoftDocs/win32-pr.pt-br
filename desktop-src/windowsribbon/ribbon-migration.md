---
title: migrando para a estrutura da faixa de Windows
description: um aplicativo que se baseia em menus, barras de ferramentas e caixas de diálogo tradicionais pode ser migrado para a interface do usuário rica, dinâmica e controlada por contexto do sistema de comando Windows Ribbon framework.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows Faixa de faixas, migrando para o
- Faixa de faixas, migrando para o
- migrando para a faixa de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a011e9b5dad52f6f71fab272f0fded39ec59eb71cc7311ab9cf5ffccb4dfbca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841116"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>migrando para a estrutura da faixa de Windows

um aplicativo que se baseia em menus, barras de ferramentas e caixas de diálogo tradicionais pode ser migrado para a interface do usuário rica, dinâmica e controlada por contexto do sistema de comando Windows Ribbon framework. Essa é uma maneira fácil e eficaz de modernizar e revitalize o aplicativo ao mesmo tempo em que também melhora a acessibilidade, a usabilidade e a capacidade de descoberta de sua funcionalidade.

## <a name="introduction"></a>Introdução

Em geral, a migração de um aplicativo existente para a estrutura da faixa de opções envolve o seguinte:

-   Criar uma organização de controle e layout da faixa de opção que expõe a funcionalidade do aplicativo existente e é flexível o suficiente para dar suporte à nova funcionalidade.
-   Adaptando o código do aplicativo existente.
-   Migrar recursos de aplicativo (cadeias de caracteres e imagens) existentes para a estrutura da faixa de faixas.

> [!Note]  
> As [diretrizes de experiência do usuário da faixa](https://msdn.microsoft.com/library/cc872782.aspx) de ver devem ser revisadas para determinar se o aplicativo é um candidato adequado para uma interface do usuário da faixa de faixas.

 

## <a name="design-the-ribbon-layout"></a>Criar o layout da faixa de opção

Possíveis designs de interface do usuário da faixa de opção e layouts de controle podem ser identificados executando estas etapas:

1.  Fazendo o inventário de todas as funcionalidades existentes.
2.  Convertendo essa funcionalidade em comandos da faixa de das.
3.  Organizando os comandos em grupos lógicos.

### <a name="take-inventory"></a>Fazer inventário

Na estrutura da faixa de visão, a funcionalidade exposta por um aplicativo que manipula o estado ou a exibição de um espaço de trabalho ou documento é considerada um comando. O que constitui um comando pode variar e depende da natureza e do domínio do aplicativo existente.

A tabela a seguir lista um conjunto de comandos básicos para um aplicativo de edição de texto hipotético:



| Símbolo           | ID     | Descrição               |
|------------------|--------|---------------------------|
| \_novo arquivo de ID \_    | 0xE100 | Novo documento              |
| \_salvar arquivo de ID \_   | 0xE103 | Salvar documento             |
| \_salvar arquivo de ID \_ | 0xE104 | Salvar como... '       |
| arquivo de ID \_ \_ aberto   | 0xE101 | Abrir... '          |
| \_saída do arquivo de ID \_   | 0xE102 | Sair do aplicativo      |
| \_desfazer edição de ID \_   | 0xE12B | Desfazer                      |
| edição de ID \_ \_ recortada    | 0xE123 | Recortar texto selecionado         |
| ID \_ Editar \_ cópia   | 0xE122 | Copiar texto selecionado        |
| \_Editar \_ colar ID  | 0xE125 | Colar texto da área de transferência |
| edição de ID \_ \_ limpar  | 0xE120 | Excluir texto selecionado      |
| \_zoom da exibição de ID \_   | 1242   | Aplicar zoom... '          |



 

Olhe além dos menus e barras de ferramentas existentes ao criar um inventário de comandos. Considere todas as maneiras como um usuário pode interagir com o espaço de trabalho. Embora nem todos os comandos sejam adequados para inclusão na faixa de faixas, esse exercício pode expor comandos que foram anteriormente obscurecidos por camadas de interface do usuário.

### <a name="translate"></a>Translate

Nem todos os comandos precisam ser representados na interface do usuário da faixa de para. Por exemplo, inserir texto, alterar uma seleção, rolar ou mover o ponto de inserção com o mouse tudo qualificado como comandos no editor de texto hipotético, no entanto, eles não são adequados para expor em uma barra de comandos, pois cada um envolve uma interação direta com a interface do usuário do aplicativo.

Por outro lado, algumas funcionalidades podem não ser consideradas como um comando no sentido tradicional. Por exemplo, em vez de ser ocultado em uma caixa de diálogo, os ajustes de margem da página da impressora podem ser representados na faixa de bits como um grupo de controles Spinner em uma guia contextual ou no [modo de aplicativo](ribbon-applicationmodes.md).

> [!Note]  
> Anote a ID numérica que pode ser atribuída a cada comando. Algumas estruturas de interface do usuário, como MFC (MFC), definem IDs para comandos como o menu arquivo e editar (0xE100 para 0xE200).

 

### <a name="organize"></a>Organizar

Antes de tentar organizar o inventário de comandos, as [diretrizes de experiência do usuário da faixa](https://msdn.microsoft.com/library/cc872782.aspx) de opções devem ser examinadas para obter as práticas recomendadas ao implementar uma interface do usuário da faixa.

Em geral, as seguintes regras podem ser aplicadas à organização de comando da faixa de opções:

-   Os comandos que operam no arquivo ou o aplicativo geral provavelmente pertencem ao [menu do aplicativo](windowsribbon-controls-applicationmenu.md).
-   Comandos usados com frequência, como recortar, copiar e colar (como no exemplo do editor de texto) normalmente são colocados em uma guia página inicial padrão. Em aplicativos mais complexos, eles podem estar duplicados em outro lugar na interface do usuário da faixa de faixas.
-   Os comandos importantes ou frequentemente usados podem garantir a inclusão padrão na [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md).

A estrutura da faixa de visão também fornece controles ContextMenu e Minibarra por meio da exibição ContextPopup. Esses recursos não são obrigatórios, mas se seu aplicativo tiver um ou mais menus de contexto existentes, a migração dos comandos que eles contêm poderá permitir a reutilização da base de código existente com associação automática a recursos existentes.

Como cada aplicativo é diferente, leia as diretrizes e tente aplicá-los à extensão mais completa possível. Uma das metas da estrutura da faixa de faixas é fornecer uma experiência do usuário familiar e consistente, e esse objetivo será mais atingível se os designs de novos aplicativos espelharem os aplicativos da faixa de das faixas de uma forma mais bem possível.

## <a name="adapt-your-code"></a>Adapte seu código

Depois que os comandos da faixa de faixas forem identificados e organizados em agrupamentos lógicos, o número de etapas envolvidas na incorporação da estrutura da faixa de das faixas ao código do aplicativo existente dependerá da complexidade do aplicativo original. Em geral, há três etapas básicas:

-   Crie a marcação da faixa de opção com base na organização de comandos e na especificação de layout.
-   Substitua o menu herdado e a funcionalidade da barra de ferramentas com a funcionalidade da faixa de
-   Implemente um adaptador IUICommandHandler.

### <a name="create-the-markup"></a>Criar a marcação

A lista de comandos, bem como sua organização e layout, são declarados por meio do arquivo de marcação da faixa de opção que é consumido pelo [compilador de marcação da faixa](windowsribbon-intentcl.md)de lista.

> [!Note]  
> Muitas das etapas necessárias para adaptar um aplicativo existente são semelhantes às necessárias para iniciar um novo aplicativo da faixa de tipos. Para obter mais informações, consulte o tutorial [criando um aplicativo da faixa de Ribbon](windowsribbon-stepbystep.md) para um novo aplicativo da faixa de faixas.

 

Há duas seções principais para a marcação da faixa de faixas. A primeira seção é um manifesto de comandos e seus recursos associados (cadeias de caracteres e imagens). A segunda seção especifica a estrutura e o posicionamento dos controles na faixa de faixas.

A marcação para o editor de texto simples pode ser semelhante ao exemplo a seguir:

> [!Note]  
> Os recursos de imagem e de cadeia de caracteres são abordados posteriormente neste artigo.

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



Para evitar a redefinição de símbolos que são definidos por uma estrutura de interface do usuário, como o MFC, o exemplo anterior usa nomes de símbolo ligeiramente diferentes para cada comando (arquivo de ID \_ \_ novo versus ID \_ cmd \_ novo). No entanto, a ID numérica atribuída a cada comando deve permanecer a mesma.

Para integrar o arquivo de marcação em um aplicativo, configure uma etapa de compilação personalizada para executar o compilador de marcação da faixa de UICC.exe. Os arquivos de cabeçalho e de recurso resultantes são então incorporados ao projeto existente. Se o aplicativo de faixa de opções do editor de texto de exemplo for denominado "RibbonPad", uma linha de comando de compilação personalizada semelhante à seguinte será necessária:


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



O compilador de marcação cria um arquivo binário, um arquivo de cabeçalho (H) e um arquivo de recurso (RC). Como o aplicativo existente provavelmente tem um arquivo RC existente, inclua os arquivos H e RC gerados nesse arquivo RC, conforme mostrado no exemplo a seguir:


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a>Substituir menus herddos e barras de ferramentas

A substituição de menus e barras de ferramentas padrão por uma faixa de opções em um aplicativo herdados requer o seguinte:

1.  Remova referências de recursos de barra de ferramentas e menu do arquivo de recurso do aplicativo.
2.  Exclua todo o código de inicialização da barra de ferramentas e da barra de menus.
3.  Exclua qualquer código usado para anexar uma barra de ferramentas ou barra de menus à janela de nível superior do aplicativo.
4.  Insinue a estrutura da Faixa de Opções.
5.  Anexe a faixa de opções à janela de nível superior do aplicativo.
6.  Carregue a marcação compilada.

> [!IMPORTANT]
> As tabelas de atalho de teclado e barra de status existentes devem ser preservadas, pois a estrutura da Faixa de Opções não substitui esses recursos.

 

O exemplo a seguir demonstra como inicializar a estrutura usando [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



O exemplo a seguir demonstra como usar [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para carregar a marcação compilada:


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



A classe CApplication, mencionada acima, deve implementar um par de interfaces COM (Component Object Model) definidas pela estrutura ribbon: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) e [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).

[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) fornece a interface de retorno de chamada principal entre a estrutura e o aplicativo (por exemplo, a altura da faixa de opções é comunicada por meio de [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) enquanto os retornos de chamada para comandos individuais são fornecidos em resposta a [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).

**Dica:** Algumas estruturas de aplicativo, como MFC, exigem que a altura da barra de faixa de opções seja levada em conta ao renderizar o espaço do documento do aplicativo. Nesses casos, a adição de uma janela oculta para sobrepor a barra de faixa de opções e forçar o espaço do documento à altura desejada é necessária. Para obter um exemplo dessa abordagem, em que uma função de layout é chamada com base na altura da faixa de opções retornada pelo método [**IUIRibbon::GetHeight,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) consulte [HtmlEditRibbon Sample](windowsribbon-htmleditribbonsample.md).

O exemplo de código a seguir demonstra uma [**implementação IUIApplication::OnViewChanged:**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a>Implementar um adaptador IUICommandHandler

Dependendo do design do aplicativo original, pode ser mais fácil ter várias implementações de manipulador de comando ou um único manipulador de comando de ponte que invoca a lógica de comando existing-application. Muitos aplicativos usam mensagens WM COMMAND para essa finalidade, em que é suficiente fornecer um único manipulador de comandos de finalidade geral que simplesmente encaminha mensagens WM COMMAND para a janela de nível \_ \_ superior.

No entanto, essa abordagem requer tratamento especial para comandos como **Sair** ou **Fechar**. Como a Faixa de Opções não pode ser destruída durante o processamento de uma mensagem de janela, a mensagem WM CLOSE deve ser postada no thread da interface do usuário do aplicativo e não deve ser processada de forma síncrona, conforme mostrado no exemplo a \_ seguir:


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a>Migrando recursos

Quando o manifesto de comandos tiver sido definido, a estrutura da Faixa de Opções tiver sido declarada e o código do aplicativo for adaptado para hospedar a estrutura da Faixa de Opções, a etapa final será a especificação de recursos de cadeia de caracteres e imagem para cada comando.

> [!Note]  
> Recursos de cadeia de caracteres e imagem normalmente são fornecidos no arquivo de marcação. No entanto, eles podem ser gerados ou substituídos programaticamente implementando o método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

 

### <a name="string-resources"></a>Recursos de cadeia de caracteres

[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) é a propriedade de cadeia de caracteres mais comum definida para um Comando. Eles são renderizados como rótulos de texto para guias, grupos e controles individuais. Uma cadeia de caracteres de rótulo de um item de menu herdado normalmente pode ser rea usada para **um Command.LabelTitle** sem muita edição.

No entanto, as convenções a seguir foram alteradas com o advento da Faixa de Opções:

-   O sufixo de reellips (...), usado para indicar um comando de início de caixa de diálogo, não é mais necessário.
-   O e ampersand (&) ainda pode ser usado para indicar um atalho de teclado para um Comando que aparece em um menu, mas a propriedade [**Command.Keytip**](windowsribbon-element-command-keytip.md) com suporte pela estrutura atende a uma finalidade semelhante.

Fazendo referência ao exemplo do editor de texto, as seguintes cadeias de caracteres para LabelTitle e Keytip podem ser especificadas:



| Símbolo           | Cadeia de caracteres original | Cadeia de caracteres LabelTitle | Cadeia de caracteres de dica de chave |
|------------------|-----------------|-------------------|---------------|
| ARQUIVO DE ID \_ \_ NOVO    | &novo            | &novo              | N             |
| ID \_ FILE \_ SAVE   | &salvar           | &salvar             | S             |
| ARQUIVO DE ID \_ \_ SAVEAS | Salvar &como...       | Salvar &como          | Um             |
| ARQUIVO DE ID \_ \_ ABERTO   | &Abrir...          | &amp;Open             | O             |
| SAÍDA DO ARQUIVO DE ID \_ \_   | Sa&ir           | Sa&ir             | X             |
| ID \_ EDIT \_ UNDO   | &Desfazer           | Desfazer              | Z             |
| ID \_ EDIT \_ CUT    | Cu&t            | Cu&t              | X             |
| ID \_ EDITAR \_ CÓPIA   | &cópia           | &cópia             | C             |
| ID \_ EDITAR \_ COLAR  | &colar          | &colar            | V             |
| ID \_ EDIT \_ CLEAR  | &excluir         | &excluir           | D             |
| ZOOM DE \_ EXIBIÇÃO DE ID \_   | &Zoom...          | Zoom              | Z             |



 

Veja a seguir uma lista de outras propriedades de cadeia de caracteres que devem ser definidas na maioria dos Comandos:

-   [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)
-   [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
-   [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)

Guias, Grupos e outros recursos de interface do usuário da Faixa de Opções agora podem ser declarados com todos os recursos de cadeia de caracteres e imagem especificados.

O exemplo de marcação faixa de opções a seguir demonstra vários recursos de cadeia de caracteres:


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a>Recursos de imagem

A estrutura da Faixa de Opções dá suporte a formatos de imagem que fornecem uma aparência muito mais rica do que os formatos de imagem compatíveis com os componentes anteriores do menu e da barra de ferramentas.

Para Windows 8 posteriores, a estrutura ribbon dá suporte aos seguintes formatos gráficos: arquivos BMP (bitmap ARGB) de 32 bits e arquivos PNG (Gráficos de Rede Portátil) com transparência.

Por Windows 7 e anteriores, os recursos de imagem devem estar em conformidade com o formato gráfico BMP padrão usado Windows.

> [!Note]  
> Arquivos de imagem existentes podem ser convertidos em qualquer formato. No entanto, os resultados poderão ser menores que satisfatórios se os arquivos de imagem não deem suporte a antialiasing e transparência.

 

Não é possível especificar um único tamanho padrão para recursos de imagem na estrutura da Faixa de Opções. No entanto, para dar [suporte ao layout adaptável](windowsribbon-templates.md) de controles, as imagens podem ser especificadas em dois tamanhos (grande e pequeno). Todas as imagens na estrutura da Faixa de Opções são dimensionadas de acordo com a resolução dpi (pontos por polegada) da exibição com o tamanho renderizado exato dependendo dessa configuração de dpi. Consulte [Especificando recursos de imagem da faixa de opções](windowsribbon-imageformats.md) para obter mais informações.

O exemplo a seguir demonstra como um conjunto de imagens específicas de dpi é referenciado na marcação:


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando recursos de imagem da faixa de opções](windowsribbon-imageformats.md)
</dt> </dl>

 

 