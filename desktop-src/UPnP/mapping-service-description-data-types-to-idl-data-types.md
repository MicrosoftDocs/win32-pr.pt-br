---
title: Mapeando tipos de dados de descrição de serviço para tipos de dados IDL
description: A tabela a seguir mostra o mapeamento de tipos de dados XML especificados em uma descrição de serviço para os tipos de dados correspondentes usados em IDL.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005981"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a><span data-ttu-id="cc63e-103">Mapeando tipos de dados de descrição de serviço para tipos de dados IDL</span><span class="sxs-lookup"><span data-stu-id="cc63e-103">Mapping Service Description Data Types to IDL Data Types</span></span>

<span data-ttu-id="cc63e-104">A tabela a seguir mostra o mapeamento de tipos de dados XML especificados em uma descrição de serviço para os tipos de dados correspondentes usados em IDL.</span><span class="sxs-lookup"><span data-stu-id="cc63e-104">The following table shows the mapping of XML data types specified in a service description to the corresponding data types used in IDL.</span></span>



| <span data-ttu-id="cc63e-105">Tipo de dados XML</span><span class="sxs-lookup"><span data-stu-id="cc63e-105">XML Data Type</span></span> | <span data-ttu-id="cc63e-106">Tipo de dados IDL</span><span class="sxs-lookup"><span data-stu-id="cc63e-106">IDL Data Type</span></span>  |
|---------------|----------------|
| <span data-ttu-id="cc63e-107">bin</span><span class="sxs-lookup"><span data-stu-id="cc63e-107">bin.base64</span></span>    | <span data-ttu-id="cc63e-108">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="cc63e-108">SAFEARRAY</span></span>      |
| <span data-ttu-id="cc63e-109">bin.hex</span><span class="sxs-lookup"><span data-stu-id="cc63e-109">bin.hex</span></span>       | <span data-ttu-id="cc63e-110">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="cc63e-110">SAFEARRAY</span></span>      |
| <span data-ttu-id="cc63e-111">booleano</span><span class="sxs-lookup"><span data-stu-id="cc63e-111">boolean</span></span>       | <span data-ttu-id="cc63e-112">BOOL de variante \_</span><span class="sxs-lookup"><span data-stu-id="cc63e-112">VARIANT\_BOOL</span></span>  |
| <span data-ttu-id="cc63e-113">char</span><span class="sxs-lookup"><span data-stu-id="cc63e-113">char</span></span>          | <span data-ttu-id="cc63e-114">WCHAR \_ t</span><span class="sxs-lookup"><span data-stu-id="cc63e-114">wchar\_t</span></span>       |
| <span data-ttu-id="cc63e-115">date</span><span class="sxs-lookup"><span data-stu-id="cc63e-115">date</span></span>          | <span data-ttu-id="cc63e-116">DATE</span><span class="sxs-lookup"><span data-stu-id="cc63e-116">DATE</span></span>           |
| <span data-ttu-id="cc63e-117">dateTime</span><span class="sxs-lookup"><span data-stu-id="cc63e-117">dateTime</span></span>      | <span data-ttu-id="cc63e-118">DATE</span><span class="sxs-lookup"><span data-stu-id="cc63e-118">DATE</span></span>           |
| <span data-ttu-id="cc63e-119">dateTime.tz</span><span class="sxs-lookup"><span data-stu-id="cc63e-119">dateTime.tz</span></span>   | <span data-ttu-id="cc63e-120">DATE</span><span class="sxs-lookup"><span data-stu-id="cc63e-120">DATE</span></span>           |
| <span data-ttu-id="cc63e-121">fixed.14.4</span><span class="sxs-lookup"><span data-stu-id="cc63e-121">fixed.14.4</span></span>    | <span data-ttu-id="cc63e-122">CY</span><span class="sxs-lookup"><span data-stu-id="cc63e-122">CY</span></span>             |
| <span data-ttu-id="cc63e-123">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cc63e-123">float</span></span>         | <span data-ttu-id="cc63e-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cc63e-124">float</span></span>          |
| <span data-ttu-id="cc63e-125">i1</span><span class="sxs-lookup"><span data-stu-id="cc63e-125">i1</span></span>            | <span data-ttu-id="cc63e-126">char</span><span class="sxs-lookup"><span data-stu-id="cc63e-126">char</span></span>           |
| <span data-ttu-id="cc63e-127">i2</span><span class="sxs-lookup"><span data-stu-id="cc63e-127">i2</span></span>            | <span data-ttu-id="cc63e-128">short</span><span class="sxs-lookup"><span data-stu-id="cc63e-128">short</span></span>          |
| <span data-ttu-id="cc63e-129">i4</span><span class="sxs-lookup"><span data-stu-id="cc63e-129">i4</span></span>            | <span data-ttu-id="cc63e-130">long</span><span class="sxs-lookup"><span data-stu-id="cc63e-130">long</span></span>           |
| <span data-ttu-id="cc63e-131">INT</span><span class="sxs-lookup"><span data-stu-id="cc63e-131">int</span></span>           | <span data-ttu-id="cc63e-132">long</span><span class="sxs-lookup"><span data-stu-id="cc63e-132">long</span></span>           |
| <span data-ttu-id="cc63e-133">número</span><span class="sxs-lookup"><span data-stu-id="cc63e-133">number</span></span>        | <span data-ttu-id="cc63e-134">BSTR</span><span class="sxs-lookup"><span data-stu-id="cc63e-134">BSTR</span></span>           |
| <span data-ttu-id="cc63e-135">r4</span><span class="sxs-lookup"><span data-stu-id="cc63e-135">r4</span></span>            | <span data-ttu-id="cc63e-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cc63e-136">float</span></span>          |
| <span data-ttu-id="cc63e-137">r8</span><span class="sxs-lookup"><span data-stu-id="cc63e-137">r8</span></span>            | <span data-ttu-id="cc63e-138">double</span><span class="sxs-lookup"><span data-stu-id="cc63e-138">double</span></span>         |
| <span data-ttu-id="cc63e-139">string</span><span class="sxs-lookup"><span data-stu-id="cc63e-139">string</span></span>        | <span data-ttu-id="cc63e-140">BSTR</span><span class="sxs-lookup"><span data-stu-id="cc63e-140">BSTR</span></span>           |
| <span data-ttu-id="cc63e-141">time</span><span class="sxs-lookup"><span data-stu-id="cc63e-141">time</span></span>          | <span data-ttu-id="cc63e-142">DATE</span><span class="sxs-lookup"><span data-stu-id="cc63e-142">DATE</span></span>           |
| <span data-ttu-id="cc63e-143">time.tz</span><span class="sxs-lookup"><span data-stu-id="cc63e-143">time.tz</span></span>       | <span data-ttu-id="cc63e-144">DATE</span><span class="sxs-lookup"><span data-stu-id="cc63e-144">DATE</span></span>           |
| <span data-ttu-id="cc63e-145">ui1</span><span class="sxs-lookup"><span data-stu-id="cc63e-145">ui1</span></span>           | <span data-ttu-id="cc63e-146">unsigned char</span><span class="sxs-lookup"><span data-stu-id="cc63e-146">unsigned char</span></span>  |
| <span data-ttu-id="cc63e-147">ui2</span><span class="sxs-lookup"><span data-stu-id="cc63e-147">ui2</span></span>           | <span data-ttu-id="cc63e-148">unsigned short</span><span class="sxs-lookup"><span data-stu-id="cc63e-148">unsigned short</span></span> |
| <span data-ttu-id="cc63e-149">ui4</span><span class="sxs-lookup"><span data-stu-id="cc63e-149">ui4</span></span>           | <span data-ttu-id="cc63e-150">unsigned long</span><span class="sxs-lookup"><span data-stu-id="cc63e-150">unsigned long</span></span>  |
| <span data-ttu-id="cc63e-151">uri</span><span class="sxs-lookup"><span data-stu-id="cc63e-151">uri</span></span>           | <span data-ttu-id="cc63e-152">BSTR</span><span class="sxs-lookup"><span data-stu-id="cc63e-152">BSTR</span></span>           |
| <span data-ttu-id="cc63e-153">uuid</span><span class="sxs-lookup"><span data-stu-id="cc63e-153">uuid</span></span>          | <span data-ttu-id="cc63e-154">BSTR</span><span class="sxs-lookup"><span data-stu-id="cc63e-154">BSTR</span></span>           |



 

 

 




