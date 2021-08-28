---
title: grupo (Windows estrutura da faixa de faixas)
description: O grupo organiza comandos e controles relacionados em uma guia.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c153f8cd9d1fc0d2d2bdbaabab0b2e15e099e50d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467413"
---
# <a name="group-windows-ribbon-framework"></a>grupo (Windows estrutura da faixa de faixas)

O grupo organiza comandos e controles relacionados em uma [guia](windowsribbon-controls-tab.md).

-   [Detalhes](#details)
-   [Propriedades do grupo](#group-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

A captura de tela a seguir ilustra o controle de grupo da faixa de opções.

![captura de tela com textos explicativos mostrando um grupo.](images/controls/group.png)

## <a name="group-properties"></a>Propriedades do grupo

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de grupo.

Normalmente, uma propriedade de grupo é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de grupo.




| Chave de propriedade | Observações | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Só pode ser atualizado por meio de invalidação.<blockquote>[!Note]<br />A estrutura requer que o valor de <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> para um controle de grupo comece com a letra maiúscula Z. Se o valor fornecido pelo aplicativo no método de retorno de chamada <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler:: updateproperty</strong></a> não começar com a letra Z, esse valor será ignorado e um valor será gerado pela estrutura em vez disso. O valor da estrutura é a letra Z seguida de um valor numérico começando em 1 e aumentando sequencialmente, conforme necessário, para os controles de grupo subsequentes (Z1, Z2,..., ZX).</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Só pode ser atualizado por meio de invalidação. | 
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

[**Elemento Group**](windowsribbon-element-group.md)
</dt> </dl>

