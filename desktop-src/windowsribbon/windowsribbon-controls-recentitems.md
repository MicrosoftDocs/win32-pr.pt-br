---
title: Itens recentes
description: A lista itens recentes é um painel no menu do aplicativo que exibe os itens usados mais recentemente (MRU) para um aplicativo.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1d67c38e1eb9014cfd3349881ed2849755ebc89489cc925052aa690f54adc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810868"
---
# <a name="recent-items"></a>Itens recentes

A lista itens recentes é um painel no [menu do aplicativo](windowsribbon-controls-applicationmenu.md) que exibe os itens usados mais recentemente (MRU) para um aplicativo.

-   [Detalhes](#details)
-   [Propriedades de itens recentes](#recent-items-properties)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

a captura de tela a seguir ilustra uma lista de itens recentes do WordPad para Windows 7).

![captura de tela da lista de itens recentes na faixa de faixas do Microsoft Paint.](images/controls/recentitems.png)

O [menu do aplicativo](windowsribbon-controls-applicationmenu.md) pode ter no máximo uma lista [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) , representada por um elemento **ApplicationMenu. RecentItems** , para exibir documentos, imagens, filmes e outros projetos em que um usuário está trabalhando. O número de itens listados varia de zero até o número máximo especificado na marcação, com um valor padrão de dez. Os itens recentes são exibidos como uma lista numerada de cadeias de caracteres que indicam nomes de arquivo. É recomendável que a propriedade [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) seja usada para fornecer o caminho completo para o local do arquivo, conforme mostrado na captura de tela a seguir.

![captura de tela de uma lista de itens recentes em um menu de aplicativo.](images/overviews/applicationmenu-menurecentitems.png)

O elemento [**RecentItems**](windowsribbon-element-recentitems.md) tem um atributo *EnablePinning* que, se definido como `true` , exibe um ícone de pino à direita de cada item na lista, conforme mostrado na captura de tela a seguir.

> [!Note]  
> A fixação será habilitada por padrão se o atributo *EnablePinning* não for especificado.

 

![captura de tela de itens recentes fixando em um menu de aplicativo.](images/overviews/applicationmenu-menurecentitemspinned.png)

O algoritmo de fixação destina-se a impedir que os itens caiam na lista de **itens recentes** . O algoritmo produz o seguinte comportamento:

-   Um novo item é sempre adicionado na parte superior da lista de **itens recentes** .
-   Os itens serão movidos para baixo na lista ao longo do tempo. Quando a lista estiver cheia (atingir o número máximo de itens especificados na marcação), os itens mais antigos ficarão na parte inferior da lista à medida que novos itens forem adicionados à parte superior da lista.
-   Se um item já aparecer em algum lugar na lista, mas for acessado novamente, ele voltará para o topo da lista.
-   Se um item for fixado, ele ainda fará a viagem na lista, mas não cairá na parte inferior. Em vez disso, quando a lista estiver cheia, o primeiro item desafixado acima do item fixado será desativado quando um novo item for adicionado à lista.
-   Se o número de itens fixados atingir o número máximo de itens, nenhum novo item será adicionado à lista, até que ele seja desafixado.

## <a name="recent-items-properties"></a>Propriedades de itens recentes

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle itens recentes.

Normalmente, uma propriedade Items recentes é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle itens recentes.



| Chave de propriedade                                                                       | Observações                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [\_KeyTip PKEY \_ UI](windowsribbon-reference-properties-uipkey-keytip.md)           | Só pode ser atualizado por meio de invalidação. |
| [\_RecentItems PKEY \_ UI](windowsribbon-reference-properties-uipkey-recentitems.md) | Só pode ser atualizado por meio de invalidação. |



 

## <a name="remarks"></a>Comentários

o método [IApplicationDocumentLists:: getlist](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) pode ser usado para recuperar a lista MRU Windows Shell para o aplicativo da faixa de faixas. O objeto recuperado por esse método pode então ser usado pelo aplicativo para criar os dados exigidos pela estrutura da faixa de faixas para preencher a lista de **itens recentes** do [menu do aplicativo](windowsribbon-controls-applicationmenu.md).

> [!Note]  
> Ao usar esse método, *ListType* deve ter o valor `ADLT_RECENT` .

 

Para obter um exemplo de como implementar uma lista de itens MRU em um aplicativo da estrutura da faixa de faixas, consulte o [exemplo HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de controle da estrutura de faixa](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação de itens recentes**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 