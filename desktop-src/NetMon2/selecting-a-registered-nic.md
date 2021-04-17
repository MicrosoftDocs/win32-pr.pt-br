---
description: Para selecionar uma das NICs registradas no computador local, chame a função GetNPPBlobFromUI.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Selecionando uma NIC registrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759618"
---
# <a name="selecting-a-registered-nic"></a><span data-ttu-id="b1dc5-103">Selecionando uma NIC registrada</span><span class="sxs-lookup"><span data-stu-id="b1dc5-103">Selecting a Registered NIC</span></span>

<span data-ttu-id="b1dc5-104">Para selecionar uma das NICs registradas no computador local, chame a função [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="b1dc5-104">To select one of the NICs registered on the local computer, call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span> <span data-ttu-id="b1dc5-105">Essa função usa o Monitor de Rede interface do usuário para exibir as NICs registradas e retorna o BLOB NPP que representa a NIC que você selecionar.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-105">This function uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you select.</span></span> <span data-ttu-id="b1dc5-106">Você pode exibir todas as NICs registradas no computador local ou em um conjunto menor de NICs filtradas.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-106">You can display all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="b1dc5-107">Para filtrar as NICs exibidas, forneça um [*blob de filtro*](f.md) quando a chamada for feita.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-107">To filter the displayed NICs, provide a [*filter BLOB*](f.md) when the call is made.</span></span>

> [!Note]  
> <span data-ttu-id="b1dc5-108">Quando a função [**GetNPPBlobFromUI**](getnppblobfromui.md) é chamada, o [*localizador de NPP*](n.md) se comunica com as DLLs do NPP para obter as estruturas de blob NPP que representam as NICs registradas.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the [*NPP Finder*](n.md) communicates with the NPP DLLs to obtain the NPP BLOB structures that represent the registered NICs.</span></span> <span data-ttu-id="b1dc5-109">Para obter mais informações e um procedimento sobre como usar a interface do usuário do Monitor de Rede diretamente, consulte o tópico "selecionar uma caixa de diálogo de rede" na ajuda online do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-109">For more information, and a procedure about how to use the Network Monitor UI directly, see the "Select a Network Dialog Box" topic in the Network Monitor online help.</span></span>

 

<span data-ttu-id="b1dc5-110">Quando você chama a função [**GetNPPBlobFromUI**](getnppblobfromui.md) , a caixa de diálogo **selecionar uma rede** é exibida.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-110">When you call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="b1dc5-111">A partir dele, você pode exibir os detalhes do NPPs registrados no computador local.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-111">From it, you can view the details of the NPPs registered on the local computer.</span></span> <span data-ttu-id="b1dc5-112">Essas informações incluem NPPs local e NPPs remota.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-112">This information includes both local NPPs and remote NPPs.</span></span> <span data-ttu-id="b1dc5-113">Na caixa de diálogo, você pode selecionar uma NIC específica e exibir os detalhes de sua estrutura de BLOB NPP associada.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-113">From the dialog box, you can select a specific NIC and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="b1dc5-114">A ilustração a seguir mostra as configurações típicas de um NPP NDIS fornecido pelo Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-114">The following illustration shows typical settings of an NDIS NPP supplied by Network Monitor.</span></span>

![configurações típicas de um NPP NDIS fornecido pelo monitor de rede](images/networkdb.png)

<span data-ttu-id="b1dc5-116">A tabela a seguir lista os tópicos que descrevem cada método de seleção de NIC.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-116">The following table lists topics that describe each NIC selection method.</span></span>



| <span data-ttu-id="b1dc5-117">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="b1dc5-117">For information about</span></span>                                                                          | <span data-ttu-id="b1dc5-118">Consulte</span><span class="sxs-lookup"><span data-stu-id="b1dc5-118">See</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1dc5-119">Como especificar um filtro que limita as NICs exibidas na caixa de diálogo **selecionar uma rede** .</span><span class="sxs-lookup"><span data-stu-id="b1dc5-119">How to specify a filter that limits the NICs displayed in the **Select a network** dialog box.</span></span> | [<span data-ttu-id="b1dc5-120">Especificando um BLOB de filtro</span><span class="sxs-lookup"><span data-stu-id="b1dc5-120">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="b1dc5-121">Como selecionar uma NIC chamando a função [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="b1dc5-121">How to select a NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>      | [<span data-ttu-id="b1dc5-122">Selecionando uma NIC usando GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="b1dc5-122">Selecting a NIC using GetNPPBlobFromUI</span></span>](getnppblobfromui.md)                                       |
| <span data-ttu-id="b1dc5-123">Como selecionar uma NIC de uma tabela de BLOB NPP fornecida.</span><span class="sxs-lookup"><span data-stu-id="b1dc5-123">How to select a NIC from a supplied NPP BLOB table.</span></span>                                            | [<span data-ttu-id="b1dc5-124">Selecionando uma NIC de uma tabela de BLOB NPP fornecida</span><span class="sxs-lookup"><span data-stu-id="b1dc5-124">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



