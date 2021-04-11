---
title: OP_PACKAGE_PART
description: Definição de IDL de OP_PACKAGE_PART
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104162953"
---
# <a name="op_package_part-structure"></a><span data-ttu-id="a1b25-103">Estrutura de OP_PACKAGE_PART</span><span class="sxs-lookup"><span data-stu-id="a1b25-103">OP_PACKAGE_PART structure</span></span>

<span data-ttu-id="a1b25-104">Define uma estrutura que contém um conjunto de dados identificado por um GUID.</span><span class="sxs-lookup"><span data-stu-id="a1b25-104">Defines a structure that contains a data set identified by a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b25-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1b25-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a><span data-ttu-id="a1b25-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a1b25-106">Members</span></span>

### <a name="parttype"></a><span data-ttu-id="a1b25-107">Parte</span><span class="sxs-lookup"><span data-stu-id="a1b25-107">PartType</span></span>

<span data-ttu-id="a1b25-108">Identifica a estrutura serializada contida em parte de acordo com a tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="a1b25-108">Identifies the serialized structure contained in Part per the following table:</span></span>

|<span data-ttu-id="a1b25-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a1b25-109">PartType</span></span>|<span data-ttu-id="a1b25-110">Significado</span><span class="sxs-lookup"><span data-stu-id="a1b25-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="a1b25-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span><span class="sxs-lookup"><span data-stu-id="a1b25-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span></span>|<span data-ttu-id="a1b25-112">Contém uma estrutura de ODJ_WIN7_BLOB serializada.</span><span class="sxs-lookup"><span data-stu-id="a1b25-112">Contains a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="a1b25-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span><span class="sxs-lookup"><span data-stu-id="a1b25-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span></span>|<span data-ttu-id="a1b25-114">Contém uma estrutura de OP_JOIN_PROV2_PART serializada.</span><span class="sxs-lookup"><span data-stu-id="a1b25-114">Contains a serialized OP_JOIN_PROV2_PART structure.</span></span>|
|<span data-ttu-id="a1b25-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span><span class="sxs-lookup"><span data-stu-id="a1b25-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span></span>|<span data-ttu-id="a1b25-116">Contém uma estrutura de OP_JOIN_PROV3_PART serializada.</span><span class="sxs-lookup"><span data-stu-id="a1b25-116">Contains a serialized OP_JOIN_PROV3_PART structure.</span></span>|
|<span data-ttu-id="a1b25-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span><span class="sxs-lookup"><span data-stu-id="a1b25-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span></span>|<span data-ttu-id="a1b25-118">Contém uma estrutura de OP_CERT_PART serializada.</span><span class="sxs-lookup"><span data-stu-id="a1b25-118">Contains a serialized OP_CERT_PART structure.</span></span>|
|<span data-ttu-id="a1b25-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span><span class="sxs-lookup"><span data-stu-id="a1b25-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span></span>|<span data-ttu-id="a1b25-120">Contém uma estrutura de OP_POLICY_PART serializada.</span><span class="sxs-lookup"><span data-stu-id="a1b25-120">Contains a serialized OP_POLICY_PART structure.</span></span>|

### <a name="ulflags"></a><span data-ttu-id="a1b25-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="a1b25-121">ulFlags</span></span>

<span data-ttu-id="a1b25-122">Deve ser definido como zero ou mais dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="a1b25-122">Must be set to zero or more of the following flags:</span></span>

|<span data-ttu-id="a1b25-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a1b25-123">Value</span></span>|<span data-ttu-id="a1b25-124">Significado</span><span class="sxs-lookup"><span data-stu-id="a1b25-124">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="a1b25-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a1b25-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span></span>|<span data-ttu-id="a1b25-126">Essa parte do pacote é considerada essencial.</span><span class="sxs-lookup"><span data-stu-id="a1b25-126">This package part is considered essential.</span></span> <span data-ttu-id="a1b25-127">Se o consumidor não reconhecer essa parte do pacote ou não conseguir processá-la com êxito, a operação geral deverá falhar.</span><span class="sxs-lookup"><span data-stu-id="a1b25-127">If the consumer does not recognize this package part or fails to successfully process it, the overall operation must fail.</span></span>|

### <a name="part"></a><span data-ttu-id="a1b25-128">Parte</span><span class="sxs-lookup"><span data-stu-id="a1b25-128">Part</span></span>

<span data-ttu-id="a1b25-129">Contém uma estrutura serializada em uma estrutura de OP_BLOB.</span><span class="sxs-lookup"><span data-stu-id="a1b25-129">Contains a serialized structure in an OP_BLOB structure.</span></span> <span data-ttu-id="a1b25-130">A estrutura específica é determinada por partType.</span><span class="sxs-lookup"><span data-stu-id="a1b25-130">The specific structure is determined by PartType.</span></span>

### <a name="extension"></a><span data-ttu-id="a1b25-131">Extensão</span><span class="sxs-lookup"><span data-stu-id="a1b25-131">Extension</span></span>

<span data-ttu-id="a1b25-132">Reservado para uso futuro e deve ser definido como todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="a1b25-132">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1b25-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1b25-133">See also</span></span>

[<span data-ttu-id="a1b25-134">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="a1b25-134">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="a1b25-135">**BLOB de OP \_**</span><span class="sxs-lookup"><span data-stu-id="a1b25-135">**OP\_BLOB**</span></span>](odj-op_blob.md)
