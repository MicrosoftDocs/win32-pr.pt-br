---
title: Uniões de RPC
description: Uniões encapsuladas e não encapsuladas e seu formato com RPC (chamada de procedimento remoto).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454076"
---
# <a name="rpc-unions"></a>Uniões de RPC

As uniões encapsuladas e não encapsuladas compartilham um<> formato de braço de União comum \_ \_ :

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

O campo de braços de União \_<2> consiste em duas partes. Se a União for uma União de estilo MIDL 1,0, os quatro bits superiores conterão o alinhamento do braço Union (alinhamento do maior braço alinhado). Caso contrário, os 4 bits superiores são zero. Os 12 bits inferiores contêm o número de braços na União. Em outras palavras:

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

A descrição do deslocamento \_ para \_ \_ o arm<2> campos contêm um deslocamento relativo assinado para a descrição do tipo do ARM. No entanto, o campo está sobrecarregado com otimização para tipos simples. Para isso, o byte superior desse campo de deslocamento é \_ \_ o byte da União mágica FC \_ (0x80) e o byte inferior do curto é o tipo de caractere de formato real do ARM. Assim, há dois intervalos para os valores de deslocamento: "80 *XX*" significa que *XX* é uma cadeia de caracteres de formato de tipo; e todo o restante dentro do intervalo (80 FF.. 7F FF) significa um deslocamento real. Isso faz com que os deslocamentos do intervalo <80 00.. 80 FF > não disponíveis como deslocamentos. O compilador verifica a partir da versão de MIDL 5.1.164.

A descrição padrão do \_ arm \_<2> o campo indica o tipo de braço de União para o ARM padrão, se houver. Se não houver um ARM padrão especificado para a União, a descrição padrão do \_ arm \_<2> campo será 0xFFFF e uma exceção será gerada se o \_ valor switch for não corresponder a nenhum dos valores de case do ARM. Se o ARM padrão for especificado, mas vazio, a descrição padrão do \_ arm \_<2> campo será zero. Caso contrário, a descrição padrão do \_ arm \_<2> campo tem a mesma semântica que o deslocamento \_ para a descrição do \_ ARM \_<2> campos.

Veja a seguir um resumo:

-   0-padrão vazio
-   FFFF-nenhum padrão
-   80xx – tipo simples
-   outro deslocamento relativo

## <a name="encapsulated-unions"></a>Uniões encapsuladas

Uma União encapsulada vem de uma sintaxe de União especial em IDL. Efetivamente, uma União encapsulada é uma estrutura de pacote com um campo discriminante no início da estrutura e a União como o único outro membro.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

Um tipo de opção de União encapsulada \_<1> campo tem duas partes. O Nibble inferior fornece o tipo de comutador real e o Nibble superior fornece o incremento de memória para ultrapassar que é um valor que o ponteiro de memória deve ser incrementado para ignorar o \_ campo switch é, que inclui qualquer preenchimento entre o \_ campo switch is () da estrutura construída pelo stub e o campo Union real.

O tamanho da memória \_<2> campo é o tamanho somente da União e é idêntico a uniões não encapsuladas. Para obter o tamanho total da estrutura que contém a União, adicione o tamanho da memória \_<2> ao incremento de memória para intervir, ou seja, o Nibble superior do tipo de comutador \_<1> campo e, em seguida, alinhe pelo alinhamento correspondente ao incremento.

## <a name="nonencapsulated-unions"></a>Uniões não encapsuladas

Uma União não encapsulada é uma situação típica em que uma União é um argumento ou campo e a opção é outro argumento ou campo, respectivamente.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Em que:

O tipo de opção \_<campo 1> é um caractere de formato para o discriminante.

A opção \_ é o \_ descritor<> o campo é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado. No entanto, para a opção \_ é a \_ Descrição<>, se a União for inserida em uma estrutura, o campo de deslocamento da opção \_ é \_ Descrição<> é o deslocamento para o \_ campo switch é a partir da posição da União na estrutura (não do início da estrutura).

A descrição do deslocamento \_ para \_ \_ o tamanho e do \_ ARM<o \_ campo 2> fornece o deslocamento para a descrição do tamanho e do ARM da União, que é idêntica à das uniões encapsuladas e é compartilhada por todas as uniões não encapsuladas do mesmo tipo:

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 