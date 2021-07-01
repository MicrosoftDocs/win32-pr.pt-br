---
title: Ponteiros (RPC)
description: Saiba mais sobre um ponteiro comum RPC, que é definido como tudo que não seja ponteiros de interface e ponteiros de contagem de byte.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119701"
---
# <a name="pointers-rpc"></a>Ponteiros (RPC)

## <a name="common-pointers"></a>Ponteiros comuns

Um ponteiro comum é definido como tudo que não seja ponteiros de interface e ponteiros de contagem de byte.

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

O primeiro formato será usado se o ponteiro for um ponteiro para um tipo simples ou um ponteiro de cadeia de caracteres nãoized. O segundo formato é usado para ponteiros para todos os outros tipos. Atributos de ponteiro indicam qual layout de descrição ele é com o sinalizador FC \_ SIMPLE \_ POINTER.

o \_ tipo de<1> é um dos seguintes.



| Caractere de formato | Descrição                              |
|------------------|------------------------------------------|
| FC \_ RP           | Um ponteiro de referência.                     |
| FC \_ UP           | Um ponteiro exclusivo.                        |
| FC \_ FP           | Um ponteiro completo.                          |
| FC \_ OP           | Um ponteiro exclusivo em uma interface de objeto. |



 

O motivo para distinguir o FC OP é semântico: em interfaces de objeto, um ponteiro in,out deve ser liberado antes de desmarcar um novo objeto e atribuir um novo valor \_ \[ de \] ponteiro.

Atributos \_ de ponteiro<1> podem ter qualquer um dos sinalizadores mostrados na tabela a seguir.



| Atributo | Sinalizador              | Descrição                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC \_ ALLOCATE \_ ALL \_ NODES | O ponteiro faz parte de um esquema de alocação \_ (todos os nós).                                                                                                                                                                   |
| 02   | FC \_ DONT \_ FREE           | Um ponteiro allocate(don't \_ free).                                                                                                                                                                                                      |
| 04   | FC \_ ALLOCED \_ ON \_ STACK   | Um ponteiro cujo referent é alocado na pilha do stub.                                                                                                                                                                            |
| 08   | FC \_ SIMPLE \_ POINTER      | Um ponteiro para um tipo simples ou uma cadeia de caracteres não compatível. Esse sinalizador que está sendo definido indica o layout da descrição do ponteiro como o layout de ponteiro simples descrito acima, caso contrário, o formato do descritor com o deslocamento é indicado. |
| 10   | FC \_ POINTER \_ DEREF       | Um ponteiro que deve ser desreferenciado antes de manipular o referenciamento do ponteiro.                                                                                                                                                           |



 

Os ponteiros que têm tamanho \_ is(), max \_ \_ is(), length is(), last \_ is() e/ou first \_ is() aplicados a \_ \_ eles têm \_ descrições de cadeia de caracteres de formato idênticas a um ponteiro para uma matriz do tipo apropriado (por exemplo, uma matriz compatível se size is() for aplicado, uma matriz variável compatível se size is() e length for aplicado).

## <a name="interface-pointers"></a>Ponteiros de interface

Uma cadeia de caracteres de formato de ponteiro de interface de objeto tem um dos dois formatos, dependendo se o IID correspondente é conhecido pelo compilador.

Um ponteiro de interface com uma IID constante tem a seguinte descrição:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

O iid<16> parte é o IID real para o ponteiro de interface. A iid é escrita na cadeia de caracteres de formato em um formato idêntico à estrutura de dados guid: long, short, short, char \[ 8 \] .

A descrição de um ponteiro de interface com iid \_ is() aplicada a ele é:

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

A descrição iid<> é um descritor de correlação e tem 4 ou \_ 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado. O valor calculado pela função **NdrComputeConformance** é o ponteiro IID.

## <a name="byte-count-pointers"></a>Ponteiros de contagem de byte

Os ponteiros de contagem de byte estão relacionados a um atributo de otimização especial chamado \[ **contagem de \_ byte** \] . Os seguintes formatos são usados:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

–e –

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

A descrição da contagem de<> é um descritor de correlação e tem 4 ou \_ \_ 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.

A descrição \_ do<> é uma descrição do tipo de pointee.

 

 
