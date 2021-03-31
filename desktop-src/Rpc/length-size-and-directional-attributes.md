---
title: Atributos de comprimento, tamanho e direção
description: Ao passar matrizes entre o cliente e o servidor, os atributos relacionados ao tamanho \ Max \_ são \ e \ Size \_ is \ determinam quantos elementos de matriz o stub do servidor aloca.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ffbf1ac75ad82a89e258ab595590fce2190b9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641601"
---
# <a name="length-size-and-directional-attributes"></a>Atributos de comprimento, tamanho e direção

Na passagem de matrizes entre o cliente e o servidor, os atributos relacionados ao tamanho \[ [**máximo \_ é**](/windows/desktop/Midl/max-is) \] e o \[ [**tamanho \_**](/windows/desktop/Midl/size-is) \] determinam quantos elementos de matriz o stub do servidor aloca. O comprimento dos atributos relacionados ao comprimento \[ [**\_ é**](/windows/desktop/Midl/length-is) \] , \[ [**primeiro \_**](/windows/desktop/Midl/first-is) \] , e \[ o [**último \_ é**](/windows/desktop/Midl/last-is) \] determinar quantos elementos são transmitidos ao servidor e ao cliente.

Diferentes atributos direcionais podem ser aplicados a parâmetros. No entanto, algumas combinações de atributos direcionais podem causar erros. Por exemplo, suponha que você esteja escrevendo uma interface que especifica um procedimento com dois parâmetros, uma matriz e o comprimento transmitido da matriz. O termo *dir \_ attr* se refere ao atributo direcional aplicado ao parâmetro como:

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

O comportamento do compilador MIDL para cada combinação de atributos direcionais é descrito na tabela a seguir.



| Array                                          | Parâmetro de comprimento                               | Ações de stub durante chamada do cliente para o servidor                                                                                                                                                                                                                          | Ações de stub em retorno do servidor para o cliente                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**no**](/windows/desktop/Midl/in)\]                          | \[[**no**](/windows/desktop/Midl/in)\]                          | Transmita o comprimento e o número de elementos indicados pelo parâmetro.                                                                                                                                                                                              | Nenhum dado transmitido.                                                                                                                                                                                                 |
| \[[**no**](/windows/desktop/Midl/in)\]                          | \[[**fora**](/windows/desktop/Midl/out-idl)\]                    | Não legal; Erro do compilador MIDL.                                                                                                                                                                                                                                         | Não legal; Erro do compilador MIDL.                                                                                                                                                                                      |
| \[[**no**](/windows/desktop/Midl/in)\]                          | \[[**entrada**](/windows/desktop/Midl/in), [ **saída**](/windows/desktop/Midl/out-idl)\] | Transmita o comprimento e o número de elementos indicados pelo parâmetro de comprimento.                                                                                                                                                                                       | Transmita apenas o comprimento.                                                                                                                                                                                            |
| \[[**fora**](/windows/desktop/Midl/out-idl)\]                    | \[[**no**](/windows/desktop/Midl/in)\]                          | Transmita o comprimento.<br/> Se o tamanho da matriz for fixo, aloque o tamanho da matriz no servidor, mas não transmita nenhum elemento.<br/> Se o tamanho da matriz não estiver associado, não legal: erro do compilador MIDL.<br/>                                                              | Transmita o número de elementos indicados pelo comprimento.<br/> Observe que o comprimento pode ser alterado e pode ter um valor diferente do valor no cliente. Não transmita o comprimento.<br/>          |
| \[[**fora**](/windows/desktop/Midl/out-idl)\]                    | \[[**fora**](/windows/desktop/Midl/out-idl)\]                    | Aloque espaço para o parâmetro de comprimento no servidor, mas não transmita o parâmetro. Se o tamanho da matriz for fixo, aloque o tamanho da matriz no servidor, mas não transmita nenhum elemento.<br/> Se o tamanho da matriz não for corrigido, não legal: erro do compilador MIDL.<br/> | Transmita o comprimento e o número de elementos indicados pelo comprimento conforme definido pelo aplicativo do servidor.                                                                                                             |
| \[[**fora**](/windows/desktop/Midl/out-idl)\]                    | \[[**entrada**](/windows/desktop/Midl/in), [ **saída**](/windows/desktop/Midl/out-idl)\] | Transmita o parâmetro de comprimento. Se o tamanho da matriz for associado, aloque o tamanho da matriz no servidor, mas não transmita nenhum elemento.<br/> Se o tamanho da matriz não estiver associado, não legal: erro do compilador MIDL.<br/>                                                           | Transmita o comprimento. Transmita o número de elementos de matriz indicados pelo comprimento.<br/>                                                                                                                       |
| \[[**entrada**](/windows/desktop/Midl/in), [ **saída**](/windows/desktop/Midl/out-idl)\] | \[[**no**](/windows/desktop/Midl/in)\]                          | Transmita o comprimento e o número de elementos indicados pelo parâmetro.                                                                                                                                                                                              | Não transmita o comprimento. Transmita o número de elementos indicados pelo comprimento.<br/> Observe que o comprimento pode ser alterado e pode ter um valor diferente do valor original no cliente.<br/> |
| \[[**entrada**](/windows/desktop/Midl/in), [ **saída**](/windows/desktop/Midl/out-idl)\] | \[[**fora**](/windows/desktop/Midl/out-idl)\]                    | Não legal; Erro do compilador MIDL.                                                                                                                                                                                                                                         | Não legal; Erro do compilador MIDL.                                                                                                                                                                                      |
| \[[**entrada**](/windows/desktop/Midl/in), [ **saída**](/windows/desktop/Midl/out-idl)\] | \[[**entrada**](/windows/desktop/Midl/in), [ **saída**](/windows/desktop/Midl/out-idl)\] | Transmita o comprimento e o número de elementos indicados pelo parâmetro.                                                                                                                                                                                              | Transmita o comprimento e o número de elementos indicados pelo parâmetro.                                                                                                                                           |



 

Em geral, você não deve modificar os parâmetros de comprimento ou tamanho no lado do servidor. Se você alterar o parâmetro de comprimento, poderá órfã memória. Para obter mais informações, consulte [órfãos de memória](memory-orphaning.md).

 

