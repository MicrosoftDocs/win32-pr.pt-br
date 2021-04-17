---
description: O tipo de dados de data/hora tem a hora e a data armazenadas individualmente, usando inteiros não assinados como campos de bits, compactados da seguinte maneira.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Data/hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748565"
---
# <a name="timedate"></a><span data-ttu-id="e2284-103">Data/hora</span><span class="sxs-lookup"><span data-stu-id="e2284-103">Time/Date</span></span>

<span data-ttu-id="e2284-104">O tipo de dados de data/hora tem a hora e a data armazenadas individualmente, usando inteiros não assinados como campos de bits, compactados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="e2284-104">The Time/Date data type has the time and the date stored individually, using unsigned integers as bit fields, packed as follows.</span></span>

## <a name="time"></a><span data-ttu-id="e2284-105">Hora</span><span class="sxs-lookup"><span data-stu-id="e2284-105">Time</span></span>

<span data-ttu-id="e2284-106">O tempo é codificado em um inteiro sem sinal de 2 bytes com os campos de bits a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2284-106">Time is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="e2284-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="e2284-107">Contents</span></span>           | <span data-ttu-id="e2284-108">Bits</span><span class="sxs-lookup"><span data-stu-id="e2284-108">Bits</span></span>        | <span data-ttu-id="e2284-109">Intervalo de valor</span><span class="sxs-lookup"><span data-stu-id="e2284-109">Value range</span></span> |
|--------------------|-------------|-------------|
| <span data-ttu-id="e2284-110">horas</span><span class="sxs-lookup"><span data-stu-id="e2284-110">hours</span></span>              | <span data-ttu-id="e2284-111">0 1 2 3 4</span><span class="sxs-lookup"><span data-stu-id="e2284-111">0 1 2 3 4</span></span>   | <span data-ttu-id="e2284-112">0–23</span><span class="sxs-lookup"><span data-stu-id="e2284-112">0–23</span></span>        |
| <span data-ttu-id="e2284-113">minutes</span><span class="sxs-lookup"><span data-stu-id="e2284-113">minutes</span></span>            | <span data-ttu-id="e2284-114">5 6 7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="e2284-114">5 6 7 8 9 A</span></span> | <span data-ttu-id="e2284-115">0–59</span><span class="sxs-lookup"><span data-stu-id="e2284-115">0–59</span></span>        |
| <span data-ttu-id="e2284-116">intervalos de 2 segundos</span><span class="sxs-lookup"><span data-stu-id="e2284-116">2-second intervals</span></span> | <span data-ttu-id="e2284-117">B C D E F</span><span class="sxs-lookup"><span data-stu-id="e2284-117">B C D E F</span></span>   | <span data-ttu-id="e2284-118">0 – 29</span><span class="sxs-lookup"><span data-stu-id="e2284-118">0–29</span></span>        |



 

## <a name="date"></a><span data-ttu-id="e2284-119">Data</span><span class="sxs-lookup"><span data-stu-id="e2284-119">Date</span></span>

<span data-ttu-id="e2284-120">A data é codificada em um inteiro sem sinal de 2 bytes com os campos de bits a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2284-120">Date is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="e2284-121">Sumário</span><span class="sxs-lookup"><span data-stu-id="e2284-121">Contents</span></span> | <span data-ttu-id="e2284-122">Bits</span><span class="sxs-lookup"><span data-stu-id="e2284-122">Bits</span></span>          | <span data-ttu-id="e2284-123">Intervalo de valor</span><span class="sxs-lookup"><span data-stu-id="e2284-123">Value range</span></span>              |
|----------|---------------|--------------------------|
| <span data-ttu-id="e2284-124">ano</span><span class="sxs-lookup"><span data-stu-id="e2284-124">year</span></span>     | <span data-ttu-id="e2284-125">0 1 2 3 4 5 6</span><span class="sxs-lookup"><span data-stu-id="e2284-125">0 1 2 3 4 5 6</span></span> | <span data-ttu-id="e2284-126">0 – 119 (relativa a 1980)</span><span class="sxs-lookup"><span data-stu-id="e2284-126">0–119 (relative to 1980)</span></span> |
| <span data-ttu-id="e2284-127">mês</span><span class="sxs-lookup"><span data-stu-id="e2284-127">month</span></span>    | <span data-ttu-id="e2284-128">7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="e2284-128">7 8 9 A</span></span>       | <span data-ttu-id="e2284-129">1–12</span><span class="sxs-lookup"><span data-stu-id="e2284-129">1–12</span></span>                     |
| <span data-ttu-id="e2284-130">dia</span><span class="sxs-lookup"><span data-stu-id="e2284-130">day</span></span>      | <span data-ttu-id="e2284-131">B C D E F</span><span class="sxs-lookup"><span data-stu-id="e2284-131">B C D E F</span></span>     | <span data-ttu-id="e2284-132">1–31</span><span class="sxs-lookup"><span data-stu-id="e2284-132">1–31</span></span>                     |



 

 

 



