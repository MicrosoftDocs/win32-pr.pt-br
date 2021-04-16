---
description: Um aplicativo pode descompactar uma parte de um arquivo compactado por vez usando as funções LZSeek e LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lendo de arquivos compactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757853"
---
# <a name="reading-from-compressed-files"></a><span data-ttu-id="0f5ec-103">Lendo de arquivos compactados</span><span class="sxs-lookup"><span data-stu-id="0f5ec-103">Reading from Compressed Files</span></span>

<span data-ttu-id="0f5ec-104">Além de descompactar um arquivo completo em uma única operação, um aplicativo pode descompactar um arquivo compactado uma parte por vez usando as funções [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) e [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) .</span><span class="sxs-lookup"><span data-stu-id="0f5ec-104">In addition to decompressing a complete file in a single operation, an application can decompress a compressed file a portion at a time by using the [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) and [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) functions.</span></span> <span data-ttu-id="0f5ec-105">Essas funções são particularmente úteis quando é necessário para extrair partes de arquivos grandes.</span><span class="sxs-lookup"><span data-stu-id="0f5ec-105">These functions are particularly useful when it is necessary to extract parts of large files.</span></span> <span data-ttu-id="0f5ec-106">Por exemplo, um fabricante de fontes pode ter arquivos compactados contendo métricas de fonte, além de dados de caractere.</span><span class="sxs-lookup"><span data-stu-id="0f5ec-106">For example, a font manufacturer may have compressed files containing font metrics in addition to character data.</span></span> <span data-ttu-id="0f5ec-107">Para usar as informações nesses arquivos, um aplicativo precisará descompactar o arquivo; no entanto, a maioria dos aplicativos usaria apenas parte do arquivo em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="0f5ec-107">To use the information in these files, an application would need to decompress the file; however, most applications would use only part of the file at any particular time.</span></span> <span data-ttu-id="0f5ec-108">Para obter informações sobre métricas de fonte, o aplicativo extrairia dados do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="0f5ec-108">To get information about font metrics, the application would extract data from the header.</span></span> <span data-ttu-id="0f5ec-109">Para obter informações do texto, o aplicativo reposicionará o ponteiro de arquivo chamando **LZSeek** e extrairá os dados de caractere chamando **LZRead**.</span><span class="sxs-lookup"><span data-stu-id="0f5ec-109">To get information from the text, the application would reposition the file pointer by calling **LZSeek** and extract character data by calling **LZRead**.</span></span>

 

 



