---
title: A função type_UserUnmarshal de dados
description: O tipo função UserUnmarshal é uma função auxiliar para os \_ atributos \ wire \_ marshal\ e \ user \_ marshal\.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05281e7ae9d25ee25b4e3198dd834c78d81c3f53
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884151"
---
# <a name="the-type_userunmarshal-function"></a>O tipo \_ Função UserUnmarshal

O **&lt; tipo função &gt; \_ UserUnmarshal** é uma função auxiliar para os atributos \[ [de marshal de \_ transmissão](/windows/desktop/Midl/wire-marshal) \] e marshal \[ [ \_ de](/windows/desktop/Midl/user-marshal) \] usuário. Os stubs chamam essa função para desmarcar dados no lado do cliente ou do servidor. A função é definida como:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

O tipo no nome da função significa o tipo userm especificado na definição de tipo de marshal de &lt; &gt; **\[ \_ \] transmissão** ou **\[ \_ marshal \]** de usuário. Esse tipo pode ser nãotransmitível ou até mesmo , quando usado com o atributo **\[ \_ de marshal \]** do usuário, desconhecido para o compilador MIDL. O nome do tipo de transmissão (o nome do tipo permitido) não é usado no protótipo de função. Observe, no entanto, que o tipo de transmissão define o layout de transmissão para os dados conforme especificado pelo OSF DCE.

O *parâmetro pFlags* é um ponteiro para um **campo de sinalizador longo sem** sinal. A palavra superior do sinalizador contém sinalizadores de representação de dados NDR conforme definido pelo OSF DCE para representações de ponto flutuante, ordem de byte e caractere. A palavra inferior contém um sinalizador de contexto de marshaling conforme definido pelo canal COM. O layout exato dos sinalizadores dentro do campo é descrito em [O tipo \_ Função UserSize](the-type-usersize-function.md).

O *parâmetro pBuffer* é o ponteiro de buffer atual. Esse ponteiro pode ou não estar alinhado na entrada. Sua função **&lt; &gt; \_ UserUnmarshal** do tipo deve alinhar o ponteiro do buffer adequadamente, desmarcar os dados e retornar a nova posição do buffer, que é o endereço do primeiro byte após o objeto não desmarque.

O *parâmetro pMyObj* é um ponteiro para um objeto de tipo definido pelo usuário.

Em um ambiente heterogêneo, o mecanismo NDR executa qualquer conversão de dados necessária antes de chamar o **&lt; tipo função &gt; \_ UserUnmarshal.** Observe que o mecanismo NDR executa essa conversão de dados de acordo com a definição de tipo de transmissão fornecida para esse tipo de dados de usuário. O sinalizador indica a representação de dados do remetente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Regras de marshaling para marshal \_ de usuário e marshaling de \_ transmissão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[marshal \_ de usuário](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
