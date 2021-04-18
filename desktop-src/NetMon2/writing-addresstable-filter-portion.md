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
# <a name="writing-addresstable-filter-portion"></a><span data-ttu-id="d86ea-103">Gravando parte de filtro de ADDRESStable</span><span class="sxs-lookup"><span data-stu-id="d86ea-103">Writing ADDRESSTABLE Filter Portion</span></span>

<span data-ttu-id="d86ea-104">O filtro de endereço notifica o driver de Monitor de Rede para aceitar quadros que tenham uma de uma variedade de tipos de endereço MAC especificados (Ethernet, token ring e FDDI).</span><span class="sxs-lookup"><span data-stu-id="d86ea-104">The address filter notifies the Network Monitor driver to accept frames that have one of a variety of specified MAC address types (Ethernet, Token Ring, and FDDI).</span></span> <span data-ttu-id="d86ea-105">Você pode especificar um máximo de oito pares de endereços.</span><span class="sxs-lookup"><span data-stu-id="d86ea-105">You can specify a maximum of eight address pairs.</span></span> <span data-ttu-id="d86ea-106">Um par de endereços pode especificar uma origem, um destino, ambos ou nenhum.</span><span class="sxs-lookup"><span data-stu-id="d86ea-106">An address pair can specify a source, a destination, both, or neither.</span></span>

<span data-ttu-id="d86ea-107">A parte de endereço do filtro consiste em duas estruturas: [**AddressTable**](addresstable.md) e [**ADDRESSPAIR**](addresspair.md).</span><span class="sxs-lookup"><span data-stu-id="d86ea-107">The address portion of the filter consists of two structures: [**ADDRESSTABLE**](addresstable.md) and [**ADDRESSPAIR**](addresspair.md).</span></span>

<span data-ttu-id="d86ea-108">Se você não especificar nenhum endereço, todos os quadros passarão pelo filtro de endereço.</span><span class="sxs-lookup"><span data-stu-id="d86ea-108">If you specify NO addresses, then ALL frames will pass the address filter.</span></span> <span data-ttu-id="d86ea-109">No entanto, se você especificar qualquer endereço, somente os quadros que passarem pelo filtro de endereço determinado serão aprovados.</span><span class="sxs-lookup"><span data-stu-id="d86ea-109">However, if you specify any addresses, only those frames that pass the given address filter will pass.</span></span>

<span data-ttu-id="d86ea-110">A criação do filtro de endereço envolve a alocação de uma estrutura de [**AddressTable**](addresstable.md) e o preenchimento de membros da estrutura [**ADDRESSPAIR**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="d86ea-110">Building the address filter involves allocating an [**ADDRESSTABLE**](addresstable.md) structure and filling in members of the [**ADDRESSPAIR**](addresspair.md) structure.</span></span>

<span data-ttu-id="d86ea-111">**Para criar a parte de endereço de um filtro de captura**</span><span class="sxs-lookup"><span data-stu-id="d86ea-111">**To build the address portion of a capture filter**</span></span>

1.  <span data-ttu-id="d86ea-112">Use o sinalizador **CAPTUREFILTER \_ flags \_ local \_ somente** da estrutura [**CAPTUREFILTER**](capturefilter.md) para restringir a captura para o tráfego de e para o computador local.</span><span class="sxs-lookup"><span data-stu-id="d86ea-112">Use the **CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY** flag of the [**CAPTUREFILTER**](capturefilter.md) structure to restrict the capture to traffic to and from your local computer.</span></span>

    <span data-ttu-id="d86ea-113">A definição desse sinalizador não definirá a NIC para o modo promíscuo; o arquivo de captura capturará somente o tráfego local.</span><span class="sxs-lookup"><span data-stu-id="d86ea-113">Setting this flag will not set the NIC to promiscuous mode; the capture file will capture only local traffic.</span></span>

2.  <span data-ttu-id="d86ea-114">Use o seguinte código de exemplo para definir a estrutura de [**AddressTable**](addresstable.md) :</span><span class="sxs-lookup"><span data-stu-id="d86ea-114">Use the following example code to define the [**ADDRESSTABLE**](addresstable.md) structure:</span></span>

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

3.  <span data-ttu-id="d86ea-115">Use as informações, listadas na tabela a seguir, para selecionar um tipo de sinalizador [**ADDRESSPAIR**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="d86ea-115">Use the information, listed in the following table, to select an [**ADDRESSPAIR**](addresspair.md) flag type.</span></span> 

    | <span data-ttu-id="d86ea-116">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="d86ea-116">Flag</span></span>                             | <span data-ttu-id="d86ea-117">Significado</span><span class="sxs-lookup"><span data-stu-id="d86ea-117">Meaning</span></span>                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="d86ea-118">sinalizadores de endereço \_ \_ correspondem ao \_ DST</span><span class="sxs-lookup"><span data-stu-id="d86ea-118">ADDRESS\_FLAGS\_MATCH\_DST</span></span>       | <span data-ttu-id="d86ea-119">Corresponde a um endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="d86ea-119">Matches a destination address.</span></span>                                                        |
    | <span data-ttu-id="d86ea-120">os \_ sinalizadores de endereço \_ correspondem \_ src</span><span class="sxs-lookup"><span data-stu-id="d86ea-120">ADDRESS\_FLAGS\_MATCH\_SRC</span></span>       | <span data-ttu-id="d86ea-121">Corresponde a um endereço de origem</span><span class="sxs-lookup"><span data-stu-id="d86ea-121">Matches a source address</span></span>                                                              |
    | <span data-ttu-id="d86ea-122">\_exclusão de sinalizadores de endereço \_</span><span class="sxs-lookup"><span data-stu-id="d86ea-122">ADDRESS\_FLAGS\_EXCLUDE</span></span>          | <span data-ttu-id="d86ea-123">Exclui o quadro se esse endereço for encontrado (uma origem ou destino definido).</span><span class="sxs-lookup"><span data-stu-id="d86ea-123">Excludes the frame if this address is found (either a defined source or destination).</span></span> |
    | <span data-ttu-id="d86ea-124">Endereço do \_ grupo de horário de Verão dos sinalizadores de endereços \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="d86ea-124">ADDRESS\_FLAGS\_DST\_GROUP\_ADDR</span></span> | <span data-ttu-id="d86ea-125">Corresponde ao bit do grupo (do endereço de destino) somente para mensagens do tipo de difusão.</span><span class="sxs-lookup"><span data-stu-id="d86ea-125">Matches group bit (of the destination address) only for broadcast-type messages.</span></span>      |
    | <span data-ttu-id="d86ea-126">sinalizadores de endereço \_ \_ correspondem a \_ ambos</span><span class="sxs-lookup"><span data-stu-id="d86ea-126">ADDRESS\_FLAGS\_MATCH\_BOTH</span></span>      | <span data-ttu-id="d86ea-127">Corresponde tanto ao destino quanto aos endereços de origem.</span><span class="sxs-lookup"><span data-stu-id="d86ea-127">Matches both the destination and source addresses.</span></span>                                    |

    

     

4.  <span data-ttu-id="d86ea-128">Preencha um endereço de destino, que é avaliado em relação ao sinalizador [**ADDRESSPAIR**](addresspair.md) que você selecionar.</span><span class="sxs-lookup"><span data-stu-id="d86ea-128">Fill in a destination address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
5.  <span data-ttu-id="d86ea-129">Preencha um endereço de origem, que é avaliado em relação ao sinalizador [**ADDRESSPAIR**](addresspair.md) que você selecionar.</span><span class="sxs-lookup"><span data-stu-id="d86ea-129">Fill in a source address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
6.  <span data-ttu-id="d86ea-130">Preencha a estrutura de [**AddressTable**](addresstable.md) com uma matriz de estruturas [**ADDRESSPAIR**](addresspair.md) , que inclui os pares de endereços que o driver avalia.</span><span class="sxs-lookup"><span data-stu-id="d86ea-130">Populate the [**ADDRESSTABLE**](addresstable.md) structure with an array of [**ADDRESSPAIR**](addresspair.md) structures, which includes the address pairs that the driver evaluates.</span></span> <span data-ttu-id="d86ea-131">Todos os pares de endereços são avaliados como uma instrução OR lógica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2).</span><span class="sxs-lookup"><span data-stu-id="d86ea-131">All address pairs are evaluated as a logical OR statement (ADDRESSPAIR 1 \|\| ADDRESSPAIR 2).</span></span> <span data-ttu-id="d86ea-132">Você pode incluir um máximo de oito pares de endereços em um filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="d86ea-132">You can include a maximum of eight address pairs in a capture filter.</span></span>

 

 



