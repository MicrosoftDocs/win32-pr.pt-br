---
title: Botão de Divisão
description: O botão de divisão é um controle composto com o qual o usuário pode selecionar um valor padrão associado a um botão primário ou selecionar em uma lista de valores mutuamente exclusivos exibidos em uma lista suspensa associada a um botão secundário.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105784991"
---
# <a name="split-button"></a>Botão de Divisão

O botão de divisão é um controle composto com o qual o usuário pode selecionar um valor padrão associado a um botão primário ou selecionar em uma lista de valores mutuamente exclusivos exibidos em uma lista suspensa associada a um botão secundário.

-   [Introdução](#introduction)
-   [Propriedades do botão de divisão](#split-button-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Esse controle é útil para expor itens bem relacionados em casos em que um padrão óbvio está disponível e onde os itens individuais podem ser representados por uma imagem, texto ou ambos.

A captura de tela a seguir ilustra o botão de divisão da faixa de opções.

![captura de tela de um controle SplitButton em uma faixa de uma amostra.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Propriedades do botão de divisão

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle do botão de divisão.

Normalmente, uma propriedade de botão de divisão é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas com o controle de botão de divisão.



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
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.<br/> Se todos os itens filho estiverem desabilitados, a estrutura definirá <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> como false (0). Caso contrário, se um ou mais itens filhos estiverem habilitados, UI_PKEY_Enabled será definido como true (-1).
<blockquote>
[!Important]<br />
A propriedade <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> para o controle do botão de divisão deve ser invalidada depois que um ou mais itens filho são habilitados ou desabilitados. Isso garante que a estrutura consulta o valor da propriedade atualizado e atualiza o estado do controle do botão de divisão na interface do usuário da faixa de da.
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

[Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>