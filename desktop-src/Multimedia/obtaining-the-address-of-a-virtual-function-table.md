---
title: Obtendo o endereço de uma tabela de funções virtuais
description: Obtendo o endereço de uma tabela de funções virtuais
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a0fbf941114cfff2b930ed329f7a35962b9ef07158fd5fda16a19a73c0f692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038426"
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



 

 




