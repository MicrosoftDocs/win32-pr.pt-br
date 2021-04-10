---
description: O exemplo a seguir ilustra como iniciar um arquivo HTML no final de uma instalação.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Usando uma ação personalizada para iniciar um arquivo instalado no final da instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170419"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a>Usando uma ação personalizada para iniciar um arquivo instalado no final da instalação

O exemplo a seguir ilustra como iniciar um arquivo HTML no final de uma instalação. O instalador instala o componente que contém o arquivo e, em seguida, publica um evento de controle no final da instalação para executar uma ação personalizada que abre o arquivo. Essa abordagem pode ser usada para iniciar um tutorial de ajuda no final da primeira instalação de um aplicativo.

O exemplo deve atender às especificações a seguir.

-   O instalador executará a ação personalizada somente se o nível [*completo da interface do usuário*](f-gly.md) for usado para instalar um aplicativo.
-   O instalador executará a ação personalizada somente se o componente que contém o arquivo HTML for instalado para ser executado localmente no computador.
-   A ação personalizada só é executada na primeira instalação do aplicativo.
-   A instalação não falhará se a ação personalizada falhar.

O exemplo inclui um componente hipotético chamado tutorial que controla pelo menos um recurso, um arquivo chamado tutorial.htm. O identificador para esse arquivo na coluna arquivo da tabela de arquivos é tutorial. A discussão a seguir pressupõe que você já criou os recursos exigidos pelo tutorial e fez todas as entradas necessárias no [recurso](feature-table.md), [componente](component-table.md), [arquivo](file-table.md), [diretório](directory-table.md)e tabelas [FeatureComponents](featurecomponents-table.md) para instalar esse componente. Para obter mais informações, consulte [um exemplo de instalação](an-installation-example.md).

Os tópicos a seguir contêm informações sobre como criar ações personalizadas necessárias e adicioná-las a um pacote de instalação.

-   [Criando a ação personalizada de inicialização](authoring-the-launch-custom-action.md)
-   [Adicionando inicialização às tabelas CustomAction e binary](adding-launch-to-the-customaction-and-binary-tables.md)
-   [Adicionar um evento de controle ao final da instalação para executar a inicialização](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



