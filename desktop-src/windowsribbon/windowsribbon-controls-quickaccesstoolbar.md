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
# <a name="quick-access-toolbar"></a>Barra de ferramentas de acesso rápido

A barra de ferramentas de acesso rápido (QAT) é uma barra de ferramentas pequena e personalizável que expõe um conjunto de comandos que são especificados pelo aplicativo ou selecionados pelo usuário.

- [Introdução](#introduction)
- [Implementar a barra de ferramentas de acesso rápido](#implement-the-quick-access-toolbar)
  - [Marcação](#markup)
  - [Código](#code)
- [Persistência de QAT](#qat-persistence)
- [Propriedades da barra de ferramentas de acesso rápido](#quick-access-toolbar-properties)
- [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Por padrão, a barra de ferramentas de acesso rápido (QAT) está localizada na barra de título da janela do aplicativo, mas pode ser configurada para ser exibida abaixo da faixa de faixas. Além de expor comandos, a barra de ferramentas de acesso rápido (QAT) também inclui um menu suspenso personalizável que contém o conjunto completo de comandos de QAT (barra de ferramentas de acesso rápido) padrão (se ocultos ou exibidos na barra de ferramentas de acesso rápido (QAT)) e um conjunto de opções de barra de ferramentas de acesso rápido (QAT) e de faixa.

A captura de tela a seguir mostra um exemplo da barra de ferramentas de acesso rápido da faixa de opções (QAT).

![captura de tela do qat na faixa de faixas do Microsoft Paint.](images/markup/qat-and-menu.png)

A barra de ferramentas de acesso rápido (QAT) consiste em uma combinação de até 20 comandos especificados pelo aplicativo (conhecido como a lista de padrões do aplicativo) ou selecionados pelo usuário. A barra de ferramentas de acesso rápido (QAT) pode conter comandos exclusivos que não estão disponíveis em outro lugar na interface do usuário da faixa de guia.

> [!Note]
> Embora quase todos os controles de faixa de opções permitam que seu comando associado seja adicionado à barra de ferramentas de acesso rápido (QAT) por meio do menu de contexto mostrado na captura de tela a seguir, os comandos expostos em um [Popup de contexto](windowsribbon-controls-contextpopup.md) não fornecem esse menu de contexto.
>
> ![captura de tela do menu de contexto do comando na faixa de faixas do Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implementar a barra de ferramentas de acesso rápido

Assim como todos os controles de estrutura da faixa de opções do Windows, aproveitar ao máximo a barra de ferramentas de acesso rápido (QAT) requer um componente de marcação que controla sua apresentação na faixa de opções e um componente de código que governa sua funcionalidade.

### <a name="markup"></a>Marcação

O controle de barra de ferramentas de acesso rápido (QAT) é declarado e associado a uma ID de comando, na marcação por meio do elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) . A ID de comando é usada para identificar e associar a barra de ferramentas de acesso rápido (QAT) a um manipulador de comandos definido pelo aplicativo.

Além do manipulador de comando básico para a funcionalidade principal de barra de ferramentas de acesso rápido (QAT), declarar o atributo de elemento opcional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) faz com que a estrutura adicione um item de **mais comandos** à lista de comandos do menu suspenso qat (barra de ferramentas de acesso rápido) que exige a definição de um manipulador de comandos secundário.

Para fins de consistência em aplicativos de faixa de ferramentas, é recomendável que o manipulador de comandos *CustomizeCommandName* inicie uma caixa de diálogo de personalização de barra de acesso rápido (qat). Como a estrutura da faixa de faixas fornece apenas o ponto de partida na interface do usuário, o aplicativo é exclusivamente responsável por fornecer a implementação da caixa de diálogo de personalização quando a notificação de retorno de chamada para esse comando é recebida.

A captura de tela a seguir mostra um menu suspenso de barra de ferramentas de acesso rápido (QAT) com o item de comando **mais comandos** .

![captura de tela de um menu qat com mais comandos... item de comando.](images/markup/qat-customizecommandname.png)

A lista de padrões do aplicativo para a barra de ferramentas de acesso rápido (QAT) é especificada por meio da propriedade [QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , que identifica uma lista padrão de comandos recomendados, todos listados no menu suspenso barra de ferramentas de acesso rápido (qat).

Para exibir comandos da lista de padrões do aplicativo na barra de ferramentas de acesso rápido (QAT), o atributo *ApplicationDefaults. IsChecked* de cada elemento de controle deve ter um valor de `true` . As imagens anteriores mostram os resultados da definição desse atributo como `true` para os comandos **salvar**, **desfazer** e **refazer** .

[QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) dá suporte a três tipos de controles de faixa de opção: [botão](windowsribbon-controls-button.md), [botão de alternância](windowsribbon-controls-togglebutton.md)e [caixa de seleção](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 e mais recente: há suporte para todos os controles baseados na galeria ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)e [DropDownGallery](windowsribbon-element-dropdowngallery.md)).
>
> Os itens em um controle Galeria podem dar suporte ao realce ao focalizar. Para dar suporte ao realce de foco, a Galeria deve ser uma galeria de itens e usar um [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) do tipo [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).

O exemplo a seguir demonstra a marcação básica para um elemento [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .

Esta seção de código mostra as declarações de comando para um elemento de [barra de ferramentas de acesso rápido (qat)](windowsribbon-element-quickaccesstoolbar.md) .

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

Esta seção de código mostra as declarações de controle para um elemento de [barra de ferramentas de acesso rápido (qat)](windowsribbon-element-quickaccesstoolbar.md) .

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

### <a name="code"></a>Código

O aplicativo da estrutura da faixa de ferramentas deve fornecer um método de retorno de chamada do manipulador de comandos para manipular a barra de ferramentas de acesso rápido (QAT) Esse manipulador funciona de maneira semelhante aos manipuladores da Galeria de comandos, exceto que a barra de ferramentas de acesso rápido (QAT) não oferece suporte a categorias. Para obter mais informações, consulte [trabalhando com galerias](ribbon-controls-galleries.md).

A coleção de comandos da barra de ferramentas de acesso rápido (QAT) é recuperada como um objeto [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por meio da chave de propriedade [ \_ \_ ItemsSource da interface do usuário PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) . Adicionar comandos à barra de ferramentas de acesso rápido (QAT) em tempo de execução é feito adicionando um objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) ao **IUICollection**.

Diferentemente de galerias de comandos, uma propriedade de tipo de comando ([ \_ \_ CommandType PKEY de interface do usuário](windowsribbon-reference-properties-uipkey-commandtype.md)) não é necessária para o objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) da barra de ferramentas de acesso rápido (qat). No entanto, o comando deve existir na lista de padrões da faixa de ferramentas ou do aplicativo de acesso rápido (QAT); um novo comando não pode ser criado em tempo de execução e adicionado à barra de ferramentas de acesso rápido (QAT).

> [!Note]  
> O aplicativo da faixa de faixas não pode substituir a barra de ferramentas de acesso rápido (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por um objeto de coleção personalizado derivado de IEnumUnknown.

O exemplo a seguir demonstra uma implementação de manipulador de comando de QAT (barra de ferramentas de acesso rápido) básica.

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

## <a name="qat-persistence"></a>Persistência de QAT

Os itens de comando e as configurações da barra de ferramentas de acesso rápido (QAT) podem ser persistidos entre sessões de aplicativo usando as funções [IUIRibbon:: SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e [IUIRibbon:: LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) . Para obter mais informações, consulte [Persisteting State](ribbon-statepersistence.md).

## <a name="quick-access-toolbar-properties"></a>Propriedades da barra de ferramentas de acesso rápido

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de barra de ferramentas de acesso rápido (qat).

Normalmente, uma propriedade de barra de ferramentas de acesso rápido (QAT) é atualizada na interface do usuário da faixa de modo invalidando o comando associado ao controle por meio de uma chamada para o método [IUIFramework:: InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [IUICommandHandler:: updateproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [IUICommandHandler:: updateproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de barra de ferramentas de acesso rápido (QAT).

| Chave de propriedade | Observações |
|---|---|
| [IU \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) | Dá suporte a [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (não dá suporte a [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) retorna um ponteiro para um objeto IUICollection que representa os comandos no qat. Cada comando é identificado por sua ID de comando, que é obtida chamando o método [IUISimplePropertySet:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) e passando a interface de usuário da chave de propriedade [ \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md). |

Não há nenhuma chave de propriedade associada ao item de comando **mais comandos** do menu suspenso da barra de ferramentas de acesso rápido (qat)

## <a name="related-topics"></a>Tópicos relacionados

- [Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
- [Elemento de marcação QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md)