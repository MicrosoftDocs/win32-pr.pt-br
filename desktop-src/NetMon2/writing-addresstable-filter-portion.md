---
description: O filtro de endereço notifica o driver Monitor de Rede para aceitar quadros que têm uma variedade de tipos de endereço MAC especificados (Ethernet, Anel de Token e FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Escrevendo parte do filtro ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a18f8004ea4c38607d6c1c7b8fa741315b41fefe5b4d31b103167d415eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128786"
---
# <a name="writing-addresstable-filter-portion"></a>Escrevendo parte do filtro ADDRESSTABLE

O filtro de endereço notifica o driver Monitor de Rede para aceitar quadros que têm uma variedade de tipos de endereço MAC especificados (Ethernet, Anel de Token e FDDI). Você pode especificar um máximo de oito pares de endereços. Um par de endereços pode especificar uma origem, um destino, ambos ou nenhum deles.

A parte de endereço do filtro consiste em duas estruturas: [**ADDRESSTABLE**](addresstable.md) e [**ADDRESSPAIR.**](addresspair.md)

Se você especificar NENHUM endereço, TODOS os quadros passarão pelo filtro de endereço. No entanto, se você especificar endereços, somente os quadros que passam pelo filtro de endereço especificado passarão.

A criação do filtro de endereço envolve a alocação de uma estrutura [**ADDRESSTABLE**](addresstable.md) e o preenchimento de membros da [**estrutura ADDRESSPAIR.**](addresspair.md)

**Para criar a parte de endereço de um filtro de captura**

1.  Use o **sinalizador CAPTUREFILTER \_ FLAGS \_ LOCAL \_ ONLY** da estrutura [**CAPTUREFILTER**](capturefilter.md) para restringir a captura ao tráfego de e para o computador local.

    Definir esse sinalizador não definirá a NIC para o modo promiscuo; o arquivo de captura capturará apenas o tráfego local.

2.  Use o seguinte código de exemplo para definir a [**estrutura ADDRESSTABLE:**](addresstable.md)

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  Use as informações listadas na tabela a seguir para selecionar um [**tipo de sinalizador ADDRESSPAIR.**](addresspair.md) 

    | Sinalizador                             | Significado                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | SINALIZADORES \_ DE \_ ENDEREÇOS \_ CORRESPONDEREM A DST       | Corresponde a um endereço de destino.                                                        |
    | SINALIZADORES \_ DE ENDEREÇO \_ \_ CORRESPONDEREM AO SRC       | Corresponde a um endereço de origem                                                              |
    | EXCLUSÃO \_ DE SINALIZADORES \_ DE ENDEREÇO          | Exclui o quadro se esse endereço for encontrado (uma origem ou destino definidos). |
    | COMPLEMENTO \_ DE \_ GRUPO DST \_ \_ SINALIZADORES DE ENDEREÇO | Corresponde ao bit do grupo (do endereço de destino) somente para mensagens de tipo de difusão.      |
    | OS \_ SINALIZADORES DE \_ ENDEREÇO \_ CORRESPONDEREM A AMBOS      | Corresponde aos endereços de origem e de destino.                                    |

    

     

4.  Preencha um endereço de destino, que é avaliado em relação ao [**sinalizador ADDRESSPAIR**](addresspair.md) selecionado.
5.  Preencha um endereço de origem, que é avaliado em relação [**ao sinalizador ADDRESSPAIR**](addresspair.md) selecionado.
6.  Preencha a estrutura [**ADDRESSTABLE**](addresstable.md) com uma matriz de estruturas [**ADDRESSPAIR,**](addresspair.md) que inclui os pares de endereços que o driver avalia. Todos os pares de endereços são avaliados como uma instrução OR lógica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). Você pode incluir um máximo de oito pares de endereços em um filtro de captura.

 

 



