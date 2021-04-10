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
# <a name="persisting-ribbon-state"></a>Estado da faixa de medida persistente

O Windows Ribon Framework (faixa de opções) fornece a capacidade de preservar o estado de uma variedade de configurações de usuário e preferências entre sessões de aplicativos.

-   [Introdução](#introduction)
-   [Uma experiência previsível](#a-predictable-experience)
-   [Salvar configurações da faixa de opções](#save-ribbon-settings)
-   [Carregar configurações da faixa de opções](#load-ribbon-settings)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Vários aspectos de uma faixa de opções, incluindo preferências de configuração e interação, podem ser personalizados por um usuário em tempo de execução para melhorar a usabilidade e a produtividade. A estrutura da faixa de opções fornece a funcionalidade para preservar essas configurações em sessões de aplicativos por meio de dois métodos definidos na implementação da interface [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) e [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Uma experiência previsível

As [diretrizes de experiência do usuário da faixa](https://msdn.microsoft.com/library/cc872782.aspx) de guia aconselham que, para fornecer a experiência de usuário mais previsível possível, os aplicativos de faixa de das faixas devem preservar o estado da faixa de faixas (além da última guia selecionada) à medida que o aplicativo é fechado. Dessa forma, quando o mesmo aplicativo é iniciado, as configurações e personalizações da sessão anterior podem ser restauradas e o usuário pode esperar continuar interagindo com o aplicativo da mesma maneira que o deixou.

As configurações da faixa de opções que podem ser modificadas em tempo de execução e preservadas entre sessões de aplicativo são listadas no menu de contexto do comando. Entre elas estão:

-   Comandos adicionados à lista de comandos da [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) pelo usuário. Especificado por um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por meio da chave de propriedade [ \_ PKEY \_ ItemsSource da interface do usuário](windowsribbon-reference-properties-uipkey-itemssource.md) .

    A captura de tela a seguir mostra o comando adicionar ao menu de contexto **da barra de ferramentas de acesso rápido** .

    ![captura de tela do menu de contexto do comando na faixa de faixas do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   O estado de encaixe da [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) preferencial. Especificado pelo valor [**de \_ CONTROLDOCK da interface**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) do usuário da chave de propriedade [ \_ PKEY \_ QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) .

    Esta captura de tela mostra a [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) em seu local da barra de título do aplicativo padrão e a **barra de ferramentas mostrar acesso rápido abaixo do comando do menu de contexto da faixa de da**

    ![captura de tela do menu de contexto do comando na faixa de faixas do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Esta captura de tela mostra a [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) abaixo da faixa de faixas.

    ![captura de tela da barra de ferramentas de acesso rápido encaixada abaixo da faixa de faixas.](images/controls/qat-dockbottom.png)

-   O estado da faixa de faixas minimizada conforme especificado pelo valor booliano da chave de propriedade [ \_ PKEY \_ minimizada da interface do usuário](windowsribbon-reference-properties-uipkey-minimized.md) .

    > [!Note]  
    > O estado de faixa de faixas minimizada não é equivalente ao estado recolhido da faixa de para. No estado recolhido, a faixa de faixas é completamente oculta e não pode ser interagindo. A estrutura invocará esse estado automaticamente se a janela do aplicativo for reduzida em tamanho, tanto horizontal quanto verticalmente, até o ponto em que a faixa de opções obscurece o espaço de trabalho do aplicativo. A estrutura restaura a faixa de faixas quando o tamanho da janela do aplicativo é aumentado.

     

    Esta captura de tela mostra o comando minimizar menu de contexto da **faixa de** medida.

    ![captura de tela do menu de contexto do comando na faixa de faixas do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Esta captura de tela mostra uma faixa de medida minimizada.

    ![captura de tela da faixa de faixas do Microsoft Paint minimizada.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Salvar configurações da faixa de opções

O método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) grava uma representação binária do estado de faixa de forma persistente (descrito na seção anterior) em um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) . Em seguida, o aplicativo salva o conteúdo do objeto IStream em um arquivo ou no registro do Windows.

O exemplo a seguir demonstra o código básico necessário para gravar o estado da faixa de opções em um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) usando o método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .


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



## <a name="load-ribbon-settings"></a>Carregar configurações da faixa de opções

O método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) é usado para recuperar as informações de estado da faixa de forma persistente armazenadas como um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) pelo método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) . As informações no objeto IStream são aplicadas à interface do usuário da faixa de Ribbon quando o aplicativo é inicializado.

O exemplo a seguir demonstra o código básico necessário para carregar o estado da faixa de opções de um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) com o método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .


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



Para obter um desempenho ideal, o método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) deve ser chamado da função de retorno de chamada [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante a fase de inicialização da estrutura, conforme mostrado no exemplo a seguir.


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



Várias instâncias do mesmo aplicativo de estrutura da faixa de das faixas podem gerenciar cada Estado da faixa de forma independentemente como objetos [IStream](/windows/win32/api/objidl/nn-objidl-istream) separados ou como um grupo por meio de um único objeto IStream.

Ao sincronizar o estado da faixa de medida em um grupo de instâncias do aplicativo, cada janela de nível superior deve escutar uma notificação de [ \_ ativação do WM](../inputdev/wm-activate.md) . A janela de nível superior sendo desativada salva seu estado da faixa de forma usando o método [**IUIRibbon:: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e a janela de nível superior que está sendo ativada carrega o estado da faixa de forma usando o método [**IUIRibbon:: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 