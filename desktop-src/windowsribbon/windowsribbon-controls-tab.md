---
title: Guia (Windows Ribbon Framework)
description: Uma guia contém grupos de controles relacionados.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294734"
---
# <a name="tab-windows-ribbon-framework"></a>Guia (Windows Ribbon Framework)

Uma guia contém [grupos](windowsribbon-controls-group.md) de controles relacionados.

-   [Detalhes](#details)
-   [Guia Propriedades](#tab-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

Há três tipos de guia na estrutura da faixa de tipos.



| Tipo               | Descrição                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guia núcleo**       | Guias principais que organizam as funções padrão do aplicativo.                                                                                                                                                                                                                   |
| **Guia contextual** | Guias que são exibidas durante o documento específico ou Estados do espaço de trabalho. Por exemplo, se um usuário selecionar um determinado tipo de objeto, como uma imagem contida no cabeçalho de uma tabela, várias guias contextuais poderão ser exibidas para expor a funcionalidade de tabela e imagem. |
| **Guia modal**      | Guias de núcleo que são exibidas durante um documento específico ou [modo de aplicativo](ribbon-applicationmodes.md)de espaço de trabalho, como Visualizar impressão.                                                                                                                                        |



 

A captura de tela a seguir mostra uma guia principal do Paint do Windows 7.

![captura de tela que mostra um controle de guia de núcleo.](images/controls/coretab.png)

## <a name="tab-properties"></a>Guia Propriedades

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle guia.

Normalmente, uma Propriedade Tab é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle guia.



| Chave de propriedade                                                                                     | Observações                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [\_Rótulo de PKEY da interface do usuário \_](windowsribbon-reference-properties-uipkey-label.md)                           | Só pode ser atualizado por meio de invalidação. |
| [\_KeyTip PKEY \_ UI](windowsribbon-reference-properties-uipkey-keytip.md)                         | Só pode ser atualizado por meio de invalidação. |
| [\_TooltipDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Só pode ser atualizado por meio de invalidação. |
| [\_TooltipTitle PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Só pode ser atualizado por meio de invalidação. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação de guia**](windowsribbon-element-tab.md)
</dt> </dl>

 

 
