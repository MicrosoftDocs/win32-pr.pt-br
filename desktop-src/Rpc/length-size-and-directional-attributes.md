---
title: Atributos de comprimento, tamanho e direcional
description: Ao passar matrizes entre o cliente e o servidor, os atributos relacionados ao tamanho \ max is\ e \ size is\ determinam quantos elementos de matriz o stub do \_ \_ servidor aloca.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e91424a93a53fe710c945011d19f8f97dc0f65e4899bc3305be5725d5a08e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020127"
---
# <a name="length-size-and-directional-attributes"></a>Atributos de comprimento, tamanho e direcional

Ao passar matrizes entre o cliente e o servidor, o tamanho máximo dos atributos relacionados ao tamanho é e o tamanho é determinar quantos elementos de matriz o \[ [**\_**](/windows/desktop/Midl/max-is) \] \[ [**\_**](/windows/desktop/Midl/size-is) \] stub do servidor aloca. O comprimento dos atributos relacionados ao comprimento é , primeiro é e o último é determinar quantos elementos são transmitidos para o \[ [**\_**](/windows/desktop/Midl/length-is)servidor \] e o \[ [**\_**](/windows/desktop/Midl/first-is) \] \[ [**\_**](/windows/desktop/Midl/last-is) \] cliente.

Atributos direcionais diferentes podem ser aplicados a parâmetros. No entanto, algumas combinações de atributos direcionais podem causar erros. Por exemplo, suponha que você está escrevendo uma interface que especifica um procedimento com dois parâmetros, uma matriz e o comprimento transmitido da matriz. O termo *dir \_ attr* refere-se ao atributo direcional aplicado ao parâmetro como:

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

O comportamento do compilador MIDL para cada combinação de atributos direcionais é descrito na tabela a seguir.



| Array                                          | Parâmetro length                               | Ações de stub durante a chamada do cliente para o servidor                                                                                                                                                                                                                          | Ações de stub no retorno do servidor para o cliente                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**Em**](/windows/desktop/Midl/in)\]                          | \[[**Em**](/windows/desktop/Midl/in)\]                          | Transmita o comprimento e o número de elementos indicados pelo parâmetro .                                                                                                                                                                                              | Nenhum dado transmitido.                                                                                                                                                                                                 |
| \[[**Em**](/windows/desktop/Midl/in)\]                          | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Não legal; Erro do compilador MIDL.                                                                                                                                                                                                                                         | Não legal; Erro do compilador MIDL.                                                                                                                                                                                      |
| \[[**Em**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita o comprimento e o número de elementos indicados pelo parâmetro length.                                                                                                                                                                                       | Transmita somente o comprimento.                                                                                                                                                                                            |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**Em**](/windows/desktop/Midl/in)\]                          | Transmita o comprimento.<br/> Se o tamanho da matriz for fixo, aloce o tamanho da matriz no servidor, mas não transmita nenhum elemento.<br/> Se o tamanho da matriz não estiver vinculado, não é legal: erro do compilador MIDL.<br/>                                                              | Transmita o número de elementos indicados pelo comprimento.<br/> Observe que o comprimento pode ser alterado e pode ter um valor diferente do valor no cliente. Não transmita o comprimento.<br/>          |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Aloce espaço para o parâmetro length no servidor, mas não transmita o parâmetro . Se o tamanho da matriz for fixo, aloce o tamanho da matriz no servidor, mas não transmita nenhum elemento.<br/> Se o tamanho da matriz não for fixo, não é legal: erro do compilador MIDL.<br/> | Transmita o comprimento e o número de elementos indicados pelo comprimento conforme definido pelo aplicativo de servidor.                                                                                                             |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita o parâmetro length. Se o tamanho da matriz estiver vinculado, aloce o tamanho da matriz no servidor, mas não transmita nenhum elemento.<br/> Se o tamanho da matriz não estiver vinculado, não é legal: erro do compilador MIDL.<br/>                                                           | Transmita o comprimento. Transmita o número de elementos de matriz indicados pelo comprimento.<br/>                                                                                                                       |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**Em**](/windows/desktop/Midl/in)\]                          | Transmita o comprimento e o número de elementos indicados pelo parâmetro .                                                                                                                                                                                              | Não transmita o comprimento. Transmita o número de elementos indicados pelo comprimento.<br/> Observe que o comprimento pode ser alterado e pode ter um valor diferente do valor original no cliente.<br/> |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Não legal; Erro do compilador MIDL.                                                                                                                                                                                                                                         | Não legal; Erro do compilador MIDL.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmita o comprimento e o número de elementos indicados pelo parâmetro .                                                                                                                                                                                              | Transmita o comprimento e o número de elementos indicados pelo parâmetro .                                                                                                                                           |



 

Em geral, você não deve modificar os parâmetros de tamanho ou tamanho no lado do servidor. Se você alterar o parâmetro length, poderá ficar órfão na memória. Para obter mais informações, consulte [Órfão de memória.](memory-orphaning.md)

 

