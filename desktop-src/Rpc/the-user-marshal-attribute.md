---
title: O atributo user_marshal
description: O atributo \ user \_ Marshal \ é um atributo de tipo ACF semelhante em sintaxe para \ representa \_ como \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- RPC, atributos user_marshal de chamada de procedimento remoto
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0501cfd3199d41a49da7f54919c86f9332ce976f33963f23c63a7938338da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923526"
---
# <a name="the-user_marshal-attribute"></a>O \_ atributo de marshaling do usuário

O \[ [atributo \_ Marshal do usuário](/windows/desktop/Midl/user-marshal) \] é um atributo de tipo ACF semelhante na sintaxe para \[ [representar \_ como](/windows/desktop/Midl/represent-as) \] . Assim como acontece com o atributo IDL, o \[ [ \_ marshaling](/windows/desktop/Midl/wire-marshal) \] é uma maneira mais eficiente de empacotar dados em uma rede. Como um atributo ACF, o **\[ \_ marshaling \] do usuário** permite que você realize marshaling de tipos de dados personalizados que são desconhecidos para MIDL. Cada tipo específico de aplicativo tem um tipo de transmissão correspondente que define a representação de transmissão.

O tipo específico do aplicativo pode ser um tipo simples, composto ou de ponteiro. A principal restrição é que a instância do tipo deve ter um tamanho de memória fixo e bem definido. Se o tamanho da instância do tipo precisar ser alterado, use um campo de ponteiro em vez de uma matriz compatível. Como alternativa, você pode definir um ponteiro para o tipo de alteração.

Assim como acontece com o atributo de **\[ \_ marshaling \] de fio** , você fornece rotinas para o dimensionamento, o marshaling, o desempacotamento e a liberação de passagens. A tabela a seguir descreve os quatro nomes de rotina fornecidos pelo usuário. O <type> é o *tipo* de usuário especificado na definição de tipo de **\[ \_ marshaling \] do usuário** .



| Rotina                                                            | Descrição                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_Usersize](the-type-usersize-function.md)           | Dimensiona o buffer de dados RPC antes do marshaling no lado do cliente ou do servidor. |
| [<type>\_Usermarshal](the-type-usermarshal-function.md)     | Realiza marshaling dos dados no lado do cliente ou do servidor.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Desempacota os dados no lado do cliente ou do servidor.                         |
| [<type>\_Isfree](the-type-userfree-function.md)           | Libera os dados no lado do servidor.                                        |



 

Essas rotinas fornecidas pelo usuário são fornecidas pelo cliente ou pelo aplicativo de servidor, com base nos atributos direcionais.

Se o parâmetro for \[ [](/windows/desktop/Midl/in) \] somente, o cliente transmitirá para o servidor. O cliente precisa das funções **<type> \_ usersize** e **<type> \_ usermarshal** . O servidor precisa das funções **<type> \_ UserUnmarshal** e **<type> \_ userfree** .

Para um \[ [](/windows/desktop/Midl/out-idl) \] parâmetro somente out, o servidor transmite para o cliente. O servidor precisa das funções **<type> \_ usersize** e **<type> \_ usermarshal** , enquanto o cliente precisa da função **<type> \_ usermarshal** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O \_ atributo de marshaling de fio](the-wire-marshal-attribute.md)
</dt> <dt>

[Regras de marshaling para marshaling de usuário e \_ marshaling de conexão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Marshal do usuário \_](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[\_marshaling de transmissão](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 