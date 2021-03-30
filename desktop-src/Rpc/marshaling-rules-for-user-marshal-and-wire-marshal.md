---
title: Regras de marshaling para user_marshal e wire_marshal
description: A especificação uso-DCE para empacotamento de tipos de ponteiros inseridos requer que você observe as seguintes restrições ao implementar o tipo \_ usersize, digite \_ usermarshal e digite \_ funções UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641489"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão

A especificação uso-DCE para empacotamento de tipos de ponteiros inseridos requer que você observe as seguintes restrições ao implementar as <type> \_ funções usersize, <type> \_ usermarshal e <type> \_ UserUnMarshal. (As regras e os exemplos fornecidos aqui são para o marshaling. No entanto, suas rotinas de dimensionamento e desempacotamento devem seguir as mesmas restrições):

-   Se o tipo de fio for um tipo simples sem ponteiros, sua rotina de marshaling para o tipo de usuário correspondente deve simplesmente empacotar os dados de acordo com o layout do tipo de cabo. Por exemplo:

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Observe que o tipo de fio, **Long**, é um tipo simples. A função do manipulador de identificadores do \_ \_ usermarshal realiza um **longo tempo** sempre que um objeto identificador de identificador \_ é passado para ele.

-   Se o tipo de fio for um ponteiro para outro tipo, sua rotina de marshaling para o tipo de usuário correspondente deverá empacotar os dados de acordo com o layout do tipo ao qual o tipo de fio aponta. O mecanismo de NDR cuida do ponteiro. Por exemplo:

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Observe que o tipo de fio **, \_ tipo de fio**, é um tipo de ponteiro. A \_ função de Usermarshal de dados de manipulador \_ realiza marshaling dos dados relacionados ao identificador, usando o layout HDATA, em vez do \* layout HDATA.

-   Um tipo de fio deve ser um tipo de dados simples ou um tipo de ponteiro. Se seu tipo Transmissible deve ser algo diferente (uma estrutura com ponteiros, por exemplo), use um ponteiro para o tipo desejado como o tipo de cabo.

O efeito dessas restrições é que os tipos definidos com os atributos \[ [**\_ empacotamento de fio**](/windows/desktop/Midl/wire-marshal) \] ou \[ [**\_ marshaling do usuário**](/windows/desktop/Midl/user-marshal) \] podem ser inseridos livremente em outros tipos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_marshaling de transmissão**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**Marshal do usuário \_**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[A \_ função de Usersize do tipo](the-type-usersize-function.md)
</dt> <dt>

[A \_ função de Usermarshal do tipo](the-type-usermarshal-function.md)
</dt> <dt>

[O tipo \_ UserUnMarshalFunction](the-type-userunmarshal-function.md)
</dt> <dt>

[O tipo \_ UserFreeFunction](the-type-userfree-function.md)
</dt> </dl>

 

 