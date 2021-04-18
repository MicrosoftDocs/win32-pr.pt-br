---
description: O filtro de endereço notifica o driver de Monitor de Rede para aceitar quadros que tenham uma de uma variedade de tipos de endereço MAC especificados (Ethernet, token ring e FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Gravando parte de filtro de ADDRESStable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755986"
---
# <a name="writing-addresstable-filter-portion"></a>Gravando parte de filtro de ADDRESStable

O filtro de endereço notifica o driver de Monitor de Rede para aceitar quadros que tenham uma de uma variedade de tipos de endereço MAC especificados (Ethernet, token ring e FDDI). Você pode especificar um máximo de oito pares de endereços. Um par de endereços pode especificar uma origem, um destino, ambos ou nenhum.

A parte de endereço do filtro consiste em duas estruturas: [**AddressTable**](addresstable.md) e [**ADDRESSPAIR**](addresspair.md).

Se você não especificar nenhum endereço, todos os quadros passarão pelo filtro de endereço. No entanto, se você especificar qualquer endereço, somente os quadros que passarem pelo filtro de endereço determinado serão aprovados.

A criação do filtro de endereço envolve a alocação de uma estrutura de [**AddressTable**](addresstable.md) e o preenchimento de membros da estrutura [**ADDRESSPAIR**](addresspair.md) .

**Para criar a parte de endereço de um filtro de captura**

1.  Use o sinalizador **CAPTUREFILTER \_ flags \_ local \_ somente** da estrutura [**CAPTUREFILTER**](capturefilter.md) para restringir a captura para o tráfego de e para o computador local.

    A definição desse sinalizador não definirá a NIC para o modo promíscuo; o arquivo de captura capturará somente o tráfego local.

2.  Use o seguinte código de exemplo para definir a estrutura de [**AddressTable**](addresstable.md) :

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

3.  Use as informações, listadas na tabela a seguir, para selecionar um tipo de sinalizador [**ADDRESSPAIR**](addresspair.md) . 

    | Sinalizador                             | Significado                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | sinalizadores de endereço \_ \_ correspondem ao \_ DST       | Corresponde a um endereço de destino.                                                        |
    | os \_ sinalizadores de endereço \_ correspondem \_ src       | Corresponde a um endereço de origem                                                              |
    | \_exclusão de sinalizadores de endereço \_          | Exclui o quadro se esse endereço for encontrado (uma origem ou destino definido). |
    | Endereço do \_ grupo de horário de Verão dos sinalizadores de endereços \_ \_ \_ | Corresponde ao bit do grupo (do endereço de destino) somente para mensagens do tipo de difusão.      |
    | sinalizadores de endereço \_ \_ correspondem a \_ ambos      | Corresponde tanto ao destino quanto aos endereços de origem.                                    |

    

     

4.  Preencha um endereço de destino, que é avaliado em relação ao sinalizador [**ADDRESSPAIR**](addresspair.md) que você selecionar.
5.  Preencha um endereço de origem, que é avaliado em relação ao sinalizador [**ADDRESSPAIR**](addresspair.md) que você selecionar.
6.  Preencha a estrutura de [**AddressTable**](addresstable.md) com uma matriz de estruturas [**ADDRESSPAIR**](addresspair.md) , que inclui os pares de endereços que o driver avalia. Todos os pares de endereços são avaliados como uma instrução OR lógica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). Você pode incluir um máximo de oito pares de endereços em um filtro de captura.

 

 



