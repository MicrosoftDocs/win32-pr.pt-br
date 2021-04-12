---
description: A tabela de mídia descreve o conjunto de discos que compõem a mídia de origem para a instalação do.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Tabela de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297900"
---
# <a name="media-table"></a><span data-ttu-id="47c35-103">Tabela de mídia</span><span class="sxs-lookup"><span data-stu-id="47c35-103">Media Table</span></span>

<span data-ttu-id="47c35-104">A tabela de mídia descreve o conjunto de discos que compõem a mídia de origem para a instalação do.</span><span class="sxs-lookup"><span data-stu-id="47c35-104">The Media table describes the set of disks that make up the source media for the installation.</span></span>

<span data-ttu-id="47c35-105">A tabela de mídia contém as colunas mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="47c35-105">The Media table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="47c35-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="47c35-106">Column</span></span>       | <span data-ttu-id="47c35-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="47c35-107">Type</span></span>                     | <span data-ttu-id="47c35-108">Chave</span><span class="sxs-lookup"><span data-stu-id="47c35-108">Key</span></span> | <span data-ttu-id="47c35-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="47c35-109">Nullable</span></span> |
|--------------|--------------------------|-----|----------|
| <span data-ttu-id="47c35-110">DiskId</span><span class="sxs-lookup"><span data-stu-id="47c35-110">DiskId</span></span>       | [<span data-ttu-id="47c35-111">Inteiro</span><span class="sxs-lookup"><span data-stu-id="47c35-111">Integer</span></span>](integer.md)   | <span data-ttu-id="47c35-112">S</span><span class="sxs-lookup"><span data-stu-id="47c35-112">Y</span></span>   | <span data-ttu-id="47c35-113">N</span><span class="sxs-lookup"><span data-stu-id="47c35-113">N</span></span>        |
| <span data-ttu-id="47c35-114">LastSequence</span><span class="sxs-lookup"><span data-stu-id="47c35-114">LastSequence</span></span> | [<span data-ttu-id="47c35-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="47c35-115">Integer</span></span>](integer.md)   | <span data-ttu-id="47c35-116">N</span><span class="sxs-lookup"><span data-stu-id="47c35-116">N</span></span>   | <span data-ttu-id="47c35-117">N</span><span class="sxs-lookup"><span data-stu-id="47c35-117">N</span></span>        |
| <span data-ttu-id="47c35-118">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="47c35-118">DiskPrompt</span></span>   | [<span data-ttu-id="47c35-119">Text</span><span class="sxs-lookup"><span data-stu-id="47c35-119">Text</span></span>](text.md)         | <span data-ttu-id="47c35-120">N</span><span class="sxs-lookup"><span data-stu-id="47c35-120">N</span></span>   | <span data-ttu-id="47c35-121">S</span><span class="sxs-lookup"><span data-stu-id="47c35-121">Y</span></span>        |
| <span data-ttu-id="47c35-122">Gabinete</span><span class="sxs-lookup"><span data-stu-id="47c35-122">Cabinet</span></span>      | [<span data-ttu-id="47c35-123">Gabinete</span><span class="sxs-lookup"><span data-stu-id="47c35-123">Cabinet</span></span>](cabinet.md)   | <span data-ttu-id="47c35-124">N</span><span class="sxs-lookup"><span data-stu-id="47c35-124">N</span></span>   | <span data-ttu-id="47c35-125">S</span><span class="sxs-lookup"><span data-stu-id="47c35-125">Y</span></span>        |
| <span data-ttu-id="47c35-126">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="47c35-126">VolumeLabel</span></span>  | [<span data-ttu-id="47c35-127">Text</span><span class="sxs-lookup"><span data-stu-id="47c35-127">Text</span></span>](text.md)         | <span data-ttu-id="47c35-128">N</span><span class="sxs-lookup"><span data-stu-id="47c35-128">N</span></span>   | <span data-ttu-id="47c35-129">S</span><span class="sxs-lookup"><span data-stu-id="47c35-129">Y</span></span>        |
| <span data-ttu-id="47c35-130">Fonte</span><span class="sxs-lookup"><span data-stu-id="47c35-130">Source</span></span>       | [<span data-ttu-id="47c35-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="47c35-131">Property</span></span>](property.md) | <span data-ttu-id="47c35-132">N</span><span class="sxs-lookup"><span data-stu-id="47c35-132">N</span></span>   | <span data-ttu-id="47c35-133">S</span><span class="sxs-lookup"><span data-stu-id="47c35-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="47c35-134">Colunas</span><span class="sxs-lookup"><span data-stu-id="47c35-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="47c35-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span><span class="sxs-lookup"><span data-stu-id="47c35-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span></span>
</dt> <dd>

<span data-ttu-id="47c35-136">Determina a ordem de classificação da tabela.</span><span class="sxs-lookup"><span data-stu-id="47c35-136">Determines the sort order for the table.</span></span> <span data-ttu-id="47c35-137">Esse número deve ser igual ou maior que 1.</span><span class="sxs-lookup"><span data-stu-id="47c35-137">This number must be equal to or greater than 1.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span><span class="sxs-lookup"><span data-stu-id="47c35-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span></span>
</dt> <dd>

<span data-ttu-id="47c35-139">Número de sequência do arquivo para o último arquivo desta mídia.</span><span class="sxs-lookup"><span data-stu-id="47c35-139">File sequence number for the last file for this media.</span></span> <span data-ttu-id="47c35-140">Os números na coluna LastSequence especificam quais dos arquivos na tabela de [arquivos](file-table.md) são encontrados em um determinado disco de origem.</span><span class="sxs-lookup"><span data-stu-id="47c35-140">The numbers in the LastSequence column specify which of the files in the [File](file-table.md) table are found on a particular source disk.</span></span> <span data-ttu-id="47c35-141">Cada disco de origem contém todos os arquivos com números de sequência (conforme mostrado na coluna sequência da tabela de arquivos) menor ou igual ao valor na coluna LastSequence e maior que o valor de LastSequence do disco anterior (ou maior que 0, para a primeira entrada na tabela de mídia).</span><span class="sxs-lookup"><span data-stu-id="47c35-141">Each source disk contains all files with sequence numbers (as shown in the Sequence column of the File table) less than or equal to the value in the LastSequence column, and greater than the LastSequence value of the previous disk (or greater than 0, for the first entry in the Media table).</span></span> <span data-ttu-id="47c35-142">Esse número deve ser não negativo; o limite máximo é de 32767 arquivos.</span><span class="sxs-lookup"><span data-stu-id="47c35-142">This number must be non-negative; the maximum limit is 32767 files.</span></span> <span data-ttu-id="47c35-143">Para obter mais informações sobre como criar um pacote de Windows Installer com mais arquivos, consulte [criando um pacote grande](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-143">For more information about creating a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="47c35-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="47c35-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span></span>
</dt> <dd>

<span data-ttu-id="47c35-145">O nome do disco, que geralmente é o texto visível impresso no disco.</span><span class="sxs-lookup"><span data-stu-id="47c35-145">The disk name, which is usually the visible text printed on the disk.</span></span> <span data-ttu-id="47c35-146">Esse texto localizável é usado para solicitar ao usuário quando esse disco precisa ser inserido.</span><span class="sxs-lookup"><span data-stu-id="47c35-146">This localizable text is used to prompt the user when this disk needs to be inserted.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Gabinete</span><span class="sxs-lookup"><span data-stu-id="47c35-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Cabinet</span></span>
</dt> <dd>

<span data-ttu-id="47c35-148">O nome do gabinete se alguns ou todos os arquivos armazenados na mídia forem compactados em um arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="47c35-148">The name of the cabinet if some or all of the files stored on the media are compressed into a cabinet file.</span></span> <span data-ttu-id="47c35-149">Se nenhum gabinete for usado, essa coluna deverá ficar em branco.</span><span class="sxs-lookup"><span data-stu-id="47c35-149">If no cabinets are used, this column must be blank.</span></span> <span data-ttu-id="47c35-150">O nome do gabinete deve usar a sintaxe do tipo de dados de [gabinete](cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="47c35-150">The name of the cabinet must use the syntax of the [Cabinet](cabinet.md) data type.</span></span> <span data-ttu-id="47c35-151">Windows Installer sempre requer uma origem válida para reparar arquivos incluídos em arquivos de gabinete inseridos.</span><span class="sxs-lookup"><span data-stu-id="47c35-151">Windows Installer always requires a valid source to repair files included in embedded cabinet files.</span></span> <span data-ttu-id="47c35-152">Quando Windows Installer instala um pacote que contém um arquivo de gabinete inserido, uma cópia do arquivo de gabinete pode ser salva pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="47c35-152">When Windows Installer installs a package containing an embedded cabinet file, a copy of the cabinet file can be saved by the system.</span></span> <span data-ttu-id="47c35-153">Esta cópia não pode ser usada para reparar o arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="47c35-153">This copy cannot be used to repair the cabinet file.</span></span> <span data-ttu-id="47c35-154">Para conservar o espaço em disco, use arquivos de gabinete externo em vez de arquivos de gabinete inseridos.</span><span class="sxs-lookup"><span data-stu-id="47c35-154">To conserve disk space, use external cabinet files instead of embedded cabinet files.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="47c35-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span></span>
</dt> <dd>

<span data-ttu-id="47c35-156">O rótulo atribuído ao volume.</span><span class="sxs-lookup"><span data-stu-id="47c35-156">The label attributed to the volume.</span></span> <span data-ttu-id="47c35-157">Esse é o rótulo de volume retornado pela função [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) .</span><span class="sxs-lookup"><span data-stu-id="47c35-157">This is the volume label returned by the [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="47c35-158">Se a propriedade [**SourceDir**](sourcedir.md) se referir a um volume removível (disquete ou CD-ROM), esse rótulo de volume será usado para verificar se o disco apropriado está na unidade antes de tentar instalar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="47c35-158">If the [**SourceDir**](sourcedir.md) property refers to a removable (floppy or CD-ROM) volume, then this volume label is used to verify that the proper disk is in the drive before attempting to install files.</span></span> <span data-ttu-id="47c35-159">A entrada nesta coluna deve corresponder ao rótulo de volume da mídia física.</span><span class="sxs-lookup"><span data-stu-id="47c35-159">The entry in this column must match the volume label of the physical media.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Original</span><span class="sxs-lookup"><span data-stu-id="47c35-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="47c35-161">Esse campo só é usado pela aplicação de patch e, de outra forma, é deixado em branco.</span><span class="sxs-lookup"><span data-stu-id="47c35-161">This field is only used by patching and is otherwise left blank.</span></span> <span data-ttu-id="47c35-162">Uma transformação de patch pode inserir uma propriedade aqui que é o local do arquivo de gabinete que contém os arquivos de patch ou quaisquer arquivos novos adicionados pelo patch.</span><span class="sxs-lookup"><span data-stu-id="47c35-162">A patch transform can enter a property here that is the location of the cabinet file containing the patch files or any new files added by the patch.</span></span> <span data-ttu-id="47c35-163">Uma fonte diferente precisa ser especificada para esses arquivos porque a origem do pacote de patch pode ser armazenada separadamente da origem do produto.</span><span class="sxs-lookup"><span data-stu-id="47c35-163">A different source needs to be specified for these files because the source of the patch package can be stored separately from the product's source.</span></span> <span data-ttu-id="47c35-164">Se o campo de gabinete estiver vazio, o instalador ignorará o valor nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="47c35-164">If the Cabinet field is empty, the installer ignores the value in this column.</span></span> <span data-ttu-id="47c35-165">Se esse campo estiver vazio, o instalador usará o valor da propriedade [**SourceDir**](sourcedir.md) como a origem do gabinete.</span><span class="sxs-lookup"><span data-stu-id="47c35-165">If this field is empty, the installer uses the value of the [**SourceDir**](sourcedir.md) property as the source of the cabinet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47c35-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="47c35-166">Remarks</span></span>

<span data-ttu-id="47c35-167">Se o nome do gabinete for precedido por um sinal numérico ( \# ), os arquivos que fazem referência a esse registro de tabela de mídia serão empacotados em um arquivo de gabinete armazenado no banco de dados como um fluxo separado.</span><span class="sxs-lookup"><span data-stu-id="47c35-167">If the cabinet name is preceded by a number sign (\#), then the files referencing this Media table record are packed in a cabinet file that is stored within the database as a separate stream.</span></span>

<span data-ttu-id="47c35-168">Para obter mais informações sobre como adicionar gabinetes às tabelas de arquivos e tabelas de mídia, consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-168">For more information about how to add cabinets to the File tables and Media tables, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="47c35-169">Windows Installer requer que o arquivo. msi esteja no primeiro disco de mídia removível (CD, DVD ou disquete) usado para a instalação do produto.</span><span class="sxs-lookup"><span data-stu-id="47c35-169">Windows Installer requires that the .msi file be on the first disk of removable media (CD, DVD or floppy) used for the product's installation.</span></span>

<span data-ttu-id="47c35-170">**Determinando o Sourcemode**</span><span class="sxs-lookup"><span data-stu-id="47c35-170">**Determining the SourceMode**</span></span>

<span data-ttu-id="47c35-171">A propriedade de [**Resumo contagem de palavras**](word-count-summary.md) determina o modo de origem para a instalação atual.</span><span class="sxs-lookup"><span data-stu-id="47c35-171">The [**Word Count Summary**](word-count-summary.md) property determines the source mode for the current install.</span></span> <span data-ttu-id="47c35-172">Se essa propriedade for definida como 2 ou 3, uma instalação de gabinete será presumida.</span><span class="sxs-lookup"><span data-stu-id="47c35-172">If this property is set to 2 or 3, a cabinet install is assumed.</span></span> <span data-ttu-id="47c35-173">Nesse modo, supõe-se que os arquivos de gabinete existam no diretório indicado pela propriedade [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="47c35-173">In this mode, the cabinet files are assumed to exist in the directory indicated by the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="47c35-174">Se o valor do tipo de origem for 0 ou 1, todos os arquivos de origem serão considerados na árvore cuja raiz é indicada pela propriedade **SourceDir** .</span><span class="sxs-lookup"><span data-stu-id="47c35-174">If the Source Type value is 0 or 1, all source files are assumed to exist in the tree whose root is indicated by the **SourceDir** property.</span></span>

<span data-ttu-id="47c35-175">Observe que isso só se aplica a arquivos na tabela de arquivos que não têm os bits compactados ou não compactados definidos na coluna atributos.</span><span class="sxs-lookup"><span data-stu-id="47c35-175">Note that this only applies to files in the File table that do not have either the Compressed or Uncompressed bits set in the attributes column.</span></span> <span data-ttu-id="47c35-176">Esses bits substituem o valor da propriedade de [**Resumo de contagem de palavras**](word-count-summary.md) ao determinar se um arquivo específico é compactado ou descompactado.</span><span class="sxs-lookup"><span data-stu-id="47c35-176">These bits override the value of the [**Word Count Summary**](word-count-summary.md) property when determining if a particular file is compressed or uncompressed.</span></span>

## <a name="validation"></a><span data-ttu-id="47c35-177">Validação</span><span class="sxs-lookup"><span data-stu-id="47c35-177">Validation</span></span>

<dl>

[<span data-ttu-id="47c35-178">ICE03</span><span class="sxs-lookup"><span data-stu-id="47c35-178">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="47c35-179">ICE04</span><span class="sxs-lookup"><span data-stu-id="47c35-179">ICE04</span></span>](ice04.md)  
[<span data-ttu-id="47c35-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="47c35-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="47c35-181">ICE35</span><span class="sxs-lookup"><span data-stu-id="47c35-181">ICE35</span></span>](ice35.md)  
[<span data-ttu-id="47c35-182">ICE58</span><span class="sxs-lookup"><span data-stu-id="47c35-182">ICE58</span></span>](ice58.md)  
[<span data-ttu-id="47c35-183">ICE71</span><span class="sxs-lookup"><span data-stu-id="47c35-183">ICE71</span></span>](ice71.md)  
[<span data-ttu-id="47c35-184">ICE81</span><span class="sxs-lookup"><span data-stu-id="47c35-184">ICE81</span></span>](ice81.md)  
</dl>

 

 
