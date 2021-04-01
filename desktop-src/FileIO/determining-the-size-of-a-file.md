---
description: A função GetFiles recupera o tamanho de um arquivo.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Determinando o tamanho de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921860"
---
# <a name="determining-the-size-of-a-file"></a><span data-ttu-id="67b16-103">Determinando o tamanho de um arquivo</span><span class="sxs-lookup"><span data-stu-id="67b16-103">Determining the Size of a File</span></span>

<span data-ttu-id="67b16-104">A função [**GetFiles**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera o tamanho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="67b16-104">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span>

<span data-ttu-id="67b16-105">Como a implementação de arquivos do sistema de arquivos NTFS permite vários fluxos dentro de um arquivo, qualquer aplicativo que você escreve que acesse arquivos deve considerar a possibilidade de que o criador do arquivo possa incluir vários fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="67b16-105">Because the NTFS file system implementation of files allows for multiple streams within a file, any application you write that accesses files must account for the possibility that the creator of the file can include multiple streams in the file.</span></span> <span data-ttu-id="67b16-106">Se vários fluxos não forem verificados em um arquivo, o aplicativo poderá subestimar o tamanho total do arquivo, entre outros erros.</span><span class="sxs-lookup"><span data-stu-id="67b16-106">If multiple streams are not checked for in a file, the application can underestimate the total size of the file, among other errors.</span></span>

 

 



