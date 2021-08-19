---
title: Problemas de empacotamento do compilador C
description: Os níveis de empacotamento afetam o layout de memória dos tipos para MIDL e o compilador do Microsoft C/C++ da mesma maneira.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL compiler MIDL , problemas de empacotamento do compilador C
- empacotando MIDL
- layout de memória MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d355214c7f3222d67fd7673de4f9d32d19b4c885e8f97143c80df7b98bc0e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807889"
---
# <a name="c-compiler-packing-issues"></a>Problemas de empacotamento do compilador C

Os níveis de empacotamento afetam o layout de memória dos tipos para MIDL e o compilador do Microsoft C/C++ da mesma maneira. Em ambientes de build da Microsoft, como o ambiente de build definido pelo VC++ ou o SDK (Kit de Desenvolvimento de Software de Plataforma), o nível de empacotamento padrão para compiladores MIDL e C/C++ é o mesmo; o nível de empacotamento padrão para os ambientes de build de 32 e 64 bits Windows build é 8.

## <a name="natural-alignment"></a>Alinhamento natural

Para tipos na memória, o alinhamento padrão é o mesmo que seu alinhamento natural.

-   Um tipo base, como short, float e \_ int64, e um ponteiro é alinhado naturalmente se sua representação começa em um endereço que tem \_ seu tamanho de módulo. Todos os tipos de base com suporte no momento têm tamanhos de 1, 2, 4 ou 8. Os ponteiros têm um tamanho de 4 em ambientes de 32 bits e 8 em ambientes de 64 bits.
-   Um tipo composto será alinhado naturalmente se cada um de seus componentes estiver alinhado naturalmente em relação ao início do tipo e se não houver lacunas desnecessárias (preenchimento) entre componentes. Componentes compostos, como campos ou elementos, são recursados para componentes de ponteiro ou tipo base.

Uma regra simples para ajudar a lembrar esse comportamento é que o alinhamento natural de um tipo é igual aos maiores alinhamentos de seus componentes.

Há uma conexão entre o alinhamento e o tamanho da memória de um tipo em linguagens como C ou C++ e IDL, conforme expresso pelo **operador sizeof().** O tamanho é um múltiplo do alinhamento (o múltiplo mínimo que abrange o tipo). Isso se segue de uma representação de matriz na memória.

O alinhamento natural é importante porque o acesso a dados desalinhados pode causar uma exceção em alguns sistemas. Os dados podem ser marcados para uma manipulação segura quando desalinhados, mas normalmente isso envolve uma penalidade de velocidade que pode ser substancial em algumas plataformas.

> [!Note]  
> Na memória, os objetos de tipos com um alinhamento natural de *n* têm a garantia de serem alinhados corretamente quando colocados em endereços que são um múltiplo de *n*.

 

## <a name="packing-versus-alignment"></a>Empacotamento versus alinhamento

Especificar um nível de empacotamento maior que o alinhamento natural de um tipo não altera o alinhamento do tipo. Especificar um nível de empacotamento menor que o alinhamento natural reduz o alinhamento do tipo ao nível de empacotamento. Como resultado, os tipos empacotados podem ser colocados na memória em endereços que são um múltiplo do nível de empacotamento (o alinhamento reduzido) sem causar um desalinhamento. Isso afeta tipos simples e tipos de componente. Para tipos compostos, o layout interno do tipo pode ser afetado, pois o alinhamento reduzido dos componentes pode alterar o tamanho do preenchimento necessário para o alinhamento adequado dos componentes, reduzindo assim o tamanho do tipo.

Uma regra simples para ajudar a lembrar esse comportamento é que o novo alinhamento de um tipo empacotado é o menor do nível de empacotamento e seu alinhamento natural. O tamanho do tipo é um múltiplo do novo alinhamento. O **operador sizeof()** retorna o tamanho reduzido para tipos empacotados.

Por exemplo, com o nível de empacotamento 2, um longo se alinha a 2 e, portanto, pode ser colocado em qualquer endereço, não apenas nos endereços que são um múltiplo de 4, como seria o caso com alinhamento natural. Uma estrutura com um curto e um longo, empacotada em 2, não precisa da lacuna interna entre o curto e o longo a seguir que foi necessário para o alinhamento natural; portanto, não apenas a estrutura agora está alinhada a 2, mas também tem seu tamanho reduzido de 8 para 6.

Por exemplo, considere um tipo composto que consiste em um caractere de 1 byte, um inteiro de 4 bytes de comprimento e um caractere de 1 byte:

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

Essa estrutura é naturalmente alinhada em 4 e tem o tamanho natural de 12.

Para o nível de empacotamento 4 ou superior, a estrutura **mystruct** é alinhada em 4 e é `sizeof(struct mystructtype)` igual a 12. A estrutura será desalinhada se estiver localizada na memória em um endereço que não seja um múltiplo de 4.

Para o nível de empacotamento 2, a estrutura é alinhada a 2 e seu tamanho é 8. A estrutura empacotada com o nível 2 será desalinhada se localizada na memória em um endereço que não seja um múltiplo de 2.

Para o nível de empacotamento 1, a estrutura é alinhada a 1 e seu tamanho é 6. A estrutura empacotada com nível 1 pode ser colocada em qualquer lugar sem causar uma falha de desalinhamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>


</dt> <dt>

[/zp](./-zp.md)
</dt> <dt>

[/pack](./-pack.md)
</dt> </dl>

 

 