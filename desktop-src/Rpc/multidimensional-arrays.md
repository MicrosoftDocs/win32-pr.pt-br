---
title: Matrizes multidimensionais
description: Os atributos de matriz também podem ser usados com matrizes multidimensionais.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7dac2b6d093fa56383ecaf976a83acf13fec9aa0c3820c1d608ccb69e9e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928075"
---
# <a name="multidimensional-arrays"></a>Matrizes multidimensionais

Os atributos de matriz também podem ser usados com matrizes multidimensionais. No entanto, tenha cuidado para garantir que cada dimensão da matriz tenha um atributo correspondente. Por exemplo:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

A matriz anterior é uma matriz compatível (de tamanho d1size) de 30 matrizes de elementos (com elementos d2len enviados para cada um). A vírgula entre parênteses do \[ [**tamanho \_ é**](/windows/desktop/Midl/size-is) o \] atributo especifica que o valor em d1size é aplicado à primeira dimensão da matriz. Da mesma forma, o comando nos parênteses de \[ [**length \_ é**](/windows/desktop/Midl/length-is) o \] atributo indica que o valor em d2len é aplicado à segunda dimensão da matriz.

O compilador MIDL 2,0 fornece dois métodos de marshaling de parâmetros: modo misto (/**os**) e totalmente interpretado (/**OIF** ou/**Oicf**). Por padrão, o compilador MIDL compila interfaces no modo misto. Você não precisa especificar explicitamente a opção [**/os**](/windows/desktop/Midl/-os) para obter marshaling de modo misto.

O método totalmente interpretado realiza marshaling de dados completamente offline. Isso reduz consideravelmente o tamanho do código stub, mas também resulta em desempenho reduzido. No marshaling de modo misto, os stubs realiza marshaling de alguns parâmetros online. Embora isso resulte em um tamanho maior de stub, ele também oferece maior desempenho.

> [!Caution]  
> Tenha cuidado ao compilar arquivos IDL nesse modo. O uso de matrizes multidimensionais no modo misto pode resultar em parâmetros que não são empacotados corretamente. A opção de linha de comando [**/Oicf**](/windows/desktop/Midl/-oi) é recomendada quando sua interface define parâmetros que são matrizes multidimensionais.

 

O \[ atributo de [**cadeia de caracteres**](/windows/desktop/Midl/string) \] também pode ser usado com matrizes multidimensionais. O atributo aplica-se à dimensão menos significativa, como uma matriz de cadeias de caracteres compatível. Você também pode usar atributos de ponteiro multidimensional. Por exemplo:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

No exemplo anterior, a variável ptr2d é um ponteiro para um bloco de ponteiros de tamanho d1len, cada um dos quais aponta para d2len ponteiros para **Long**.

Matrizes multidimensionais não são equivalentes a matrizes de ponteiros. Uma matriz multidimensional é um bloco de dados único e grande na memória. Uma matriz de ponteiros contém apenas um bloco de ponteiros na matriz. Os dados aos quais os ponteiros apontam podem estar em qualquer lugar na memória. Além disso, a sintaxe ANSI C permite que apenas a dimensão de matriz mais significativa (mais à esquerda) não seja especificada em uma matriz multidimensional. Portanto, a seguir está uma instrução válida:

`long a1[] [20]`

Compare isso com a seguinte instrução inválida:

`long a1[20] []`

 

 