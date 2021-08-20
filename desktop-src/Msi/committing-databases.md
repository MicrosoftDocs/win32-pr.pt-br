---
description: As alterações feitas no banco de dados de instalação não são escritas no banco de dados até que você chame MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Commitindo bancos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1ab5f4da5b82fb3b6b2ac7d2371bd8046ab87a23d2ef43b6473f7e36a4771a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145345"
---
# <a name="committing-databases"></a>Commitindo bancos de dados

As alterações feitas no banco de dados de instalação não são escritas no banco de dados até que você chame [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

**Para garantir que as alterações feitas em um banco de dados sejam finalizadas**

1.  Verifique se uma tabela será escrita quando você chamar [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) chamando [**MsiDatabaseIsTablePersistent.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta)
2.  Chame a [**função MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) para finalizar as alterações no banco de dados.

As alterações feitas em um banco de dados são acumuladas e não são refletidas no banco de dados real até que você chame [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Colunas ou linhas temporárias não são comprometidas com o banco de dados. Quando um banco de dados é fechado, todas as alterações feitas desde o **último MsiDatabaseCommit** são automaticamente recompodas.

 

 



