---
title: Sintaxe da cadeia de caracteres (tempo generalizado)
description: Um formato de cadeia de caracteres de tempo definido pelos padrões ASN. 1. | Sintaxe da cadeia de caracteres (tempo generalizado)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe de cadeia de caracteres (tempo generalizado)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172689"
---
# <a name="stringgeneralized-time-syntax"></a><span data-ttu-id="78c46-105">Sintaxe da cadeia de caracteres (tempo generalizado)</span><span class="sxs-lookup"><span data-stu-id="78c46-105">String(Generalized-Time) syntax</span></span>

<span data-ttu-id="78c46-106">Um formato de cadeia de caracteres de tempo definido pelos padrões ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="78c46-106">A time string format defined by ASN.1 standards.</span></span> <span data-ttu-id="78c46-107">Use essa sintaxe para armazenar valores de tempo no formato Generalized-Time.</span><span class="sxs-lookup"><span data-stu-id="78c46-107">Use this syntax for storing time values in Generalized-Time format.</span></span>

<span data-ttu-id="78c46-108">O formato para a sintaxe de Generalized-Time é "AAAAMMDDHHMMSS. 0Z".</span><span class="sxs-lookup"><span data-stu-id="78c46-108">The format for the Generalized-Time syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="78c46-109">Um exemplo de um valor aceitável é "20010928060000.0 Z".</span><span class="sxs-lookup"><span data-stu-id="78c46-109">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="78c46-110">O "Z" indica que não há diferencial de tempo.</span><span class="sxs-lookup"><span data-stu-id="78c46-110">The "Z" indicates no time differential.</span></span> <span data-ttu-id="78c46-111">Active Directory armazena data/hora como GMT (hora de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="78c46-111">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="78c46-112">Se nenhum diferencial de tempo for especificado, GMT será o padrão.</span><span class="sxs-lookup"><span data-stu-id="78c46-112">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="78c46-113">Se o tempo for especificado em um fuso horário diferente de GMT, o diferencial entre o fuso horário e o GMT será acrescentado à cadeia de caracteres em vez de "Z" no formato "AAAAMMDDHHMMSS. 0 \[ +/- \] hhmm".</span><span class="sxs-lookup"><span data-stu-id="78c46-113">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="78c46-114">Um exemplo de um valor aceitável é "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="78c46-114">An example of an acceptable value is "20010928060000.0+0200".</span></span> <span data-ttu-id="78c46-115">O diferencial é baseado na fórmula: GMT = local + diferencial.</span><span class="sxs-lookup"><span data-stu-id="78c46-115">The differential is based on the formula: GMT=Local+differential.</span></span>

<span data-ttu-id="78c46-116">Para obter mais informações, consulte ISO 8601 e X680.</span><span class="sxs-lookup"><span data-stu-id="78c46-116">For more information, see ISO 8601 and X680.</span></span>



| <span data-ttu-id="78c46-117">Entrada</span><span class="sxs-lookup"><span data-stu-id="78c46-117">Entry</span></span> | <span data-ttu-id="78c46-118">Valor</span><span class="sxs-lookup"><span data-stu-id="78c46-118">Value</span></span> |
|--------------|----------------------------------------------------------------------------|
| <span data-ttu-id="78c46-119">Nome</span><span class="sxs-lookup"><span data-stu-id="78c46-119">Name</span></span>         | <span data-ttu-id="78c46-120">Cadeia de caracteres (em tempo geral)</span><span class="sxs-lookup"><span data-stu-id="78c46-120">String(Generalized-Time)</span></span>                                                   |
| <span data-ttu-id="78c46-121">ID da sintaxe</span><span class="sxs-lookup"><span data-stu-id="78c46-121">Syntax ID</span></span>    | <span data-ttu-id="78c46-122">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="78c46-122">2.5.5.11</span></span>                                                                   |
| <span data-ttu-id="78c46-123">ID DO OM</span><span class="sxs-lookup"><span data-stu-id="78c46-123">OM ID</span></span>        | <span data-ttu-id="78c46-124">24</span><span class="sxs-lookup"><span data-stu-id="78c46-124">24</span></span>                                                                         |
| <span data-ttu-id="78c46-125">Tipo de MAPI</span><span class="sxs-lookup"><span data-stu-id="78c46-125">MAPI Type</span></span>    | <span data-ttu-id="78c46-126">SYSTIME</span><span class="sxs-lookup"><span data-stu-id="78c46-126">SYSTIME</span></span>                                                                    |
| <span data-ttu-id="78c46-127">Tipo de ADS</span><span class="sxs-lookup"><span data-stu-id="78c46-127">ADS Type</span></span>     | <span data-ttu-id="78c46-128">ADSTYPE \_ \_ hora UTC</span><span class="sxs-lookup"><span data-stu-id="78c46-128">ADSTYPE\_UTC\_TIME</span></span>                                                         |
| <span data-ttu-id="78c46-129">Tipo de variante</span><span class="sxs-lookup"><span data-stu-id="78c46-129">Variant Type</span></span> | <span data-ttu-id="78c46-130">Data de VT \_</span><span class="sxs-lookup"><span data-stu-id="78c46-130">VT\_DATE</span></span>                                                                   |
| <span data-ttu-id="78c46-131">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="78c46-131">SDS Type</span></span>     | [<span data-ttu-id="78c46-132">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="78c46-132">System.DateTime</span></span>](/dotnet/api/system.datetime) |



## <a name="see-also"></a><span data-ttu-id="78c46-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="78c46-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c46-134">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="78c46-134">System.DateTime</span></span>](/dotnet/api/system.datetime)
</dt> </dl>

 

 
