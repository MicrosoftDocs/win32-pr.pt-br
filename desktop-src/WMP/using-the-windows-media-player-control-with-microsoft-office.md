---
title: Usando o controle do Windows Media Player com Microsoft Office
description: Usando o controle do Windows Media Player com Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, Office
- Modelo de objeto do Windows Media Player, Office
- modelo de objeto, Office
- Windows Media Player Mobile, Office
- Controle ActiveX do Windows Media Player, Office
- Controle ActiveX móvel do Windows Media Player, Office
- Controle ActiveX, Office
- Inserção de documentos do Office
- inserindo, documentos do Office
- Controle ActiveX do Windows Media Player, Excel
- Controle ActiveX móvel do Windows Media Player, Excel
- Controle ActiveX, Excel
- incorporação, planilhas do Excel
- Inserção de planilha do Excel
- Controle ActiveX do Windows Media Player, PowerPoint
- Controle ActiveX móvel do Windows Media Player, PowerPoint
- Controle ActiveX, PowerPoint
- inserindo, apresentações de slides do PowerPoint
- Inserção de apresentação de slides do PowerPoint
- Controle ActiveX do Windows Media Player, Word
- Controle ActiveX móvel do Windows Media Player, Word
- Controle ActiveX, Word
- Inserção de documento do Word
- inserindo, documentos do Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916332"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>Usando o controle do Windows Media Player com Microsoft Office

Esta seção descreve como inserir o controle ActiveX do Windows Media Player 9 Series ou posterior em vários documentos criados usando o Microsoft Office XP.

No Microsoft Word, Excel e PowerPoint®, você insere o controle selecionando **objeto** no menu **Inserir** e, em seguida, escolhendo **Windows Media Player** na lista de tipos de objetos disponíveis. O controle do Windows Media Player aparece no documento no local atual. Você pode selecionar **Formatar controle** ( **Formatar objeto** no Excel) no menu de atalho do controle para ajustar o layout, o estilo de disposição do texto e outras opções de formato. No Word e no Excel, você deve estar no modo de design para fazer isso.

Depois de posicionar e formatar o controle, você poderá configurá-lo usando a caixa de diálogo de **Propriedades** , que pode ser acessada na **Toolbox Control** ou no menu de atalho no modo de design para Word e Excel. Aqui você pode especificar as propriedades básicas de controle do Player, como o nome do controle, a URL de um arquivo de mídia digital e o modo de interface do usuário. A definição da propriedade **UIMODE** como "None" oculta tudo no controle, exceto a janela de vídeo ou visualização, permitindo que você adicione seus próprios botões e escreva o código de script usando Visual Basic for Applications (VBA) para manipular os cliques de botão e os eventos de controle do jogador.

Na caixa de diálogo **Propriedades** básicas, você também pode acessar a caixa de diálogo Propriedades de controle mais sofisticadas do **Windows Media Player** clicando duas vezes na linha "(personalizado)" ou clicando no botão de reticências ("...") depois de selecionar essa linha. Nessa caixa de diálogo, você pode modificar todas as propriedades de controle do Player disponíveis.

> [!Note]  
> Você deve ter cuidado para não tomar ações em manipuladores de eventos de controle do Player que resultarão no controle que está sendo destruído. Por exemplo, se você inserir o controle do Windows Media Player em um slide em uma apresentação do PowerPoint, não chame o **próximo** método do PowerPoint do evento **openStateChange** do Player ou de qualquer outro evento.

 

> [!Note]  
> Além disso, você não deve definir a propriedade **Player. URL** de um manipulador de eventos de controle de jogador.

 

No FrontPage, adicione o controle do Windows Media Player a uma página da Web selecionando **componente da Internet** no menu **Inserir** . Na caixa de diálogo **Inserir componente da Web** , selecione **controles avançados** na lista **tipo de componente** e, em seguida, selecione **controle ActiveX** na lista de opções de controle. Na próxima janela da caixa de diálogo, selecione **Windows Media Player**. Se não estiver listado, clique em **Personalizar** e marque a caixa de seleção **Windows Media Player** na lista **controle** .

Depois que o controle do Windows Media Player é inserido, você pode posicioná-lo e redimensioná-lo e modificar suas propriedades selecionando **Propriedades do controle ActiveX** no menu de atalho do controle. Na exibição HTML, os valores de propriedade que você especifica aparecem no elemento OBJECT que representa o controle do Windows Media Player. O nome do objeto aparece como o atributo de ID e as propriedades de controle aparecem como marcas PARAM. O nome do objeto fornece acesso ao modelo de objeto de controle do Windows Media Player, que você pode programar usando o Microsoft JScript. Para obter mais informações, consulte [usando o controle do Windows Media Player em uma página da Web](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de controle do Player**](player-control-guide.md)
</dt> </dl>

 

 




