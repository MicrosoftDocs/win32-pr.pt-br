---
description: A tabela patch especifica o arquivo que deve receber um patch específico e o local físico dos arquivos de patch nas imagens de mídia.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Tabela de patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663372"
---
# <a name="patch-table"></a><span data-ttu-id="f98af-103">Tabela de patches</span><span class="sxs-lookup"><span data-stu-id="f98af-103">Patch Table</span></span>

<span data-ttu-id="f98af-104">A tabela patch especifica o arquivo que deve receber um patch específico e o local físico dos arquivos de patch nas imagens de mídia.</span><span class="sxs-lookup"><span data-stu-id="f98af-104">The Patch table specifies the file that is to receive a particular patch and the physical location of the patch files on the media images.</span></span>

<span data-ttu-id="f98af-105">A tabela patch tem as seguintes colunas.</span><span class="sxs-lookup"><span data-stu-id="f98af-105">The Patch table has the following columns.</span></span>



| <span data-ttu-id="f98af-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="f98af-106">Column</span></span>      | <span data-ttu-id="f98af-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f98af-107">Type</span></span>                               | <span data-ttu-id="f98af-108">Chave</span><span class="sxs-lookup"><span data-stu-id="f98af-108">Key</span></span> | <span data-ttu-id="f98af-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f98af-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="f98af-110">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="f98af-110">File\_</span></span>      | [<span data-ttu-id="f98af-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="f98af-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="f98af-112">S</span><span class="sxs-lookup"><span data-stu-id="f98af-112">Y</span></span>   | <span data-ttu-id="f98af-113">N</span><span class="sxs-lookup"><span data-stu-id="f98af-113">N</span></span>        |
| <span data-ttu-id="f98af-114">Sequência</span><span class="sxs-lookup"><span data-stu-id="f98af-114">Sequence</span></span>    | [<span data-ttu-id="f98af-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="f98af-115">Integer</span></span>](integer.md)             | <span data-ttu-id="f98af-116">S</span><span class="sxs-lookup"><span data-stu-id="f98af-116">Y</span></span>   | <span data-ttu-id="f98af-117">N</span><span class="sxs-lookup"><span data-stu-id="f98af-117">N</span></span>        |
| <span data-ttu-id="f98af-118">PatchSize</span><span class="sxs-lookup"><span data-stu-id="f98af-118">PatchSize</span></span>   | [<span data-ttu-id="f98af-119">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="f98af-119">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="f98af-120">N</span><span class="sxs-lookup"><span data-stu-id="f98af-120">N</span></span>   | <span data-ttu-id="f98af-121">N</span><span class="sxs-lookup"><span data-stu-id="f98af-121">N</span></span>        |
| <span data-ttu-id="f98af-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="f98af-122">Attributes</span></span>  | [<span data-ttu-id="f98af-123">Inteiro</span><span class="sxs-lookup"><span data-stu-id="f98af-123">Integer</span></span>](integer.md)             | <span data-ttu-id="f98af-124">N</span><span class="sxs-lookup"><span data-stu-id="f98af-124">N</span></span>   | <span data-ttu-id="f98af-125">N</span><span class="sxs-lookup"><span data-stu-id="f98af-125">N</span></span>        |
| <span data-ttu-id="f98af-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f98af-126">Header</span></span>      | [<span data-ttu-id="f98af-127">Binary</span><span class="sxs-lookup"><span data-stu-id="f98af-127">Binary</span></span>](binary.md)               | <span data-ttu-id="f98af-128">N</span><span class="sxs-lookup"><span data-stu-id="f98af-128">N</span></span>   | <span data-ttu-id="f98af-129">S</span><span class="sxs-lookup"><span data-stu-id="f98af-129">Y</span></span>        |
| <span data-ttu-id="f98af-130">StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="f98af-130">StreamRef\_</span></span> | [<span data-ttu-id="f98af-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="f98af-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="f98af-132">N</span><span class="sxs-lookup"><span data-stu-id="f98af-132">N</span></span>   | <span data-ttu-id="f98af-133">S</span><span class="sxs-lookup"><span data-stu-id="f98af-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f98af-134">Colunas</span><span class="sxs-lookup"><span data-stu-id="f98af-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f98af-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="f98af-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="f98af-136">O patch é aplicado ao arquivo especificado pelo identificador nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="f98af-136">The patch is applied to the file specified by the identifier in this column.</span></span> <span data-ttu-id="f98af-137">Essa é uma chave primária para a tabela e é uma chave estrangeira para a [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f98af-137">This is a primary key for the table and it is a foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="f98af-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="f98af-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="f98af-139">Essa é a posição do arquivo de patch na ordem de sequência dos arquivos nas imagens de mídia.</span><span class="sxs-lookup"><span data-stu-id="f98af-139">This is the position of the patch file in the sequence order of files on the media images.</span></span> <span data-ttu-id="f98af-140">A ordem de sequência deve corresponder à ordem dos arquivos no arquivo de gabinete do pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="f98af-140">The sequence order must correspond to the order of the files in the patch package cabinet file.</span></span> <span data-ttu-id="f98af-141">Esta é uma chave primária para esta tabela.</span><span class="sxs-lookup"><span data-stu-id="f98af-141">This is a primary key for this table.</span></span> <span data-ttu-id="f98af-142">O limite máximo é de 32767 arquivos, para criar um pacote de Windows Installer com mais arquivos, consulte [criando um pacote grande](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="f98af-142">The maximum limit is 32767 files, to create a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="f98af-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span><span class="sxs-lookup"><span data-stu-id="f98af-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span></span>
</dt> <dd>

<span data-ttu-id="f98af-144">Essa coluna fornece o tamanho do patch em bytes gravados como um inteiro longo.</span><span class="sxs-lookup"><span data-stu-id="f98af-144">This column gives the size of the patch in bytes written as a long integer.</span></span>

</dd> <dt>

<span data-ttu-id="f98af-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="f98af-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="f98af-146">Inteiro que contém os sinalizadores de bit que representam os atributos de patch.</span><span class="sxs-lookup"><span data-stu-id="f98af-146">Integer containing bit flags representing patch attributes.</span></span> <span data-ttu-id="f98af-147">Insira um valor de 1 nesta coluna para indicar que a falha ao aplicar esse patch não é um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="f98af-147">Insert a value of 1 in this column to indicate that the failure to apply this patch is not a fatal error.</span></span>



| <span data-ttu-id="f98af-148">Constante</span><span class="sxs-lookup"><span data-stu-id="f98af-148">Constant</span></span>                         | <span data-ttu-id="f98af-149">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="f98af-149">Hexadecimal</span></span> | <span data-ttu-id="f98af-150">Decimal</span><span class="sxs-lookup"><span data-stu-id="f98af-150">Decimal</span></span> | <span data-ttu-id="f98af-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="f98af-151">Description</span></span>                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| <span data-ttu-id="f98af-152">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="f98af-152">(none)</span></span>                           | <span data-ttu-id="f98af-153">0x000</span><span class="sxs-lookup"><span data-stu-id="f98af-153">0x000</span></span>       | <span data-ttu-id="f98af-154">0</span><span class="sxs-lookup"><span data-stu-id="f98af-154">0</span></span>       | <span data-ttu-id="f98af-155">A falha ao aplicar esse patch é um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="f98af-155">Failure to apply this patch is a fatal error.</span></span>                        |
| <span data-ttu-id="f98af-156">**msidbPatchAttributesNonVital**</span><span class="sxs-lookup"><span data-stu-id="f98af-156">**msidbPatchAttributesNonVital**</span></span> | <span data-ttu-id="f98af-157">0x001</span><span class="sxs-lookup"><span data-stu-id="f98af-157">0x001</span></span>       | <span data-ttu-id="f98af-158">1</span><span class="sxs-lookup"><span data-stu-id="f98af-158">1</span></span>       | <span data-ttu-id="f98af-159">Indica que a falha ao aplicar esse patch não é um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="f98af-159">Indicates that the failure to apply this patch is not a fatal error.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f98af-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Verga</span><span class="sxs-lookup"><span data-stu-id="f98af-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="f98af-161">Esta coluna é o cabeçalho de patch de fluxo binário usado para validação de patch.</span><span class="sxs-lookup"><span data-stu-id="f98af-161">This column is the binary stream patch header used for patch validation.</span></span> <span data-ttu-id="f98af-162">Essa coluna deverá ser nula se a \_ coluna StreamRef não for nula.</span><span class="sxs-lookup"><span data-stu-id="f98af-162">This column should be null if the StreamRef\_ column is not null.</span></span> <span data-ttu-id="f98af-163">Nesse caso, o fluxo do cabeçalho de patch é armazenado na [tabela MsiPatchHeaders](msipatchheaders-table.md) para superar a limitação de nome de fluxo descrita em [limitações de OLE em fluxos](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="f98af-163">In this case, the patch header stream is stored in the [MsiPatchHeaders table](msipatchheaders-table.md) to overcome the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

</dd> <dt>

<span data-ttu-id="f98af-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="f98af-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span></span>
</dt> <dd>

<span data-ttu-id="f98af-165">Chave externa na tabela MsiPatchHeaders especificando a linha que contém o fluxo do cabeçalho de patch.</span><span class="sxs-lookup"><span data-stu-id="f98af-165">External key into the MsiPatchHeaders table specifying the row that contains the patch header stream.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f98af-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="f98af-166">Remarks</span></span>

<span data-ttu-id="f98af-167">Essa tabela é processada pela [ação PatchFiles](patchfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="f98af-167">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="f98af-168">Normalmente, ele é adicionado ao pacote de instalação por uma transformação de um pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="f98af-168">It is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="f98af-169">Normalmente, ele não é criado diretamente em um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="f98af-169">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="f98af-170">Validação</span><span class="sxs-lookup"><span data-stu-id="f98af-170">Validation</span></span>

<dl>

[<span data-ttu-id="f98af-171">ICE03</span><span class="sxs-lookup"><span data-stu-id="f98af-171">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f98af-172">ICE06</span><span class="sxs-lookup"><span data-stu-id="f98af-172">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f98af-173">ICE29</span><span class="sxs-lookup"><span data-stu-id="f98af-173">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="f98af-174">ICE45</span><span class="sxs-lookup"><span data-stu-id="f98af-174">ICE45</span></span>](ice45.md)  
</dl>

 

 



