---
description: Um aplicativo pode descompactar um único arquivo compactado usando as funções LZOpenFile, LZCopy e LZClose.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Descompactando um único arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8da6ee4ee80e42d6ff70c3d9c50efdc572f97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778606"
---
# <a name="decompressing-a-single-file"></a><span data-ttu-id="2607c-103">Descompactando um único arquivo</span><span class="sxs-lookup"><span data-stu-id="2607c-103">Decompressing a Single File</span></span>

<span data-ttu-id="2607c-104">Um aplicativo pode descompactar um único arquivo compactado executando as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="2607c-104">An application can decompress a single compressed file by performing the following tasks:</span></span>

1.  <span data-ttu-id="2607c-105">Abra o arquivo de origem chamando a função [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="2607c-105">Open the source file by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="2607c-106">Abra o arquivo de destino chamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="2607c-106">Open the destination file by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="2607c-107">Copie o arquivo de origem para o arquivo de destino chamando a função [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) e passando os identificadores retornados por [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="2607c-107">Copy the source file to the destination file by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function and passing the handles returned by [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
4.  <span data-ttu-id="2607c-108">Feche os arquivos chamando a função [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="2607c-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



