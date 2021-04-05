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
# <a name="compressed-and-uncompressed-sources"></a>Fontes compactadas e descompactadas

Os autores de pacotes podem reduzir o tamanho de seus pacotes de instalação compactando os arquivos de origem e incluindo-os em [arquivos de gabinete](cabinet-files.md). A imagem do arquivo de origem pode ser compactada, descompactada ou uma mistura de ambos os tipos.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Fontes compactadas
</dt> <dd>

Uma fonte que consiste inteiramente em arquivos compactados deve incluir o bit de sinalizador compactado na propriedade de [**Resumo contagem de palavras**](word-count-summary.md) . Os arquivos de origem compactados devem ser armazenados em arquivos de gabinete localizados em um fluxo de dados dentro do arquivo. msi ou em um arquivo de gabinete separado localizado na raiz da árvore de origem. Todos os gabinetes na origem devem ser listados na tabela de [mídia](media-table.md).

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Fontes não compactadas
</dt> <dd>

Uma fonte que consiste inteiramente em arquivos de origem não compactados deve omitir o bit de sinalizador compactado da propriedade de [**Resumo contagem de palavras**](word-count-summary.md) . Todos os arquivos descompactados na origem devem existir na árvore de origem especificada pela tabela de [diretórios](directory-table.md).

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Fontes mistas 
</dt> <dd>

Para misturar arquivos de origem compactados e descompactados no mesmo pacote, substitua a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) padrão definindo os sinalizadores de bit MsidbFileAttributesCompressed ou msidbFileAttributesNoncompressed em arquivos específicos. Esses sinalizadores de bit são definidos na coluna atributos da [tabela de arquivos](file-table.md) se o estado de compactação do arquivo não corresponder ao padrão especificado pela propriedade [**Resumo de contagem de palavras**](word-count-summary.md) .

Por exemplo, se a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) tiver o bit de sinalizador compactado definido, todos os arquivos serão tratados como compactados em um gabinete. Todos os arquivos descompactados na origem devem incluir msidbFileAttributesNoncompressed na coluna atributos da [tabela de arquivos](file-table.md). Os arquivos descompactados devem estar localizados na raiz da árvore de origem.

Se a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) tiver o sinalizador descompactado definido, os arquivos serão tratados como não compactados por padrão e todos os arquivos compactados deverão incluir msidbFileAttributesCompressed na coluna atributos da tabela de arquivos. Todos os arquivos compactados devem ser armazenados em arquivos de gabinete localizados em um fluxo de dados dentro do arquivo. msi ou em um arquivo de gabinete separado localizado na raiz da árvore de origem.

Para obter mais informações, consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

</dd> </dl>

 

 



