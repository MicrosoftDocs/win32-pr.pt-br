---
title: Caixa de seleção
description: A caixa de seleção é um controle no qual o usuário pode clicar para fornecer entrada para um aplicativo. O controle fornece um estado de alternância que é representado visualmente.
ms.assetid: fe07aa5c-1818-41e2-b48d-5fefe50d733f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b68e850d86bd9b15a354cfa41789406e328a57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478882"
---
# <a name="check-box"></a>Caixa de seleção

A caixa de seleção é um controle no qual o usuário pode clicar para fornecer entrada para um aplicativo. O controle fornece um estado de alternância que é representado visualmente.

-   [Detalhes](#details)
-   [Propriedades da caixa de seleção](#check-box-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

A caixa de seleção não dá suporte a um estado terciário ou indeterminado.

A captura de tela a seguir ilustra o elemento da caixa de seleção faixa de opções.

![captura de tela de um controle de caixa de seleção na faixa de faixas do Microsoft Paint.](images/controls/checkbox.png)

## <a name="check-box-properties"></a>Propriedades da caixa de seleção

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle caixa de seleção.

Normalmente, uma propriedade da caixa de seleção é atualizada na interface do usuário da faixa de lista ao invalidar o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle caixa de seleção.




| Chave de propriedade | Observações | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a> | Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Se o comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando <code>UI_INVALIDATIONS_VALUE</code> for passada como o valor de <em>flags</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Só pode ser atualizado por meio de invalidação. | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de controle da estrutura de faixa](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação da caixa de seleção**](windowsribbon-element-checkbox.md)
</dt> </dl>

