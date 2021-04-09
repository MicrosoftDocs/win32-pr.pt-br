---
description: Quando as estruturas de dados de tamanho variavelmente são usadas para transmitir informações entre a TAPI e o aplicativo, o aplicativo é responsável por alocar a memória necessária.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Estruturas de dados de tamanho variavelmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171239"
---
# <a name="variably-sized-data-structures"></a>Estruturas de dados de tamanho variavelmente

Quando as estruturas de dados de tamanho variavelmente são usadas para transmitir informações entre a TAPI e o aplicativo, o aplicativo é responsável por alocar a memória necessária. A quantidade de memória alocada deve ser pelo menos grande o suficiente para a parte fixa da estrutura de dados e é definida pelo aplicativo no membro **dwTotalSize** da estrutura de dados. Os membros **dwUsedSize** e **dwNeededSize** são preenchidos pela TAPI. Se **dwTotalSize** for menor que o tamanho da parte fixa, LINEERR/PHONEERR \_ STRUCTURETOOSMALL será retornado. Se uma função retornar êxito, todos os campos na parte fixa terão sido preenchidos. Os membros **dwUsedSize** e **dwNeededSize** podem ser comparados para determinar se todas as partes variáveis foram preenchidas e quanto espaço seria necessário para preenchê-las.

Se **dwNeededSize** for igual a **dwUsedSize**, todas as partes fixas e variáveis serão preenchidas. Se **dwNeededSize** for maior que **dwUsedSize**, algumas partes variáveis podem ter sido preenchidas, mas exatamente quais campos de tamanho de variavelmente foram preenchidos são indefinidos. Nenhuma parte variável é truncada e as partes variáveis que teriam sido truncadas devido a espaço insuficiente são indicadas tendo as partes correspondentes de "deslocamento" e "tamanho" definidas como zero. Se esses não forem ambos zero (e nenhum erro for retornado), eles indicarão o deslocamento e o tamanho dos dados de parte variável não truncados válidos.

Um aplicativo sempre pode garantir que todas as partes variáveis sejam preenchidas alocando e indicando **dwNeededSize** bytes para a estrutura e chamando a função "Get" novamente até que a função retorne Success e **dwNeededSize** seja igual a **dwUsedSize**. Isso deve ocorrer na segunda tentativa, exceto pelas condições de corrida que causam alterações no tamanho das partes variáveis entre chamadas, o que deve ser uma ocorrência rara.

> [!Note]  
> Todas as cadeias de texto, independentemente da codificação, em estruturas de tamanho variadas devem ser terminadas em **nulo** de acordo com as convenções normais de manipulação de cadeia de caracteres C.

 

 

 



