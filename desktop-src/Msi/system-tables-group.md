---
description: As tabelas do grupo de tabelas do sistema acompanham as tabelas e colunas do banco de dados de instalação.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Grupo de Tabelas do Sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c05bfd06bcff049d2aea847a2bb8d0c4c3fc3d1443a615f75912ac7d4f86d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623915"
---
# <a name="system-tables-group"></a>Grupo de Tabelas do Sistema

As tabelas do grupo de tabelas do sistema acompanham as tabelas e colunas do banco de dados de instalação.

-   A [ \_ tabela Tabelas](-tables-table.md) rastreia todas as tabelas no banco de dados. Isso inclui tabelas que você pode ter criado para suas próprias ações personalizadas. Consulte esta tabela para descobrir se existe uma tabela.
-   A [ \_ tabela Colunas rastreia](-columns-table.md) colunas no banco de dados de instalação. Atualmente, as colunas temporárias não são rastreadas por esta tabela. Consulte esta tabela para descobrir se uma determinada coluna existe.
-   A [ \_ Fluxos lista](-streams-table.md) fluxos de dados OLE inseridos.
-   A [ \_ tabela Armazenamentos lista](-storages-table.md) os armazenamentos de dados OLE inseridos.
-   A [ \_ tabela Validação](-validation-table.md). A \_ tabela Validação rastreia os tipos e os intervalos permitidos de cada coluna no banco de dados. A tabela Validação é usada durante o processo de validação do banco de dados para garantir que todas as colunas sejam \_ contabiladas e tenham os valores corretos. Esta tabela não é enviada com o banco de dados do instalador.

 

 



