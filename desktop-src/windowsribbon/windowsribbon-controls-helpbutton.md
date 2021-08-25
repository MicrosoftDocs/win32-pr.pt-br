---
title: Botão Ajuda
description: O Botão de Ajuda é um controle que o usuário pode clicar para exibir o sistema de ajuda do aplicativo.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 295b3c7feae2aecada128dadbccd093f654c6a6660a68f4790975aee060aaf61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933376"
---
# <a name="help-button"></a>Botão Ajuda

O Botão de Ajuda é um controle que o usuário pode clicar para exibir o sistema de ajuda do aplicativo.

-   [Detalhes](#details)
-   [Propriedades do botão ajuda](#help-button-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

A captura de tela a seguir ilustra o Botão de Ajuda da Faixa de Opções.

![captura de tela mostrando o botão de ajuda.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Propriedades do botão ajuda

A estrutura da Faixa de Opções define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle Botão de Ajuda.

Normalmente, uma propriedade do Botão de Ajuda é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o [**método IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [**método IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

A tabela a seguir lista as chaves de propriedade associadas ao controle Botão de Ajuda.



| Chave de propriedade                                                                                     | Observações                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Dica de \_ tecla PKEY \_ da interface do usuário](windowsribbon-reference-properties-uipkey-keytip.md)                         | Só pode ser atualizado por meio de invalidação. |
| [Rótulo \_ PKEY da interface do \_ usuário](windowsribbon-reference-properties-uipkey-label.md)                           | Só pode ser atualizado por meio de invalidação. |
| [Dica \_ de ferramenta PKEY \_ da interface do usuárioDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Só pode ser atualizado por meio de invalidação. |
| [Dica de \_ ferramenta PKEY \_ da interface do usuário](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Só pode ser atualizado por meio de invalidação. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de Controle da Estrutura de Faixa de Opções](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento HelpButton**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 