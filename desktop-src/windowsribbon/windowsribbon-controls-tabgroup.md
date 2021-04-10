---
title: Grupo de guias
description: Um grupo de guias é um controle contextual que é oculto ou exibido em tempo de execução, com base em um documento ou em um estado de espaço de trabalho. O grupo de guias contém um conjunto de controles de guia relacionados ao contexto.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294351"
---
# <a name="tab-group"></a>Grupo de guias

Um grupo de guias é um controle contextual que é oculto ou exibido em tempo de execução, com base em um documento ou em um estado de espaço de trabalho. O grupo de guias contém um conjunto de controles de [guia](windowsribbon-controls-tab.md) relacionados ao contexto.

-   [Detalhes](#details)
-   [Propriedades do grupo de guias](#tab-group-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

Normalmente, um grupo de guias é exibido durante os Estados específicos do documento ou do espaço de trabalho, como quando um usuário seleciona um determinado tipo de objeto. Por exemplo, a seleção de uma imagem contida no cabeçalho de uma tabela pode exigir que várias guias contextuais sejam exibidas, expondo a funcionalidade de tabela e imagem.

> [!IMPORTANT]
> Um grupo de guias não dá suporte A [modos de aplicativo](ribbon-applicationmodes.md). No entanto, os controles de [guia](windowsribbon-controls-tab.md) individuais dentro de um grupo de guias podem.

 

A captura de tela a seguir mostra uma [guia](windowsribbon-controls-tab.md) contextual do Paint do Windows 7.

![captura de tela que mostra um controle de guia contextual.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>Propriedades do grupo de guias

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de grupo de guias.

Normalmente, uma propriedade de grupo de guias é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de grupo de guias.



| Chave de propriedade                                                                                     | Observações                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ContextAvailable PKEY \_ UI](windowsribbon-reference-properties-uipkey-contextavailable.md)     | Dá suporte a [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [\_KeyTip PKEY \_ UI](windowsribbon-reference-properties-uipkey-keytip.md)                         | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_Rótulo de PKEY da interface do usuário \_](windowsribbon-reference-properties-uipkey-label.md)                           | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_TooltipDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_TooltipTitle PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação TabGroup**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 