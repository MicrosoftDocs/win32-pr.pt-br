---
title: O user_marshal atributo
description: O atributo \ \_ user marshal\ é um atributo do tipo ACF semelhante na sintaxe a \ represent \_ as\ .
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- RPC de Chamada de Procedimento Remoto , atributos, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b769e6a7e176d5aeba68afd322cdd6f24d76c6b5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883743"
---
# <a name="the-user_marshal-attribute"></a>O atributo \_ de marshal do usuário

O \[ [atributo de \_ marshal](/windows/desktop/Midl/user-marshal) \] do usuário é um atributo do tipo ACF semelhante à sintaxe a \[ [ser \_ representada como](/windows/desktop/Midl/represent-as) \] . Assim como no atributo IDL, o marshal de transmissão oferece uma maneira mais eficiente de efetuar marshal de dados em uma \[ [ \_ ](/windows/desktop/Midl/wire-marshal) \] rede. Como um atributo ACF, **\[ o marshal \_ de \]** usuário permite que você faça marshal de tipos de dados personalizados desconhecidos para MIDL. Cada tipo específico do aplicativo tem um tipo transmitível correspondente que define a representação de transmissão.

O tipo específico do aplicativo pode ser simples, composto ou tipo de ponteiro. A principal restrição é que a instância de tipo deve ter um tamanho de memória fixo e bem definido. Se o tamanho da instância de tipo precisar ser alterado, use um campo de ponteiro em vez de uma matriz compatível. Como alternativa, você pode definir um ponteiro para o tipo aceitável.

Assim como no **\[ atributo wire \_ marshal, \]** você fornece rotinas para as passagens de empacotamento, marshaling, desmarque e liberação. A tabela a seguir descreve os quatro nomes de rotina fornecidos pelo usuário. O &lt; tipo é o tipo &gt; userm *especificado* na definição de tipo **\[ de \_ \] marshal** do usuário.



| Rotina                                                            | Description                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [&lt;tipo &gt; \_ UserSize](the-type-usersize-function.md)           | Tamanhos do buffer de dados RPC antes do marshaling no lado do cliente ou do servidor. |
| [&lt;tipo &gt; \_ UserMarshal](the-type-usermarshal-function.md)     | Marshals dos dados no lado do cliente ou do servidor.                           |
| [&lt;type &gt; \_ UserUnmarshal](the-type-userunmarshal-function.md) | Desmarcala os dados no lado do cliente ou do servidor.                         |
| [&lt;tipo &gt; \_ UserFree](the-type-userfree-function.md)           | Libera os dados no lado do servidor.                                        |



 

Essas rotinas fornecidas pelo usuário são fornecidas pelo cliente ou pelo aplicativo de servidor, com base nos atributos direcionais.

Se o parâmetro estiver \[ [em](/windows/desktop/Midl/in) \] somente, o cliente transmitirá para o servidor. O cliente precisa do **&lt; tipo &gt; \_ UserSize** e **&lt; digitar funções &gt; \_ UserMarshal.** O servidor precisa do **&lt; tipo &gt; \_ UserUnmarshal** e **&lt; do tipo funções &gt; \_ UserFree.**

Para um \[ [parâmetro](/windows/desktop/Midl/out-idl) \] out-only, o servidor transmite para o cliente. O servidor precisa do **&lt; tipo &gt; \_ UserSize** e digitar **&lt; funções &gt; \_ UserMarshal,** enquanto o cliente precisa do **&lt; tipo função &gt; \_ UserMarshal.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O atributo wire \_ marshal](the-wire-marshal-attribute.md)
</dt> <dt>

[Regras de marshaling para marshal de usuário e marshaling \_ de transmissão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[marshal \_ de usuário](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 
