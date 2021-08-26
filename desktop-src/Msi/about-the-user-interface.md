---
description: Windows O instalador contém a funcionalidade que permite que os desenvolvedores de pacotes de instalação autor de uma GUI (interface gráfica do usuário) que é exibida para o usuário final durante a instalação.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: Sobre o Interface do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff4613e82bc25a0a9555904a6bab276b31e16642186401bbb5cc0caff58e973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996976"
---
# <a name="about-the-user-interface"></a>Sobre o Interface do Usuário

Windows O instalador contém a funcionalidade que permite que os desenvolvedores de pacotes de instalação autor de uma GUI (interface gráfica do usuário) que é exibida para o usuário final durante a instalação. Essa interface do usuário pode exibir o [comportamento do assistente de interface](user-interface-wizard-behavior.md)do usuário, exibir caixas de diálogo e botões e apresentar controles interativos aos usuários durante a instalação.

A interface do usuário interna do instalador é gerenciada e controlada por meio de um conjunto de tabelas de banco de dados Windows instalador em si. O instalador fornece apenas um pequeno conjunto de caixas de diálogo padrão que se destinam a lidar com mensagens de erro e informações. Todas as caixas de diálogo personalizadas devem ser criadas pelo autor do pacote.

Não há nenhuma API Windows instalador específica para permitir que um autor de pacote crie uma interface do usuário programaticamente. É possível usar a API do Microsoft Windows para criar uma interface do usuário programaticamente; no entanto, é recomendável que os autores do pacote usem a interface do usuário interna fornecida.

Os autores do pacote do instalador criam caixas de diálogo personalizadas inserindo o nome da caixa de diálogo personalizada na coluna "Diálogo" da tabela de diálogo e especificando o tamanho, a posição e outros atributos usando as \_ colunas restantes.

Windows O instalador também implementa vários controles padrão que um autor de pacote pode colocar nas caixas de diálogo. Nem todos os controles Windows microsoft padrão estão disponíveis e controles personalizados não podem ser criados para uso com a interface do usuário do instalador.

Os controles são criados em uma caixa de diálogo específica inserindo o nome da caixa de diálogo, a chave primária para a entrada da caixa de diálogo na tabela de diálogo, no segundo campo da tabela de controle e especificando o tamanho, a posição e outros atributos do controle usando as colunas restantes.

Os controles ativos devem ser vinculados a um ControlEvent na [tabela ControlEvent](controlevent-table.md) para permitir a interação do usuário com a instalação. Os controles passivos que recebem e exibem informações devem ser inscritos em um ControlEvent apropriado na [tabela EventMapping](eventmapping-table.md).

Para obter mais informações sobre ControlEvents, consulte [Visão geral do ControlEvent.](controlevent-overview.md) Observe que um controle publica um ControlEvent se listado na tabela ControlEvent e assina um evento se listado na tabela EventMapping.

A exibição da interface do usuário do instalador durante a instalação é gerenciada por meio das tabelas de sequência da interface do usuário: [InstallUISequence Table](installuisequence-table.md)e [AdminUISequence Table](adminuisequence-table.md). Uma dessas tabelas de sequência é executada dependendo da ação de nível superior que iniciou a instalação: [INSTALL,](install-action.md) [ADMIN](admin-action.md)ou [ADVERTISE](advertise-action.md).

Para obter mais informações sobre como implementar uma interface do usuário no instalador do [Windows,](using-the-user-interface.md)consulte Usando o Interface do Usuário , o esquema [Interface do Usuário](user-interface-schema.md), bem como os tópicos individuais para caixas de diálogo e controles.

 

 



