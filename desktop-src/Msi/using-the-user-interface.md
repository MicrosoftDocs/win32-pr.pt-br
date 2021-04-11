---
description: Esta seção se preocupa principalmente com a forma como os desenvolvedores de pacotes de instalação criam uma interface do usuário de instalação (IU) usando o banco de dados do instalador e a interface de usuário interna.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Usando a interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714d41ab6b91bb0f3ce519887f7004f919c5c6b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169518"
---
# <a name="using-the-user-interface"></a>Usando a interface do usuário

Esta seção se preocupa principalmente com a forma como os desenvolvedores de pacotes de instalação criam uma interface do usuário de instalação (IU) usando o banco de dados do instalador e a interface de usuário interna. Para obter mais informações sobre a diferença entre uma interface de usuário interna e externa, consulte [sobre a interface do usuário](about-the-user-interface.md).

Para exibir uma sequência de caixa de diálogo ou um mural durante a instalação, o nome da caixa de diálogo deve ser inserido na coluna ação da tabela de sequência de ação apropriada. O nome da caixa de diálogo deve aparecer na tabela [InstallUISequence](installuisequence-table.md) ou [AdminUISequence](adminuisequence-table.md) dependendo se a interface do usuário está agendada para ser executada sob a ação [instalar](install-action.md), [anunciar](advertise-action.md)ou [administrador](admin-action.md).

Embora o instalador ofereça suporte à criação de caixas de diálogo e de murals personalizados, também há vários nomes reservados para determinadas sequências de caixas de diálogo. Como o instalador usa esses nomes ao executar determinadas ações, esses nomes só devem ser usados com os tipos de caixas de diálogo para os quais estão reservados. Uma lista desses nomes reservados e uma descrição de cada uma das sequências de caixas de diálogo especiais é fornecida nas [caixas de diálogo](dialog-boxes.md).

As propriedades de cada caixa de diálogo ou mensagem na interface do usuário devem ser especificadas nas tabelas de [diálogo](dialog-table.md) e de [mural](billboard-table.md) , respectivamente. O estilo de cada caixa de diálogo também deve ser especificado na tabela de diálogo, definindo o sinalizador de [bits de estilo da caixa de diálogo](dialog-style-bits.md) .

Os controles e o texto devem ser adicionados à caixa de diálogo, e eles devem estar vinculados a [ControlEvents](controlevent-overview.md), para permitir que o usuário interaja com o processo de instalação. Consulte [adicionando controles e texto](adding-controls-and-text.md) para obter mais informações sobre como adicionar controles a uma caixa de diálogo.

Windows Installer manipulador de interface do usuário interno pode mostrar ou ocultar seletivamente caixas de diálogo para controlar o nível de interatividade do usuário final durante a instalação. Esses níveis de interatividade de usuário final são referidos como Full, Reduced, Basic e None. Consulte [níveis de interface do usuário](user-interface-levels.md). para obter uma descrição completa desses UIlevels.

Há dois métodos para definir o nível de interface do usuário. O nível da interface do usuário pode ser definido programaticamente com uma chamada para [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui), e o primeiro parâmetro de **MsiSetInternalUI** especifica o nível da interface do usuário. Os desenvolvedores de pacotes também podem definir o nível de interface do usuário usando a [opção de linha de comando](command-line-options.md) "/q".

O comportamento de cada um dos níveis de interface do usuário é determinado pela criação do arquivo. msi pelo desenvolvedor do pacote. O autor de uma interface do usuário interna tem flexibilidade em como esses níveis se comportam para um pacote. A disponibilidade desses níveis depende da criação do pacote de instalação. O autor deve especificar cada caixa de diálogo e controle na interface do usuário nas tabelas de diálogo e controle.

-   Normalmente, uma interface do usuário completa exibe o [comportamento do assistente de interface](user-interface-wizard-behavior.md), como cada caixa de diálogo em uma sequência contendo um botão de **>>avançar** . Essa forma de interface do usuário é familiar para muitos usuários e é o tipo mais comum de interface do usuário para criar um autor. O instalador apresenta uma sequência lógica de caixas de diálogo e solicita que o usuário interaja com controles localizados em cada caixa de diálogo.
-   Uma interface do usuário reduzida normalmente suprime a exibição do comportamento do assistente.
-   Uma interface do usuário básica normalmente exibe apenas mensagens de progresso para o usuário.
-   Um nível de interface de usuário nenhum significa uma instalação silenciosa.

Windows Installer fornece um indicador de barra de progresso exclusivo no [controle ProgressBar](progressbar-control.md) que exibe ao usuário uma estimativa do tempo total restante até que a instalação seja concluída. Para obter mais informações sobre a barra de progresso, consulte [criando um controle ProgressBar](authoring-a-progressbar-control.md).

Os autores da interface do usuário devem facilitar a acessibilidade de seus aplicativos ou produtos para todos os usuários. Para saber mais sobre Acessibilidade Ativa e Windows Installer, consulte [acessibilidade](accessibility.md).

Para obter mais informações sobre como criar uma interface do usuário, consulte [adicionando controles e texto](adding-controls-and-text.md), [criando um controle ProgressBar](authoring-a-progressbar-control.md), [Criando mensagens de prompt de disco](authoring-disk-prompt-messages.md), [criando uma condicional "Aguarde...". Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md)e [visualizando a interface do usuário](previewing-the-user-interface.md). Para obter mais informações sobre autores de autor, consulte [exibindo os murals em uma caixa de diálogo sem janela restrita](displaying-billboards-on-a-modeless-dialog.md)

A partir do Windows Installer 4,5, uma interface do usuário personalizada pode ser inserida no pacote Windows Installer. Para obter um exemplo de uma interface do usuário personalizada inserida, consulte [usando uma interface do usuário inserida](using-an-embedded-ui.md).

 

 



