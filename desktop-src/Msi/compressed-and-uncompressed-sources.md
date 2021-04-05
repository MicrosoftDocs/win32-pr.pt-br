---
description: Os autores de pacotes podem reduzir o tamanho de seus pacotes de instalação compactando os arquivos de origem e incluindo-os em arquivos de gabinete. A imagem do arquivo de origem pode ser compactada, descompactada ou uma mistura de ambos os tipos.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Fontes compactadas e descompactadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dc706a73d52f1dac35c917bd6c178a543ab300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921157"
---
# <a name="compressed-and-uncompressed-sources"></a><span data-ttu-id="adcff-104">Fontes compactadas e descompactadas</span><span class="sxs-lookup"><span data-stu-id="adcff-104">Compressed and Uncompressed Sources</span></span>

<span data-ttu-id="adcff-105">Os autores de pacotes podem reduzir o tamanho de seus pacotes de instalação compactando os arquivos de origem e incluindo-os em [arquivos de gabinete](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="adcff-105">Package authors can reduce the size of their installation packages by compressing the source files and including them in [cabinet files](cabinet-files.md).</span></span> <span data-ttu-id="adcff-106">A imagem do arquivo de origem pode ser compactada, descompactada ou uma mistura de ambos os tipos.</span><span class="sxs-lookup"><span data-stu-id="adcff-106">The source file image can be compressed, uncompressed, or a mixture of both types.</span></span>

<dl> <dt>

<span data-ttu-id="adcff-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Fontes compactadas</span><span class="sxs-lookup"><span data-stu-id="adcff-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Compressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="adcff-108">Uma fonte que consiste inteiramente em arquivos compactados deve incluir o bit de sinalizador compactado na propriedade de [**Resumo contagem de palavras**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="adcff-108">A source consisting entirely of compressed files should include the compressed flag bit in the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="adcff-109">Os arquivos de origem compactados devem ser armazenados em arquivos de gabinete localizados em um fluxo de dados dentro do arquivo. msi ou em um arquivo de gabinete separado localizado na raiz da árvore de origem.</span><span class="sxs-lookup"><span data-stu-id="adcff-109">The compressed source files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span> <span data-ttu-id="adcff-110">Todos os gabinetes na origem devem ser listados na tabela de [mídia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="adcff-110">All of the cabinets in the source must be listed in the [Media table](media-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="adcff-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Fontes não compactadas</span><span class="sxs-lookup"><span data-stu-id="adcff-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Uncompressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="adcff-112">Uma fonte que consiste inteiramente em arquivos de origem não compactados deve omitir o bit de sinalizador compactado da propriedade de [**Resumo contagem de palavras**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="adcff-112">A source consisting entirely of uncompressed source files should omit the compressed flag bit from the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="adcff-113">Todos os arquivos descompactados na origem devem existir na árvore de origem especificada pela tabela de [diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="adcff-113">All of the uncompressed files in the source must exist in the source tree specified by the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="adcff-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Fontes mistas</span><span class="sxs-lookup"><span data-stu-id="adcff-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Mixed Sources</span></span> 
</dt> <dd>

<span data-ttu-id="adcff-115">Para misturar arquivos de origem compactados e descompactados no mesmo pacote, substitua a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) padrão definindo os sinalizadores de bit MsidbFileAttributesCompressed ou msidbFileAttributesNoncompressed em arquivos específicos.</span><span class="sxs-lookup"><span data-stu-id="adcff-115">To mix compressed and uncompressed source files in the same package, override the [**Word Count Summary**](word-count-summary.md) property default by setting the msidbFileAttributesCompressed or msidbFileAttributesNoncompressed bit flags on particular files.</span></span> <span data-ttu-id="adcff-116">Esses sinalizadores de bit são definidos na coluna atributos da [tabela de arquivos](file-table.md) se o estado de compactação do arquivo não corresponder ao padrão especificado pela propriedade [**Resumo de contagem de palavras**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="adcff-116">These bit flags are set in the Attributes column of the [File table](file-table.md) if the compression state of the file does not match the default specified by the [**Word Count Summary**](word-count-summary.md) property.</span></span>

<span data-ttu-id="adcff-117">Por exemplo, se a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) tiver o bit de sinalizador compactado definido, todos os arquivos serão tratados como compactados em um gabinete.</span><span class="sxs-lookup"><span data-stu-id="adcff-117">For example, if the [**Word Count Summary**](word-count-summary.md) property has the compressed flag bit set, all files are treated as compressed into a cabinet.</span></span> <span data-ttu-id="adcff-118">Todos os arquivos descompactados na origem devem incluir msidbFileAttributesNoncompressed na coluna atributos da [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="adcff-118">Any uncompressed files in the source must include msidbFileAttributesNoncompressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="adcff-119">Os arquivos descompactados devem estar localizados na raiz da árvore de origem.</span><span class="sxs-lookup"><span data-stu-id="adcff-119">The uncompressed files must be located at the root of the source tree.</span></span>

<span data-ttu-id="adcff-120">Se a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) tiver o sinalizador descompactado definido, os arquivos serão tratados como não compactados por padrão e todos os arquivos compactados deverão incluir msidbFileAttributesCompressed na coluna atributos da tabela de arquivos.</span><span class="sxs-lookup"><span data-stu-id="adcff-120">If the [**Word Count Summary**](word-count-summary.md) property has the uncompressed flag set, files are treated as uncompressed by default and any compressed files must include msidbFileAttributesCompressed in the Attributes column of the File table.</span></span> <span data-ttu-id="adcff-121">Todos os arquivos compactados devem ser armazenados em arquivos de gabinete localizados em um fluxo de dados dentro do arquivo. msi ou em um arquivo de gabinete separado localizado na raiz da árvore de origem.</span><span class="sxs-lookup"><span data-stu-id="adcff-121">All of the compressed files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span>

<span data-ttu-id="adcff-122">Para obter mais informações, consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="adcff-122">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

</dd> </dl>

 

 



