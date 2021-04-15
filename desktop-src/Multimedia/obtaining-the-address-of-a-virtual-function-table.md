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
# <a name="obtaining-the-address-of-a-virtual-function-table"></a>Obtendo o endereço de uma tabela de funções virtuais

Em um aplicativo escrito na linguagem de programação C, você pode recuperar o endereço da estrutura **IAVIStreamVtbl** usando a função NewBall. Essa função retorna o endereço de uma estrutura que contém um ponteiro para **IAVIStreamVtbl**. As informações após o ponteiro **IAVIStreamVtbl** especificam os dados usados internamente pelo AVIBall. Seu manipulador de fluxo pode acrescentar suas próprias informações após o ponteiro **IAVIStreamVtbl** . Essas informações são retornadas em chamadas subsequentes para seu manipulador de fluxo.


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



 

 




