---
title: Transmit_as e Represent_as
description: Transmitir \_ como e representar \_ como compartilhar o mesmo layout, exceto para o token principal; o token lê a \_ transmissão FC \_ como ou FC \_ representa \_ como, mas o código subjacente é comum.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917345"
---
# <a name="transmit_as-and-represent_as"></a>Transmitir \_ como e representar \_ como

Transmitir \_ como e representar \_ como compartilhar o mesmo layout, exceto para o token principal; o token lê a \_ transmissão FC \_ como ou FC \_ representa \_ como, mas o código subjacente é comum.

A descrição tem o seguinte layout:

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

Os sinalizadores<1> byte consiste no Nibble superior do sinalizador e no Nibble inferior do alinhamento.

O Nibble de alinhamento mantém o alinhamento de fios do tipo transmitido. Isso é necessário quando o dimensionamento do buffer e o uso do tamanho do tipo transmitido do código de formato.

O Nibble do sinalizador pode ter os seguintes sinalizadores:

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

O \_ tipo apresentado \_ é \_ um sinalizador de matriz marca um argumento de transmissão de nível superior como (ou representa como), sendo uma matriz de algo e valor de aprovado por. O intérprete [**– Oi**](/windows/desktop/Midl/-oi) usa esse sinalizador para percorrer esse argumento (que é, na verdade, um ponteiro na pilha, não na matriz). Os outros dois sinalizadores também são usados apenas em interpretadores anteriores para passar corretamente por um tipo apresentado na pilha.

O \_ índice quintuple<2> é um índice da rotina de retorno de chamada quintuple (isso é, na verdade, um quádruplo) de funções. A tabela é comum para transmitir como e representar como e há um mapeamento óbvio para a posição das rotinas, como o mesmo serviço de pontos de entrada é transmitido como e representa como códigos. O mapeamento é de \_ local => para \_ transmissão, para \_ local => de \_ transmissão, \_ Inst gratuito => \_ transmissão gratuita, \_ local livre => Free \_ Inst.

O \_ tamanho da memória de tipo apresentado \_ \_<2> sempre fornece um tamanho para o tipo apresentado/local, incluindo os tipos de representações desconhecidos.

O tamanho do buffer de tipo transmitido \_ \_ \_<2> é zero, quando o tamanho é variável ou o tamanho fixo real. Essa é uma otimização que permite ignorar alguns retornos de chamada ao dimensionar o buffer.

O deslocamento do tipo transmitido \_ \_<2> é o deslocamento de tipo relativo usual para a cadeia de caracteres de formato do tipo transmitido.

 

 