---
title: A função type_UserMarshal
description: A \_ função de Usermarshal do tipo é uma função auxiliar para os \_ atributos \ Wire Marshal e \ user \_ Marshal \.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366674"
---
# <a name="the-type_usermarshal-function"></a>A \_ função de Usermarshal do tipo

A função **<type> \_ usermarshal** é uma função auxiliar para os \[ [atributos \_ marshaling de conexão](/windows/desktop/Midl/wire-marshal) \] e \[ [ \_ Marshal do usuário](/windows/desktop/Midl/user-marshal) \] . Os stubs chamam essa função para realizar marshaling de dados no lado do cliente ou do servidor. A função é definida como:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

O <type> no nome da função significa o tipo de usuário especificado na definição de tipo de marshaling de **\[ \_ \] conexão** ou de **\[ usuário \_ \]** . Esse tipo pode ser não transmitido ou até mesmo — quando usado com o atributo **\[ \_ Marshal \] do usuário** — um tipo desconhecido para o compilador MIDL. O nome do tipo de fio (o nome do tipo Transmissible) não é usado no protótipo de função. Observe, no entanto, que o tipo de conexão define o layout de fio para os dados, conforme especificado pelo uso DCE.

O parâmetro *pFlags* é um ponteiro para um campo de sinalizador longo não assinado. A palavra superior do sinalizador contém sinalizadores de representação de dados de NDR, conforme definido pelo uso DCE para pontos flutuantes, ordem de bytes e representações de caracteres. A palavra inferior contém um sinalizador de contexto de marshaling, conforme definido pelo canal COM. O layout exato dos sinalizadores dentro do campo é descrito na [função do tipo \_ usersize](the-type-usersize-function.md).

O parâmetro *pBuffer* é o ponteiro de buffer atual. Esse ponteiro pode ou não estar alinhado na entrada. Sua função **<type> \_ usermarshal** deve alinhar o ponteiro do buffer adequadamente, empacotar os dados e retornar a nova posição do buffer, que é o endereço do primeiro byte após o objeto marshaled. Tenha em mente que a especificação de tipo de conexão determina o layout real dos dados no buffer.

O parâmetro *pMyObj* é um ponteiro para um objeto de tipo de usuário.

O valor de retorno é a nova posição do buffer, que é o endereço do primeiro byte após o objeto sem marshaling.

O estouro de buffer pode ocorrer quando você calcula incorretamente o tamanho dos dados e tenta realizar marshaling de mais dados do que o esperado. Você deve ter cuidado para evitar essa situação. Você pode verificar em relação a ele usando o ponteiro retornado pelo **<type> \_ usermarshal** . Caso contrário, você correrá o risco de ter o mecanismo de NDR disparar uma exceção de estouro de buffer posteriormente.

As exceções devem ser capturadas e manipuladas localmente, as exceções não devem ter permissão para propigatedr a pilha de chamadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshaling de transmissão](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Marshal do usuário \_](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 