---
title: Barra de ferramentas de acesso rápido
description: A barra de ferramentas de acesso rápido (QAT) é uma barra de ferramentas pequena e personalizável que expõe um conjunto de comandos que são especificados pelo aplicativo ou selecionados pelo usuário.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007565"
---
# <a name="quick-access-toolbar"></a><span data-ttu-id="ee882-103">Barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="ee882-103">Quick Access Toolbar</span></span>

<span data-ttu-id="ee882-104">A barra de ferramentas de acesso rápido (QAT) é uma barra de ferramentas pequena e personalizável que expõe um conjunto de comandos que são especificados pelo aplicativo ou selecionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ee882-104">The Quick Access Toolbar (QAT) is a small, customizable toolbar that exposes a set of Commands that are specified by the application or selected by the user.</span></span>

- [<span data-ttu-id="ee882-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="ee882-105">Introduction</span></span>](#introduction)
- [<span data-ttu-id="ee882-106">Implementar a barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="ee882-106">Implement the Quick Access Toolbar</span></span>](#implement-the-quick-access-toolbar)
  - [<span data-ttu-id="ee882-107">Marcação</span><span class="sxs-lookup"><span data-stu-id="ee882-107">Markup</span></span>](#markup)
  - [<span data-ttu-id="ee882-108">Código</span><span class="sxs-lookup"><span data-stu-id="ee882-108">Code</span></span>](#code)
- [<span data-ttu-id="ee882-109">Persistência de QAT</span><span class="sxs-lookup"><span data-stu-id="ee882-109">QAT Persistence</span></span>](#qat-persistence)
- [<span data-ttu-id="ee882-110">Propriedades da barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="ee882-110">Quick Access Toolbar Properties</span></span>](#quick-access-toolbar-properties)
- [<span data-ttu-id="ee882-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee882-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="ee882-112">Introdução</span><span class="sxs-lookup"><span data-stu-id="ee882-112">Introduction</span></span>

<span data-ttu-id="ee882-113">Por padrão, a barra de ferramentas de acesso rápido (QAT) está localizada na barra de título da janela do aplicativo, mas pode ser configurada para ser exibida abaixo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="ee882-113">By default, the Quick Access Toolbar (QAT) is located in the title bar of the application window but can be configured to display below the ribbon.</span></span> <span data-ttu-id="ee882-114">Além de expor comandos, a barra de ferramentas de acesso rápido (QAT) também inclui um menu suspenso personalizável que contém o conjunto completo de comandos de QAT (barra de ferramentas de acesso rápido) padrão (se ocultos ou exibidos na barra de ferramentas de acesso rápido (QAT)) e um conjunto de opções de barra de ferramentas de acesso rápido (QAT) e de faixa.</span><span class="sxs-lookup"><span data-stu-id="ee882-114">In addition to exposing Commands, the Quick Access Toolbar (QAT) also includes a customizable drop-down menu that contains the complete set of default Quick Access Toolbar (QAT) Commands (whether hidden or displayed in the Quick Access Toolbar (QAT)) and a set of Quick Access Toolbar (QAT) and ribbon options.</span></span>

<span data-ttu-id="ee882-115">A captura de tela a seguir mostra um exemplo da barra de ferramentas de acesso rápido da faixa de opções (QAT).</span><span class="sxs-lookup"><span data-stu-id="ee882-115">The following screen shot shows an example of the Ribbon Quick Access Toolbar (QAT).</span></span>

![captura de tela do qat na faixa de faixas do Microsoft Paint.](images/markup/qat-and-menu.png)

<span data-ttu-id="ee882-117">A barra de ferramentas de acesso rápido (QAT) consiste em uma combinação de até 20 comandos especificados pelo aplicativo (conhecido como a lista de padrões do aplicativo) ou selecionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ee882-117">The Quick Access Toolbar (QAT) consists of a combination of up to 20 Commands either specified by the application (known as the application defaults list) or selected by the user.</span></span> <span data-ttu-id="ee882-118">A barra de ferramentas de acesso rápido (QAT) pode conter comandos exclusivos que não estão disponíveis em outro lugar na interface do usuário da faixa de guia.</span><span class="sxs-lookup"><span data-stu-id="ee882-118">The Quick Access Toolbar (QAT) can contain unique Commands that are not available elsewhere in the ribbon UI.</span></span>

> [!Note]
> <span data-ttu-id="ee882-119">Embora quase todos os controles de faixa de opções permitam que seu comando associado seja adicionado à barra de ferramentas de acesso rápido (QAT) por meio do menu de contexto mostrado na captura de tela a seguir, os comandos expostos em um [Popup de contexto](windowsribbon-controls-contextpopup.md) não fornecem esse menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="ee882-119">While almost all ribbon controls allow their associated Command to be added to the Quick Access Toolbar (QAT) through the context menu shown in the following screen shot, Commands exposed in a [Context Popup](windowsribbon-controls-contextpopup.md) do not provide this context menu.</span></span>
>
> ![captura de tela do menu de contexto do comando na faixa de faixas do Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a><span data-ttu-id="ee882-121">Implementar a barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="ee882-121">Implement the Quick Access Toolbar</span></span>

<span data-ttu-id="ee882-122">Assim como todos os controles de estrutura da faixa de opções do Windows, aproveitar ao máximo a barra de ferramentas de acesso rápido (QAT) requer um componente de marcação que controla sua apresentação na faixa de opções e um componente de código que governa sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="ee882-122">As with all Windows Ribbon framework controls, taking full advantage of the Quick Access Toolbar (QAT) requires both a markup component that controls its presentation within the ribbon and a code component that governs its functionality.</span></span>

### <a name="markup"></a><span data-ttu-id="ee882-123">Marcação</span><span class="sxs-lookup"><span data-stu-id="ee882-123">Markup</span></span>

<span data-ttu-id="ee882-124">O controle de barra de ferramentas de acesso rápido (QAT) é declarado e associado a uma ID de comando, na marcação por meio do elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="ee882-124">The Quick Access Toolbar (QAT) control is declared, and associated with a Command ID, in markup through the [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span> <span data-ttu-id="ee882-125">A ID de comando é usada para identificar e associar a barra de ferramentas de acesso rápido (QAT) a um manipulador de comandos definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee882-125">The Command ID is used to identify and bind the Quick Access Toolbar (QAT) to a Command handler defined by the application.</span></span>

<span data-ttu-id="ee882-126">Além do manipulador de comando básico para a funcionalidade principal de barra de ferramentas de acesso rápido (QAT), declarar o atributo de elemento opcional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) faz com que a estrutura adicione um item de **mais comandos** à lista de comandos do menu suspenso qat (barra de ferramentas de acesso rápido) que exige a definição de um manipulador de comandos secundário.</span><span class="sxs-lookup"><span data-stu-id="ee882-126">In addition to the basic Command handler for primary Quick Access Toolbar (QAT) functionality, declaring the optional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element attribute causes the framework to add a **More Commands** item to the Command list of the Quick Access Toolbar (QAT) drop-down menu that requires a secondary Command handler be defined.</span></span>

<span data-ttu-id="ee882-127">Para fins de consistência em aplicativos de faixa de ferramentas, é recomendável que o manipulador de comandos *CustomizeCommandName* inicie uma caixa de diálogo de personalização de barra de acesso rápido (qat).</span><span class="sxs-lookup"><span data-stu-id="ee882-127">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a Quick Access Toolbar (QAT) customization dialog.</span></span> <span data-ttu-id="ee882-128">Como a estrutura da faixa de faixas fornece apenas o ponto de partida na interface do usuário, o aplicativo é exclusivamente responsável por fornecer a implementação da caixa de diálogo de personalização quando a notificação de retorno de chamada para esse comando é recebida.</span><span class="sxs-lookup"><span data-stu-id="ee882-128">Because the Ribbon framework only provides the launching point in the UI, the application is solely responsible for providing the customization dialog implementation when the callback notification for this Command is received.</span></span>

<span data-ttu-id="ee882-129">A captura de tela a seguir mostra um menu suspenso de barra de ferramentas de acesso rápido (QAT) com o item de comando **mais comandos** .</span><span class="sxs-lookup"><span data-stu-id="ee882-129">The following screen shot shows a Quick Access Toolbar (QAT) drop-down menu with the **More Commands** Command item.</span></span>

![captura de tela de um menu qat com mais comandos... item de comando.](images/markup/qat-customizecommandname.png)

<span data-ttu-id="ee882-131">A lista de padrões do aplicativo para a barra de ferramentas de acesso rápido (QAT) é especificada por meio da propriedade [QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , que identifica uma lista padrão de comandos recomendados, todos listados no menu suspenso barra de ferramentas de acesso rápido (qat).</span><span class="sxs-lookup"><span data-stu-id="ee882-131">The application defaults list for the Quick Access Toolbar (QAT) is specified through the [QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) property which identifies a default list of recommended Commands, all of which are listed in the Quick Access Toolbar (QAT) drop-down menu.</span></span>

<span data-ttu-id="ee882-132">Para exibir comandos da lista de padrões do aplicativo na barra de ferramentas de acesso rápido (QAT), o atributo *ApplicationDefaults. IsChecked* de cada elemento de controle deve ter um valor de `true` .</span><span class="sxs-lookup"><span data-stu-id="ee882-132">To display Commands from the application defaults list in the Quick Access Toolbar (QAT) toolbar, the *ApplicationDefaults.IsChecked* attribute of each control element must have a value of `true`.</span></span> <span data-ttu-id="ee882-133">As imagens anteriores mostram os resultados da definição desse atributo como `true` para os comandos **salvar**, **desfazer** e **refazer** .</span><span class="sxs-lookup"><span data-stu-id="ee882-133">The preceding images show the results of setting this attribute to `true` for the **Save**, **Undo**, and **Redo** Commands.</span></span>

<span data-ttu-id="ee882-134">[QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) dá suporte a três tipos de controles de faixa de opção: [botão](windowsribbon-controls-button.md), [botão de alternância](windowsribbon-controls-togglebutton.md)e [caixa de seleção](windowsribbon-controls-checkbox.md).</span><span class="sxs-lookup"><span data-stu-id="ee882-134">[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supports three types of Ribbon controls: [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), and [Check Box](windowsribbon-controls-checkbox.md).</span></span>

> [!Note]
> <span data-ttu-id="ee882-135">Windows 8 e mais recente: há suporte para todos os controles baseados na galeria ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)e [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span><span class="sxs-lookup"><span data-stu-id="ee882-135">Windows 8 and newer: All gallery-based controls are supported ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md), and [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span></span>
>
> <span data-ttu-id="ee882-136">Os itens em um controle Galeria podem dar suporte ao realce ao focalizar.</span><span class="sxs-lookup"><span data-stu-id="ee882-136">Items in a gallery control can support highlighting on hover.</span></span> <span data-ttu-id="ee882-137">Para dar suporte ao realce de foco, a Galeria deve ser uma galeria de itens e usar um [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) do tipo [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span><span class="sxs-lookup"><span data-stu-id="ee882-137">To support hover highlighting, the gallery must be an items gallery and use a [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) of type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span></span>

<span data-ttu-id="ee882-138">O exemplo a seguir demonstra a marcação básica para um elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="ee882-138">The following example demonstrates the basic markup for a [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

<span data-ttu-id="ee882-139">Esta seção de código mostra as declarações de comando para um elemento de [barra de ferramentas de acesso rápido (qat)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="ee882-139">This section of code shows the Command declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

<span data-ttu-id="ee882-140">Esta seção de código mostra as declarações de controle para um elemento de [barra de ferramentas de acesso rápido (qat)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="ee882-140">This section of code shows the control declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a><span data-ttu-id="ee882-141">Código</span><span class="sxs-lookup"><span data-stu-id="ee882-141">Code</span></span>

<span data-ttu-id="ee882-142">O aplicativo da estrutura da faixa de ferramentas deve fornecer um método de retorno de chamada do manipulador de comandos para manipular a barra de ferramentas de acesso rápido (QAT)</span><span class="sxs-lookup"><span data-stu-id="ee882-142">The Ribbon framework application must provide a Command handler callback method to manipulate the Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="ee882-143">Esse manipulador funciona de maneira semelhante aos manipuladores da Galeria de comandos, exceto que a barra de ferramentas de acesso rápido (QAT) não oferece suporte a categorias.</span><span class="sxs-lookup"><span data-stu-id="ee882-143">This handler works in a similar fashion to Command gallery handlers, except that the Quick Access Toolbar (QAT) does not support categories.</span></span> <span data-ttu-id="ee882-144">Para obter mais informações, consulte [trabalhando com galerias](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="ee882-144">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="ee882-145">A coleção de comandos da barra de ferramentas de acesso rápido (QAT) é recuperada como um objeto [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por meio da chave de propriedade [ \_ \_ ItemsSource da interface do usuário PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="ee882-145">The Quick Access Toolbar (QAT) Command collection is retrieved as an [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span> <span data-ttu-id="ee882-146">Adicionar comandos à barra de ferramentas de acesso rápido (QAT) em tempo de execução é feito adicionando um objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) ao **IUICollection**.</span><span class="sxs-lookup"><span data-stu-id="ee882-146">Adding Commands to the Quick Access Toolbar (QAT) at run time is accomplished by adding an [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object to the **IUICollection**.</span></span>

<span data-ttu-id="ee882-147">Diferentemente de galerias de comandos, uma propriedade de tipo de comando ([ \_ \_ CommandType PKEY de interface do usuário](windowsribbon-reference-properties-uipkey-commandtype.md)) não é necessária para o objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) da barra de ferramentas de acesso rápido (qat).</span><span class="sxs-lookup"><span data-stu-id="ee882-147">Unlike Command galleries, a command type property ([UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) is not required for the Quick Access Toolbar (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object.</span></span> <span data-ttu-id="ee882-148">No entanto, o comando deve existir na lista de padrões da faixa de ferramentas ou do aplicativo de acesso rápido (QAT); um novo comando não pode ser criado em tempo de execução e adicionado à barra de ferramentas de acesso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="ee882-148">However, the Command must exist in the ribbon or Quick Access Toolbar (QAT) application defaults list; a new Command cannot be created at run time and added to the Quick Access Toolbar (QAT).</span></span>

> [!Note]  
> <span data-ttu-id="ee882-149">O aplicativo da faixa de faixas não pode substituir a barra de ferramentas de acesso rápido (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por um objeto de coleção personalizado derivado de IEnumUnknown.</span><span class="sxs-lookup"><span data-stu-id="ee882-149">The Ribbon application cannot replace the Quick Access Toolbar (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) with a custom collection object derived from IEnumUnknown.</span></span>

<span data-ttu-id="ee882-150">O exemplo a seguir demonstra uma implementação de manipulador de comando de QAT (barra de ferramentas de acesso rápido) básica.</span><span class="sxs-lookup"><span data-stu-id="ee882-150">The following example demonstrates a basic Quick Access Toolbar (QAT) Command handler implementation.</span></span>

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a><span data-ttu-id="ee882-151">Persistência de QAT</span><span class="sxs-lookup"><span data-stu-id="ee882-151">QAT Persistence</span></span>

<span data-ttu-id="ee882-152">Os itens de comando e as configurações da barra de ferramentas de acesso rápido (QAT) podem ser persistidos entre sessões de aplicativo usando as funções [IUIRibbon:: SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e [IUIRibbon:: LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="ee882-152">Quick Access Toolbar (QAT) Command items and settings can be persisted across application sessions using the [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) and [IUIRibbon::LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) functions.</span></span> <span data-ttu-id="ee882-153">Para obter mais informações, consulte [Persisteting State](ribbon-statepersistence.md).</span><span class="sxs-lookup"><span data-stu-id="ee882-153">For more information, see [Persisting Ribbon State](ribbon-statepersistence.md).</span></span>

## <a name="quick-access-toolbar-properties"></a><span data-ttu-id="ee882-154">Propriedades da barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="ee882-154">Quick Access Toolbar Properties</span></span>

<span data-ttu-id="ee882-155">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de barra de ferramentas de acesso rápido (qat).</span><span class="sxs-lookup"><span data-stu-id="ee882-155">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Quick Access Toolbar (QAT) control.</span></span>

<span data-ttu-id="ee882-156">Normalmente, uma propriedade de barra de ferramentas de acesso rápido (QAT) é atualizada na interface do usuário da faixa de modo invalidando o comando associado ao controle por meio de uma chamada para o método [IUIFramework:: InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="ee882-156">Typically, a Quick Access Toolbar (QAT) property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [IUIFramework::InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="ee882-157">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [IUICommandHandler:: updateproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="ee882-157">The invalidation event is handled, and the property updates defined, by the [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="ee882-158">O método de retorno de chamada [IUICommandHandler:: updateproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="ee882-158">The [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="ee882-159">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="ee882-159">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="ee882-160">Em alguns casos, uma propriedade pode ser recuperada por meio do método [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="ee882-160">In some cases, a property can be retrieved through the [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

<span data-ttu-id="ee882-161">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de barra de ferramentas de acesso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="ee882-161">The following table lists the property keys that are associated with the Quick Access Toolbar (QAT) control.</span></span>

| <span data-ttu-id="ee882-162">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="ee882-162">Property Key</span></span> | <span data-ttu-id="ee882-163">Observações</span><span class="sxs-lookup"><span data-stu-id="ee882-163">Notes</span></span> |
|---|---|
| [<span data-ttu-id="ee882-164">IU \_ PKEY \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="ee882-164">UI\_PKEY\_ItemsSource</span></span>](windowsribbon-reference-properties-uipkey-itemssource.md) | <span data-ttu-id="ee882-165">Dá suporte a [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (não dá suporte a [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) retorna um ponteiro para um objeto IUICollection que representa os comandos no qat.</span><span class="sxs-lookup"><span data-stu-id="ee882-165">Supports [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (does not support [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)).[IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) returns a pointer to an IUICollection object that represents the commands in the QAT.</span></span> <span data-ttu-id="ee882-166">Cada comando é identificado por sua ID de comando, que é obtida chamando o método [IUISimplePropertySet:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) e passando a interface de usuário da chave de propriedade [ \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md).</span><span class="sxs-lookup"><span data-stu-id="ee882-166">Each Command is identified by its Command ID, which is obtained by calling the [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method and passing in the property key [UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md).</span></span> |

<span data-ttu-id="ee882-167">Não há nenhuma chave de propriedade associada ao item de comando **mais comandos** do menu suspenso da barra de ferramentas de acesso rápido (qat)</span><span class="sxs-lookup"><span data-stu-id="ee882-167">There are no property keys associated with the **More Commands** Command item of the Quick Access Toolbar (QAT) drop-down menu</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee882-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee882-168">Related topics</span></span>

- [<span data-ttu-id="ee882-169">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="ee882-169">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
- [<span data-ttu-id="ee882-170">Elemento de marcação QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="ee882-170">QuickAccessToolbar markup element</span></span>](windowsribbon-element-quickaccesstoolbar.md)