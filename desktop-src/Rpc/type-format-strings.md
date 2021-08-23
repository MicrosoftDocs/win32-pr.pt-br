---
title: Cadeias de caracteres de formato de tipo
description: Caracteres de formato denotam objetos de interesse para o mecanismo NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f4aa17494cbef0f3bcc232f89104e3502f94de4a3285a1da6cc0229af0fe26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011114"
---
# <a name="type-format-strings"></a>Cadeias de caracteres de formato de tipo

Caracteres de formato denotam objetos de interesse para o mecanismo NDR. Há um caractere de formato para cada tipo básico, para vários tipos complexos e para descrições de ponteiros, empacotamento, alinhamento e outros objetos diversos. Para tipos compostos, várias categorias de estruturas e matrizes são reconhecidas com base em suas propriedades de desempenho. Uma cadeia de caracteres de formato para cada categoria começa com um token FC que identifica a cadeia de caracteres de formato específica. Os caracteres de formato para as categorias de estruturas e matrizes podem compartilhar as correções no nome do token FC principal mostrado na tabela a seguir.



| Caractere de formato | Descrição                                    |
|------------------|------------------------------------------------|
| C                | Indica informações de conformidade no tipo. |
| V                | Indica informações de variação no tipo.    |
| P                | Indica que os ponteiros fazem parte do tipo.     |



 

Por exemplo, FC CSTRUCT e FC CARRAY identificam a estrutura compatível e \_ \_ os descritores de matriz compatíveis, respectivamente.

A seguir estão os caracteres de formato com significados especiais.



| Caractere de formato | Descrição                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| FC \_ PP           | Indica o início da seção de descrição do ponteiro de uma estrutura ou matriz. |



 

As cadeias de caracteres de formato de tipo NDR RPC são descritas mais detalhadamente nos tópicos a seguir:

-   [Tipos simples](simple-types-tfs.md)
-   [Ponteiros](pointers-tfs.md)
-   [matrizes](arrays-tfs.md)
-   [Cadeias de caracteres](strings-tfs.md)
-   [Descritores de correlação](correlation-descriptors-tfs.md)
-   [Estruturas](structures-tfs.md)
-   [Layout do ponteiro](pointer-layout-tfs.md)
-   [Uniões](unions-tfs.md)
-   [Transmitir \_ como e Representar \_ como](transmit-as-and-represent-as-tfs.md)
-   [Marshal do usuário](user-marshal-tfs.md)

 

 




