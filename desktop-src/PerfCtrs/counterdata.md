---
description: A tabela de comDados contém uma linha para cada contador que é coletada em um momento específico. Haverá um grande número dessas linhas.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828393"
---
# <a name="counterdata"></a><span data-ttu-id="86d65-104">Dados</span><span class="sxs-lookup"><span data-stu-id="86d65-104">CounterData</span></span>

<span data-ttu-id="86d65-105">A tabela de **comDados** contém uma linha para cada contador que é coletada em um momento específico.</span><span class="sxs-lookup"><span data-stu-id="86d65-105">The **CounterData** table contains a row for each counter that is collected at a particular time.</span></span> <span data-ttu-id="86d65-106">Haverá um grande número dessas linhas.</span><span class="sxs-lookup"><span data-stu-id="86d65-106">There will be a large number of these rows.</span></span>

<span data-ttu-id="86d65-107">A tabela de **comDados** define os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="86d65-107">The **CounterData** table defines the following fields:</span></span>

-   <span data-ttu-id="86d65-108">**GUID:** GUID para este conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="86d65-108">**GUID:** GUID for this data set.</span></span> <span data-ttu-id="86d65-109">Use essa chave para ingressar com a tabela [**DisplayToID**](displaytoid.md) .</span><span class="sxs-lookup"><span data-stu-id="86d65-109">Use this key to join with the [**DisplayToID**](displaytoid.md) table.</span></span>
-   <span data-ttu-id="86d65-110">**Counterid:** Identifica o contador.</span><span class="sxs-lookup"><span data-stu-id="86d65-110">**CounterID:** Identifies the counter.</span></span> <span data-ttu-id="86d65-111">Use essa chave para ingressar com a tabela de [**detalhes**](counterdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="86d65-111">Use this key to join with the [**CounterDetails**](counterdetails.md) table.</span></span>
-   <span data-ttu-id="86d65-112">**RecordIndex:** O índice de exemplo para um identificador de contador e GUID de coleção específicos.</span><span class="sxs-lookup"><span data-stu-id="86d65-112">**RecordIndex:** The sample index for a specific counter identifier and collection GUID.</span></span> <span data-ttu-id="86d65-113">O valor aumenta para cada exemplo sucessivo nesse arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="86d65-113">The value increases for each successive sample in this log file.</span></span>
-   <span data-ttu-id="86d65-114">**DateTime:** A hora em que a coleção foi iniciada, em hora UTC.</span><span class="sxs-lookup"><span data-stu-id="86d65-114">**CounterDateTime:** The time the collection was started, in UTC time.</span></span>
-   <span data-ttu-id="86d65-115">**Valor:** O valor formatado do contador.</span><span class="sxs-lookup"><span data-stu-id="86d65-115">**CounterValue:** The formatted value of the counter.</span></span> <span data-ttu-id="86d65-116">Esse valor pode ser zero para o primeiro registro se o contador exigir dois exemplos para computar um valor de exibição.</span><span class="sxs-lookup"><span data-stu-id="86d65-116">This value may be zero for the first record if the counter requires two sample to compute a displayable value.</span></span>
-   <span data-ttu-id="86d65-117">**FirstValueA:** Combine esse valor de 32 bits com o valor de **FirstValueB** para criar o membro **primeirovalue** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="86d65-117">**FirstValueA:** Combine this 32-bit value with the value of **FirstValueB** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="86d65-118">**FirstValueA** contém os bits de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="86d65-118">**FirstValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="86d65-119">**FirstValueB:** Combine esse valor de 32 bits com o valor de **FirstValueA** para criar o membro **primeirovalue** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="86d65-119">**FirstValueB:** Combine this 32-bit value with the value of **FirstValueA** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="86d65-120">**FirstValueB** contém os bits de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="86d65-120">**FirstValueB** contains the high order bits.</span></span>
-   <span data-ttu-id="86d65-121">**SecondValueA:** Combine esse valor de 32 bits com o valor de **SecondValueB** para criar o membro **segundovalue** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="86d65-121">**SecondValueA:** Combine this 32-bit value with the value of **SecondValueB** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="86d65-122">**SecondValueA** contém os bits de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="86d65-122">**SecondValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="86d65-123">**SecondValueB:** Combine esse valor de 32 bits com o valor de **SecondValueA** para criar o membro **segundovalue** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="86d65-123">**SecondValueB:** Combine this 32-bit value with the value of **SecondValueA** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="86d65-124">**SecondValueB** contém os bits de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="86d65-124">**SecondValueB** contains the high order bits.</span></span>

<span data-ttu-id="86d65-125">Os campos **GUID**, **counterid** e **RecordIndex** compõem a chave primária desta tabela.</span><span class="sxs-lookup"><span data-stu-id="86d65-125">The **GUID**, **CounterID**, and **RecordIndex** fields make up the primary key for this table.</span></span>

 

 



