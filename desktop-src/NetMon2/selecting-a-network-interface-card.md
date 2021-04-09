---
description: Monitor de Rede fornece três funções para selecionar uma placa de interface de rede (NIC). Essas funções fornecem três maneiras de enumerar um conjunto de NICs e selecionar aquela que você deseja usar. A tabela a seguir lista essas funções.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Selecionando uma placa de interface de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091392"
---
# <a name="selecting-a-network-interface-card"></a><span data-ttu-id="29eb0-105">Selecionando uma placa de interface de rede</span><span class="sxs-lookup"><span data-stu-id="29eb0-105">Selecting a Network Interface Card</span></span>

<span data-ttu-id="29eb0-106">Monitor de Rede fornece três funções para selecionar uma placa de interface de rede (NIC).</span><span class="sxs-lookup"><span data-stu-id="29eb0-106">Network Monitor provides three functions for selecting a network interface card (NIC).</span></span> <span data-ttu-id="29eb0-107">Essas funções fornecem três maneiras de enumerar um conjunto de NICs e selecionar aquela que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="29eb0-107">These functions provide three ways to enumerate a set of NICs and select the one you want to use.</span></span> <span data-ttu-id="29eb0-108">A tabela a seguir lista essas funções.</span><span class="sxs-lookup"><span data-stu-id="29eb0-108">The following table lists these functions.</span></span>



| <span data-ttu-id="29eb0-109">Função</span><span class="sxs-lookup"><span data-stu-id="29eb0-109">Function</span></span>                                                 | <span data-ttu-id="29eb0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="29eb0-110">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29eb0-111">**GetNPPBlobFromUI**</span><span class="sxs-lookup"><span data-stu-id="29eb0-111">**GetNPPBlobFromUI**</span></span>](getnppblobfromui.md)             | <span data-ttu-id="29eb0-112">Usa o Monitor de Rede interface do usuário para exibir as NICs registradas e retorna o BLOB NPP que representa a NIC em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="29eb0-112">Uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you are interested in.</span></span>           |
| [<span data-ttu-id="29eb0-113">**GetNPPBlobTable**</span><span class="sxs-lookup"><span data-stu-id="29eb0-113">**GetNPPBlobTable**</span></span>](getnppblobtable.md)               | <span data-ttu-id="29eb0-114">Retorna uma tabela de BLOB.</span><span class="sxs-lookup"><span data-stu-id="29eb0-114">Returns a BLOB table.</span></span> <span data-ttu-id="29eb0-115">O aplicativo deve enumerar a tabela e selecionar um BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="29eb0-115">The application must enumerate the table and select an NPP BLOB.</span></span>                                                       |
| [<span data-ttu-id="29eb0-116">**SelectNPPBlobFromTable**</span><span class="sxs-lookup"><span data-stu-id="29eb0-116">**SelectNPPBlobFromTable**</span></span>](selectnppblobfromtable.md) | <span data-ttu-id="29eb0-117">Usa a interface Monitor de Rede para exibir os BLOBs NPP fornecidos e retorna o BLOB NPP que representa a NIC em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="29eb0-117">Uses the Network Monitor interface to display the supplied NPP BLOBs and returns the NPP BLOB that represents the NIC you are interested in.</span></span> |



 

<span data-ttu-id="29eb0-118">Cada NIC é representada por um BLOB (objeto binário grande) NPP.</span><span class="sxs-lookup"><span data-stu-id="29eb0-118">Each NIC is represented by an NPP binary large object (BLOB).</span></span> <span data-ttu-id="29eb0-119">Essas funções podem retornar um único BLOB NPP dos registrados no computador, um único BLOB de NPP de uma tabela de BLOB NPP fornecida ou uma tabela de BLOBs NPP que o chamador deve usar para selecionar um BLOB específico.</span><span class="sxs-lookup"><span data-stu-id="29eb0-119">These functions can return a single NPP BLOB from those registered on the computer, a single NPP BLOB from a supplied NPP BLOB table, or a table of NPP BLOBs that the caller must then use to select a specific BLOB.</span></span> <span data-ttu-id="29eb0-120">Nos dois primeiros casos, ao selecionar as NICs registradas ou de uma tabela de BLOB NPP fornecida, a interface do usuário do Monitor de Rede exibe as NICs que você pode selecionar.</span><span class="sxs-lookup"><span data-stu-id="29eb0-120">In the first two cases, when selecting from the registered NICs or from a supplied NPP BLOB table, the Network Monitor UI displays the NICs you can select.</span></span>

> [!Note]  
> <span data-ttu-id="29eb0-121">Monitor de Rede usa um recurso chamado NPP Finder para enumerar as NICs registradas no computador local.</span><span class="sxs-lookup"><span data-stu-id="29eb0-121">Network Monitor uses a feature called the NPP Finder to enumerate the NICs registered on the local computer.</span></span> <span data-ttu-id="29eb0-122">O NPP Finder é um componente do Npptools.dll.</span><span class="sxs-lookup"><span data-stu-id="29eb0-122">The NPP Finder is a component of Npptools.dll.</span></span>

 



| <span data-ttu-id="29eb0-123">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="29eb0-123">For information about</span></span>                            | <span data-ttu-id="29eb0-124">Consulte</span><span class="sxs-lookup"><span data-stu-id="29eb0-124">See</span></span>                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29eb0-125">Selecionando uma NIC registrada no computador local</span><span class="sxs-lookup"><span data-stu-id="29eb0-125">Selecting a NIC registered on the local computer</span></span> | [<span data-ttu-id="29eb0-126">Selecionando uma NIC registrada</span><span class="sxs-lookup"><span data-stu-id="29eb0-126">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="29eb0-127">Selecionando uma NIC de uma tabela de BLOB NPP fornecida</span><span class="sxs-lookup"><span data-stu-id="29eb0-127">Selecting a NIC from a supplied NPP BLOB table</span></span>   | [<span data-ttu-id="29eb0-128">Selecionando uma NIC de uma tabela de BLOB NPP fornecida</span><span class="sxs-lookup"><span data-stu-id="29eb0-128">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| <span data-ttu-id="29eb0-129">Recuperando uma tabela de BLOB NPP</span><span class="sxs-lookup"><span data-stu-id="29eb0-129">Retrieving an NPP BLOB table</span></span>                     | [<span data-ttu-id="29eb0-130">Selecionando uma NIC de uma tabela de BLOB NPP retornada</span><span class="sxs-lookup"><span data-stu-id="29eb0-130">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



