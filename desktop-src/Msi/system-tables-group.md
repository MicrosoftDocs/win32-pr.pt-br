---
description: As tabelas do grupo tabelas do sistema controlam as tabelas e colunas do banco de dados de instalação.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Grupo de tabelas do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090931"
---
# <a name="system-tables-group"></a>Grupo de tabelas do sistema

As tabelas do grupo tabelas do sistema controlam as tabelas e colunas do banco de dados de instalação.

-   A [ \_ tabela tabelas](-tables-table.md) controla todas as tabelas no banco de dados. Isso inclui tabelas que você pode ter criado para suas próprias ações personalizadas. Consulte esta tabela para descobrir se existe uma tabela.
-   A [ \_ tabela Columns](-columns-table.md) controla as colunas no banco de dados de instalação. As colunas temporárias não são rastreadas atualmente por esta tabela. Consulte esta tabela para saber se existe uma determinada coluna.
-   A [ \_ tabela de fluxos](-streams-table.md) lista os fluxos de dados OLE inseridos.
-   A [ \_ tabela de armazenamentos](-storages-table.md) lista armazenamentos de dados OLE inseridos.
-   A [ \_ tabela de validação](-validation-table.md). A \_ tabela de validação controla os tipos e os intervalos permitidos de cada coluna no banco de dados. A \_ tabela de validação é usada durante o processo de validação do banco de dados para garantir que todas as colunas sejam contadas e tenham os valores corretos. Esta tabela não é enviada com o banco de dados do instalador.

 

 



