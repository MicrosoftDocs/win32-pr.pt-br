---
description: O Windows usa um ponteiro de arquivo para controlar os bytes lidos ou gravados.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Posicionando um ponteiro de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785464"
---
# <a name="positioning-a-file-pointer"></a><span data-ttu-id="353a7-103">Posicionando um ponteiro de arquivo</span><span class="sxs-lookup"><span data-stu-id="353a7-103">Positioning a File Pointer</span></span>

<span data-ttu-id="353a7-104">Quando um aplicativo chama [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir um arquivo pela primeira vez, o Windows coloca o [ponteiro do arquivo](file-pointers.md) no início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="353a7-104">When an application calls [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open a file for the first time, Windows places the [file pointer](file-pointers.md) at the beginning of the file.</span></span> <span data-ttu-id="353a7-105">À medida que os bytes são lidos ou gravados no arquivo, o Windows avança o ponteiro do arquivo o número de bytes lidos ou gravados.</span><span class="sxs-lookup"><span data-stu-id="353a7-105">As bytes are read from or written to the file, Windows advances the file pointer the number of bytes read or written.</span></span>

<span data-ttu-id="353a7-106">Um aplicativo pode posicionar o ponteiro do arquivo para um deslocamento especificado chamando [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span><span class="sxs-lookup"><span data-stu-id="353a7-106">An application can position the file pointer to a specified offset by calling [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span></span>

<span data-ttu-id="353a7-107">A função [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) também pode ser usada para consultar a posição do ponteiro do arquivo atual, especificando um método de movimentação do **arquivo \_ atual** e uma distância de zero.</span><span class="sxs-lookup"><span data-stu-id="353a7-107">The [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function can also be used to query the current file pointer position by specifying a move method of **FILE\_CURRENT** and a distance of zero.</span></span>

 

 



