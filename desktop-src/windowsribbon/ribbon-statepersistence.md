---
title: Persistindo o estado da faixa de opções
description: O Windows Framework (Faixa de Opções) fornece a capacidade de preservar o estado de uma variedade de configurações e preferências do usuário entre as sessões do aplicativo.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e506d1cc8138f569dc21b491cc11ed58411131c0dd80532c19043c5974995e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707925"
---
# <a name="persisting-ribbon-state"></a>Persistindo o estado da faixa de opções

O Windows Framework (Faixa de Opções) fornece a capacidade de preservar o estado de uma variedade de configurações e preferências do usuário entre as sessões do aplicativo.

-   [Introdução](#introduction)
-   [Uma experiência previsível](#a-predictable-experience)
-   [Salvar faixa de opções Configurações](#save-ribbon-settings)
-   [Carregar faixa de opções Configurações](#load-ribbon-settings)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Vários aspectos de uma faixa de opções, incluindo preferências de configuração e interação, podem ser personalizados por um usuário em tempo de execução para melhorar a usabilidade e a produtividade. A estrutura ribbon fornece a funcionalidade para preservar essas configurações em sessões de aplicativo por meio de dois métodos definidos na implementação da interface [**IUIRibbon:**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) e [**IUIRibbon::SaveSettingsToStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)

## <a name="a-predictable-experience"></a>Uma experiência previsível

As Diretrizes de Experiência do Usuário da Faixa de Opções aconselham que, para fornecer a experiência do usuário mais previsível possível, os [aplicativos](https://msdn.microsoft.com/library/cc872782.aspx) da Faixa de Opções devem preservar o estado da faixa de opções (além da última guia selecionada) conforme o aplicativo é fechado. Dessa forma, quando o mesmo aplicativo é lançado, as configurações e as personalizações da sessão anterior podem ser restauradas e o usuário pode esperar continuar interagindo com o aplicativo da mesma maneira que o deixou.

As configurações da faixa de opções que podem ser modificadas em tempo de operação e preservadas entre as sessões do aplicativo são listadas no menu Contexto de comando. Eles incluem:

-   Comandos adicionados à [lista Comando da Barra](windowsribbon-controls-quickaccesstoolbar.md) de Ferramentas de Acesso Rápido pelo usuário. Especificado por um objeto [**IUICollection por**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) meio da chave de propriedade [ \_ PKEY \_ ItemsSource da](windowsribbon-reference-properties-uipkey-itemssource.md) interface do usuário.

    A captura de tela a seguir mostra o **menu de contexto** Adicionar à Barra de Ferramentas de Acesso Rápido.

    ![captura de tela do menu de contexto de comando na faixa de opções do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   O estado [de encaixe da barra de ferramentas de acesso](windowsribbon-controls-quickaccesstoolbar.md) rápido preferencial. Especificado pelo valor [**\_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) da interface do usuário da chave de propriedade [ \_ \_ QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) da interface do usuário.

    Esta captura de tela mostra a [Barra](windowsribbon-controls-quickaccesstoolbar.md) de Ferramentas de Acesso Rápido no local da barra de título do aplicativo padrão e a **barra** de ferramentas Mostrar Acesso Rápido abaixo do comando do menu de contexto faixa de opções.

    ![captura de tela do menu de contexto de comando na faixa de opções do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Esta captura de tela mostra a [Barra de Ferramentas de Acesso Rápido](windowsribbon-controls-quickaccesstoolbar.md) abaixo da faixa de opções.

    ![captura de tela da barra de ferramentas de acesso rápido encaixada abaixo da faixa de opções.](images/controls/qat-dockbottom.png)

-   O estado minimizado da faixa de opções, conforme especificado pelo valor booliana da chave de [ \_ propriedade PKEY \_ Minimizada](windowsribbon-reference-properties-uipkey-minimized.md) da interface do usuário.

    > [!Note]  
    > O estado minimizado da faixa de opções não é equivalente ao estado recolhido da faixa de opções. Quando em estado recolhido, a faixa de opções fica completamente oculta e não pode ser interage com ela. A estrutura invocará esse estado automaticamente se a janela do aplicativo for reduzida de tamanho, horizontal ou verticalmente, até o ponto em que a faixa de opções obscurece o workspace do aplicativo. A estrutura restaura a faixa de opções quando o tamanho da janela do aplicativo é aumentado.

     

    Esta captura de tela mostra o comando do menu de contexto Minimizar **a Faixa** de Opções.

    ![captura de tela do menu de contexto de comando na faixa de opções do Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Esta captura de tela mostra uma faixa de opções minimizada.

    ![captura de tela da faixa de opções de pintura minimizada da Microsoft.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Salvar faixa de opções Configurações

O [**método IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) grava uma representação binária do estado da faixa de opções persistente (descrito na seção anterior) em um [objeto IStream.](/windows/win32/api/objidl/nn-objidl-istream) Em seguida, o aplicativo salva o conteúdo do objeto IStream em um arquivo ou no Windows registro.

O exemplo a seguir demonstra o código básico necessário para gravar o estado da faixa de opções em um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) usando o [**método IUIRibbon::SaveSettingsToStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)


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



## <a name="load-ribbon-settings"></a>Carregar faixa de opções Configurações

O [**método IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) é usado para recuperar as informações de estado da faixa de opções persistente armazenadas como um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) pelo método [**IUIRibbon::SaveSettingsToStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) As informações no objeto IStream são aplicadas à interface do usuário da faixa de opções quando o aplicativo é inicializado.

O exemplo a seguir demonstra o código básico necessário para carregar o estado da faixa de opções de um objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) com o [**método IUIRibbon::LoadSettingsFromStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)


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



Para obter um desempenho ideal, o método [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) deve ser chamado da função de retorno de chamada [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) durante a fase de inicialização da estrutura, conforme mostrado no exemplo a seguir.


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



Várias instâncias do mesmo aplicativo de estrutura da Faixa de Opções podem gerenciar cada estado da faixa de opções independentemente como objetos [IStream separados](/windows/win32/api/objidl/nn-objidl-istream) ou como um grupo por meio de um único objeto IStream.

Ao sincronizar o estado da faixa de opções em um grupo de instâncias de aplicativo, cada janela de nível superior deve escutar uma [notificação WM \_ ACTIVATE.](../inputdev/wm-activate.md) A janela de nível superior que está sendo desativada salva seu estado de faixa de opções usando o método [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e a janela de nível superior que está sendo ativada carrega seu estado de faixa de opções usando o método [**IUIRibbon::LoadSettingsFromStream.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Barra de Ferramentas de Acesso Rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 