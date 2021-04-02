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
# <a name="committing-databases"></a><span data-ttu-id="070df-103">Confirmando bancos de dados</span><span class="sxs-lookup"><span data-stu-id="070df-103">Committing Databases</span></span>

<span data-ttu-id="070df-104">As alterações feitas no banco de dados de instalação não são gravadas no banco de dados até que você chame [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="070df-104">Changes made to the installation database are not written to the database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span>

<span data-ttu-id="070df-105">**Para garantir que as alterações feitas em um banco de dados sejam finalizadas**</span><span class="sxs-lookup"><span data-stu-id="070df-105">**To ensure changes made in a database are finalized**</span></span>

1.  <span data-ttu-id="070df-106">Verifique se uma tabela será gravada quando você chamar [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) chamando [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span><span class="sxs-lookup"><span data-stu-id="070df-106">Check to see whether a table will be written when you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) by calling [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span></span>
2.  <span data-ttu-id="070df-107">Chame a função [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) para finalizar as alterações no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="070df-107">Call the [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) function to finalize changes to the database.</span></span>

<span data-ttu-id="070df-108">As alterações feitas em um banco de dados são acumuladas e não são refletidas no banco de dados real até que você chame [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="070df-108">Changes made in a database are accumulated and are not reflected in the actual database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="070df-109">Colunas ou linhas temporárias não são confirmadas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="070df-109">Temporary columns or rows are not committed to the database.</span></span> <span data-ttu-id="070df-110">Quando um banco de dados é fechado, todas as alterações feitas desde a última **MsiDatabaseCommit** são revertidas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="070df-110">When a database is closed, all changes made since the last **MsiDatabaseCommit** are automatically rolled back.</span></span>

 

 



