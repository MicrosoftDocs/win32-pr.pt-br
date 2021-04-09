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
# <a name="data-x-file-format-binary-encoding"></a><span data-ttu-id="68c25-103">Dados (formato de arquivo X, codificação binária)</span><span class="sxs-lookup"><span data-stu-id="68c25-103">Data (X file format, binary encoding)</span></span>

<span data-ttu-id="68c25-104">Um objeto de dados tem a seguinte definição de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="68c25-104">A data object has the following syntax definition.</span></span>


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



<span data-ttu-id="68c25-105">Observe que, na \_ lista de números e \_ nos dados da lista flutuante em arquivos binários, a vírgula do token \_ e o \_ ponto e vírgula do token não são usados.</span><span class="sxs-lookup"><span data-stu-id="68c25-105">Note that in number\_list and float\_list data in binary files, TOKEN\_COMMA and TOKEN\_SEMICOLON are not used.</span></span> <span data-ttu-id="68c25-106">A vírgula e o ponto e vírgula são usados em dados da lista de cadeia de caracteres \_ .</span><span class="sxs-lookup"><span data-stu-id="68c25-106">The comma and semicolon are used in string\_list data.</span></span> <span data-ttu-id="68c25-107">Observe também que você só pode usar \_ a referência de dados para membros de dados opcionais.</span><span class="sxs-lookup"><span data-stu-id="68c25-107">Also note that you can only use data\_reference for optional data members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68c25-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68c25-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68c25-109">Codificação binária</span><span class="sxs-lookup"><span data-stu-id="68c25-109">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



