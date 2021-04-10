---
description: 'Saiba mais sobre: colunas'
title: Colunas
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090900"
---
# <a name="columns"></a><span data-ttu-id="14ed8-103">Colunas</span><span class="sxs-lookup"><span data-stu-id="14ed8-103">Columns</span></span>


<span data-ttu-id="14ed8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="14ed8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="columns"></a><span data-ttu-id="14ed8-105">Colunas</span><span class="sxs-lookup"><span data-stu-id="14ed8-105">Columns</span></span>

<span data-ttu-id="14ed8-106">Uma tabela pode ser criada com um conjunto inicial de colunas chamando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou sem um conjunto inicial de colunas chamando [JetCreateTable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="14ed8-106">A table can be created either with an initial set of columns by calling [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or without an initial set of columns by calling [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="14ed8-107">As tabelas no ESE podem conter até 127 colunas de comprimento fixo, 128 colunas de comprimento variável e 64.993 colunas marcadas.</span><span class="sxs-lookup"><span data-stu-id="14ed8-107">Tables in ESE can contain up to 127 fixed-length columns, 128 variable-length columns, and 64,993 tagged columns.</span></span> <span data-ttu-id="14ed8-108">As colunas são identificadas por seu nome e ID e podem ser adicionadas dinamicamente à tabela com [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="14ed8-108">Columns are identified by their name and ID and can be dynamically added to the table with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="14ed8-109">As colunas são criadas com um tipo de dados específico e um conjunto opcional de atributos, como se a coluna tem comprimento fixo ou se pode ser nula ou não.</span><span class="sxs-lookup"><span data-stu-id="14ed8-109">Columns are created with a specific data type and an optional set of attributes, such as whether the column is fixed-length or whether it can be NULL or not.</span></span>

<span data-ttu-id="14ed8-110">O tipo de uma coluna determina os dados que podem ser armazenados na coluna e muitas das propriedades da coluna, incluindo sua ordem de indexação.</span><span class="sxs-lookup"><span data-stu-id="14ed8-110">The type of a column determines the data that may be stored in the column and many of the properties of the column, including its order for indexing.</span></span> <span data-ttu-id="14ed8-111">O ESE dá suporte a uma ampla gama de tipos de coluna, variando de tamanho de 1 a 2 GB (2146483647 caracteres ASCII ou 1073741823 caracteres Unicode).</span><span class="sxs-lookup"><span data-stu-id="14ed8-111">ESE supports a wide range of column types, ranging in size from 1 bit to 2 GB (2146483647 ASCII characters or 1073741823 Unicode characters).</span></span> <span data-ttu-id="14ed8-112">Para obter uma lista completa dos tipos de dados de coluna com suporte pelo ESE, consulte o tópico [JET_COLTYP](./jet-coltyp.md) .</span><span class="sxs-lookup"><span data-stu-id="14ed8-112">For a complete list of the column data types supported by ESE, see the [JET_COLTYP](./jet-coltyp.md) topic.</span></span> <span data-ttu-id="14ed8-113">Os tópicos a seguir discutem alguns dos tipos de colunas com suporte no ESE:</span><span class="sxs-lookup"><span data-stu-id="14ed8-113">The topics below discuss a few of the columns types supported by ESE:</span></span>

  - [<span data-ttu-id="14ed8-114">Colunas marcadas, fixas e variáveis</span><span class="sxs-lookup"><span data-stu-id="14ed8-114">Tagged, Fixed and Variable Columns</span></span>](./tagged-fixed-and-variable-columns.md)

  - [<span data-ttu-id="14ed8-115">Colunas de versão, incremento automático e caução</span><span class="sxs-lookup"><span data-stu-id="14ed8-115">Version, Auto-Increment and Escrow Columns</span></span>](./version-auto-increment-and-escrow-columns.md)

  - [<span data-ttu-id="14ed8-116">Colunas de valor longo</span><span class="sxs-lookup"><span data-stu-id="14ed8-116">Long Value Columns</span></span>](./long-value-columns.md)

  - [<span data-ttu-id="14ed8-117">Colunas esparsas com valores múltiplos</span><span class="sxs-lookup"><span data-stu-id="14ed8-117">Multi-Valued Sparse Columns</span></span>](./multi-valued-sparse-columns.md)

  - [<span data-ttu-id="14ed8-118">Colunas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="14ed8-118">User Defined Columns</span></span>](./user-defined-columns.md)

  - [<span data-ttu-id="14ed8-119">Usando colunas em uma tabela</span><span class="sxs-lookup"><span data-stu-id="14ed8-119">Using Columns in a Table</span></span>](./using-columns-in-a-table.md)
