---
description: Um aplicativo pode descompactar vários arquivos usando as funções LZOpenFile, LZCopy e LZClose.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Descompactando vários arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784008"
---
# <a name="decompressing-multiple-files"></a><span data-ttu-id="a2e5b-103">Descompactando vários arquivos</span><span class="sxs-lookup"><span data-stu-id="a2e5b-103">Decompressing Multiple Files</span></span>

<span data-ttu-id="a2e5b-104">Um aplicativo pode descompactar vários arquivos executando as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="a2e5b-104">An application can decompress multiple files by performing the following tasks:</span></span>

1.  <span data-ttu-id="a2e5b-105">Abra os arquivos de origem chamando a função [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-105">Open the source files by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="a2e5b-106">Abra os arquivos de destino chamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="a2e5b-106">Open the destination files by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="a2e5b-107">Copie os arquivos de origem para os arquivos de destino chamando a função [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-107">Copy the source files to the destination files by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function.</span></span>
4.  <span data-ttu-id="a2e5b-108">Feche os arquivos chamando a função [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="a2e5b-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



