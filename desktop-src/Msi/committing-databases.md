---
description: As alterações feitas no banco de dados de instalação não são gravadas no banco de dados até que você chame MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Confirmando bancos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829192"
---
# <a name="committing-databases"></a>Confirmando bancos de dados

As alterações feitas no banco de dados de instalação não são gravadas no banco de dados até que você chame [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

**Para garantir que as alterações feitas em um banco de dados sejam finalizadas**

1.  Verifique se uma tabela será gravada quando você chamar [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) chamando [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).
2.  Chame a função [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) para finalizar as alterações no banco de dados.

As alterações feitas em um banco de dados são acumuladas e não são refletidas no banco de dados real até que você chame [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Colunas ou linhas temporárias não são confirmadas no banco de dados. Quando um banco de dados é fechado, todas as alterações feitas desde a última **MsiDatabaseCommit** são revertidas automaticamente.

 

 



