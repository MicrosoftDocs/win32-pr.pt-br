---
title: Criando e excluindo um arquivo
description: Criando e excluindo um arquivo
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- e/s de arquivo multimídia, criando arquivos
- e/s de arquivo, criando arquivos
- entrada e saída (e/s), criando arquivos
- E/s (entrada e saída), criando arquivos
- Criando arquivos de e/s
- e/s de arquivo multimídia, excluindo arquivos
- e/s de arquivo, excluindo arquivos
- entrada e saída (e/s), excluindo arquivos
- E/s (entrada e saída), excluindo arquivos
- excluindo arquivos de e/s
- função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640617"
---
# <a name="creating-and-deleting-a-file"></a><span data-ttu-id="f0a13-114">Criando e excluindo um arquivo</span><span class="sxs-lookup"><span data-stu-id="f0a13-114">Creating and Deleting a File</span></span>

<span data-ttu-id="f0a13-115">Para criar um arquivo, defina o parâmetro *dwOpenFlags* da função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) como MMIO \_ Create.</span><span class="sxs-lookup"><span data-stu-id="f0a13-115">To create a file, set the *dwOpenFlags* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to MMIO\_CREATE.</span></span> <span data-ttu-id="f0a13-116">O exemplo a seguir cria um arquivo e o abre para leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="f0a13-116">The following example creates a file and opens it for reading and writing.</span></span>


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



<span data-ttu-id="f0a13-117">Se o arquivo que você está criando já existir, ele será truncado para comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="f0a13-117">If the file you are creating already exists, it will be truncated to zero length.</span></span>

<span data-ttu-id="f0a13-118">Para excluir um arquivo, defina o parâmetro *dwOpenFlags* da função **mmioOpen** como MMIO \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="f0a13-118">To delete a file, set the *dwOpenFlags* parameter of the **mmioOpen** function to MMIO\_DELETE.</span></span> <span data-ttu-id="f0a13-119">Depois de excluir um arquivo, ele não pode ser recuperado por nenhum meio padrão.</span><span class="sxs-lookup"><span data-stu-id="f0a13-119">After you delete a file, it cannot be recovered by any standard means.</span></span> <span data-ttu-id="f0a13-120">Se seu aplicativo estiver excluindo um arquivo na solicitação de um usuário, consulte o usuário antes de excluir o arquivo para certificar-se de que o usuário deseja excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="f0a13-120">If your application is deleting a file at the request of a user, query the user before deleting the file to make sure the user wants to delete it.</span></span>

 

 