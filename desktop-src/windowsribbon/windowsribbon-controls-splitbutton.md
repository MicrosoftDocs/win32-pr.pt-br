---
title: Botão de Divisão
description: O Botão Dividir é um controle composto com o qual o usuário pode selecionar um valor padrão vinculado a um botão primário ou selecionar em uma lista de valores mutuamente exclusivos exibidos em uma lista de listas listadas vinculadas a um botão secundário.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5d9554af8c580b5288a2f18eaef89a1d7e864bae628ebac59599f6b7f820f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202483"
---
# <a name="split-button"></a>Botão de Divisão

O Botão Dividir é um controle composto com o qual o usuário pode selecionar um valor padrão vinculado a um botão primário ou selecionar em uma lista de valores mutuamente exclusivos exibidos em uma lista de listas listadas vinculadas a um botão secundário.

-   [Introdução](#introduction)
-   [Propriedades do botão Dividir](#split-button-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Esse controle é útil para expor itens intimamente relacionados em casos em que um padrão óbvio está disponível e em que os itens individuais podem ser representados por uma imagem, texto ou ambos.

A captura de tela a seguir ilustra o Botão de Divisão da Faixa de Opções.

![captura de tela de um controle splitbutton em uma faixa de opções de exemplo.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Propriedades do botão Dividir

A estrutura ribbon define uma coleção de chaves [de propriedade](windowsribbon-reference-properties.md) para o controle Dividir Botão.

Normalmente, uma propriedade Botão de Divisão é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [**método IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

A tabela a seguir lista as chaves de propriedade associadas ao controle Dividir Botão.



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
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a><br/> Se todos os itens filho estão desabilitados, a estrutura <a href="windowsribbon-reference-properties-uipkey-enabled.md">define UI_PKEY_Enabled</a> como false (0). Caso contrário, se um ou mais itens filho estão habilitados, UI_PKEY_Enabled é definido como true (-1).
<blockquote>
[!Important]<br />
A <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> para o controle Dividir Botão deve ser invalidada depois que um ou mais itens filho são habilitados ou desabilitados. Isso garante que a estrutura consulte o valor da propriedade atualizada e atualize o estado do controle Dividir Botão na interface do usuário da faixa de opções.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
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

[**Elemento de marcação SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>