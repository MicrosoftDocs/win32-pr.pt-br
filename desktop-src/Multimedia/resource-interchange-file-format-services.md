---
title: Serviços de formato de arquivo de intercâmbio de recursos
description: Serviços de formato de arquivo de intercâmbio de recursos
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- E/S de arquivo multimídia, formato de arquivo de intercâmbio de recursos (PDF)
- E/S de arquivo, formato de arquivo de intercâmbio de recursos (FORMAT)
- entrada e saída (E/S), formato de arquivo de intercâmbio de recursos (FORMAT)
- E/S (entrada e saída), formato de arquivo de intercâmbio de recursos (FORMAT)
- Função mmioOpen
- formato de arquivo de intercâmbio de recursos (PDF)
- CHANG (formato de arquivo de intercâmbio de recursos)
- E/S DO BLUES
- Parte DE HASH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5967165996b2a7fb9ed9b40c9a1f3c5608cd3bb4eb1e6cf05ae351f6ce6f2a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801915"
---
# <a name="resource-interchange-file-format-services"></a>Serviços de formato de arquivo de intercâmbio de recursos

O formato preferencial para arquivos multimídia é o formato de arquivo de intercâmbio de recursos (PDF). As funções de E/S do arquivo DEM funcionam com os serviços básicos de E/S de arquivo armazenado em buffer e sem buffer. Você pode abrir, ler e gravar arquivos HASH da mesma maneira que outros tipos de arquivo. Para obter informações detalhadas sobre o HASH, [consulte Funções e Macros DE ARQUIVO AVIFile.](avifile-functions-and-macros.md)

Os arquivos PDF usam códigos de quatro caracteres para identificar elementos de arquivo. Esses códigos são quantidades de 32 bits que representam uma sequência de um a quatro caracteres alfanuméricos ASCII, preenchimento à direita com caracteres de espaço. O tipo de dados para códigos de quatro caracteres **é FOURCC.** Use a [**macro mmio GATESCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) para converter quatro caracteres em um código de quatro caracteres. Para converter uma cadeia de caracteres terminada em nulo em um código de quatro caracteres, use a [**função mmioStringTo BOOCC.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

O bloco de construção básico de um arquivo HASH é uma *parte*. Uma parte é uma unidade lógica de dados multimídia, como um único quadro em um clipe de vídeo. Cada parte contém os seguintes campos:

-   Um código de quatro caracteres que especifica o identificador de partes
-   Um valor doubleword que especifica o tamanho do membro de dados na parte
-   Um campo de dados

A ilustração a seguir mostra uma parte "HASH" que contém dois subchunks.

![parte de chunk que contém duas imagens de subchunks](images/mmio1.gif)

Uma parte contida em outra parte é um *subchunk*. As únicas partes permitidas para conter subchunks são aquelas com um identificador de partes de "HASH" ou "LIST". Uma parte que contém outra parte é chamada de *parte pai.* A primeira parte em um arquivo HASH deve ser uma parte "HASH". Todas as outras partes no arquivo são subchunks da parte "HASH".

As partes "BYTES" incluem um campo adicional nos primeiros quatro bytes do campo de dados. Esse campo adicional fornece *o tipo de* formulário do campo. O tipo de formulário é um código de quatro caracteres que identifica o formato dos dados armazenados no arquivo. Por exemplo, os arquivos waveform-audio da Microsoft têm um tipo de formulário "WAVE".

Partes "LIST" também incluem um campo adicional nos primeiros quatro bytes do campo de dados. Esse campo adicional contém *o tipo de* lista do campo. O tipo de lista é um código de quatro caracteres que identifica o conteúdo da lista. Por exemplo, uma parte "LIST" com um tipo de lista de "INFO" pode conter partes "ICOP" e "ICRD", fornecendo informações de data de criação e direitos autorais. A ilustração a seguir mostra uma parte "HASH" que contém uma parte "LIST" e outra subchunk (a parte "LIST" contém dois subchunks).

![parte de chunk que contém uma imagem de bloco de lista](images/mmio2.gif)

Os serviços de E/S de arquivo multimídia incluem duas funções que você pode usar para navegar entre partes em um arquivo DEVM: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) e [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend). Você pode usar essas funções como funções de busca de alto nível. Quando você entra em uma parte, a posição do arquivo é definida como o campo de dados da parte (8 bytes do início da parte). Para partes "BYTES" e "LIST", a posição do arquivo é definida como o local após o tipo de formulário ou tipo de lista (12 bytes do início da parte). Quando você sai de uma parte, a posição do arquivo é definida para o local após o final da parte.

Para criar uma nova parte, use a [**função mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para gravar um header de partes na posição atual em um arquivo aberto. As **funções mmioAscend**, **mmioDescend** e **mmioCreateChunk** usam a estrutura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) para especificar e recuperar informações sobre partes "DOUG".

 

 