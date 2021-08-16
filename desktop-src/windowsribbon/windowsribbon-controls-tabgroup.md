---
title: Grupo de guias
description: Um Grupo de Guias é um controle contextual que é oculto ou exibido em tempo de executar, com base em um documento ou estado do workspace. O Grupo de Guias contém um conjunto de controles Tab relacionados ao contexto.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ddf1c34903f0660f6f5ead5eb76cd17934ac5cc987358f24c32bc127c73706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117851251"
---
# <a name="tab-group"></a>Grupo de guias

Um Grupo de Guias é um controle contextual que é oculto ou exibido em tempo de executar, com base em um documento ou estado do workspace. O Grupo de Guias contém um conjunto de controles [Tab](windowsribbon-controls-tab.md) relacionados ao contexto.

-   [Detalhes](#details)
-   [Propriedades do grupo de guias](#tab-group-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

Normalmente, um Grupo de Guias é exibido durante estados específicos de documento ou workspace, como quando um usuário seleciona um tipo de objeto específico. Por exemplo, a seleção de uma imagem contida no header de uma tabela pode exigir a exibição de várias guias contextuais que expõem a funcionalidade de tabela e imagem.

> [!IMPORTANT]
> Um Grupo de Guias não dá suporte aos [modos de aplicativo](ribbon-applicationmodes.md). No entanto, os controles [tab](windowsribbon-controls-tab.md) individuais em um Grupo de Guias podem.

 

A captura de tela a seguir mostra uma [guia](windowsribbon-controls-tab.md) contextual Windows 7 Paint.

![captura de tela que mostra um controle de tabulação contextual.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>Propriedades do grupo de guias

A estrutura ribbon define uma coleção de chaves [de propriedade para](windowsribbon-reference-properties.md) o controle Grupo de Guias.

Normalmente, uma propriedade Grupo de Guias é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o [**método IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [**método IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

A tabela a seguir lista as chaves de propriedade associadas ao controle Grupo de Guias.



| Chave de propriedade                                                                                     | Observações                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contexto \_ PKEY da \_ interface do usuárioAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md)     | Dá [**suporte a IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) [**e IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) |
| [Dica de \_ tecla PKEY \_ da interface do usuário](windowsribbon-reference-properties-uipkey-keytip.md)                         | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [Rótulo \_ PKEY da interface do \_ usuário](windowsribbon-reference-properties-uipkey-label.md)                           | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [Dica \_ de ferramenta PKEY \_ da interface do usuárioDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [Dica de \_ ferramenta PKEY \_ da interface do usuário](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de Controle da Estrutura de Faixa de Opções](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação TabGroup**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 