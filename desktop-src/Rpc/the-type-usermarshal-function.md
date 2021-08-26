---
title: A função type_UserMarshal de dados
description: O tipo função UserMarshal é uma função auxiliar para os \_ atributos \ wire \_ marshal\ e \ user \_ marshal\.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffea134b78ae8187fce3fab7876150c0a7a8cd7f892ebac602966712ec1b60e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016466"
---
# <a name="the-type_usermarshal-function"></a>O tipo \_ Função UserMarshal

A **<type> \_ função UserMarshal** é uma função auxiliar para os atributos de marshal \[ [de \_ transmissão](/windows/desktop/Midl/wire-marshal) \] e marshal \[ [ \_ de](/windows/desktop/Midl/user-marshal) \] usuário. Os stubs chamam essa função para fazer marshal de dados no lado do cliente ou do servidor. A função é definida como:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

O <type> no nome da função significa o tipo userm especificado na definição de tipo de marshal de **\[ \_ \] transmissão** ou **\[ \_ marshal \]** de usuário. Esse tipo pode ser nãotransmitível ou até mesmo , quando usado com o atributo **\[ \_ de marshal \]** do usuário, um tipo desconhecido para o compilador MIDL. O nome do tipo de transmissão (o nome do tipo permitido) não é usado no protótipo de função. Observe, no entanto, que o tipo de transmissão define o layout de transmissão para os dados conforme especificado pelo OSF DCE.

O *parâmetro pFlags* é um ponteiro para um campo de sinalizador longo sem sinal. A palavra superior do sinalizador contém sinalizadores de representação de dados NDR conforme definido pelo OSF DCE para representações de ponto flutuante, ordem de byte e caractere. A palavra inferior contém um sinalizador de contexto de marshaling conforme definido pelo canal COM. O layout exato dos sinalizadores dentro do campo é descrito em [O tipo \_ Função UserSize](the-type-usersize-function.md).

O *parâmetro pBuffer* é o ponteiro de buffer atual. Esse ponteiro pode ou não estar alinhado na entrada. Sua **<type> \_ função UserMarshal** deve alinhar o ponteiro do buffer adequadamente, efetuar marshal dos dados e retornar a nova posição do buffer, que é o endereço do primeiro byte após o objeto marshaled. Tenha em mente que a especificação de tipo de transmissão determina o layout real dos dados no buffer.

O *parâmetro pMyObj* é um ponteiro para um objeto de tipo de usuário.

O valor de retorno é a nova posição do buffer, que é o endereço do primeiro byte após o objeto não desmarque.

O estouro de buffer pode ocorrer quando você calcula incorretamente o tamanho dos dados e tenta efetuar marshal de mais dados do que o esperado. Você deve ter cuidado para evitar essa situação. Você pode verificar isso usando o ponteiro que **<type> \_ UserMarshal** retorna. Caso contrário, você corre o risco de fazer com que o mecanismo de NDR aumente uma exceção de estouro de buffer mais tarde.

As exceções devem ser capturadas e tratadas localmente, as exceções não devem ter permissão para criar a pilha de chamada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Regras de marshaling para marshal \_ de usuário e marshaling de \_ transmissão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[marshal \_ de usuário](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 