---
title: In-Ribbon Galeria de In-Ribbon
description: A In-Ribbon é um controle que exibe uma coleção de itens relacionados ou Comandos na Faixa de Opções. Se houver muitos itens na galeria, uma seta de expansão será fornecida para exibir o restante da coleção em um painel expandido.
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713455e962996e2cc1a70b418000d0f94a383174
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479792"
---
# <a name="in-ribbon-gallery"></a>In-Ribbon Galeria de In-Ribbon

A In-Ribbon é um controle que exibe uma coleção de itens relacionados ou Comandos na Faixa de Opções. Se houver muitos itens na galeria, uma seta de expansão será fornecida para exibir o restante da coleção em um painel expandido.

-   [Detalhes](#details)
-   [Propriedades da Galeria na Faixa de Opções](#in-ribbon-gallery-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

A captura de tela a seguir ilustra o controle faixa de In-Ribbon galeria no Microsoft Paint.

![captura de tela de um controle inribbongallery na faixa de opções de pintura da Microsoft.](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a>In-Ribbon da Galeria de In-Ribbon

A estrutura ribbon define uma coleção de chaves [de propriedade](windowsribbon-reference-properties.md) para o controle In-Ribbon Gallery.

Normalmente, uma propriedade In-Ribbon Gallery é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [**método IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

A tabela a seguir lista as chaves de propriedade associadas ao controle In-Ribbon Gallery.




| Chave de propriedade | Observações | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(válido somente para uma galeria de itens)<br /> | Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a><blockquote>[!Note]<br />Se o Comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando for passado como o valor dos <code>UI_INVALIDATIONS_VALUE</code> <em>sinalizadores</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Só pode ser atualizado por meio de invalidação. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Só pode ser atualizado por meio de invalidação. | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de Controle da Estrutura de Faixa de Opções](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento InRibbonGallery**](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> <dt>

[Exemplo da Galeria](windowsribbon-gallerysample.md)
</dt> </dl>

