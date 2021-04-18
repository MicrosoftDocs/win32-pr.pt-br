---
description: Ao selecionar uma NIC (placa de interface de rede) registrada listada em um computador local, você pode usar um BLOB de filtro para desconsiderar as NICs nas quais você não está interessado.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Especificando um BLOB de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796394"
---
# <a name="specifying-a-filter-blob"></a><span data-ttu-id="159e7-103">Especificando um BLOB de filtro</span><span class="sxs-lookup"><span data-stu-id="159e7-103">Specifying a Filter BLOB</span></span>

<span data-ttu-id="159e7-104">Ao selecionar uma NIC (placa de interface de rede) registrada listada em um computador local, você pode usar um [*blob de filtro*](f.md) para desconsiderar as NICs nas quais você não está interessado.</span><span class="sxs-lookup"><span data-stu-id="159e7-104">When you select a registered network interface card (NIC) listed on a local computer, you can use a [*filter BLOB*](f.md) to disregard the NICs you are not interested in.</span></span> <span data-ttu-id="159e7-105">Por exemplo, você pode restringir a pesquisa de um tipo específico de cartão (como ETHERNET) ou um endereço MAC específico.</span><span class="sxs-lookup"><span data-stu-id="159e7-105">For example, you could restrict the search for a specific type of card (such as ETHERNET) or a specific MAC address.</span></span>

<span data-ttu-id="159e7-106">Durante a pesquisa de uma NIC, cada entrada no BLOB de filtro deve corresponder a uma entrada equivalente no BLOB NPP que representa a NIC.</span><span class="sxs-lookup"><span data-stu-id="159e7-106">During the search for a NIC, every entry in the filter BLOB must match an equivalent entry in the NPP BLOB that represents the NIC.</span></span> <span data-ttu-id="159e7-107">Os BLOBs de filtro também podem ser [*BLOBs especiais*](s.md).</span><span class="sxs-lookup"><span data-stu-id="159e7-107">Filter BLOBs can also be [*special BLOBs*](s.md).</span></span>

<span data-ttu-id="159e7-108">Quando a função [**GetNPPBlobFromUI**](getnppblobfromui.md) é chamada, o blob de filtro restringe as NICs exibidas na caixa de diálogo **selecionar uma rede** .</span><span class="sxs-lookup"><span data-stu-id="159e7-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the filter BLOB restricts the NICs displayed in the **Select a network** dialog box.</span></span> <span data-ttu-id="159e7-109">Quando a função [**GetNPPBlobTable**](getnppblobtable.md) é chamada, o blob de filtro restringe as NICs retornadas na tabela de BLOB.</span><span class="sxs-lookup"><span data-stu-id="159e7-109">When the [**GetNPPBlobTable**](getnppblobtable.md) function is called, the filter BLOB restricts the NICs returned in the BLOB table.</span></span>

<span data-ttu-id="159e7-110">Para usar o filtro, você deve criar um BLOB de filtro, definir os valores das propriedades que você deseja filtrar (incluindo quaisquer entradas de BLOB especiais) e, em seguida, especificar o filtro de BLOB e uma chamada para a função [**GetNPPBlobTable**](getnppblobtable.md) ou [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="159e7-110">To use the filter, you must create a filter BLOB, set the values of the properties you want to filter on (including any special BLOB entries), and then specify the BLOB filter and a call to the [**GetNPPBlobTable**](getnppblobtable.md) or [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>



| <span data-ttu-id="159e7-111">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="159e7-111">For information on</span></span>                                 | <span data-ttu-id="159e7-112">Consulte</span><span class="sxs-lookup"><span data-stu-id="159e7-112">See</span></span>                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="159e7-113">Como selecionar uma NIC registrada em um computador local</span><span class="sxs-lookup"><span data-stu-id="159e7-113">How to select a NIC registered on a local computer</span></span> | [<span data-ttu-id="159e7-114">Selecionando uma NIC registrada</span><span class="sxs-lookup"><span data-stu-id="159e7-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="159e7-115">Recuperando uma tabela de BLOB NPP</span><span class="sxs-lookup"><span data-stu-id="159e7-115">Retrieving an NPP BLOB table</span></span>                       | [<span data-ttu-id="159e7-116">Selecionando uma NIC de uma tabela de BLOB NPP retornada</span><span class="sxs-lookup"><span data-stu-id="159e7-116">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



