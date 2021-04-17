---
description: Use esta diretriz para criar um pacote Windows Installer que contenha mais de 32767 arquivos.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Criando um pacote grande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754650"
---
# <a name="authoring-a-large-package"></a><span data-ttu-id="940bc-103">Criando um pacote grande</span><span class="sxs-lookup"><span data-stu-id="940bc-103">Authoring a Large Package</span></span>

<span data-ttu-id="940bc-104">Use esta diretriz para criar um pacote Windows Installer que contenha mais de 32767 arquivos.</span><span class="sxs-lookup"><span data-stu-id="940bc-104">Use this guideline to author a Windows Installer package that contains more than 32767 files.</span></span>

<span data-ttu-id="940bc-105">Se seu pacote de Windows Installer contiver mais de 32767 arquivos, você deverá alterar o esquema do banco de dados para aumentar o limite das seguintes colunas:</span><span class="sxs-lookup"><span data-stu-id="940bc-105">If your Windows Installer package contains more than 32767 files, you must change the schema of the database to increase the limit of the following columns:</span></span>

-   <span data-ttu-id="940bc-106">A coluna sequence da [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="940bc-106">The Sequence column of the [File table](file-table.md).</span></span>
-   <span data-ttu-id="940bc-107">A coluna LastSequence da [tabela de mídia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="940bc-107">The LastSequence column of the [Media table](media-table.md).</span></span>
-   <span data-ttu-id="940bc-108">A coluna sequence da [tabela patch](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="940bc-108">The Sequence column of the [Patch table](patch-table.md).</span></span>

<span data-ttu-id="940bc-109">Para obter mais informações, consulte [formato de definição de coluna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="940bc-109">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

<span data-ttu-id="940bc-110">**Para aumentar o limite de uma coluna de banco de dados**</span><span class="sxs-lookup"><span data-stu-id="940bc-110">**To increase the limit of a database column**</span></span>

1.  <span data-ttu-id="940bc-111">Exporte a tabela para um arquivo. IDT.</span><span class="sxs-lookup"><span data-stu-id="940bc-111">Export the table to an .idt file.</span></span> <span data-ttu-id="940bc-112">Para obter detalhes, consulte [Msidb.exe](msidb-exe.md), [exportar arquivos](export-files.md)e [importar e exportar](importing-and-exporting.md).</span><span class="sxs-lookup"><span data-stu-id="940bc-112">For details, see [Msidb.exe](msidb-exe.md), [Export Files](export-files.md), and [Importing and Exporting](importing-and-exporting.md).</span></span>
2.  <span data-ttu-id="940bc-113">Edite o arquivo. IDT para alterar o tipo de coluna de i2 para I4 ou de i2 para i4.</span><span class="sxs-lookup"><span data-stu-id="940bc-113">Edit the .idt file to change the column type from i2 to i4, or from I2 to I4.</span></span>
3.  <span data-ttu-id="940bc-114">Exporte a tabela de [ \_ validação](-validation-table.md) para um arquivo. IDT.</span><span class="sxs-lookup"><span data-stu-id="940bc-114">Export the [\_Validation](-validation-table.md) table to an .idt file.</span></span>
4.  <span data-ttu-id="940bc-115">Edite o arquivo. IDT para alterar os valores na coluna MaxValue da tabela de [ \_ validação](-validation-table.md) para acomodar as larguras de coluna aumentadas.</span><span class="sxs-lookup"><span data-stu-id="940bc-115">Edit the .idt file to change the values in the MaxValue column of the [\_Validation](-validation-table.md) table to accommodate the increased column widths.</span></span>
5.  <span data-ttu-id="940bc-116">Importe os arquivos. IDT de volta para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="940bc-116">Import the .idt files back into the database.</span></span>

<span data-ttu-id="940bc-117">Observe que as transformações e os patches não podem ser criados entre dois pacotes com tipos de coluna diferentes.</span><span class="sxs-lookup"><span data-stu-id="940bc-117">Note that transforms and patches cannot be created between two packages with different column types.</span></span>

 

 



