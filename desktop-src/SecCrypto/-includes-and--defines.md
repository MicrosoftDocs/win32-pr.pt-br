---
description: Todos os exemplos na documentação do SDK de criptografia são considerados como tendo as seguintes opções de \# inclusão e \# definição de diretivas do compilador.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#inclui e #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9834fd8103b9fd28a01e416bd1df8b03fb7ad680
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105810518"
---
# <a name="includes-and-defines"></a><span data-ttu-id="664bc-103">\#inclui e \# define</span><span class="sxs-lookup"><span data-stu-id="664bc-103">\#includes and \#defines</span></span>

<span data-ttu-id="664bc-104">Todos os exemplos na documentação do SDK de criptografia são considerados como tendo as seguintes opções de **\# inclusão** e **\# definição** de diretivas do compilador.</span><span class="sxs-lookup"><span data-stu-id="664bc-104">All of the examples in the Cryptography SDK documentation are assumed to have the following **\#include** and **\#define** compiler directives.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



<span data-ttu-id="664bc-105">Além disso, a constante do **\_ Win32 \_ WinNT** deve ser definida adequadamente.</span><span class="sxs-lookup"><span data-stu-id="664bc-105">Additionally, the **\_WIN32\_WINNT** constant must be appropriately defined.</span></span> <span data-ttu-id="664bc-106">Para obter mais informações sobre o **\_ Win32 \_ WinNT**, consulte [usando os cabeçalhos do Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="664bc-106">For more information about **\_WIN32\_WINNT**, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

 

 
