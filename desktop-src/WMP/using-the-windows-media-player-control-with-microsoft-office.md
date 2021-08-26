---
title: usando o controle de Windows Media Player com Microsoft Office
description: usando o controle de Windows Media Player com Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, inserindo controle de ActiveX
- modelo de objeto Windows Media Player, inserindo ActiveX controle
- modelo de objeto, inserindo ActiveX controle
- Windows Media Player controle de ActiveX móvel, incorporando
- Windows Media Player controle de ActiveX, inserindo
- Windows Media Player controle de ActiveX móvel, incorporando
- controle de ActiveX, inserindo
- Windows Media Player, Office
- modelo de objeto Windows Media Player, Office
- modelo de objeto, Office
- Windows Media Player Móvel, Office
- Windows Media Player ActiveX controle Office
- Windows Media Player controle de ActiveX móvel, Office
- controle de ActiveX, Office
- Office incorporação de documentos
- inserindo, Officendo documentos
- Windows Media Player ActiveX controle Excel
- Windows Media Player controle de ActiveX móvel, Excel
- controle de ActiveX, Excel
- inserindo, Excel planilhas
- inserção de planilha Excel
- Windows Media Player ActiveX controle PowerPoint
- Windows Media Player controle de ActiveX móvel, PowerPoint
- controle de ActiveX, PowerPoint
- inserindo, PowerPoint apresentações de slides
- inserção de apresentação de slides PowerPoint
- Windows Media Player ActiveX controle, Word
- Windows Media Player controle de ActiveX móvel, Word
- controle de ActiveX, Word
- Inserção de documento do Word
- inserindo, documentos do Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418c082cad2793e3ebd676c4d648339f9e637f46c7519efc1b426a44b69ee05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001396"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>usando o controle de Windows Media Player com Microsoft Office

esta seção descreve como inserir o controle de ActiveX do Windows Media Player 9 Series ou posterior em vários documentos criados usando o Microsoft Office XP.

em Microsoft Word, Excel e PowerPoint®, você insere o controle selecionando **objeto** no menu **inserir** e, em seguida, escolhendo **Windows Media Player** na lista de tipos de objetos disponíveis. o controle de Windows Media Player aparece no documento no local atual. você pode selecionar **formatar controle** ( **formatar objeto** no Excel) no menu de atalho do controle para ajustar o layout, o estilo de disposição do texto e outras opções de formato. no Word e Excel, você deve estar no modo de design para fazer isso.

Depois de posicionar e formatar o controle, você poderá configurá-lo usando a caixa de diálogo de **Propriedades** , que pode ser acessada na **Toolbox Control** ou no menu de atalho no modo de design para Word e Excel. Aqui você pode especificar as propriedades básicas de controle do Player, como o nome do controle, a URL de um arquivo de mídia digital e o modo de interface do usuário. a definição da propriedade **uiMode** como "none" oculta tudo no controle, exceto a janela de vídeo ou visualização, permitindo que você adicione seus próprios botões e escreva o código de script usando Visual Basic for Applications (VBA) para manipular os cliques de botão e os eventos de controle do jogador.

na caixa de diálogo **propriedades** básicas, você também pode acessar a caixa de diálogo **propriedades do controle de Windows Media Player** mais sofisticada clicando duas vezes na linha "(personalizado)" ou clicando no botão de reticências ("...") depois de selecionar essa linha. Nessa caixa de diálogo, você pode modificar todas as propriedades de controle do Player disponíveis.

> [!Note]  
> Você deve ter cuidado para não tomar ações em manipuladores de eventos de controle do Player que resultarão no controle que está sendo destruído. por exemplo, se você inserir o controle de Windows Media Player em um slide em uma apresentação de PowerPoint, não chame o método PowerPoint **Next** a partir do evento **openStateChange** do Player ou de qualquer outro evento.

 

> [!Note]  
> Além disso, você não deve definir a propriedade **Player. URL** de um manipulador de eventos de controle de jogador.

 

no FrontPage, adicione o controle de Windows Media Player a uma página **da web** , selecionando componente a partir do menu **inserir** . na caixa de diálogo **inserir componente da Web** , selecione **controles avançados** na lista **tipo de componente** e, em seguida, selecione **ActiveX controle** na lista de opções de controle. na próxima janela da caixa de diálogo, selecione **Windows Media Player**. se não estiver listado, clique em **personalizar** e marque a caixa de seleção **Windows Media Player** na lista de **controles** .

depois que o controle de Windows Media Player é inserido, você pode posicioná-lo e redimensioná-lo e modificar suas propriedades selecionando **ActiveX propriedades de controle** no menu de atalho do controle. na exibição HTML, os valores de propriedade que você especifica aparecem no elemento OBJECT que representa o controle Windows Media Player. O nome do objeto aparece como o atributo de ID e as propriedades de controle aparecem como marcas PARAM. o nome do objeto fornece acesso ao modelo de objeto de controle de Windows Media Player, que você pode programar usando o Microsoft JScript. para obter mais informações, consulte [usando o controle de Windows Media Player em uma página da Web](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de controle do Player**](player-control-guide.md)
</dt> </dl>

 

 




