---
title: Uniões RPC
description: Uniões encapsuladas e não truncadas e seu formato com RPC (Chamada de Procedimento Remoto).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5948a0557ea968a385324244d569d3578ec5d6c0dec4af5261866ed3ba2dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011014"
---
# <a name="rpc-unions"></a>Uniões RPC

As uniões encapsuladas e não encapsuladas compartilham um formato de<> de \_ \_ união comum:

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

O campo \_ de<2> é composto por duas partes. Se a união for uma união de estilo MIDL 1.0, os 4 bits superiores conterão o alinhamento do braço de união (alinhamento do maior arm alinhado). Caso contrário, os 4 bits superiores serão zero. Os 12 bits inferiores contêm o número de mãos na união. Em outras palavras:

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

O deslocamento para a descrição do<2> campos contém um deslocamento com assinatura relativo para \_ \_ a \_ descrição do tipo do arm. No entanto, o campo é sobrecarregado com otimização para tipos simples. Para eles, o byte superior desse campo de deslocamento é FC \_ MAGIC \_ UNION BYTE (0x80) e o byte inferior do curto é o tipo de caractere de formato real do \_ arm. Assim, há dois intervalos para os valores de deslocamento: "80 *xx"* significa que *xx* é uma cadeia de caracteres de formato de tipo; e todo o resto dentro do intervalo (80 FF .. 7f FF) significa um deslocamento real. Isso faz deslocamentos do intervalo <80 00 .. 80 FF > indisponíveis como deslocamentos. O compilador verifica isso desde a versão MIDL 5.1.164.

A descrição padrão do<campo 2> indica o tipo de arm de união para o \_ \_ arm padrão, se for o caso. Se não houver nenhum arm padrão especificado para a união, a descrição padrão do arm<2 campo> será 0xFFFF e uma exceção será apriida se o valor switch for não corresponder a nenhum dos valores de caso do \_ \_ \_ arm. Se o arm padrão for especificado, mas vazio, a descrição do arm \_ \_ padrão<2> campo será zero. Caso contrário, a descrição do<2> campo tem a mesma semântica que o deslocamento para arm \_ \_ description<\_ \_ \_ 2> campos.

Veja a seguir um resumo:

-   0 – padrão vazio
-   FFFF – sem padrão
-   80xx – tipo simples
-   outros - deslocamento relativo

## <a name="encapsulated-unions"></a>Uniões encapsuladas

Uma união encapsulada vem de uma sintaxe de união especial em IDL. Efetivamente, uma união encapsulada é uma estrutura de pacote com um campo discriminante no início da estrutura e a união como o único outro membro.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

O tipo de composição de uma união \_ encapsulada<1> campo tem duas partes. A nibble inferior fornece o tipo de comutamento real, e a nibble superior fornece o incremento de memória para passar, ou seja, uma quantidade que o ponteiro de memória deve ser incrementado para ignorar o campo é o comutamento, que inclui qualquer preenchimento entre o campo switch is() da estrutura construída por stub e o campo de união \_ \_ real.

O tamanho da<2> campo é apenas o tamanho da união e é idêntico a uniões não \_ não truncadas. Para obter o tamanho total da estrutura que contém a união, adicione o tamanho da memória<2> ao incremento de memória para passar por cima, ou seja, para a parte superior do tipo de opção<1 campo> e, em seguida, alinhe pelo alinhamento correspondente ao \_ \_ incremento.

## <a name="nonencapsulated-unions"></a>Uniões não truncadas

Uma união não truncada é uma situação típica em que uma união é um argumento ou campo e a opção é outro argumento ou campo, respectivamente.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Em que:

O tipo \_ de<1> campo é um caractere de formato para o discriminante.

A opção é descritor<> campo é um descritor de correlação e tem 4 ou \_ \_ 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado. No entanto, para a opção é descrição<>, se a união for inserida em uma estrutura, o campo de deslocamento da opção é descrição<> é o deslocamento para o campo é o campo da posição da união na estrutura (não do início da \_ \_ \_ \_ \_ estrutura).

O deslocamento para tamanho e descrição do arm<campo 2> fornece o deslocamento para o tamanho da união e a descrição do arm, que é idêntico ao das uniões \_ \_ \_ \_ encapsuladas e é compartilhado por todas as uniões não encapsuladas do mesmo tipo \_ :

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 