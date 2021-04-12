---
title: O atributo wire_marshal
description: O atributo \ Wire \_ Marshal \ é um atributo de tipo IDL semelhante à sintaxe para \ transmitir \_ como \, mas fornecendo uma maneira mais eficiente de realizar marshaling de dados em uma rede.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- RPC, atributos wire_marshal de chamada de procedimento remoto
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366409"
---
# <a name="the-wire_marshal-attribute"></a>O \_ atributo de marshaling de fio

O \[ atributo de [ \_ marshaling de fio](/windows/desktop/Midl/wire-marshal) \] é um atributo de tipo IDL semelhante à sintaxe para \[ [transmitir \_ como](/windows/desktop/Midl/transmit-as) \] , mas fornecendo uma maneira mais eficiente de realizar marshaling de dados em uma rede.

Use o atributo de \[ **\_ marshaling de fio** \] para especificar um tipo de dados que será transmitido no lugar do tipo de dados específico do aplicativo. Cada tipo específico de aplicativo tem um tipo de transmissão correspondente que define a representação de transmissão (a representação usada na rede). O tipo específico do aplicativo não precisa ser transmititable, mas deve ser um tipo que o MIDL reconhece. Para empacotar um tipo desconhecido para MIDL, use o \[ [ \_ marshaling do usuário](/windows/desktop/Midl/user-marshal)do atributo ACF \] .

O tipo específico do aplicativo pode ser um tipo simples, composto ou de ponteiro. A principal restrição é que a instância do tipo deve ter um tamanho de memória fixo e bem definido. Se o tamanho da instância do tipo precisar ser alterado, use um campo de ponteiro em vez de uma matriz compatível. Como alternativa, você pode definir um ponteiro para o tipo de alteração.

Você deve fornecer as rotinas para o dimensionamento, o marshaling e o desempacotamento dos dados, bem como a liberação da memória associada. A tabela a seguir descreve os quatro nomes de rotina fornecidos pelo usuário. O <type> é o tipo de usuário especificado na definição do \[ tipo de **\_ marshaling de fio** \] .



| Rotina                                                            | Descrição                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_Usersize](the-type-usersize-function.md)           | Dimensiona o buffer de dados RPC antes do marshaling no lado do cliente ou do servidor. |
| [<type>\_Usermarshal](the-type-usermarshal-function.md)     | Realiza marshaling dos dados no lado do cliente ou do servidor.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Desempacota os dados no lado do cliente ou do servidor.                         |
| [<type>\_Isfree](the-type-userfree-function.md)           | Libera os dados no lado do servidor.                                        |



 

Essas rotinas fornecidas pelo programador são fornecidas pelo cliente ou pelo aplicativo de servidor com base nos atributos direcionais.

Se o parâmetro for \[ [](/windows/desktop/Midl/in) \] somente, o cliente transmitirá para o servidor. O cliente precisa das funções **<type> \_ usersize** e **<type> \_ usermarshal** . O servidor precisa das funções **<type> \_ UserUnmarshal** e **<type> \_ userfree** .

Para um \[ [](/windows/desktop/Midl/out-idl) \] parâmetro somente out, o servidor transmite para o cliente. O servidor precisa das funções **<type> \_ usersize** e **<type> \_ usermarshal** , enquanto o cliente precisa da função **<type> \_ usermarshal** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O \_ atributo de marshaling do usuário](the-user-marshal-attribute.md)
</dt> <dt>

[Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshaling de transmissão](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Marshal do usuário \_](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 