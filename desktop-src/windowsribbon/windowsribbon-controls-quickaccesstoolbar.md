---
title: Barra de Ferramentas de Acesso Rápido
description: A QAT (Barra de Ferramentas de Acesso Rápido) é uma barra de ferramentas pequena e personalizável que expõe um conjunto de Comandos que são especificados pelo aplicativo ou selecionados pelo usuário.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d63eb3f7b1a2c1213430f86a9a12fe4517c738290ed736eb1d356420aa145cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110717"
---
# <a name="quick-access-toolbar"></a>Barra de Ferramentas de Acesso Rápido

A QAT (Barra de Ferramentas de Acesso Rápido) é uma barra de ferramentas pequena e personalizável que expõe um conjunto de Comandos que são especificados pelo aplicativo ou selecionados pelo usuário.

- [Introdução](#introduction)
- [Implementar a barra de ferramentas de acesso rápido](#implement-the-quick-access-toolbar)
  - [Marcação](#markup)
  - [Código](#code)
- [Persistência de QAT](#qat-persistence)
- [Propriedades da barra de ferramentas de acesso rápido](#quick-access-toolbar-properties)
- [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Por padrão, a QAT (Barra de Ferramentas de Acesso Rápido) está localizada na barra de título da janela do aplicativo, mas pode ser configurada para exibição abaixo da faixa de opções. Além de expor comandos, a QAT (Barra de Ferramentas de Acesso Rápido) também inclui um menu suspenso personalizável que contém o conjunto completo de comandos padrão da QAT (Barra de Ferramentas de Acesso Rápido) (ocultos ou exibidos na QAT (Barra de Ferramentas de Acesso Rápido)) e um conjunto de opções de faixa de opções da QAT (Barra de Ferramentas de Acesso Rápido).

A captura de tela a seguir mostra um exemplo da QAT (Barra de Ferramentas de Acesso Rápido) da Faixa de Opções.

![captura de tela do qat na faixa de opções de pintura da Microsoft.](images/markup/qat-and-menu.png)

A QAT (Barra de Ferramentas de Acesso Rápido) consiste em uma combinação de até 20 comandos especificados pelo aplicativo (conhecido como a lista de padrões do aplicativo) ou selecionados pelo usuário. A QAT (Barra de Ferramentas de Acesso Rápido) pode conter comandos exclusivos que não estão disponíveis em outro lugar na interface do usuário da faixa de opções.

> [!Note]
> Embora quase todos os controles de faixa de opções permitam que seu Comando associado seja adicionado à QAT (Barra de Ferramentas de Acesso Rápido) por meio do menu de contexto mostrado na captura de tela a seguir, comandos expostos em um [Pop-up](windowsribbon-controls-contextpopup.md) de contexto não fornecem esse menu de contexto.
>
> ![captura de tela do menu de contexto de comando na faixa de opções do Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implementar a barra de ferramentas de acesso rápido

Assim como ocorre com todos os controles de estrutura da faixa de opções do Windows, aproveitar ao máximo a QAT (Barra de Ferramentas de Acesso Rápido) requer um componente de marcação que controla sua apresentação na faixa de opções e um componente de código que rege sua funcionalidade.

### <a name="markup"></a>Marcação

O controle QAT (Quick Access Toolbar) é declarado e associado a uma ID de comando, na marcação por meio do [elemento QuickAccessToolbar.](windowsribbon-element-quickaccesstoolbar.md) A ID do Comando é usada para identificar e vincular a QAT (Barra de Ferramentas de Acesso Rápido) a um manipulador de comandos definido pelo aplicativo.

Além do manipulador de comandos básico para **a** funcionalidade primária da QAT (Barra de Ferramentas de Acesso Rápido), declarar o atributo opcional de elemento *CustomCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) faz com que a estrutura adicione um item Mais Comandos à lista comando do menu suspenso da QAT (Barra de Ferramentas de Acesso Rápido) opcional que requer que um manipulador de comandos secundário seja definido.

Para consistência entre aplicativos da Faixa de Opções, é recomendável que o manipulador de comandos *CustomizeCommandName* iniciar uma caixa de diálogo de personalização da QAT (Barra de Ferramentas de Acesso Rápido). Como a estrutura da Faixa de Opções fornece apenas o ponto de lançamento na interface do usuário, o aplicativo é exclusivamente responsável por fornecer a implementação da caixa de diálogo de personalização quando a notificação de retorno de chamada para esse comando é recebida.

A captura de tela a seguir mostra um menu suspenso da QAT (Barra de Ferramentas de Acesso Rápido) com o item **Comando** Mais Comandos.

![captura de tela de um menu qat com mais comandos... item de comando.](images/markup/qat-customizecommandname.png)

A lista de padrões do aplicativo para a QAT (Barra de Ferramentas de Acesso Rápido) é especificada por meio da propriedade [QuickAccessToolbar.ApplicationDefaults,](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) que identifica uma lista padrão de Comandos recomendados, todos listados no menu suspenso da QAT (Barra de Ferramentas de Acesso Rápido).

Para exibir Comandos da lista de padrões do aplicativo na barra de ferramentas da QAT (Barra de Ferramentas de Acesso Rápido), o atributo *ApplicationDefaults.IsChecked* de cada elemento de controle deve ter um valor `true` de . As imagens anteriores mostram os resultados da configuração desse atributo como para os `true` comandos **Salvar**, **Desfazer** **e** Refazer.

[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) dá suporte a três tipos de controles de Faixa de Opções: [Botão](windowsribbon-controls-button.md) [,](windowsribbon-controls-togglebutton.md)Botão de Alternância e Caixa de [Seleção](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 e mais novos: todos os controles baseados em galeria têm suporte ([ComboBox,](windowsribbon-element-combobox.md) [InRibbonGallery,](windowsribbon-element-inribbongallery.md) [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)e [DropDownGallery](windowsribbon-element-dropdowngallery.md)).
>
> Itens em um controle de galeria podem dar suporte ao realçamento ao passar o mouse. Para dar suporte ao realamento de foco, a galeria deve ser uma galeria de itens e usar [um FlowMenuLayout](windowsribbon-element-flowmenulayout.md) do [tipo VerticalMenuLayout.](windowsribbon-element-verticalmenulayout.md)

O exemplo a seguir demonstra a marcação básica para um [elemento QuickAccessToolbar.](windowsribbon-element-quickaccesstoolbar.md)

Esta seção de código mostra as declarações de comando para um [elemento QAT (Barra](windowsribbon-element-quickaccesstoolbar.md) de Ferramentas de Acesso Rápido).

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

Esta seção de código mostra as declarações de controle para um [elemento QAT (Barra](windowsribbon-element-quickaccesstoolbar.md) de Ferramentas de Acesso Rápido).

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

O aplicativo de estrutura ribbon deve fornecer um método de retorno de chamada do manipulador de comandos para manipular a QAT (Barra de Ferramentas de Acesso Rápido). Esse manipulador funciona de maneira semelhante aos manipuladores da galeria de comandos, exceto que a QAT (Barra de Ferramentas de Acesso Rápido) não dá suporte a categorias. Para obter mais informações, consulte [Trabalhando com galerias.](ribbon-controls-galleries.md)

A coleção de comandos da QAT (Barra de Ferramentas de Acesso Rápido) é recuperada como um objeto [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por meio da chave de propriedade [ \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) da interface do usuário. A adição de comandos à QAT (Barra de Ferramentas de Acesso Rápido) em tempo de operação é realizada adicionando um objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) à **IUICollection**.

Ao contrário das galerias de comandos, uma propriedade de tipo de comando ([UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) não é necessária para o objeto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) da QAT (Barra de Ferramentas de Acesso Rápido). No entanto, o Comando deve existir na faixa de opções ou na lista de padrões do aplicativo QAT (Barra de Ferramentas de Acesso Rápido). um novo Comando não pode ser criado em tempo de executar e adicionado à QAT (Barra de Ferramentas de Acesso Rápido).

> [!Note]  
> O aplicativo Ribbon não pode substituir a [IUICollection da IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) da QAT (Barra de Ferramentas de Acesso Rápido) por um objeto de coleção personalizado derivado de IEnumUnknown.

O exemplo a seguir demonstra uma implementação básica do manipulador de comandos da QAT (Barra de Ferramentas de Acesso Rápido).

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

As configurações e os itens de comando da QAT (Barra de Ferramentas de Acesso Rápido) podem ser persistido entre as sessões do aplicativo usando as funções [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e [IUIRibbon::LoadSettingsFromStream.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) Para obter mais informações, consulte [Persisting Ribbon State](ribbon-statepersistence.md).

## <a name="quick-access-toolbar-properties"></a>Propriedades da barra de ferramentas de acesso rápido

A estrutura ribbon define uma coleção de chaves [de propriedade](windowsribbon-reference-properties.md) para o controle QAT (Barra de Ferramentas de Acesso Rápido).

Normalmente, uma propriedade QAT (Barra de Ferramentas de Acesso Rápido) é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o [método IUIFramework::InvalidateUICommand.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [IUICommandHandler::UpdateProperty.](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [método IUIFramework::SetUICommandProperty.](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

A tabela a seguir lista as chaves de propriedade associadas ao controle QAT (Barra de Ferramentas de Acesso Rápido).

| Chave de propriedade | Observações |
|---|---|
| [Itens \_ PKEY da \_ interface do usuárioSource](windowsribbon-reference-properties-uipkey-itemssource.md) | Dá [suporte a IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (não dá suporte a [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) retorna um ponteiro para um objeto IUICollection que representa os comandos no QAT. Cada comando é identificado por sua ID de comando, que é obtida chamando o método [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) e passando a chave de propriedade [IU \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md). |

Não há chaves de propriedade associadas ao item **Comando Mais** Comandos do menu suspenso da QAT (Barra de Ferramentas de Acesso Rápido)

## <a name="related-topics"></a>Tópicos relacionados

- [Windows Biblioteca de Controle da Estrutura de Faixa de Opções](windowsribbon-controls-entry.md)
- [Elemento de marcação QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md)