---
title: Buscando uma nova posição em um arquivo
description: Buscando uma nova posição em um arquivo
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- e/s de arquivo multimídia, migrando para o início dos arquivos
- e/s de arquivo, migrando para o início dos arquivos
- entrada e saída (e/s), migrando para o início dos arquivos
- E/s (entrada e saída), movendo para o início dos arquivos
- migrando para O início dos arquivos de e/s
- e/s de arquivo multimídia, buscando nova posição nos arquivos
- e/s de arquivo, buscando nova posição nos arquivos
- entrada e saída (e/s), buscando nova posição nos arquivos
- E/s (entrada e saída), buscando nova posição nos arquivos
- Buscando nova posição em arquivos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949ca3e9d118fdd83e5b53ae9336ad8ab601c64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293905"
---
# <a name="seeking-to-a-new-position-in-a-file"></a><span data-ttu-id="e4947-113">Buscando uma nova posição em um arquivo</span><span class="sxs-lookup"><span data-stu-id="e4947-113">Seeking to a New Position in a File</span></span>

<span data-ttu-id="e4947-114">O exemplo a seguir passa para o início de um arquivo aberto usando a função [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .</span><span class="sxs-lookup"><span data-stu-id="e4947-114">The following example moves to the beginning of an open file using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



<span data-ttu-id="e4947-115">O exemplo a seguir passa para o final de um arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="e4947-115">The following example moves to the end of an open file.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



<span data-ttu-id="e4947-116">O exemplo a seguir passa para uma posição de 10 bytes do final de um arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="e4947-116">The following example moves to a position 10 bytes from the end of an open file.</span></span>


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 