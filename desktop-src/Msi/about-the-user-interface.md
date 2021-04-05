---
description: O Windows Installer contém funcionalidade que permite que os desenvolvedores de pacotes de instalação criem uma GUI (interface gráfica do usuário) que é exibida para o usuário final durante a instalação.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: Sobre a interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8639a19c5ec045d77cb90648323388d5cb6e452
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828095"
---
# <a name="about-the-user-interface"></a>Sobre a interface do usuário

O Windows Installer contém funcionalidade que permite que os desenvolvedores de pacotes de instalação criem uma GUI (interface gráfica do usuário) que é exibida para o usuário final durante a instalação. Essa interface do usuário pode exibir o [comportamento do assistente de interface do usuário](user-interface-wizard-behavior.md), exibir caixas de diálogo e murals e apresentar controles interativos aos usuários durante a instalação.

A interface do usuário interna do instalador é gerenciada e controlada por meio de um conjunto de tabelas de banco de dados dentro Windows Installer si mesma. O instalador fornece apenas um pequeno conjunto de caixas de diálogo padrão que se destinam a lidar com mensagens de erro e informações. Todas as caixas de diálogo personalizadas devem ser criadas pelo autor do pacote.

Não há uma API de Windows Installer específica para permitir que um autor de pacote crie uma interface do usuário programaticamente. É possível usar a API do Microsoft Windows para criar uma interface do usuário de forma programática; no entanto, é recomendável que os autores de pacote usem a interface do usuário interna fornecida.

Os autores do pacote do instalador criam caixas de diálogo personalizadas digitando o nome da caixa de diálogo personalizada na \_ coluna "caixa de diálogo" da tabela de diálogo e especificando o tamanho, a posição e outros atributos usando as colunas restantes.

O Windows Installer também implementa vários controles padrão que um autor de pacote pode inserir nas caixas de diálogo. Nem todos os controles padrão do Microsoft Windows estão disponíveis, e os controles personalizados não podem ser criados para uso com a interface do usuário do instalador.

Os controles são criados em uma caixa de diálogo específica digitando o nome da caixa de diálogo, a chave primária para a entrada da caixa de diálogo na tabela de diálogo, no segundo campo da tabela de controle e especificando o tamanho, a posição e outros atributos do controle usando as colunas restantes.

Os controles ativos devem ser vinculados a um ControlEvent, na [tabela ControlEvent,](controlevent-table.md) para permitir a interação do usuário com a instalação. Controles passivos que recebem e exibem informações devem ser assinados para um ControlEvent, apropriado na [tabela EventMappings](eventmapping-table.md).

Para obter mais informações sobre ControlEvents, consulte [visão geral do ControlEvent,](controlevent-overview.md). Observe que um controle publica um ControlEvent, se listado na tabela ControlEvent, e se inscreve em um evento, se listado na tabela EventMappings.

A exibição da interface do usuário do instalador durante a instalação é gerenciada por meio das tabelas de sequência de interface do usuário: [tabela InstallUISequence](installuisequence-table.md)e [tabela AdminUISequence](adminuisequence-table.md). Uma dessas tabelas de sequência é executada dependendo da ação de nível superior que iniciou a instalação: [instalar](install-action.md), [administrar](admin-action.md)ou [anunciar](advertise-action.md).

Para obter mais informações sobre como implementar uma interface do usuário no Windows Installer, consulte [usando a interface do usuário](using-the-user-interface.md), o [esquema de interface do usuário](user-interface-schema.md), bem como os tópicos individuais para caixas de diálogo e controles.

 

 



