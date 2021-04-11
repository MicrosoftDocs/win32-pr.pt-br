---
title: Serviços de formato de arquivo de intercâmbio de recursos
description: Serviços de formato de arquivo de intercâmbio de recursos
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- e/s de arquivo multimídia, formato de arquivo de intercâmbio de recursos (RIFF)
- e/s de arquivo, formato de arquivo de intercâmbio de recursos (RIFF)
- entrada e saída (e/s), formato de arquivo de intercâmbio de recursos (RIFF)
- E/s (entrada e saída), formato de arquivo de intercâmbio de recursos (RIFF)
- função mmioOpen
- formato de arquivo de intercâmbio de recursos (RIFF)
- RIFF (formato de arquivo de intercâmbio de recursos)
- E/S DO RIFF
- Parte do RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cca3792ccded248951065c7b69f2e50d27e0ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293908"
---
# <a name="resource-interchange-file-format-services"></a>Serviços de formato de arquivo de intercâmbio de recursos

O formato preferencial para arquivos de multimídia é o formato de arquivo de intercâmbio de recursos (RIFF). As funções de e/s de arquivo RIFF funcionam com os serviços de e/s de arquivo em buffer básico e sem buffer. Você pode abrir, ler e gravar arquivos RIFF da mesma maneira que outros tipos de arquivo. Para obter informações detalhadas sobre o RIFF, consulte [funções e macros do avifile](avifile-functions-and-macros.md).

Os arquivos RIFF usam códigos de quatro caracteres para identificar elementos de arquivo. Esses códigos são quantidades de 32 bits que representam uma sequência de um a quatro caracteres alfanuméricos ASCII, preenchidos à direita com caracteres de espaço. O tipo de dados para códigos de quatro caracteres é **FOURCC**. Use a macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) para converter quatro caracteres em um código de quatro caracteres. Para converter uma cadeia de caracteres terminada em nulo em um código de quatro caracteres, use a função [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) .

O bloco de construção básico de um arquivo RIFF é uma *parte*. Uma parte é uma unidade lógica de dados de multimídia, como um único quadro em um clipe de vídeo. Cada parte contém os seguintes campos:

-   Um código de quatro caracteres que especifica o identificador da parte
-   Um valor doubleword especificando o tamanho do membro de dados na parte
-   Um campo de dados

A ilustração a seguir mostra uma parte "RIFF" que contém duas subpartes.

![a parte do riff que contém duas imagens de subpartes](images/mmio1.gif)

Uma parte contida em outra parte é uma *subparte*. As únicas partes com permissão para conter subpartes são aquelas com um identificador de parte de "RIFF" ou "LIST". Uma parte que contém outra parte é chamada de *parte pai*. A primeira parte em um arquivo RIFF deve ser uma parte "RIFF". Todas as outras partes no arquivo são subpartes da parte "RIFF".

As partes de "RIFF" incluem um campo adicional nos primeiros quatro bytes do campo de dados. Esse campo adicional fornece o *tipo de formulário* do campo. O tipo de formulário é um código de quatro caracteres que identifica o formato dos dados armazenados no arquivo. Por exemplo, os arquivos de áudio de forma de onda da Microsoft têm um tipo de formulário de "onda".

As partes de "LISTAr" também incluem um campo adicional nos primeiros quatro bytes do campo de dados. Esse campo adicional contém o *tipo de lista* do campo. O tipo de lista é um código de quatro caracteres que identifica o conteúdo da lista. Por exemplo, uma parte de "lista" com um tipo de lista de "informações" pode conter as partes "ICOP" e "ICRD", fornecendo informações de data e de direitos autorais. A ilustração a seguir mostra uma parte "RIFF" que contém uma parte de "lista" e outra subparte (a parte "lista" contém duas subpartes).

![parte do riff que contém uma imagem de parte da lista](images/mmio2.gif)

Os serviços de e/s de arquivo de multimídia incluem duas funções que você pode usar para navegar entre partes em um arquivo RIFF: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) e [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend). Você pode usar essas funções como funções de busca de alto nível. Quando você descende em uma parte, a posição do arquivo é definida como o campo de dados da parte (8 bytes do início da parte). Para as partes "RIFF" e "lista", a posição do arquivo é definida como o local após o tipo de formulário ou de lista (12 bytes a partir do início da parte). Quando você estiver em ordem ascendente de uma parte, a posição do arquivo será definida como o local após o final da parte.

Para criar uma nova parte, use a função [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para gravar um cabeçalho de parte na posição atual em um arquivo aberto. As funções **mmioAscend**, **mmioDescend** e **mmioCreateChunk** usam a estrutura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) para especificar e recuperar informações sobre partes "riff".

 

 