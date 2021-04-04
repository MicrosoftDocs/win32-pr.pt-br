---
title: C-problemas de empacotamento do compilador
description: Os níveis de embalagem afetam o layout de memória dos tipos do MIDL e do compilador C/C++ da Microsoft da mesma forma.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL do compilador MIDL, problemas de empacotamento do compilador C
- MIDL de empacotamento
- MIDL de layout de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823733"
---
# <a name="c-compiler-packing-issues"></a>C-problemas de empacotamento do compilador

Os níveis de embalagem afetam o layout de memória dos tipos do MIDL e do compilador C/C++ da Microsoft da mesma forma. Em ambientes do Microsoft Build, como o ambiente de compilação definido pelo VC + + ou o SDK (Kit de desenvolvimento de software) de plataforma, o nível de embalagem padrão para compiladores MIDL e C/C++ é o mesmo; o nível de embalagem padrão para os ambientes de Build do Windows de 32 bits e 64 bits é 8.

## <a name="natural-alignment"></a>Alinhamento natural

Para tipos na memória, o alinhamento padrão é o mesmo que seu alinhamento natural.

-   Um tipo base, como Short, float e \_ \_ Int64, e um ponteiro é alinhado naturalmente se sua representação começa em um endereço que tem seu tamanho de módulo. Todos os tipos de base com suporte no momento têm tamanhos de 1, 2, 4 ou 8. Os ponteiros têm um tamanho de 4 em ambientes de 32 bits e 8 em ambientes de 64 bits.
-   Um tipo composto é alinhado naturalmente se cada um de seus componentes está alinhado naturalmente em relação ao início do tipo e se não há lacunas desnecessárias (preenchimento) entre os componentes. Componentes compostos, como campos ou elementos, são recursivamente para componentes de tipo de ponteiro ou de base.

Uma regra simples para ajudar a lembrar esse comportamento é que o alinhamento natural de um tipo é igual aos maiores alinhamentos de seus componentes.

Há uma conexão entre o alinhamento e o tamanho da memória de um tipo em linguagens como C ou C++ e IDL, conforme expresso pelo operador **sizeof ()**. O tamanho é um múltiplo do alinhamento (o mínimo varia de abrangência do tipo). Isso segue de uma representação de matriz na memória.

O alinhamento natural é importante porque o acesso a dados desalinhados pode causar uma exceção em alguns sistemas. Os dados podem ser marcados para uma manipulação segura quando desalinhados, mas normalmente isso envolve uma penalidade de velocidade que pode ser substancial em algumas plataformas.

> [!Note]  
> Na memória, os objetos de tipos com um alinhamento natural de *n* são garantidos para serem alinhados corretamente quando colocados em endereços que são múltiplos de *n*.

 

## <a name="packing-versus-alignment"></a>Empacotamento versus alinhamento

A especificação de um nível de embalagem maior do que o alinhamento natural de um tipo não altera o alinhamento do tipo. A especificação de um nível de embalagem menor do que o alinhamento natural reduz o alinhamento de tipo ao nível de embalagem. Como resultado, os tipos empacotados podem ser colocados na memória em endereços que são um múltiplo do nível de embalagem (o alinhamento reduzido) sem causar um desalinhamento. Isso afeta os tipos simples e os tipos de componentes. Para tipos compostos, o layout interno do tipo pode ser afetado, pois o alinhamento reduzido dos componentes pode alterar o tamanho do preenchimento necessário para o alinhamento adequado dos componentes, reduzindo assim o tamanho do tipo.

Uma regra simples para ajudar a lembrar esse comportamento é que o novo alinhamento de um tipo empacotado é menor do que o nível de embalagem e seu alinhamento natural. O tamanho do tipo é um múltiplo do novo alinhamento. O operador **sizeof ()** retorna o tamanho reduzido para os tipos empacotados.

Por exemplo, com o nível de embalagem 2, um longo torna-se alinhado a 2 e, portanto, pode ser colocado em qualquer endereço par, não apenas nos endereços que são um múltiplo de 4, como seria o caso com alinhamento natural. Uma estrutura com um curto e um longo, empacotada em 2, não precisa da lacuna interna entre o curto e o seguinte que era necessário para o alinhamento natural; Portanto, não só a estrutura agora está alinhada a 2; ela também tem seu tamanho reduzido de 8 para 6.

Como exemplo, considere um tipo composto que consiste em um caractere de 1 byte, um inteiro de 4 bytes e um caractere de 1 byte:

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

Essa estrutura está naturalmente alinhada a 4 e tem o tamanho natural de 12.

Para o nível de embalagem 4 ou superior, a estrutura **MyStruct** é alinhada a 4 e `sizeof(struct mystructtype)` é igual a 12. A estrutura será desalinhada se estiver localizada na memória em um endereço que não seja um múltiplo de 4.

Para o nível de embalagem 2, a estrutura é alinhada em 2 e seu tamanho é 8. A estrutura empacotada com nível 2 será desalinhada se estiver localizada na memória em um endereço que não seja um múltiplo de 2.

Para o nível de embalagem 1, a estrutura é alinhada em 1 e seu tamanho é 6. A estrutura empacotada com o nível 1 pode ser colocada em qualquer lugar sem causar uma falha de alinhamento incorreto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>


</dt> <dt>

[/ZP](./-zp.md)
</dt> <dt>

[/Pack](./-pack.md)
</dt> </dl>

 

 