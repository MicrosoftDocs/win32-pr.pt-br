---
title: Layout do ponteiro
description: O layout do ponteiro descreve os ponteiros de uma estrutura ou de uma matriz.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6616cc7d1000b042c6039b2abf3f79d4900cd0e5fadac748881666610b139c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019187"
---
# <a name="pointer-layout"></a>Layout do ponteiro

O layout do ponteiro descreve os ponteiros de uma estrutura ou de uma matriz.

## <a name="pointer_layout"></a><> de layout do ponteiro \_

Um \_ campo de<> de layout de ponteiro consiste no pad de formato FC \_ PP FC \_ seguido por uma ou mais descrições de ponteiro, conforme descrito posteriormente e terminando com um \_ caractere de formato FC end:

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

Um layout de instância de ponteiro \_ \_<> campo é uma cadeia de caracteres de formato que descreve uma ou várias instâncias de ponteiros. Os seguintes campos são usados nesses Descritores:

-   deslocamento \_ na \_ memória

    O deslocamento assinado para o local do ponteiro na memória. Para um ponteiro que reside em uma estrutura, esse deslocamento é um deslocamento negativo do final da estrutura (o final da parte não compatível das estruturas em conformidade); para matrizes, o deslocamento é do início da matriz.

-   deslocamento \_ no \_ buffer

    O deslocamento assinado para o local do ponteiro no buffer. Para um ponteiro que reside em uma estrutura, esse deslocamento é um deslocamento negativo do final da estrutura (o final da parte não compatível das estruturas em conformidade): para matrizes, o deslocamento é do início da matriz.

-   deslocamento \_ para \_ matriz

    Deslocamento de uma estrutura delimitadora para a matriz inserida cujos ponteiros estão sendo manipulados. Para matrizes de nível superior, esse campo sempre será zero.

-   iterações

    Número total de ponteiros que têm o mesmo layout<> descrito.

-   incremento

    Incrementar entre ponteiros sucessivos durante uma repetição.

-   número \_ de \_ ponteiros

    Número de ponteiros diferentes em uma instância de repetição.

-   Descrição do ponteiro \_

    Descrição do ponteiro.

Todos os layouts de instância de ponteiro usam a seguinte instância de ponteiro único \_<8>:

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

Veja a seguir os descritores de instância:

**Instância única de um ponteiro para um tipo simples:**

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

**Ponteiro de repetição fixo:**

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

**Ponteiro de repetição de variável:**

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

Para instâncias de repetição fixa e de ponteiro de repetição variável, há um conjunto de descrições de deslocamento e ponteiro para cada ponteiro na instância de repetição.

## <a name="pointers-layout-design-issues"></a>Problemas de design de layout de ponteiros

Esta seção aborda os problemas relacionados ao processamento de estruturas de conformidade e ponteiros incorporados. O problema é que o compilador gera layouts de ponteiro para estruturas e matrizes com alguma redundância. Isso é benéfico, pois as informações são úteis e, por exemplo, uma estrutura compatível pode percorrer um layout de ponteiro para atender a todos os ponteiros da estrutura e da matriz de conformidade que faz parte da estrutura compatível. No entanto, existem algumas situações incorporadas que exigem que o mecanismo de NDR execute trabalho adicional para processar todos os layouts de ponteiro na sequência apropriada, processando cada ponteiro exatamente uma vez.

## <a name="what-the-compiler-generates"></a>O que o compilador gera

Cada objeto abordado nesta seção tem ponteiros, por exemplo, uma estrutura compatível tem ponteiros na parte da estrutura, bem como nos elementos da matriz. O elemento é uma estrutura simples com um ponteiro.

1.  Estrutura compatível, nível único

    O descritor de conformidade tem uma PP parte onde todos os ponteiros são descritos, tanto da estrutura quanto da matriz. A lista de membros tem FC \_ longo no lugar de um ponteiro. O descritor de matriz CARRAY tem elementos por meio do uso de um \_ complexo incorporado e nenhum descritor de ponteiro. O elemento ainda tem seu único descritor de ponteiro. O layout do ponteiro precede o layout do membro em uma estrutura compatível e descritores de estrutura simples.

2.  Estrutura compatível, dois ou mais níveis

    A descrição PP tem ponteiros de todos os níveis. Ele reutiliza a mesma descrição de matriz da estrutura de conformidade interna. A lista de membros tem FC \_ longo no lugar de um ponteiro. Uma estrutura incorporada vem pelo uso de um complexo incorporado. O descritor de estrutura compatível é reutilizado como está. O tamanho da parte plana da estrutura também é completo, o que significa que o tamanho da estrutura de nível superior incluirá o tamanho fixo da estrutura inserida.

3.  Estrutura complexa, nível único

    Os membros do ponteiro são marcados pelo ponteiro do FC \_ . O layout do ponteiro é simplificado, de modo que haja um descritor de ponteiro (4 bytes) para cada entrada de ponteiro de FC \_ na lista. O layout do ponteiro é movimentado em paralelo com uma movimentação de membro, ou seja, um \_ ponteiro de FC faz com que a próxima descrição do ponteiro seja processada. A matriz CARRAY tem layout de ponteiro com todos os descritores da matriz e, em seguida, o elemento, por meio do uso de um complexo incorporado. O descritor de elemento é reutilizado. O tamanho da parte plana da estrutura é concluído; em outras palavras, o tamanho fixo da estrutura de nível superior inclui o tamanho fixo da estrutura incorporada. O layout do membro precede o layout do ponteiro para estruturas complexas.

    Portanto, a geração de descrição de matriz em conformidade é diferente dependendo se é uma matriz dentro de uma estrutura compatível ou dentro de uma estrutura complexa.

4.  Estrutura complexa, 2 ou mais níveis, complexa em complexo

    A estrutura complexa de nível superior tem seus ponteiros de membro, estrutura complexa inserida tem seus ponteiros de membro. O descritor de estrutura compatível é reutilizado. O descritor de matriz na parte superior é a matriz reutilizada da estrutura inserida.

5.  Estrutura complexa com uma estrutura compatível incorporada

    A estrutura compatível de nível superior = tem seus ponteiros de membro. O descritor de estrutura compatível é reutilizado como está. O descritor de matriz é reutilizado da estrutura compatível incorporada; em outras palavras, ele não tem nenhum ponteiro no descritor de matriz. O elemento tem seu descritor de ponteiro.

6.  Matrizes de estruturas com ponteiros

    Uma matriz de estruturas simples com ponteiros é gerada como um SMFARRAY ou CARRAY dependendo se a matriz é dimensionada, mas em ambos os casos ele tem um layout de ponteiro concluído ( \_ repetição fixa ou repetição de variável \_ ). O layout do ponteiro vem antes do layout do membro.

    Uma matriz de estruturas complexas com ponteiros é gerada como \_ matriz falsa, independentemente de ser fixa ou dimensionada, e em ambos os casos, não tem nenhum layout de ponteiro.

## <a name="what-the-ndr-engine-does"></a>O que o mecanismo de NDR faz

Esta seção descreve o comportamento do mecanismo de NDR.

**A passagem de marshaling**

1.  Estruturas de conformidade e estrutura de conformidade incorporada.

    A estrutura de nível superior se comporta como uma estrutura de nível único.

2.  Estrutura complexa inserida com matriz em conformidade

    Qualquer estrutura complexa força a estrutura externa a ser uma estrutura complexa. A estrutura inserida nunca realiza marshaling de sua matriz. Cada estrutura sempre passa por ponteiros incorporados simplesmente realizando marshaling de membros e um membro que está acontecendo como um ponteiro de FC \_ .

3.  Estrutura complexa com estrutura compatível

    A estrutura compatível mais alta incorporada realiza marshaling da matriz em conformidade e de todos os pontos. O mecanismo de NDR nunca descende para estruturas de conformidade aninhadas mais profundas se houver alguma; Isso simplifica a solução, pois uma estrutura compatível é um objeto folha no que diz respeito ao marshaling de objetos inseridos. A estrutura complexa de nível superior ignora o empacotamento de matriz.

**Desempacotamento, bufsizing e liberação de passagens**

O desempacotamento é simétrico para o marshaling; a primeira operação que ele executa para estruturas complexas é descobrir o local dos pontos do buffer por meio da chamada da função **NdrComplexStructBufferSize** . Em seguida, ele desempacota os pontos de ponto em paralelo, habilitando o mesmo esquema para desempacotamento dos pontos corretamente a serem usados. Não deve haver nenhuma confusão sobre objetos e uniões de tamanho; a imagem de memória não deve ser usada para objetos dimensionados e uniões, apenas para o conteúdo do buffer.

Os sinalizadores usados para executar o marshaling e o desempacotamento corretamente são usados da mesma maneira no bufsizing e liberados para garantir que os pontos sejam percorridos exatamente uma vez.

**Endianess Pass**

A princípio, o endianess Pass é um pouco semelhante ao empacotamento/desempacotamento; são necessárias duas passagens para processar estruturas complexas. A primeira passagem converte a parte plana e localiza o local dos pontos do ponto no buffer, semelhante a como o bufsizing executa essa operação para desempacotamento. Em seguida, a segunda passagem converte os pontos.

As passagens de endianess são diferentes da seguinte maneira: todas as estruturas e todos os membros têm que ser percorridos até que o membro folha ou o elemento seja um tipo simples. Isso é diferente do desempacotamento; no desempacotamento, por exemplo, nunca há necessidade de processar estruturas de conformidade inseridas em estruturas em conformidade ou em qualquer membro da estrutura compatível, para esse assunto. Outro problema é que a conversão não é uma operação idempotente; portanto, a passagem de desempacotamento pode refazer o desempacotamento de algumas partes sem danos, enquanto a conversão precisa ser executada em uma base de tipo estritamente única vez por qualquer um.

Portanto, o algoritmo endianess pode ser resumido da seguinte maneira. A NDR tem uma noção da estrutura compatível de nível superior e um sinalizador para marcá-la, conforme apropriado. Ao passar pela primeira vez, como converter a parte plana e obter o local dos pontos, essa noção não será usada. A NDR seria decrescente pelas partes planas de todos os níveis de estruturas e nunca entraria no processamento de ponteiro. Por fim, a NDR converteria a matriz no nível superior.

Ao passar pela segunda vez, o sinalizador seria usado para marcar a passagem do ponteiro inserido para evitar a inserção de níveis mais profundos das estruturas compatíveis e, em seguida, a estrutura mais compatível. Dessa forma, o sinalizador forçaria o comportamento comum de marshaling/desmarque, que é evitar a queda em níveis mais profundos de estruturas compatíveis.

A segunda passagem para estruturas complexas com matrizes compatíveis funciona da seguinte maneira: as estruturas complexas funcionam da maneira comum; o que significa que níveis mais profundos nunca olhariam ou ignorariam seu tamanho compatível ou suas matrizes compatíveis e, em vez disso, simplesmente explicam seus membros sem tocar na matriz.

Para estruturas complexas com estruturas compatíveis, a estrutura compatível deve estar ciente se ela é de nível superior e se está em uma estrutura complexa. A parte plana da matriz é processada pela estrutura mais compatível. Na segunda passagem, a estrutura mais compatível ignoraria a parte simples e passaria pelo layout do ponteiro e retornaria. A estrutura mais complexa ignoraria sua parte plana e também ignoraria o layout do ponteiro.

**O aspecto robusto das orientações de endiaidade**

O passo a passo de endiaidade verifica as condições comuns fora do buffer e executa outras verificações de natureza não corrigida. As verificações destinadas a valores correlacionados (como o argumento de tamanho versus o tamanho compatível) não podem ser executadas usando esta etapa; eles são executados posteriormente, ao desmarcar.

 

 




