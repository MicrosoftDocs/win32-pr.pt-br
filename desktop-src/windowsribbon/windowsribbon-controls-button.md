---
title: Botão (Windows Ribbon Framework)
description: O botão é um controle no qual o usuário pode clicar para fornecer entrada para um aplicativo.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085046"
---
# <a name="button-windows-ribbon-framework"></a>Botão (Windows Ribbon Framework)

O botão é um controle no qual o usuário pode clicar para fornecer entrada para um aplicativo.

-   [Introdução](#introduction)
-   [Propriedades do botão](#button-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

A captura de tela a seguir contém três exemplos do elemento botão da faixa de opções.

![captura de tela dos controles de botão na faixa de em Microsoft WordPad.](images/controls/button.png)

## <a name="button-properties"></a>Propriedades do botão

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de botão.

Normalmente, uma propriedade Button é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de botão.



| Chave de propriedade                                                                                             | Observações                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interface do usuário \_ PKEY \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md)                               | Dá suporte a [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [\_KeyTip PKEY \_ UI](windowsribbon-reference-properties-uipkey-keytip.md)                                 | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_Rótulo de PKEY da interface do usuário \_](windowsribbon-reference-properties-uipkey-label.md)                                   | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_LabelDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-labeldescription.md)             | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_LargeHighContrastImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_LargeImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-largeimage.md)                         | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_SmallHighContrastImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_SmallImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-smallimage.md)                         | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_TooltipDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_TooltipTitle PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação de botão**](windowsribbon-element-button.md)
</dt> </dl>

 

 
