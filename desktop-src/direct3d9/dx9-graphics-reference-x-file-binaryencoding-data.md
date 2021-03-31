---
description: Um objeto de dados tem a seguinte definição de sintaxe.
ms.assetid: e636c2eb-3c11-45bf-ab0b-a14ec878742c
title: Dados (formato de arquivo X)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdf799b9f7f155c8d2a0e883c8d5e79f8091156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087221"
---
# <a name="data-x-file-format-binary-encoding"></a>Dados (formato de arquivo X, codificação binária)

Um objeto de dados tem a seguinte definição de sintaxe.


```
object                : identifier optional_name TOKEN_OBRACE
                            optional_class_id
                            data_parts_list
                            TOKEN_CBRACE

data_parts_list       : data_part
                      | data_parts_list data_part

data_part             : data_reference
                      | object
                      | number_list
                      | float_list
                      | string_list

number_list           : TOKEN_INTEGER_LIST

float_list            : TOKEN_FLOAT_LIST

string_list           : string_list_1 list_separator

string_list_1         : string
                      | string_list_1 list_separator string

list_separator        : comma
                      | semicolon

string                : token_string

identifier            : name
                      | primitive_type

data_reference        : TOKEN_OBRACE name optional_class_id TOKEN_CBRACE
```



Observe que, na \_ lista de números e \_ nos dados da lista flutuante em arquivos binários, a vírgula do token \_ e o \_ ponto e vírgula do token não são usados. A vírgula e o ponto e vírgula são usados em dados da lista de cadeia de caracteres \_ . Observe também que você só pode usar \_ a referência de dados para membros de dados opcionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação binária](binary-encoding.md)
</dt> </dl>

 

 



