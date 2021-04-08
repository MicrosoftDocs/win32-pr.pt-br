---
description: Os registros são uma maneira de se comunicar entre os nós em um grafo ou membros de um grupo.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922243"
---
# <a name="records"></a>Registros

Os registros são uma maneira de se comunicar entre os nós em um grafo ou membros de um grupo. Um registro consiste nas duas partes a seguir:

-   Cabeçalho de registro
-   Conteúdo de dados opaco específico

O cabeçalho contém informações sobre o registro, incluindo a versão, o criador e o tipo de dados que estão sendo publicados. O cabeçalho também contém um campo atributos XML que permite que os aplicativos adicionem atributos de nome-valor que descrevem os dados e pesquisem com eficiência o banco de dados de registro para obter registros específicos que foram publicados anteriormente. O conteúdo são os dados definidos pelo aplicativo e é opaco para a infraestrutura do par.

Quando um registro é publicado, ele (cabeçalho e dados) é inundado em todo o grafo ou grupo. Os pares sincronizados recebem esses dados e os armazenam em um banco de dados local. Os pares não sincronizados e offline recebem os dados na próxima vez que se conectarem e sincronizarem com o grafo ou o grupo de pares.

Para obter informações sobre como trabalhar com registros, consulte os seguintes tópicos:

-   [Dependências de registro](record-dependencies.md)
-   [Gerenciamento de registros](record-management.md)
-   [Esquema de atributo de registro](record-attribute-schema.md)
-   [Gravar formato de consulta de pesquisa](record-search-query-format.md)

 

 



