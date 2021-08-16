---
title: botão Drop-Down de Drop-Down
description: O Drop-Down botão consiste em um botão que, quando clicado, exibe uma lista de itens mutuamente exclusivos.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66945384d7df3e3ba656f75baf0661001022fa762690dc9c3ffd819ff1096691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202543"
---
# <a name="drop-down-button"></a>botão Drop-Down de Drop-Down

O Drop-Down botão consiste em um botão que, quando clicado, exibe uma lista de itens mutuamente exclusivos.

-   [Detalhes](#details)
-   [Propriedades do botão de lista listada](#drop-down-button-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

Esse controle é útil para expor itens intimamente relacionados em casos em que nenhum padrão óbvio está disponível e em que os itens individuais podem ser representados por uma imagem, texto ou ambos.

A captura de tela a seguir ilustra o botão de Drop-Down faixa de opções em uma faixa de opções de exemplo.

![captura de tela de um controle dropdownbutton em uma faixa de opções de exemplo.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a>Drop-Down do botão de Drop-Down

A estrutura ribbon define uma coleção de chaves [de propriedade](windowsribbon-reference-properties.md) para o controle Drop-Down Botão.

Normalmente, uma propriedade Drop-Down Button é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [**método IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

A tabela a seguir lista as chaves de propriedade associadas ao controle Drop-Down Button.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Chave de propriedade</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a><br/> Se todos os itens filho estão desabilitados, a estrutura <a href="windowsribbon-reference-properties-uipkey-enabled.md">define UI_PKEY_Enabled</a> como false (0). Caso contrário, se um ou mais itens filho estão habilitados, UI_PKEY_Enabled é definido como true (-1).
<blockquote>
[!Important]<br />
A <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> para o controle Drop-Down Button deve ser invalidada depois que um ou mais itens filho são habilitados ou desabilitados. Isso garante que a estrutura consulte o valor da propriedade atualizada e atualize o estado do controle Drop-Down Botão na interface do usuário da faixa de opções.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a>
<blockquote>
[!Note]<br />
Se o Comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando for passado como o valor dos <code>UI_INVALIDATIONS_VALUE</code> <em>sinalizadores</em>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de Controle da Estrutura de Faixa de Opções](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação DropDownButton**](windowsribbon-element-dropdownbutton.md)
</dt> </dl>