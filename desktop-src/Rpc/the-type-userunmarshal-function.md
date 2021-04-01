---
title: A função type_UserUnmarshal
description: A \_ função Type UserUnmarshal é uma função auxiliar para os atributos \ Wire \_ Marshal e \ user \_ Marshal \.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008323"
---
# <a name="the-type_userunmarshal-function"></a>A \_ função Type UserUnmarshal

A função **<type> \_ UserUnmarshal** é uma função auxiliar para os atributos de marshaling de \[ [conexão \_](/windows/desktop/Midl/wire-marshal) \] e de \[ [ \_ marshaling do usuário](/windows/desktop/Midl/user-marshal) \] . Os stubs chamam essa função para desempacotar dados no lado do cliente ou do servidor. A função é definida como:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

O <type> no nome da função significa o tipo de usuário especificado na definição de tipo de marshaling de **\[ \_ \] conexão** ou de **\[ usuário \_ \]** . Esse tipo pode ser não transmitido ou até mesmo — quando usado com o atributo **\[ \_ Marshal \] do usuário** — desconhecido para o compilador MIDL. O nome do tipo de fio (o nome do tipo Transmissible) não é usado no protótipo de função. Observe, no entanto, que o tipo de conexão define o layout de fio para os dados, conforme especificado pelo uso DCE.

O parâmetro *pFlags* é um ponteiro para um campo de sinalizador **longo não assinado** . A palavra superior do sinalizador contém sinalizadores de representação de dados de NDR, conforme definido pelo uso DCE para pontos flutuantes, ordem de bytes e representações de caracteres. A palavra inferior contém um sinalizador de contexto de marshaling, conforme definido pelo canal COM. O layout exato dos sinalizadores dentro do campo é descrito na [função do tipo \_ usersize](the-type-usersize-function.md).

O parâmetro *pBuffer* é o ponteiro de buffer atual. Esse ponteiro pode ou não estar alinhado na entrada. Sua função **<type> \_ UserUnmarshal** deve alinhar o ponteiro do buffer adequadamente, desempacotar os dados e retornar a nova posição do buffer, que é o endereço do primeiro byte após o objeto sem marshaling.

O parâmetro *pMyObj* é um ponteiro para um objeto de tipo definido pelo usuário.

Em um ambiente heterogêneo, o mecanismo de NDR executa qualquer conversão de dados necessária antes de chamar a função **<type> \_ UserUnmarshal** . Observe que o mecanismo de NDR realiza essa conversão de dados de acordo com a definição de tipo de fio fornecida para esse tipo de dados de usuário. O sinalizador indica a representação de dados do remetente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshaling de transmissão](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Marshal do usuário \_](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 