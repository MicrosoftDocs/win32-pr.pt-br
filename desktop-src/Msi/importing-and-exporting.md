---
description: Você pode usar o instalador para importar um arquivo de texto para um banco de dados ativo, bem como para exportar um arquivo de banco de dados para um arquivamento de texto. Isso pode ser útil para sistemas de controle do código-fonte com base em texto.
ms.assetid: 1025da16-9e1f-4fb4-9ce1-f992970eb903
title: Importando e exportando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb778f4a0fe415686c80f2609f63958ae042d920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091019"
---
# <a name="importing-and-exporting"></a><span data-ttu-id="81582-104">Importando e exportando</span><span class="sxs-lookup"><span data-stu-id="81582-104">Importing and Exporting</span></span>

<span data-ttu-id="81582-105">Você pode usar o instalador para importar um arquivo de texto para um banco de dados ativo, bem como para exportar um arquivo de banco de dados para um arquivamento de texto.</span><span class="sxs-lookup"><span data-stu-id="81582-105">You can use the installer to import a text archive into an active database as well as to export a database file to a text archive.</span></span> <span data-ttu-id="81582-106">Isso pode ser útil para sistemas de controle do código-fonte com base em texto.</span><span class="sxs-lookup"><span data-stu-id="81582-106">This can be useful for text-based source control systems.</span></span>

<span data-ttu-id="81582-107">Para importar um arquivo de texto para um banco de dados ativo, chame a função [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) .</span><span class="sxs-lookup"><span data-stu-id="81582-107">To import a text archive into an active database, call the [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) function.</span></span>

<span data-ttu-id="81582-108">Para exportar um arquivo de banco de dados para um arquivo de texto, chame a função [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) .</span><span class="sxs-lookup"><span data-stu-id="81582-108">To export a database file to a text archive, call the [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) function.</span></span>

 

 



