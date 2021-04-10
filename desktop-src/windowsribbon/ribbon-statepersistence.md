---
title: Estado da faixa de medida persistente
description: O Windows Ribon Framework (faixa de opções) fornece a capacidade de preservar o estado de uma variedade de configurações de usuário e preferências entre sessões de aplicativos.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294269"
---
# <a name="persisting-ribbon-state"></a><span data-ttu-id="1bee8-103">Estado da faixa de medida persistente</span><span class="sxs-lookup"><span data-stu-id="1bee8-103">Persisting Ribbon State</span></span>

<span data-ttu-id="1bee8-104">O Windows Ribon Framework (faixa de opções) fornece a capacidade de preservar o estado de uma variedade de configurações de usuário e preferências entre sessões de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1bee8-104">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

-   [<span data-ttu-id="1bee8-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="1bee8-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="1bee8-106">Uma experiência previsível</span><span class="sxs-lookup"><span data-stu-id="1bee8-106">A Predictable Experience</span></span>](#a-predictable-experience)
-   [<span data-ttu-id="1bee8-107">Salvar configurações da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="1bee8-107">Save Ribbon Settings</span></span>](#save-ribbon-settings)
-   [<span data-ttu-id="1bee8-108">Carregar configurações da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="1bee8-108">Load Ribbon Settings</span></span>](#load-ribbon-settings)
-   [<span data-ttu-id="1bee8-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bee8-109">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="1bee8-110">Introdução</span><span class="sxs-lookup"><span data-stu-id="1bee8-110">Introduction</span></span>

<span data-ttu-id="1bee8-111">Vários aspectos de uma faixa de opções, incluindo preferências de configuração e interação, podem ser personalizados por um usuário em tempo de execução para melhorar a usabilidade e a produtividade.</span><span class="sxs-lookup"><span data-stu-id="1bee8-111">Various aspects of a ribbon, including configuration and interaction preferences, can be customized by a user at run time to improve usability and productivity.</span></span> <span data-ttu-id="1bee8-112">A estrutura da faixa de opções fornece a funcionalidade para preservar essas configurações em sessões de aplicativos por meio de dois métodos definidos na implementação da interface [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) e [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span><span class="sxs-lookup"><span data-stu-id="1bee8-112">The Ribbon framework provides the functionality to preserve these settings across application sessions through two methods defined in the implementation of the [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) interface: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) and [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span></span>

## <a name="a-predictable-experience"></a><span data-ttu-id="1bee8-113">Uma experiência previsível</span><span class="sxs-lookup"><span data-stu-id="1bee8-113">A Predictable Experience</span></span>

<span data-ttu-id="1bee8-114">As [diretrizes de experiência do usuário da faixa](https://msdn.microsoft.com/library/cc872782.aspx) de guia aconselham que, para fornecer a experiência de usuário mais previsível possível, os aplicativos de faixa de das faixas devem preservar o estado da faixa de faixas (além da última guia selecionada) à medida que o aplicativo é fechado.</span><span class="sxs-lookup"><span data-stu-id="1bee8-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) advise that, to provide the most predictable user experience possible, Ribbon applications should preserve the state of the ribbon (aside from the last selected tab) as the application is closed.</span></span> <span data-ttu-id="1bee8-115">Dessa forma, quando o mesmo aplicativo é iniciado, as configurações e personalizações da sessão anterior podem ser restauradas e o usuário pode esperar continuar interagindo com o aplicativo da mesma maneira que o deixou.</span><span class="sxs-lookup"><span data-stu-id="1bee8-115">In this way, when the same application is launched, the settings and customizations from the previous session can be restored and the user can expect to continue interacting with the application in the same way as they left it.</span></span>

<span data-ttu-id="1bee8-116">As configurações da faixa de opções que podem ser modificadas em tempo de execução e preservadas entre sessões de aplicativo são listadas no menu de contexto do comando.</span><span class="sxs-lookup"><span data-stu-id="1bee8-116">Ribbon settings that can be modified at run time and preserved across application sessions are listed in the Command context menu.</span></span> <span data-ttu-id="1bee8-117">Entre elas estão:</span><span class="sxs-lookup"><span data-stu-id="1bee8-117">They include:</span></span>

-   <span data-ttu-id="1bee8-118">Comandos adicionados à lista de comandos da [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1bee8-118">Commands added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) Command list by the user.</span></span> <span data-ttu-id="1bee8-119">Especificado por um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por meio da chave de propriedade [ \_ PKEY \_ ItemsSource da interface do usuário](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-119">Specified by an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span>

    <span data-ttu-id="1bee8-120">A captura de tela a seguir mostra o comando adicionar ao menu de contexto **da barra de ferramentas de acesso rápido** .</span><span class="sxs-lookup"><span data-stu-id="1bee8-120">The following screen shot shows the **Add to Quick Access Toolbar** context menu Command.</span></span>

    ![captura de tela do menu de contexto do comando na faixa de faixas do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   <span data-ttu-id="1bee8-122">O estado de encaixe da [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) preferencial.</span><span class="sxs-lookup"><span data-stu-id="1bee8-122">The preferred [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) docking state.</span></span> <span data-ttu-id="1bee8-123">Especificado pelo valor [**de \_ CONTROLDOCK da interface**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) do usuário da chave de propriedade [ \_ PKEY \_ QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-123">Specified by the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) value of the [UI\_PKEY\_QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) property key.</span></span>

    <span data-ttu-id="1bee8-124">Esta captura de tela mostra a [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) em seu local da barra de título do aplicativo padrão e a **barra de ferramentas mostrar acesso rápido abaixo do comando do menu de contexto da faixa de da**</span><span class="sxs-lookup"><span data-stu-id="1bee8-124">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) in its default application title bar location and the **Show Quick Access Toolbar below the Ribbon** context menu Command.</span></span>

    ![captura de tela do menu de contexto do comando na faixa de faixas do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="1bee8-126">Esta captura de tela mostra a [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) abaixo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="1bee8-126">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) below the ribbon.</span></span>

    ![captura de tela da barra de ferramentas de acesso rápido encaixada abaixo da faixa de faixas.](images/controls/qat-dockbottom.png)

-   <span data-ttu-id="1bee8-128">O estado da faixa de faixas minimizada conforme especificado pelo valor booliano da chave de propriedade [ \_ PKEY \_ minimizada da interface do usuário](windowsribbon-reference-properties-uipkey-minimized.md) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-128">The ribbon minimized state as specified by the boolean value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key.</span></span>

    > [!Note]  
    > <span data-ttu-id="1bee8-129">O estado de faixa de faixas minimizada não é equivalente ao estado recolhido da faixa de para.</span><span class="sxs-lookup"><span data-stu-id="1bee8-129">The ribbon minimized state is not equivalent to the ribbon collapsed state.</span></span> <span data-ttu-id="1bee8-130">No estado recolhido, a faixa de faixas é completamente oculta e não pode ser interagindo.</span><span class="sxs-lookup"><span data-stu-id="1bee8-130">When in collapsed state, the ribbon is completely hidden and cannot be interacted with.</span></span> <span data-ttu-id="1bee8-131">A estrutura invocará esse estado automaticamente se a janela do aplicativo for reduzida em tamanho, tanto horizontal quanto verticalmente, até o ponto em que a faixa de opções obscurece o espaço de trabalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1bee8-131">The framework invokes this state automatically if the application window is reduced in size, either horizontally or vertically, to the point that the ribbon obscures the application workspace.</span></span> <span data-ttu-id="1bee8-132">A estrutura restaura a faixa de faixas quando o tamanho da janela do aplicativo é aumentado.</span><span class="sxs-lookup"><span data-stu-id="1bee8-132">The framework restores the ribbon when the size of the application window is increased.</span></span>

     

    <span data-ttu-id="1bee8-133">Esta captura de tela mostra o comando minimizar menu de contexto da **faixa de** medida.</span><span class="sxs-lookup"><span data-stu-id="1bee8-133">This screen shot shows the **Minimize the Ribbon** context menu Command.</span></span>

    ![captura de tela do menu de contexto do comando na faixa de faixas do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="1bee8-135">Esta captura de tela mostra uma faixa de medida minimizada.</span><span class="sxs-lookup"><span data-stu-id="1bee8-135">This screen shot shows a minimized ribbon.</span></span>

    ![captura de tela da faixa de faixas do Microsoft Paint minimizada.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a><span data-ttu-id="1bee8-137">Salvar configurações da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="1bee8-137">Save Ribbon Settings</span></span>

<span data-ttu-id="1bee8-138">O método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) grava uma representação binária do estado de faixa de forma persistente (descrito na seção anterior) em um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-138">The [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method writes a binary representation of the persistent ribbon state (outlined in the previous section) to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span> <span data-ttu-id="1bee8-139">Em seguida, o aplicativo salva o conteúdo do objeto IStream em um arquivo ou no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="1bee8-139">The application then saves the content of the IStream object to a file or the Windows registry.</span></span>

<span data-ttu-id="1bee8-140">O exemplo a seguir demonstra o código básico necessário para gravar o estado da faixa de opções em um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) usando o método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-140">The following example demonstrates the basic code required to write the ribbon state to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span>


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a><span data-ttu-id="1bee8-141">Carregar configurações da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="1bee8-141">Load Ribbon Settings</span></span>

<span data-ttu-id="1bee8-142">O método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) é usado para recuperar as informações de estado da faixa de forma persistente armazenadas como um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) pelo método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-142">The [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method is used to retrieve the persistent ribbon state information stored as an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object by the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span> <span data-ttu-id="1bee8-143">As informações no objeto IStream são aplicadas à interface do usuário da faixa de Ribbon quando o aplicativo é inicializado.</span><span class="sxs-lookup"><span data-stu-id="1bee8-143">The information in the IStream object is applied to the ribbon UI when the application initializes.</span></span>

<span data-ttu-id="1bee8-144">O exemplo a seguir demonstra o código básico necessário para carregar o estado da faixa de opções de um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) com o método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-144">The following example demonstrates the basic code required to load the ribbon state from an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object with the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



<span data-ttu-id="1bee8-145">Para obter um desempenho ideal, o método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) deve ser chamado da função de retorno de chamada [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante a fase de inicialização da estrutura, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1bee8-145">For optimal performance, the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method should be called from the [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) callback function during the framework initialization phase, as shown in the following example.</span></span>


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



<span data-ttu-id="1bee8-146">Várias instâncias do mesmo aplicativo de estrutura da faixa de das faixas podem gerenciar cada Estado da faixa de forma independentemente como objetos [IStream](/windows/win32/api/objidl/nn-objidl-istream) separados ou como um grupo por meio de um único objeto IStream.</span><span class="sxs-lookup"><span data-stu-id="1bee8-146">Multiple instances of the same Ribbon framework application can manage each ribbon state independently as separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) objects or as a group through a single IStream object.</span></span>

<span data-ttu-id="1bee8-147">Ao sincronizar o estado da faixa de medida em um grupo de instâncias do aplicativo, cada janela de nível superior deve escutar uma notificação de [ \_ ativação do WM](../inputdev/wm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-147">When synchronizing ribbon state across a group of application instances, each top-level window must listen for a [WM\_ACTIVATE](../inputdev/wm-activate.md) notification.</span></span> <span data-ttu-id="1bee8-148">A janela de nível superior sendo desativada salva seu estado da faixa de forma usando o método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e a janela de nível superior que está sendo ativada carrega o estado da faixa de forma usando o método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="1bee8-148">The top-level window being deactivated saves its ribbon state using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method, and the top-level window being activated loads its ribbon state using the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bee8-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bee8-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bee8-150">Barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="1bee8-150">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 