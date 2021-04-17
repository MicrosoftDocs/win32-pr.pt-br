---
description: A \_ tabela SummaryInformation é uma tabela especial usada com o fluxo de informações de resumo. Você pode obter ou definir o fluxo de informações de Resumo de um banco de dados Windows Installer exportando ou importando um arquivo morto de texto chamado \_ SummaryInformation. IDT.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749598"
---
# <a name="_summaryinformation"></a><span data-ttu-id="183fb-104">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="183fb-104">\_SummaryInformation</span></span>

<span data-ttu-id="183fb-105">A \_ tabela SummaryInformation é uma tabela especial usada com o [fluxo de informações de resumo](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="183fb-105">The \_SummaryInformation table is a special table used with the [Summary Information Stream](summary-information-stream.md).</span></span> <span data-ttu-id="183fb-106">Você pode obter ou definir o fluxo de informações de Resumo de um banco de dados Windows Installer exportando ou importando um [arquivo morto de texto](text-archive-files.md) chamado \_ SummaryInformation. IDT.</span><span class="sxs-lookup"><span data-stu-id="183fb-106">You can get or set the Summary Information Stream of a Windows Installer database by exporting or importing a [text archive file](text-archive-files.md) named \_SummaryInformation.idt.</span></span>

<span data-ttu-id="183fb-107">O arquivo. IDT de uma tabela SummaryInformation exportada \_ tem o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="183fb-107">The .idt file of an exported \_SummaryInformation table has the following format.</span></span>

-   <span data-ttu-id="183fb-108">A primeira linha contém os nomes de coluna de tabela separados por tabulações: PropertyId e valor.</span><span class="sxs-lookup"><span data-stu-id="183fb-108">The first row contains the table column names separated by tabs: PropertyId and Value.</span></span> <span data-ttu-id="183fb-109">Consulte o tópico [conjunto de propriedades fluxo de informações de resumo](summary-information-stream-property-set.md) para obter uma lista das propriedades e suas IDs (PID).</span><span class="sxs-lookup"><span data-stu-id="183fb-109">See the [Summary Information Stream Property Set](summary-information-stream-property-set.md) topic for a list of the properties and their ids (PID).</span></span>
-   <span data-ttu-id="183fb-110">A segunda linha contém as definições de coluna separadas por tabulações.</span><span class="sxs-lookup"><span data-stu-id="183fb-110">The second row contains the column definitions separated by tabs.</span></span> <span data-ttu-id="183fb-111">As definições de coluna são especificadas da mesma maneira que no [formato de arquivo](archive-file-format.md). IDT básico.</span><span class="sxs-lookup"><span data-stu-id="183fb-111">The column definitions are specified in the same way as in the basic .idt [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="183fb-112">A coluna PropertyId pode ser um inteiro curto não anulável.</span><span class="sxs-lookup"><span data-stu-id="183fb-112">The PropertyId column can be a non-nullable short integer.</span></span> <span data-ttu-id="183fb-113">A coluna Value pode ser uma cadeia de caracteres 255 de comprimento não anulável.</span><span class="sxs-lookup"><span data-stu-id="183fb-113">The Value column can be a non-nullable localizable string 255 characters long.</span></span>
-   <span data-ttu-id="183fb-114">A terceira linha é o nome da tabela e o nome da coluna de chave primária separados por tabulações: \_ SummaryInformation e PropertyId.</span><span class="sxs-lookup"><span data-stu-id="183fb-114">The third row is the table name and the primary key column name separated by tabs: \_SummaryInformation and PropertyId.</span></span>
-   <span data-ttu-id="183fb-115">As linhas restantes no arquivo representam a PID e o valor associado, separados por tabulações.</span><span class="sxs-lookup"><span data-stu-id="183fb-115">The remaining rows in the file represent the PID and associated value, separated by tabs.</span></span> <span data-ttu-id="183fb-116">A data e a hora em \_ SummaryInformation estão no formato: aaaa/mm/dd hh:: mm:: SS.</span><span class="sxs-lookup"><span data-stu-id="183fb-116">Date and time in\_SummaryInformation are in the format: YYYY/MM/DD hh::mm::ss.</span></span> <span data-ttu-id="183fb-117">Por exemplo, 1999/03/22 15:25:45.</span><span class="sxs-lookup"><span data-stu-id="183fb-117">For example, 1999/03/22 15:25:45.</span></span>

<span data-ttu-id="183fb-118">Veja a seguir um exemplo do [fluxo de informações de resumo](summary-information-stream.md) de um banco de dados no formato. IDT.</span><span class="sxs-lookup"><span data-stu-id="183fb-118">The following is an example of the [Summary Information Stream](summary-information-stream.md) of a database in .idt format.</span></span>

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

<span data-ttu-id="183fb-119">Quando você usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) ou o método de [importação](database-import.md) do objeto de [**banco de dados**](database-object.md) para importar uma tabela de arquivo de texto chamada \_ SummaryInformation para um banco de dados do instalador, você grava o fluxo "05SummaryInformation" no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="183fb-119">When you use [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the [**Database**](database-object.md) object to import a text archive table named \_SummaryInformation into an installer database, you write the "05SummaryInformation" stream in the database.</span></span>

 

 



