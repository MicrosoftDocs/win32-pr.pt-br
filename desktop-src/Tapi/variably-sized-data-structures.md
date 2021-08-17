---
description: Quando estruturas de dados de tamanho variavel são usadas para transmitir informações entre a TAPI e o aplicativo, o aplicativo é responsável por alocar a memória necessária.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Estruturas de dados de tamanho variavel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182e349079abbce93f533b1b6cd299ab7e0e883d71e9b845dfdaf52bf0275ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760191"
---
# <a name="variably-sized-data-structures"></a>Estruturas de dados de tamanho variavel

Quando estruturas de dados de tamanho variavel são usadas para transmitir informações entre a TAPI e o aplicativo, o aplicativo é responsável por alocar a memória necessária. A quantidade de memória alocada deve ser pelo menos grande o suficiente para a parte fixa da estrutura de dados e é definida pelo aplicativo no **membro dwTotalSize** da estrutura de dados. Os **membros dwUsedSize** e **dwNeededSize** são preenchidos pela TAPI. Se **dwTotalSize** for menor que o tamanho da parte fixa, LINEERR/PHONEERR \_ STRUCTURETOOSMALL será retornado. Se uma função retornar êxito, todos os campos na parte fixa terão sido preenchidos. Os **membros dwUsedSize** e **dwNeededSize** podem ser comparados para determinar se todas as partes variáveis foram preenchidas e quanto espaço seria necessário para preenchê-las.

Se **dwNeededSize** for igual a **dwUsedSize**, todas as partes fixas e variáveis terão sido preenchidas. Se **dwNeededSize** for maior que **dwUsedSize**, algumas partes variáveis poderão ter sido preenchidas, mas exatamente quais campos de tamanho variável foram preenchidos será indefinido. Nenhuma parte variável nunca é truncada e as partes variáveis que teriam sido truncadas devido a espaço insuficiente são indicadas tendo as partes "Offset" e "Size" correspondentes definidas como zero. Se eles não são zero (e nenhum erro foi retornado), eles indicam o deslocamento e o tamanho de dados de partes variáveis válidos e não nãotruncados.

Um aplicativo sempre pode garantir que todas as partes variáveis sejam preenchidas alocando e indicando **que dwNeededSize** bytes para a estrutura e chamando a função "Get" novamente até que a função retorne êxito e **dwNeedSize** seja igual a **dwUsedSize**. Isso deve acontecer na segunda tentativa, exceto para condições de corrida que causam alterações no tamanho de partes variáveis entre chamadas, o que deve ser uma ocorrência rara.

> [!Note]  
> Todas as cadeias de caracteres de texto, independentemente da codificação, em estruturas de tamanho variavel devem ser terminadas em **NULL** de acordo com as convenções normais de manipulação de cadeia de caracteres C.

 

 

 



