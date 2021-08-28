---
title: Regras de marshaling para user_marshal e wire_marshal
description: A especificação osF-DCE para realizar marshaling de tipos de ponteiro inserido exige que você observe as seguintes restrições ao implementar o tipo \_ UserSize, digite UserMarshal e digite \_ funções \_ UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97f073a5745570aae5c52d4a61d2454b960d77a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883825"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Regras de marshaling para marshal \_ de usuário e marshaling de \_ transmissão

A especificação osF-DCE para realizar marshaling de tipos de ponteiro inserido exige que você observe as seguintes restrições ao implementar o tipo &lt; &gt; \_ UserSize, digite UserMarshal e digite &lt; &gt; \_ &lt; funções &gt; \_ UserUnMarshal. (As regras e exemplos aqui são para marshaling. No entanto, suas rotinas de sizing e unmarshaling devem seguir as mesmas restrições:

-   Se o tipo de transmissão for um tipo simples sem ponteiros, sua rotina de marshaling para o tipo userm correspondente deverá simplesmente efetuar marshaling dos dados de acordo com o layout do tipo de transmissão. Por exemplo:

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Observe que o tipo de fio, **long,** é um tipo simples. Sua função \_ HANDLE HANDLE \_ UserMarshal faz marshal de um **longo sempre** que um objeto HANDLE HANDLE é passado para \_ ele.

-   Se o tipo de transmissão for um ponteiro para outro tipo, sua rotina de marshaling para o tipo userm correspondente deverá efetuar marshaling dos dados de acordo com o layout do tipo para o qual o tipo de transmissão aponta. O mecanismo NDR cuida do ponteiro. Por exemplo:

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Observe que o tipo de transmissão, **WIRE \_ TYPE,** é um tipo de ponteiro. Sua função HANDLE DATA UserMarshal faz marshal dos dados relacionados ao handle, usando o layout HDATA, em vez \_ \_ do layout \* HDATA.

-   Um tipo de transmissão deve ser um tipo de dados simples ou um tipo de ponteiro. Se o tipo permitido deve ser algo diferente (uma estrutura com ponteiros, por exemplo), use um ponteiro para o tipo desejado como o tipo de transmissão.

O efeito dessas restrições é que os tipos definidos com o marshal de transmissão ou atributos de marshal de usuário podem ser inseridos livremente em \[ [**\_**](/windows/desktop/Midl/wire-marshal) \] outros \[ [**\_**](/windows/desktop/Midl/user-marshal) \] tipos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**wire \_ marshal**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**marshal \_ de usuário**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[O tipo \_ Função UserSize](the-type-usersize-function.md)
</dt> <dt>

[O tipo \_ Função UserMarshal](the-type-usermarshal-function.md)
</dt> <dt>

[O tipo \_ UserUnMarshalFunction](the-type-userunmarshal-function.md)
</dt> <dt>

[O tipo \_ UserFreeFunction](the-type-userfree-function.md)
</dt> </dl>

 

 
