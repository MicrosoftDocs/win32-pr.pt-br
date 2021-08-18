---
title: palavra-chave Union (RPC)
description: As uniões exigem palavras-chave MIDL especiais para dar suporte ao uso com RPC (chamada de procedimento remoto).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fde18cca09f4db81af8eada2ae102a1bea373ed7859b3a7fc2bb9637f28d584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011004"
---
# <a name="union-keyword-rpc"></a>palavra-chave Union (RPC)

Alguns recursos da linguagem C, como uniões, exigem palavras-chave MIDL especiais para dar suporte ao uso em chamadas de procedimento remoto. Uma União na linguagem C é uma variável que contém objetos de tipos e tamanhos diferentes. O desenvolvedor geralmente cria uma variável para controlar os tipos armazenados na União. Para operar corretamente em um ambiente distribuído, a variável que indica o tipo de Union, ou *discriminante*, também deve estar disponível para o computador remoto. MIDL fornece o \[ [**\_ tipo de opção**](/windows/desktop/Midl/switch-type) \] e o \[ [**interruptor \_ são**](/windows/desktop/Midl/switch-is) \] palavras-chave para identificar o tipo e o nome de discriminante.

MIDL requer que o discriminante seja transmitido com a União de uma das duas maneiras:

-   A União e o discriminante devem ser fornecidos como parâmetros.
-   A União e o discriminante devem ser empacotados em uma estrutura.

Dois tipos fundamentais de uniões discriminadas são fornecidos por MIDL: [**\_ União não encapsulada**](/windows/desktop/Midl/nonencapsulated-unions) e [**\_ União encapsulada**](/windows/desktop/Midl/encapsulated-unions). O discriminante de uma União não encapsulada será outro parâmetro se a União for um parâmetro. Será outro campo se a União for um campo de uma estrutura. A definição de uma União encapsulada é transformada em uma definição de estrutura cujo primeiro campo é o discriminante e cujo segundo e último campos são a União. O exemplo a seguir demonstra como fornecer os parâmetros Union e discriminante como:

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

A União no exemplo anterior pode conter um único valor: **curto**, **float** ou **Char**. A definição de tipo para a União inclui o atributo de **\_ tipo de opção** MIDL que especifica o tipo de discriminante. Aqui, \[ tipo de comutador \_ (curto) \] especifica que o discriminante é do tipo **curto**. A opção deve ser um tipo inteiro.

Se Union for um membro de uma estrutura, o discriminante deverá ser um membro da mesma estrutura. Se Union for um parâmetro, o discriminante deverá ser outro parâmetro. O protótipo para a função **UnionParamProc** no exemplo anterior mostra o discriminante *sUtype* como o último parâmetro da chamada. (O discriminante pode aparecer em qualquer posição na chamada.) O tipo do parâmetro especificado na **\[ opção \_ \]** o atributo deve corresponder ao tipo especificado no atributo de **\[ \_ tipo \] de comutador** .

O exemplo a seguir demonstra o uso de uma única estrutura que empacota o discriminante com a União:

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

O compilador Microsoft RPC MIDL permite declarações Union fora de construções [**typedef**](/windows/desktop/Midl/typedef) . Esse recurso é uma extensão para o DCE IDL. Para obter mais informações, consulte [**Union**](/windows/desktop/Midl/union).

 

 