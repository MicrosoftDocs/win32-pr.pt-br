---
description: Os autores do pacote podem reduzir o tamanho de seus pacotes de instalação compactando os arquivos de origem e incluindo-os em arquivos de gabinete. A imagem do arquivo de origem pode ser compactada, descompactada ou uma combinação de ambos os tipos.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Fontes compactadas e descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7d35a5723261ab1c62866d185a8402a9607600cad906c2fb66ddc5dc85ac08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144447"
---
# <a name="compressed-and-uncompressed-sources"></a>Fontes compactadas e descompactados

Os autores do pacote podem reduzir o tamanho de seus pacotes de instalação compactando os arquivos de origem e incluindo-os em arquivos [de gabinete](cabinet-files.md). A imagem do arquivo de origem pode ser compactada, descompactada ou uma combinação de ambos os tipos.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Fontes compactadas
</dt> <dd>

Uma origem que consiste inteiramente em arquivos compactados deve incluir o bit do sinalizador compactado na propriedade [**Resumo de Contagem de**](word-count-summary.md) Palavras. Os arquivos de origem compactados devem ser armazenados em arquivos de gabinete localizados em um fluxo de dados dentro do arquivo .msi ou em um arquivo de gabinete separado localizado na raiz da árvore de origem. Todos os gabinetes na origem devem ser listados na [tabela Mídia](media-table.md).

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Fontes descompactados
</dt> <dd>

Uma origem que consiste inteiramente em arquivos de origem descompactados deve omitir o bit de sinalizador compactado da propriedade [**Resumo de Contagem de**](word-count-summary.md) Palavras. Todos os arquivos descompactados na origem devem existir na árvore de origem especificada pela [tabela Diretório](directory-table.md).

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Fontes mistas 
</dt> <dd>

Para misturar arquivos de origem compactados e descompactados no mesmo pacote, substitua a propriedade Resumo da Contagem de [**Palavras**](word-count-summary.md) padrão definindo msidbFileAttributesCompressed ou msidbFileAttributesNoncompressed bit flags em arquivos específicos. Esses sinalizadores de bits serão definidos na coluna Atributos da tabela Arquivo se o estado de compactação do arquivo não corresponder ao padrão especificado pela propriedade Resumo da Contagem [**de**](word-count-summary.md) Palavras. [](file-table.md)

Por exemplo, se a propriedade Resumo da Contagem de [**Palavras**](word-count-summary.md) tiver o bit de sinalizador compactado definido, todos os arquivos serão tratados como compactados em um gabinete. Todos os arquivos descompactados na origem devem incluir msidbFileAttributesNoncompressed na coluna Atributos da [tabela Arquivo](file-table.md). Os arquivos descompactados devem estar localizados na raiz da árvore de origem.

Se a propriedade [**Resumo**](word-count-summary.md) da Contagem de Palavras tiver o sinalizador descompactado definido, os arquivos serão tratados como descompactados por padrão e todos os arquivos compactados deverão incluir msidbFileAttributesCompressed na coluna Atributos da tabela Arquivo. Todos os arquivos compactados devem ser armazenados em arquivos de gabinete localizados em um fluxo de dados dentro do arquivo .msi ou em um arquivo de gabinete separado localizado na raiz da árvore de origem.

Para obter mais informações, consulte [Usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

</dd> </dl>

 

 



