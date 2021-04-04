---
title: Exibindo a faixa de faixas
description: A estrutura da faixa de faixas do Windows expõe um conjunto de propriedades que permitem que um aplicativo especifique como a interface do usuário da faixa de Ribbon é exibida em tempo de execução.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Faixa de-se do Windows, personalizando cores
- Faixa de faixas, personalizando cores
- Personalizando as cores da faixa de das janelas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007840"
---
# <a name="displaying-the-ribbon"></a>Exibindo a faixa de faixas

A estrutura da faixa de faixas do Windows expõe um conjunto de propriedades que permitem que um aplicativo especifique como a interface do usuário da faixa de Ribbon é exibida em tempo de execução.

-   [Introdução](#introduction)
-   [Minimizar a faixa de faixas](#minimize-the-ribbon)
-   [Ocultar a faixa de faixas](#hide-the-ribbon)
-   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Para maximizar a área disponível para o espaço do documento (ou a porta de exibição) de um aplicativo da estrutura da faixa de faixas, um aplicativo pode especificar se a interface do usuário da faixa de visão está visível ou oculta e, quando visível, se a faixa de ' está em um estado expandido ou recolhido.

As [chaves de propriedade da estrutura](windowsribbon-reference-properties-framework.md) listadas na tabela a seguir são usadas para definir explicitamente as características de exibição da interface do usuário da faixa de opções em um aplicativo da estrutura da faixa de opções. Essas propriedades não têm nenhum efeito na exibição do controle [Popup de contexto](windowsribbon-controls-contextpopup.md) .



| Estado de exibição         | Chave da propriedade da faixa de,                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| Expandido ou recolhido | [PKEY da interface do usuário \_ \_ minimizada](windowsribbon-reference-properties-uipkey-minimized.md) |
| Visível ou oculto     | [PKEY da interface do usuário \_ \_ visível](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>Minimizar a faixa de faixas

Um aplicativo da estrutura da faixa de opção pode definir dinamicamente o estado minimizado da barra de comandos da faixa de opção definindo o valor da chave de propriedade [ \_ PKEY \_ minimizada da interface do usuário](windowsribbon-reference-properties-uipkey-minimized.md) como **true** ou **false**.



| Estado de exibição | Valor da chave da propriedade |
|---------------|--------------------|
| Expanded      | **false**          |
| Recolhido     | **true**           |



 

Quando a interface do usuário da faixa de visão está em um estado minimizado, a linha da guia da faixa de faixas permanece visível e totalmente funcional.

A captura de tela a seguir mostra a faixa de opções no estado minimizado.

![captura de tela mostrando a interface do usuário da faixa de faixas minimizada.](images/overviews/ribbon-minimized.png)

> [!Note]  
> A estrutura da faixa de opção expõe essa funcionalidade ao usuário final por meio da seleção "minimizar a faixa de opção" do menu de contexto da faixa de modo.

 

## <a name="hide-the-ribbon"></a>Ocultar a faixa de faixas

Um aplicativo da estrutura da faixa de opção pode definir dinamicamente o estado visível da barra de comandos da faixa de opção, definindo o valor da chave de propriedade [ \_ PKEY \_ viewable da interface do usuário](windowsribbon-reference-properties-uipkey-viewable.md) como **true** ou **false**.



| Estado de exibição | Valor da chave da propriedade |
|---------------|--------------------|
| Visible       | **false**          |
| Hidden        | **true**           |



 

Ao contrário da propriedade [ \_ PKEY \_ minimizada da interface do usuário](windowsribbon-reference-properties-uipkey-minimized.md) , definir a [interface do usuário \_ PKEY \_ visível](windowsribbon-reference-properties-uipkey-viewable.md) como **false** renderiza a interface do usuário da faixa de opção invisível e completamente inutilizável para um usuário final.

A captura de tela a seguir mostra a faixa de opções no estado oculto.

![captura de tela mostrando a interface do usuário da faixa de faixas oculta.](images/overviews/ribbon-viewable.png)

## <a name="example"></a>Exemplo

O exemplo a seguir demonstra como definir o estado da interface do usuário da faixa de opções em tempo de execução.

Nesse caso, a função [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) é usada para expandir ou recolher a interface do usuário da faixa de opção com base no estado de alternância de um [botão de alternância](windowsribbon-controls-togglebutton.md).


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades da faixa de faixas](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 