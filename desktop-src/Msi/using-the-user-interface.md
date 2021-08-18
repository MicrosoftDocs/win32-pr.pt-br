---
description: Esta seção se preocupa principalmente com a forma como os desenvolvedores de pacotes de instalação desautorização de uma interface do usuário de instalação usando o banco de dados do instalador e a interface do usuário interna.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Usando a interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2303ddcdf589b69abb819ab1cdee9060f4918c1bd238e161677da7987300bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995986"
---
# <a name="using-the-user-interface"></a>Usando a interface do usuário

Esta seção se preocupa principalmente com a forma como os desenvolvedores de pacotes de instalação desautorização de uma interface do usuário de instalação usando o banco de dados do instalador e a interface do usuário interna. Para obter mais informações sobre a diferença entre uma interface do usuário interna e externa, consulte [Sobre o Interface do Usuário](about-the-user-interface.md).

Para exibir uma sequência ou uma caixa de diálogo durante a instalação, o nome da caixa de diálogo deve ser inserido na coluna Ação da tabela de sequência de ação apropriada. O nome da caixa de diálogo deve aparecer na tabela [InstallUISequence](installuisequence-table.md) ou [AdminUISequence,](adminuisequence-table.md) dependendo se a interface do usuário está agendada para ser executado na ação [INSTALL,](install-action.md) [ADVERTISE](advertise-action.md)ou [ADMIN](admin-action.md).

Embora o instalador seja compatível com a autorização de caixas de diálogo personalizadas e painéis, também há vários nomes reservados para determinadas sequências de caixa de diálogo. Como o instalador usa esses nomes ao executar determinadas ações, esses nomes só devem ser usados com os tipos de caixas de diálogo para os quais são reservados. Uma lista desses nomes reservados e uma descrição de cada uma das sequências especiais da caixa de diálogo é dada em Caixas [de Diálogo](dialog-boxes.md).

As propriedades de cada caixa de diálogo ou uma caixa de diálogo na interface do usuário devem ser especificadas nas tabelas [Caixa](dialog-table.md) de diálogo e [BillBoard,](billboard-table.md) respectivamente. O estilo de cada caixa de diálogo também deve ser especificado na tabela Diálogo definindo o sinalizador de bit [de estilo da](dialog-style-bits.md) caixa de diálogo.

Controles e texto devem ser adicionados à caixa de diálogo e eles devem ser vinculados a [ControlEvents](controlevent-overview.md)para permitir que o usuário interaja com o processo de instalação. Consulte [Adicionando controles e texto](adding-controls-and-text.md) para obter mais informações sobre como adicionar controles a uma caixa de diálogo.

Windows O manipulador de interface do usuário interno do instalador pode mostrar ou ocultar caixas de diálogo seletivamente para controlar o nível de interatividade do usuário final durante a instalação. Esses níveis de interatividade do usuário final são chamados de completo, reduzido, básico e nenhum. Consulte [Interface do Usuário níveis de dados.](user-interface-levels.md) para uma descrição completa desses UIlevels.

Há dois métodos para definir o nível da interface do usuário. O nível da interface do usuário pode ser definido programaticamente com uma chamada para [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)e o primeiro parâmetro **de MsiSetInternalUI especifica** o nível da interface do usuário. Os desenvolvedores de pacotes também podem definir o nível da interface do usuário usando a opção [de linha de comando](command-line-options.md) "/q".

O comportamento de cada um dos níveis de interface do usuário é determinado pela .msi pelo desenvolvedor do pacote. O autor de uma interface do usuário interna tem flexibilidade em como esses níveis se comportam para um pacote. A disponibilidade desses níveis depende da autoração do pacote de instalação. O autor deve especificar cada caixa de diálogo e controle na interface do usuário nas tabelas Diálogo e Controle.

-   Uma interface do usuário completa normalmente exibe o comportamento do assistente de [interface](user-interface-wizard-behavior.md)do usuário, como cada caixa de diálogo em uma sequência que contém um **botão>>** Próximo. Essa forma de interface do usuário é familiar para muitos usuários e é o tipo mais comum de interface do usuário para um autor criar. O instalador apresenta uma sequência lógica de caixas de diálogo e solicita que o usuário interaja com controles localizados em cada caixa de diálogo.
-   Uma interface do usuário reduzida normalmente suprime a exibição do comportamento do assistente.
-   Uma interface do usuário básica normalmente exibe apenas mensagens de progresso para o usuário.
-   Um nível de interface do usuário Nenhum significa uma instalação silenciosa.

Windows O instalador fornece um indicador de barra de progresso exclusivo no controle [ProgressBar](progressbar-control.md) que exibe ao usuário uma estimativa do tempo total restante até que a instalação seja concluída. Para obter mais informações sobre a barra de progresso, consulte [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).

Os autores da interface do usuário devem facilitar a acessibilidade de seu aplicativo ou produto para todos os usuários. Para saber mais sobre o Acessibilidade Ativa e Windows, consulte [Acessibilidade.](accessibility.md)

Para obter mais informações sobre como autor de uma interface do usuário, consulte Adicionando controles e [texto,](adding-controls-and-text.md) [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), [Authoring Disk Prompt Messages](authoring-disk-prompt-messages.md), Authoring [a Conditional "Please Wait . ." Caixa de](authoring-a-conditional-please-wait-------message-box.md)mensagem e [Visualizando o Interface do Usuário](previewing-the-user-interface.md). Para obter mais informações sobre os painéis de autor, [consulte Exibindo cartazes em uma caixa de diálogo sem modo](displaying-billboards-on-a-modeless-dialog.md)

A partir do Windows 4.5, uma interface do usuário personalizada pode ser inserida no pacote Windows Instalador. Para ver um exemplo de uma interface do usuário personalizada inserida, [consulte Usando uma interface do usuário inserida.](using-an-embedded-ui.md)

 

 



