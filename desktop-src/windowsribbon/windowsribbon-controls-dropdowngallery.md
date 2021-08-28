---
title: Drop-Down Galeria de Drop-Down
description: A Drop-Down galeria consiste em um botão que, quando clicado, exibe uma listada contendo uma coleção de itens ou comandos mutuamente exclusivos.
ms.assetid: 10644e10-f903-49f6-aecd-1a63d97fe447
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778654126a3845dfd5df90b4a137259c568f24a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481942"
---
# <a name="drop-down-gallery"></a>Drop-Down Galeria de Drop-Down

A Drop-Down galeria consiste em um botão que, quando clicado, exibe uma listada contendo uma coleção de itens ou comandos mutuamente exclusivos.

-   [Detalhes](#details)
-   [Propriedades da Galeria De lista listada](#drop-down-gallery-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

Esse controle é útil para expor itens ou comandos relacionados em que não há nenhum padrão óbvio e os itens individuais podem ser representados por uma imagem, texto ou ambos.

O suporte para barras de alça vertical e de canto, ou alças de recalque, é fornecido por meio do [**elemento DropDownGallery.MenuLayout.**](windowsribbon-element-dropdowngallery-menulayout.md)

A captura de tela a seguir ilustra a Faixa de Opções Drop-Down Galeria no Microsoft Paint.

![captura de tela de um controle dropdowngallery na faixa de opções de pintura da Microsoft.](images/controls/dropdowngallery.png)

## <a name="drop-down-gallery-properties"></a>Drop-Down da Galeria de Drop-Down

A estrutura ribbon define uma coleção de chaves [de propriedade](windowsribbon-reference-properties.md) para o controle Drop-Down Gallery.

Normalmente, uma propriedade Drop-Down Gallery é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [**método IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

A tabela a seguir lista as chaves de propriedade associadas ao controle Drop-Down Gallery.




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

[**Elemento de marcação DropDownGallery**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> <dt>

[Exemplo da Galeria](windowsribbon-gallerysample.md)
</dt> </dl>

