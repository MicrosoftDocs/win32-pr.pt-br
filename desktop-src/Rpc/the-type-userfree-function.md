---
title: A função type_UserFree
description: O tipo \_ função de usuário livre é uma função auxiliar para os atributos \ Wire \_ Marshal \ e \ user \_ Marshal \.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641135"
---
# <a name="the-type_userfree-function"></a>O tipo \_ função Userfree

A função **<type> \_ userfree** é uma função auxiliar para os \[ atributos de [ \_ marshaling de conexão](/windows/desktop/Midl/wire-marshal) \] e de \[ [ \_ marshaling do usuário](/windows/desktop/Midl/user-marshal) \] . Os stubs chamam essa função para liberar os dados no lado do servidor. A função é definida como:

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

O <type> no nome da função significa o tipo de usuário especificado na definição de tipo de marshaling de **\[ \_ \] conexão** ou de **\[ usuário \_ \]** .

O parâmetro *pFlags* é um ponteiro para um campo de sinalizador **longo não assinado** . A palavra superior do sinalizador contém sinalizadores de representação de dados de NDR, conforme definido pelo uso DCE para pontos flutuantes, ordem de bytes e representações de caracteres. A palavra inferior contém um sinalizador de contexto de marshaling, conforme definido pelo canal COM. O layout exato dos sinalizadores dentro do campo é descrito na [função do tipo \_ usersize](the-type-usersize-function.md).

O parâmetro *pMyObj* é um ponteiro para um objeto de tipo de usuário. O mecanismo de NDR libera o objeto de nível superior. Você é responsável por liberar todos os objetos aos quais o objeto de nível superior pode apontar.

As exceções devem ser capturadas e manipuladas localmente, as exceções não devem ter permissão para propigatedr a pilha de chamadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshaling de transmissão](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Marshal do usuário \_](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 