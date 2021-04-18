---
title: O atributo transmit_as
description: O atributo \ transmitir \_ como \ oferece uma maneira de controlar o marshaling de dados sem se preocupar com o marshaling de dados em um nível baixo \ 8212; ou seja, sem se preocupar com tamanhos de dados ou permutação de bytes em um ambiente heterogêneo.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- RPC, atributos transmit_as de chamada de procedimento remoto
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366410"
---
# <a name="the-transmit_as-attribute"></a>O \_ atributo transmitir como

O **\[** atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** oferece uma maneira de controlar o marshaling de dados sem se preocupar com o marshaling de dados em um nível baixo, ou seja, sem se preocupar com tamanhos de dados ou permutação de bytes em um ambiente heterogêneo. Ao permitir que você reduza a quantidade de dados transmitidos pela rede, o atributo **\[ transmitir \_ como \]** pode tornar seu aplicativo mais eficiente.

Use o atributo **\[ transmitir \_ como \]** para especificar um tipo de dados que os stubs RPC transmitirá pela rede em vez de usar o tipo de dados fornecido pelo aplicativo. Você fornece rotinas que convertem o tipo de dados de e para o tipo que é usado para transmissão. Você também deve fornecer rotinas para liberar a memória usada para o tipo de dados e o tipo transmitido. Por exemplo, o seguinte define **o \_ tipo de transmissão** como o tipo de dados transmitido para todos os dados de aplicativo especificados como sendo do tipo **\_ espec**:

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

A tabela a seguir descreve os quatro nomes de rotina fornecidos pelo programador. **Type** é o tipo de dados conhecido pelo aplicativo, e **o \_ tipo de transmissão** é o tipo de dados usado para transmissão.



| Rotina                                                 | Descrição                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo \_ para \_ transmissão**](the-type-to-xmit-function.md)     | Aloca um objeto do tipo transmitido e converte do tipo de aplicativo para o tipo transmitido pela rede (chamador e objeto chamado). |
| [**Tipo \_ de \_ transmissão**](the-type-from-xmit-function.md) | Converte do tipo transmitido para o tipo de aplicativo (chamador e objeto chamado).                                                                  |
| [**Digite \_ \_ InStr gratuito**](the-type-free-inst-function.md) | Libera recursos usados pelo tipo de aplicativo (objeto chamado somente).                                                                              |
| [**\_Transmissão gratuita de tipo \_**](the-type-free-xmit-function.md) | Libera o armazenamento retornado pelo tipo para a rotina de *****\_*** \_ transmissão** (chamador e objeto chamado).                                                      |



 

Além dessas quatro funções fornecidas pelo programador, o tipo transmitido não é manipulado pelo aplicativo. O tipo transmitido é definido somente para mover dados pela rede. Depois que os dados são convertidos no tipo usado pelo aplicativo, a memória usada pelo tipo transmitido é liberada.

Essas rotinas fornecidas pelo programador são fornecidas pelo cliente ou pelo aplicativo de servidor com base nos atributos direcionais. Se o parâmetro for **\[** [](/windows/desktop/Midl/in) **\]** somente, o cliente transmitirá para o servidor. O cliente precisa do **tipo \_ para \_ transmissão** e tipo de funções de **\_ \_ transmissão gratuita** . O servidor precisa do **tipo \_ de \_ transmissão** e **digitar \_ funções \_ Inst gratuitas** . Para um **\[** [](/windows/desktop/Midl/out-idl) **\]** parâmetro somente out, o servidor transmite para o cliente. O aplicativo de servidor deve implementar o **tipo \_ para \_ transmissão** e digitar funções de **\_ \_ transmissão gratuitas** , enquanto o programa cliente deve fornecer o **tipo da função \_ de \_ transmissão** . Para os objetos **de \_ tipo de transmissão** temporários, o stub chamará a *****\_*** \_ transmissão gratuita de tipo** para liberar qualquer memória alocada por uma chamada de **tipo \_ para \_ transmissão**.

Certas diretrizes se aplicam à instância do tipo de aplicativo. Se o tipo de aplicativo for um ponteiro ou contiver um ponteiro, o **tipo** \_ **da rotina de \_ transmissão** deverá alocar memória para os dados aos quais os ponteiros apontam (o próprio objeto de tipo de aplicativo é manipulado pelo stub da maneira usual).

Para parâmetros **de saída e \[ saída, ou um de seus componentes, de um tipo que contém o atributo transmitir como, o tipo de rotina Inst gratuita é chamado automaticamente para os objetos de dados que têm o atributo. \]** **\[ \_ \]** **\[ \] \]**  \_ **\_** Para parâmetros **in** , a  \_ rotina **\_ Inst gratuita** do tipo será chamada somente se o atributo **\[ transmitir \_ como \]** tiver sido aplicado ao parâmetro. Se o atributo tiver sido aplicado aos componentes do parâmetro, a  \_ rotina **\_ Inst gratuita** de tipo não será chamada. Não há chamadas de liberação para os dados inseridos e uma chamada na maioria-uma (relacionada ao atributo de nível superior) para um parâmetro **in** only.

Em vigor com o MIDL 2,0, tanto o cliente quanto o servidor devem fornecer todas as quatro funções. Por exemplo, uma lista vinculada pode ser transmitida como uma matriz dimensionada. O **tipo \_ para \_** a rotina de transmissão percorre a lista vinculada e copia os dados ordenados em uma matriz. Os elementos da matriz são ordenados para que os vários ponteiros associados à estrutura da lista não precisem ser transmitidos. O **tipo \_ da rotina de \_ transmissão** lê a matriz e coloca seus elementos em uma estrutura de lista vinculada.

A lista de links duplos ( \_ lista de vínculos duplas \_ ) inclui dados e ponteiros para os elementos de lista anteriores e seguintes:

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

Em vez de enviar a estrutura complexa, o **\[** atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** pode ser usado para enviá-la pela rede como uma matriz. A sequência de itens na matriz retém a ordem dos elementos na lista com um custo menor:

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

O atributo **\[ transmitir \_ como \]** aparece no arquivo IDL:

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

No exemplo a seguir, **ModifyListProc** define o parâmetro do tipo link duplo tipo \_ \_ como um parâmetro **\[ in, \] out** :

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

As quatro funções definidas pelo programador usam o nome do tipo nos nomes de função e usam os tipos apresentados e transmitidos como tipos de parâmetro, conforme necessário:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 