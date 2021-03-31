---
description: Os autores devem estar cientes das tabelas e dos campos na lista a seguir ao projetar sua interface do usuário para estar em conformidade com as diretrizes de Acessibilidade Ativa.
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: Acessibilidade (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46325c11337ef1e1db6f2da5728f06f9d4ee0649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828094"
---
# <a name="accessibility-windows-installer"></a>Acessibilidade (Windows Installer)

Os autores devem estar cientes das tabelas e dos campos na lista a seguir ao projetar sua interface do usuário para estar em conformidade com as diretrizes de Acessibilidade Ativa. A interface do usuário de um pacote do instalador deve facilitar a acessibilidade do aplicativo ou produto a todos os usuários.

-   O texto da dica de ferramenta está contido na coluna ajuda da [tabela de controle](control-table.md). Esse texto é mostrado por leitores de tela para controles que contêm uma imagem.
-   O campo de texto da [tabela de controle](control-table.md) para os controles [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [directorylist](directorylist-control.md) e [SelectionTree](selectiontree-control.md) nunca é exibido. Em vez disso, ele pode ser lido por utilitários de revisão de tela como a descrição do controle. As pessoas que não podem usar as informações visuais na tela podem interpretar as informações com a ajuda de um utilitário de revisão de tela. Os utilitários de revisão de tela (também chamados de programas de leitor de tela ou utilitários de acesso de fala) pegam as informações exibidas na tela e direcionam-no por meio de mídia alternativa, como a fala sintetizada ou uma exibição braile atualizável.
-   Os controles nas caixas de diálogo devem ser vinculados usando o \_ próximo campo de controle da [tabela de controle](control-table.md). Os controles precisam ser criados de forma que todos possam ser acessados usando a tecla TAB.
-   As teclas de atalho devem ser fornecidas para obter acesso diretamente aos controles.
-   A cor do texto exibida na interface do usuário é definida na [tabela TextStyle](textstyle-table.md). Se a cor do texto escolhida estiver muito próxima do plano de fundo, a opção de cor do texto será ignorada.
-   O tamanho e a fonte do texto são definidos na [tabela TextStyle](textstyle-table.md). Tamanhos de fonte maiores devem ser usados para pacotes destinados ao mercado asiático. Por exemplo, um tamanho de fonte de 10 pontos que é legível para texto em inglês não pode necessariamente ser verdadeiro para chinês.
-   Para os controles [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) ou [VolumeSelectCombo](volumeselectcombo-control.md), os leitores de tela pegam accName e accKeyboardShortcut de um [controle de texto](text-control.md) que deve preceder o controle na \_ próxima sequência de controle da caixa de diálogo. O leitor de tela usa accName do campo de texto do controle de texto e accKeyboardShortcut do atalho de teclado no campo de texto, se houver um atalho.
-   Como o texto estático não pode assumir o foco, um [controle de texto](text-control.md) que descreve um controle [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) ou [VolumeSelectCombo](volumeselectcombo-control.md) deve ser tornado o primeiro controle na caixa de diálogo para garantir a compatibilidade com leitores de tela.
-   Para um [controle de pressão](pushbutton-control.md) que exibe um ícone ou imagem de bitmap, AccName e accKeyboardShortcut são especificados no campo ajuda do registro da [tabela de controle](control-table.md) à esquerda do \| separador.
-   Evite o uso de controles de texto sobre bitmaps brancos, pois, em Alto Contraste preto, o texto pode se tornar invisível.
-   Não coloque um controle de texto preto em um plano de fundo que seja uma imagem de bitmap em branco. Esse texto não é visível para um usuário que altera a exibição do Windows para Alto Contraste preto.
-   Não coloque um controle de texto branco em um plano de fundo que seja uma imagem de bitmap preta. Esse texto não é visível para um usuário que altera a exibição do Windows para Alto Contraste branco.
-   Não coloque controles de [texto](text-control.md) transparentes na parte superior dos bitmaps coloridos. O texto pode não estar visível se o usuário alterar o esquema de cores de exibição. Por exemplo, o texto pode se tornar invisível se o usuário definir o parâmetro de alto contraste para acessibilidade.
-   Observe que o foco em uma caixa de diálogo não é tabulado para um controle de grupo de [botões de opção](radiobuttongroup-control.md) até que um dos botões no grupo tenha sido selecionado. Para colocar a guia foco nesse grupo de botões, especifique um dos botões como uma configuração padrão para o controle.
-   Para fornecer programas de leitor de tela com texto descritivo extra sobre um [controle de botão de opção](radiobuttongroup-control.md). Siga o exemplo fornecido em [adicionando texto extra a botões de opção](adding-extra-text-to-radio-buttons.md).
-   O tamanho relativo de caixas de diálogo, controles e fontes pode ser alterado dependendo do tamanho da fonte escolhido. Para obter mais informações, consulte [unidades de instalação](installer-units.md). Para garantir a exibição correta de texto e controles na interface do usuário, os desenvolvedores de instalação devem sempre testar seus aplicativos usando todos os tamanhos de fonte que podem ser usados.

 

 



