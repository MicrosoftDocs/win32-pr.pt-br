---
description: O banco de dados de Windows Installer consiste em muitas tabelas inter-relacionadas que juntos compõem um banco de dados relacional das informações necessárias para instalar um grupo de aplicativos.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Sobre o banco de dados do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828097"
---
# <a name="about-the-installer-database"></a>Sobre o banco de dados do instalador

O banco de dados de Windows Installer consiste em muitas tabelas inter-relacionadas que juntos compõem um banco de dados relacional das informações necessárias para instalar um grupo de aplicativos. Uma vez que o banco de dados é relacional, as tabelas são vinculadas por meio do dado nos valores de chave primária e estrangeira. Isso fornece um método eficiente para alterar o processo de instalação e significa que os usuários podem personalizar mais facilmente um aplicativo ou grupo de aplicativos grande. As tabelas de banco de dados refletem o layout geral de todo o grupo de aplicativos, incluindo:

-   Recursos disponíveis
-   Componentes
-   Relação entre recursos e componentes
-   Configurações necessárias do registro
-   Interface do usuário para o aplicativo

Para criar um banco de dados de instalação, você deve preencher as tabelas com todas as informações sobre os aplicativos e o processo de instalação. A criação manual de todas essas tabelas torna-se uma tarefa grande mesmo para uma instalação de tamanho moderado; Portanto, algumas ferramentas de terceiros estão disponíveis para ajudar na criação do banco de dados do instalador. As seções a seguir descrevem grupos de tabelas de banco de dados relacionadas.

[Grupo de tabelas principais](core-tables-group.md)

[Grupo de tabelas de arquivos](file-tables-group.md)

[Grupo de tabelas do registro](registry-tables-group.md)

[Grupo de tabelas do sistema](system-tables-group.md)

[Grupo de tabelas do localizador](locator-tables-group.md)

[Grupo de tabelas de informações do programa](program-information-tables-group.md)

[Grupo de tabelas de procedimento de instalação](installation-procedure-tables-group.md)

[Legenda do diagrama de relação de entidade](entity-relationship-diagram-legend.md)

[Arquivos mortos de texto](text-archive-files.md)

Para obter uma lista completa de todas as tabelas em um banco de dados de instalação, consulte [tabelas de banco de dados](database-tables.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



