---
description: Um arquivo morto de texto para um banco de dados Windows Installer transporta uma extensão de nome de arquivo. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato de arquivo morto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828065"
---
# <a name="archive-file-format"></a><span data-ttu-id="2ac05-103">Formato de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="2ac05-103">Archive File Format</span></span>

<span data-ttu-id="2ac05-104">Um [arquivo morto de texto](text-archive-files.md) para um banco de dados Windows Installer transporta uma extensão de nome de arquivo. IDT.</span><span class="sxs-lookup"><span data-stu-id="2ac05-104">A [text archive file](text-archive-files.md) for a Windows Installer database carries an .idt file name extension.</span></span> <span data-ttu-id="2ac05-105">Quando um banco de dados inteiro é exportado para arquivos mortos, cada tabela no banco de dados tem um arquivo. IDT separado.</span><span class="sxs-lookup"><span data-stu-id="2ac05-105">When an entire database is exported to archive files, each table in the database has a separate .idt file.</span></span> <span data-ttu-id="2ac05-106">Se uma tabela contiver uma coluna de fluxo, cada fluxo na tabela será representado por um arquivo com uma extensão de nome de arquivo. IBD.</span><span class="sxs-lookup"><span data-stu-id="2ac05-106">If a table contains a stream column, each stream in the table is represented by a file with an .ibd file name extension.</span></span> <span data-ttu-id="2ac05-107">Os arquivos. IBD são armazenados em uma pasta com o mesmo nome que a tabela.</span><span class="sxs-lookup"><span data-stu-id="2ac05-107">The .ibd files are stored in a folder with the same name as the table.</span></span>

## <a name="idt-file-format"></a><span data-ttu-id="2ac05-108">Formato de arquivo. IDT</span><span class="sxs-lookup"><span data-stu-id="2ac05-108">.idt File Format</span></span>

<span data-ttu-id="2ac05-109">O arquivo. IDT de uma tabela de banco de dados exportada que contém apenas caracteres ASCII tem o seguinte formato básico.</span><span class="sxs-lookup"><span data-stu-id="2ac05-109">The .idt file of an exported database table that contains only ASCII characters has the following basic format.</span></span>

-   <span data-ttu-id="2ac05-110">A primeira linha contém os nomes de coluna de tabela separados por tabulações.</span><span class="sxs-lookup"><span data-stu-id="2ac05-110">The first row contains the table column names separated by tabs.</span></span>
-   <span data-ttu-id="2ac05-111">A segunda linha contém as definições de coluna separadas por tabulações.</span><span class="sxs-lookup"><span data-stu-id="2ac05-111">The second row contains the column definitions separated by tabs.</span></span>
-   <span data-ttu-id="2ac05-112">Se o arquivo contiver apenas dados ASCII, a terceira linha será nome da tabela e nomes de coluna de chave primária separados por tabulações.</span><span class="sxs-lookup"><span data-stu-id="2ac05-112">If the file contain only ASCII data, the third row is table name and primary key column names separated by tabs.</span></span>
-   <span data-ttu-id="2ac05-113">As linhas restantes no arquivo representam linhas na tabela, com colunas separadas por tabulações.</span><span class="sxs-lookup"><span data-stu-id="2ac05-113">The remaining rows in the file represent rows in the table, with columns separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="2ac05-114">Se o arquivo contiver dados não ASCII, a terceira linha será a página de código numérico seguida pelo nome da tabela e nomes de coluna de chave primária separados por tabulações.</span><span class="sxs-lookup"><span data-stu-id="2ac05-114">If the file contains non-ASCII data, the third row is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span> <span data-ttu-id="2ac05-115">Um arquivo. IDT que contém informações não ASCII deve ser salvo no formato ASCII.</span><span class="sxs-lookup"><span data-stu-id="2ac05-115">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="2ac05-116">Por exemplo, um arquivo morto de texto pode conter os nomes de coluna e tabela codificados como UTF-8, mas o arquivo morto em si deve ser ASCII.</span><span class="sxs-lookup"><span data-stu-id="2ac05-116">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span> <span data-ttu-id="2ac05-117">Consulte a seção [dados ASCII em arquivos mortos de texto](ascii-data-in-text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="2ac05-117">See the section [ASCII Data in Text Archive Files](ascii-data-in-text-archive-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="2ac05-118">Os arquivos especiais [ \_ ForceCodepage](-forcecodepage.md) e [ \_ SummaryInformation](-summaryinformation.md) . IDT usam formatos estendidos.</span><span class="sxs-lookup"><span data-stu-id="2ac05-118">The special [\_ForceCodepage](-forcecodepage.md) and [\_SummaryInformation](-summaryinformation.md) .idt files use extended formats.</span></span> <span data-ttu-id="2ac05-119">Consulte as \_ seções ForceCodepage e \_ SummaryInformation para obter descrições de seus formatos.</span><span class="sxs-lookup"><span data-stu-id="2ac05-119">See the \_ForceCodepage and \_SummaryInformation sections for descriptions of their formats.</span></span>

 

## <a name="column-definitions"></a><span data-ttu-id="2ac05-120">Definições de coluna</span><span class="sxs-lookup"><span data-stu-id="2ac05-120">Column Definitions</span></span>

<span data-ttu-id="2ac05-121">As definições de coluna são indicadas por caracteres.</span><span class="sxs-lookup"><span data-stu-id="2ac05-121">Column definitions are indicated by characters.</span></span>

-   <span data-ttu-id="2ac05-122">O primeiro caractere indica o tipo de coluna.</span><span class="sxs-lookup"><span data-stu-id="2ac05-122">The first character indicates the column type.</span></span> <span data-ttu-id="2ac05-123">Uma letra minúscula indica uma coluna não anulável e uma letra maiúscula indica que a coluna pode conter valores nulos.</span><span class="sxs-lookup"><span data-stu-id="2ac05-123">A lowercase letter indicates a non-nullable column and an uppercase letter indicates that the column can contain null values.</span></span>

    | <span data-ttu-id="2ac05-124">Caractere</span><span class="sxs-lookup"><span data-stu-id="2ac05-124">Character</span></span> | <span data-ttu-id="2ac05-125">Significado</span><span class="sxs-lookup"><span data-stu-id="2ac05-125">Meaning</span></span>                   |
    |-----------|---------------------------|
    | <span data-ttu-id="2ac05-126">s, S</span><span class="sxs-lookup"><span data-stu-id="2ac05-126">s, S</span></span>      | <span data-ttu-id="2ac05-127">Coluna de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="2ac05-127">String Column</span></span>             |
    | <span data-ttu-id="2ac05-128">l, L</span><span class="sxs-lookup"><span data-stu-id="2ac05-128">l, L</span></span>      | <span data-ttu-id="2ac05-129">Coluna de cadeia de caracteres localizável</span><span class="sxs-lookup"><span data-stu-id="2ac05-129">Localizable String Column</span></span> |
    | <span data-ttu-id="2ac05-130">v, V</span><span class="sxs-lookup"><span data-stu-id="2ac05-130">v, V</span></span>      | <span data-ttu-id="2ac05-131">Coluna binária</span><span class="sxs-lookup"><span data-stu-id="2ac05-131">Binary Column</span></span>             |
    | <span data-ttu-id="2ac05-132">i, I</span><span class="sxs-lookup"><span data-stu-id="2ac05-132">i, I</span></span>      | <span data-ttu-id="2ac05-133">Coluna de inteiros</span><span class="sxs-lookup"><span data-stu-id="2ac05-133">Integer Column</span></span>            |

    

     

-   <span data-ttu-id="2ac05-134">O segundo caractere indica o tamanho dos dados da coluna.</span><span class="sxs-lookup"><span data-stu-id="2ac05-134">The second character indicates the column data size.</span></span>

    > [!Note]  
    > <span data-ttu-id="2ac05-135">Na verdade, o Windows Installer não usa o tamanho de coluna especificado para limitar o tamanho da cadeia de caracteres que pode ser inserida em um campo de coluna de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2ac05-135">The Windows Installer does not actually use the specified column size to limit the size of the string that can be entered into a string column field.</span></span> <span data-ttu-id="2ac05-136">No entanto, algumas ferramentas de criação usam o tamanho de coluna especificado para limitar o tamanho de uma cadeia de caracteres válida.</span><span class="sxs-lookup"><span data-stu-id="2ac05-136">However, some authoring tools do use the specified column size to limit the size of a valid string.</span></span> <span data-ttu-id="2ac05-137">É recomendável que as cadeias de caracteres inseridas em qualquer coluna atendam ao requisito de tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="2ac05-137">It is recommended that strings entered into any column meet the specified size requirement.</span></span>

     

    

    | <span data-ttu-id="2ac05-138">Definição de coluna</span><span class="sxs-lookup"><span data-stu-id="2ac05-138">Column Definition</span></span> | <span data-ttu-id="2ac05-139">Significado</span><span class="sxs-lookup"><span data-stu-id="2ac05-139">Meaning</span></span>                                    |
    |-------------------|--------------------------------------------|
    | <span data-ttu-id="2ac05-140">s255</span><span class="sxs-lookup"><span data-stu-id="2ac05-140">s255</span></span>              | <span data-ttu-id="2ac05-141">Coluna de cadeia de caracteres não anulável 255 longo</span><span class="sxs-lookup"><span data-stu-id="2ac05-141">Non-Nullable String Column 255 long</span></span>        |
    | <span data-ttu-id="2ac05-142">L50</span><span class="sxs-lookup"><span data-stu-id="2ac05-142">L50</span></span>               | <span data-ttu-id="2ac05-143">Coluna de cadeia de caracteres localizável inanulável 50 longo</span><span class="sxs-lookup"><span data-stu-id="2ac05-143">Nullable Localizable String Column 50 long</span></span> |
    | <span data-ttu-id="2ac05-144">i2, I2</span><span class="sxs-lookup"><span data-stu-id="2ac05-144">i2, I2</span></span>            | <span data-ttu-id="2ac05-145">Coluna de inteiro curto</span><span class="sxs-lookup"><span data-stu-id="2ac05-145">Short Integer Column</span></span>                       |
    | <span data-ttu-id="2ac05-146">i4, i4</span><span class="sxs-lookup"><span data-stu-id="2ac05-146">i4, I4</span></span>            | <span data-ttu-id="2ac05-147">Coluna de inteiro longo</span><span class="sxs-lookup"><span data-stu-id="2ac05-147">Long Integer Column</span></span>                        |

    

     

## <a name="control-character-translation"></a><span data-ttu-id="2ac05-148">Conversão de caracteres de controle</span><span class="sxs-lookup"><span data-stu-id="2ac05-148">Control Character Translation</span></span>

<span data-ttu-id="2ac05-149">Exportar uma tabela para um arquivo morto de texto traduz os caracteres de controle para evitar conflitos com delimitadores de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ac05-149">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span> <span data-ttu-id="2ac05-150">Durante a gravação no arquivo. IDT, os caracteres de controle são traduzidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="2ac05-150">While writing into the .idt file, the control characters are translated as follows.</span></span>



| <span data-ttu-id="2ac05-151">Caractere de controle</span><span class="sxs-lookup"><span data-stu-id="2ac05-151">Control Character</span></span> | <span data-ttu-id="2ac05-152">Tradução na. IDT</span><span class="sxs-lookup"><span data-stu-id="2ac05-152">Translation in .idt</span></span> | <span data-ttu-id="2ac05-153">Significado</span><span class="sxs-lookup"><span data-stu-id="2ac05-153">Meaning</span></span>         |
|-------------------|---------------------|-----------------|
| <span data-ttu-id="2ac05-154">NULO</span><span class="sxs-lookup"><span data-stu-id="2ac05-154">NULL</span></span>              | <span data-ttu-id="2ac05-155">21</span><span class="sxs-lookup"><span data-stu-id="2ac05-155">21</span></span>                  | <span data-ttu-id="2ac05-156">Nulo</span><span class="sxs-lookup"><span data-stu-id="2ac05-156">Null</span></span>            |
| <span data-ttu-id="2ac05-157">BS</span><span class="sxs-lookup"><span data-stu-id="2ac05-157">BS</span></span>                | <span data-ttu-id="2ac05-158">27</span><span class="sxs-lookup"><span data-stu-id="2ac05-158">27</span></span>                  | <span data-ttu-id="2ac05-159">Espaço de fundo</span><span class="sxs-lookup"><span data-stu-id="2ac05-159">Back Space</span></span>      |
| <span data-ttu-id="2ac05-160">HT</span><span class="sxs-lookup"><span data-stu-id="2ac05-160">HT</span></span>                | <span data-ttu-id="2ac05-161">16</span><span class="sxs-lookup"><span data-stu-id="2ac05-161">16</span></span>                  | <span data-ttu-id="2ac05-162">Tab</span><span class="sxs-lookup"><span data-stu-id="2ac05-162">Tab</span></span>             |
| <span data-ttu-id="2ac05-163">ALIMENTAÇÃO</span><span class="sxs-lookup"><span data-stu-id="2ac05-163">LF</span></span>                | <span data-ttu-id="2ac05-164">25</span><span class="sxs-lookup"><span data-stu-id="2ac05-164">25</span></span>                  | <span data-ttu-id="2ac05-165">Alimentação de linha</span><span class="sxs-lookup"><span data-stu-id="2ac05-165">Line Feed</span></span>       |
| <span data-ttu-id="2ac05-166">FF</span><span class="sxs-lookup"><span data-stu-id="2ac05-166">FF</span></span>                | <span data-ttu-id="2ac05-167">24</span><span class="sxs-lookup"><span data-stu-id="2ac05-167">24</span></span>                  | <span data-ttu-id="2ac05-168">Feed de formulário</span><span class="sxs-lookup"><span data-stu-id="2ac05-168">Form Feed</span></span>       |
| <span data-ttu-id="2ac05-169">CR</span><span class="sxs-lookup"><span data-stu-id="2ac05-169">CR</span></span>                | <span data-ttu-id="2ac05-170">17</span><span class="sxs-lookup"><span data-stu-id="2ac05-170">17</span></span>                  | <span data-ttu-id="2ac05-171">Retorno de carro</span><span class="sxs-lookup"><span data-stu-id="2ac05-171">Carriage Return</span></span> |



 

 

 



