---
title: Cadeias de formato de tipo
description: Os caracteres de formato denotam objetos de interesse para o mecanismo de NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005882"
---
# <a name="type-format-strings"></a>Cadeias de formato de tipo

Os caracteres de formato denotam objetos de interesse para o mecanismo de NDR. Há um caractere de formato para cada tipo básico, para vários tipos complexos, e para descrições de ponteiros, embalagens, alinhamento e outros objetos diversos. Para tipos compostos, várias categorias de estruturas e matrizes são reconhecidas com base em suas propriedades de desempenho. Uma cadeia de caracteres de formato para cada categoria começa com um token FC que identifica a cadeia de caracteres de formato específica. Os caracteres de formato para categorias de estruturas e matrizes podem compartilhar os em correções no nome do token FC à esquerda mostrado na tabela a seguir.



| Formatar caractere | Descrição                                    |
|------------------|------------------------------------------------|
| C                | Indica informações de conformidade no tipo. |
| V                | Indica informações de variação no tipo.    |
| P                | Indica que os ponteiros fazem parte do tipo.     |



 

Por exemplo, FC \_ CSTRUCT e FC \_ CARRAY identificam a estrutura de conformidade e os descritores de matriz em conformidade, respectivamente.

Veja a seguir os caracteres de formato com significados especiais.



| Formatar caractere | Descrição                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| FC \_ PP           | Indica o início da seção de descrição do ponteiro de uma estrutura ou matriz. |



 

As cadeias de caracteres de formato do tipo NDR RPC são descritas mais detalhadamente nos seguintes tópicos:

-   [Tipos simples](simple-types-tfs.md)
-   [Ponteiros](pointers-tfs.md)
-   [matrizes](arrays-tfs.md)
-   [Cadeias de caracteres](strings-tfs.md)
-   [Descritores de correlação](correlation-descriptors-tfs.md)
-   [Estruturas](structures-tfs.md)
-   [Layout do ponteiro](pointer-layout-tfs.md)
-   [Uniões](unions-tfs.md)
-   [Transmitir \_ como e representar \_ como](transmit-as-and-represent-as-tfs.md)
-   [Marshal do usuário](user-marshal-tfs.md)

 

 




