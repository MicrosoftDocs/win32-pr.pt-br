---
title: Ponteiros (RPC)
description: Saiba mais sobre um ponteiro comum RPC, que é definido como tudo além de ponteiros de interface e ponteiros de contagem de bytes.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a87c13f9657d56e3f85d1d5828dc097c25e29990c617c5f20679a1d6cbe91e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927346"
---
# <a name="pointers-rpc"></a>Ponteiros (RPC)

## <a name="common-pointers"></a>Ponteiros comuns

Um ponteiro comum é definido como tudo que não seja ponteiros de interface e ponteiros de contagem de bytes.

Há dois layouts possíveis para a descrição:

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

–ou–

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

O primeiro formato será usado se o ponteiro for um ponteiro para um tipo simples ou um ponteiro de cadeia de caracteres não-dimensionado. O segundo formato é usado para ponteiros para todos os outros tipos. Atributos de ponteiro indicam qual layout de descrição é com o \_ sinalizador de ponteiro simples do FC \_ .

\_o tipo de ponteiro<1> é um dos seguintes.



| Formatar caractere | Descrição                              |
|------------------|------------------------------------------|
| FC \_ RP           | Um ponteiro de referência.                     |
| FC \_ para cima           | Um ponteiro exclusivo.                        |
| \_FP FC           | Um ponteiro completo.                          |
| \_op FC           | Um ponteiro exclusivo em uma interface de objeto. |



 

O motivo para distinguir o FC \_ op é semântico: em interfaces de objeto, um \[ ponteiro de entrada \] deve ser liberado antes de desempacotar um novo objeto e atribuir um novo valor de ponteiro.

Os \_ atributos de ponteiro<1> podem ter qualquer um dos sinalizadores mostrados na tabela a seguir.



| Atributo | Sinalizador              | Descrição                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | \_alocar \_ todos os nós de FC \_ | O ponteiro é uma parte de um esquema de alocação alocar (todos os \_ nós).                                                                                                                                                                   |
| 02   | FC \_ não \_ livre           | Um ponteiro de alocação (não \_ livre).                                                                                                                                                                                                      |
| 04   | FC \_ alocado \_ na \_ pilha   | Um ponteiro cujo Referent é alocado na pilha do stub.                                                                                                                                                                            |
| 08   | \_ponteiro simples do FC \_      | Um ponteiro para um tipo simples ou cadeia de caracteres de conformidade não dimensionável. Esse sinalizador sendo definido indica o layout da descrição do ponteiro como o layout do ponteiro simples descrito acima, caso contrário, o formato do descritor com o deslocamento será indicado. |
| 10   | ponteiro de FC \_ \_ DEREF       | Um ponteiro que deve ser desreferenciado antes de manipular o Referent do ponteiro.                                                                                                                                                           |



 

Ponteiros com tamanho \_ é (), o número máximo de \_ is (), length \_ é (), Last \_ is () e/ou First \_ is () aplicado a eles têm descrições de cadeia de caracteres de formato idênticas a um ponteiro para uma matriz do tipo apropriado (por exemplo, uma matriz compatível se o tamanho for \_ () for aplicado, uma matriz de variação em conformidade se o tamanho \_ for () e o comprimento \_ for aplicado

## <a name="interface-pointers"></a>Ponteiros de interface

Uma cadeia de caracteres de formato de ponteiro de interface de objeto tem um dos dois formatos, dependendo se o IID correspondente é conhecido pelo compilador.

Um ponteiro de interface com uma IID de constante tem a seguinte descrição:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

O IID<de 16> parte é o IID real para o ponteiro da interface. O IID é gravado na cadeia de caracteres de formato em um formato idêntico à estrutura de dados GUID: longo, curto, curto, Char \[ 8 \] .

A descrição de um ponteiro de interface com IID \_ é () aplicada a ele é:

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

A descrição de IID \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado. O valor calculado pela função **NdrComputeConformance** é o ponteiro de IID.

## <a name="byte-count-pointers"></a>Ponteiros de contagem de bytes

Os ponteiros de contagem de bytes estão relacionados a um atributo de otimização especial chamado \[ **\_ contagem de bytes** \] . Os seguintes formatos são usados:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

e

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

A descrição de contagem de bytes \_ \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.

A descrição do ponto \_<> é uma descrição do tipo de ponto.

 

 
