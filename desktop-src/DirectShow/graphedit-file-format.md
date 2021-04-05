---
description: Formato de arquivo GraphEdit
ms.assetid: 84c2de05-6c8f-45f1-b789-04a24cfa3ea1
title: Formato de arquivo GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a75421ff75c9bb26901eddf423448bbd9e4f478
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646182"
---
# <a name="graphedit-file-format"></a><span data-ttu-id="5bba3-103">Formato de arquivo GraphEdit</span><span class="sxs-lookup"><span data-stu-id="5bba3-103">GraphEdit File Format</span></span>

<span data-ttu-id="5bba3-104">Quando o utilitário GraphEdit salva um grafo de filtro do DirectShow, ele cria arquivos de armazenamento com uma extensão. GRF.</span><span class="sxs-lookup"><span data-stu-id="5bba3-104">When the GraphEdit utility saves a DirectShow filter graph, it creates a storage files with a .grf extension.</span></span> <span data-ttu-id="5bba3-105">O arquivo de armazenamento contém um único fluxo chamado ActiveMovieGraph.</span><span class="sxs-lookup"><span data-stu-id="5bba3-105">The storage file contains a single stream called ActiveMovieGraph.</span></span> <span data-ttu-id="5bba3-106">Esse fluxo contém informações sobre todos os filtros, nomes de filtro, nomes de arquivos, conexões e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5bba3-106">This stream contains information about all of the filters, filter names, file names, connections, and so forth.</span></span>

<span data-ttu-id="5bba3-107">A gramática a seguir descreve a sintaxe do grafo dentro do fluxo, usando uma sintaxe modificada do BNF (formulário Backus-Naur):</span><span class="sxs-lookup"><span data-stu-id="5bba3-107">The following grammar describes the syntax of the graph within the stream, using a modified BNF (Backus-Naur Form) syntax:</span></span>


```C++
<graph> ::= 
0003\r\n<filters><connections><clock>
END | 
0002\r\n<filters><connections>
END
<filters> ::= 
FILTERS<b> 
[<filter list><b>
]
<filter list> ::= <filter><b> 
[<filter list>
]
<filter> ::= <filter id><b><name><b><class id><b>
[<file>
]<length><b1><filter data>
<class id> ::= <guid>
<file> ::= 
SOURCE <name><b> | 
SINK <name><b>
<connections> ::= 
CONNECTIONS<b> 
{<connection><b>
}
<connection> ::= <filter id><b><pin id><b><filter id><b><pin id><b><media type>
<filter id> ::= <id>
<pin id> ::= <name>
<media type> ::= <sample size><major type><b><subtype><b><flags><format>
<major type> ::= <guid>
<subtype> ::= <guid>
<flags> ::= <fixed sample size><b><temporal compression><b>
<fixed sample size> ::= 1 
| 0
<temporal compression> ::= 1 
| 0
<format> ::= <length><b1><format type><b><length><b1><format data>
<format type> ::= <guid>
<format data> ::= 
{ binary_data 
}
<clock> ::= 
CLOCK <b><required><b><clockid>
\r\n
<required> ::= 1 
| 0
<clockid> ::= <filter id> 
| <class id>
<name> ::= quote_symbol 
{ any_non_quote_character 
} quote_symbol
<length> ::= unsigned decimal number (as a string), indicating the number 
             of bytes of data in the following token.
<guid> ::= GUID in string format. for example: {CF49D4E0-1115-11CE-B03A-0020AF0BA770}
<b> ::= 
{ space_character 
} 
{ \t 
} 
{ \r 
} 
{ \n 
} { <b> 
}
<b1> ::= space_character
<id> ::= integer (as a string), such as 0001
```



<span data-ttu-id="5bba3-108">Na saída, haverá uma nova linha (" \\ r \\ n") por filtro, uma por conexão e uma para cada um dos filtros e conexões de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="5bba3-108">On output there will be a new line ("\\r\\n") per filter, one per connection, and one for each of the keywords FILTERS and CONNECTIONS.</span></span> <span data-ttu-id="5bba3-109">Cada outro caso de <b> será um único espaço.</span><span class="sxs-lookup"><span data-stu-id="5bba3-109">Each other case of <b> will be a single space.</span></span> <span data-ttu-id="5bba3-110">As palavras-chave FILTERs, CONNECTIONs e END não são localizáveis.</span><span class="sxs-lookup"><span data-stu-id="5bba3-110">The keywords FILTERS, CONNECTIONS, and END are not localizable.</span></span> <span data-ttu-id="5bba3-111">Observe também que os dados de filtro e os dados de formato são binários, portanto, eles podem conter quebras de linha incorretas, valores nulos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5bba3-111">Note also that the filter data and the format data are binary, so they might contain incorrect line breaks, null values, and so on.</span></span> <span data-ttu-id="5bba3-112">O fluxo usa caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="5bba3-112">The stream uses wide characters.</span></span>

<span data-ttu-id="5bba3-113">Veja a seguir um gráfico típico.</span><span class="sxs-lookup"><span data-stu-id="5bba3-113">The following shows a typical graph.</span></span> <span data-ttu-id="5bba3-114">(As linhas de conexão foram interrompidas quanto à clareza e os dados binários são omitidos.)</span><span class="sxs-lookup"><span data-stu-id="5bba3-114">(The connection lines have been broken for clarity, and the binary data omitted.)</span></span>


```C++
003
FILTERS
0001 "C:\SomeFile.avi" {E436EBB5-524F-11CE-9F53-0020AF0BA770} SOURCE "C:\SomeFile.avi" 0000000000 
0002 "AVI Splitter" {1B544C20-FD0B-11CE-8C63-00AA0044B51E} 0000000000 
0003 "AVI Decompressor" {CF49D4E0-1115-11CE-B03A-0020AF0BA770} 0000000000
0004 "Video Renderer" {70E102B0-5556-11CE-97C0-00AA0055595A} 0000000000
CONNECTIONS
0001 "Output" 0002 "input pin" 0000000288 
   {E436EB83-524F-11CE-9F53-0020AF0BA770} 
   {E436EB88-524F-11CE-9F53-0020AF0BA770} 1 0 0000000001 
   {00000000-0000-0000-0000-000000000000} 0000000000  
0002 "Stream 00" 0003 "In" 0000000376 
   {73646976-0000-0010-8000-00AA00389B71} 
   {64697663-0000-0010-8000-00AA00389B71} 0 0 0000000001 
   {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data>
0003 "Out" 0004 "In" 0000000376 
    {73646976-0000-0010-8000-00AA00389B71} 
    {E436EB7D-524F-11CE-9F53-0020AF0BA770} 1 0 0000129600 
    {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data> 
CLOCK 1 0000
END
```



## <a name="related-topics"></a><span data-ttu-id="5bba3-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bba3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bba3-116">Simulando a criação de gráficos com o GraphEdit</span><span class="sxs-lookup"><span data-stu-id="5bba3-116">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



