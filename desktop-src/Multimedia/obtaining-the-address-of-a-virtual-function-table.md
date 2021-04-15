---
title: Obtendo o endereço de uma tabela de funções virtuais
description: Obtendo o endereço de uma tabela de funções virtuais
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498690"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a><span data-ttu-id="957dd-103">Obtendo o endereço de uma tabela de funções virtuais</span><span class="sxs-lookup"><span data-stu-id="957dd-103">Obtaining the Address of a Virtual Function Table</span></span>

<span data-ttu-id="957dd-104">Em um aplicativo escrito na linguagem de programação C, você pode recuperar o endereço da estrutura **IAVIStreamVtbl** usando a função NewBall.</span><span class="sxs-lookup"><span data-stu-id="957dd-104">In an application written in the C programming language, you can retrieve the address of the **IAVIStreamVtbl** structure by using the NewBall function.</span></span> <span data-ttu-id="957dd-105">Essa função retorna o endereço de uma estrutura que contém um ponteiro para **IAVIStreamVtbl**.</span><span class="sxs-lookup"><span data-stu-id="957dd-105">This function returns the address of a structure containing a pointer to **IAVIStreamVtbl**.</span></span> <span data-ttu-id="957dd-106">As informações após o ponteiro **IAVIStreamVtbl** especificam os dados usados internamente pelo AVIBall.</span><span class="sxs-lookup"><span data-stu-id="957dd-106">Information following the **IAVIStreamVtbl** pointer specifies data used internally by AVIBall.</span></span> <span data-ttu-id="957dd-107">Seu manipulador de fluxo pode acrescentar suas próprias informações após o ponteiro **IAVIStreamVtbl** .</span><span class="sxs-lookup"><span data-stu-id="957dd-107">Your stream handler can append its own information after the **IAVIStreamVtbl** pointer.</span></span> <span data-ttu-id="957dd-108">Essas informações são retornadas em chamadas subsequentes para seu manipulador de fluxo.</span><span class="sxs-lookup"><span data-stu-id="957dd-108">This information is returned in subsequent calls to your stream handler.</span></span>


```C++
PAVISTREAM WINAPI NewBall(VOID) 
{ 
    PAVIBALL pball; 
    pball = (PAVIBALL) GlobalAllocPtr(GHND, sizeof(AVIBALL)); 
    if (!pball) 
        return 0; 
    pball->lpvtbl = &AVIBallHandler; 
    pball->lpvtbl->Create((PAVISTREAM) pball, 0, 0); 
    return (PAVISTREAM) pball; 
} 
```



 

 




