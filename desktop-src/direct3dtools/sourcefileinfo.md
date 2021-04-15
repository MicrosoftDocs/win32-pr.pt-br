---
description: Representa informações sobre um arquivo de código-fonte.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura SourceFileInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456692"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span data-ttu-id="cf81b-103"><span id="vspixengine.sourcefileinfo"></span>Estrutura SourceFileInfo</span><span class="sxs-lookup"><span data-stu-id="cf81b-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo structure</span></span>

<span data-ttu-id="cf81b-104">Representa informações sobre um arquivo de código-fonte.</span><span class="sxs-lookup"><span data-stu-id="cf81b-104">Represents information about a source code file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf81b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf81b-105">Syntax</span></span>


```C++
} SourceFileInfo;
```

## <a name="members"></a><span data-ttu-id="cf81b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cf81b-106">Members</span></span>

<span data-ttu-id="cf81b-107">**Nome do arquivo**</span><span class="sxs-lookup"><span data-stu-id="cf81b-107">**fileName**</span></span>  
<span data-ttu-id="cf81b-108">Uma cadeia de caracteres COM comtaining o FilePath do arquivo de origem associado.</span><span class="sxs-lookup"><span data-stu-id="cf81b-108">A COM string comtaining the filepath of the associated source file.</span></span>

<span data-ttu-id="cf81b-109">**checksumByteCount**</span><span class="sxs-lookup"><span data-stu-id="cf81b-109">**checksumByteCount**</span></span>  
<span data-ttu-id="cf81b-110">O número de bytes na soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf81b-110">The number of bytes in the checksum.</span></span> <span data-ttu-id="cf81b-111">Quando checkSumAlgorithm é igual a CHECKSUMALGORITHM:: MD5, checkSumByteCount é 16.</span><span class="sxs-lookup"><span data-stu-id="cf81b-111">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::md5, checkSumByteCount is 16.</span></span> <span data-ttu-id="cf81b-112">Quando checkSumAlgorithm é igual a CHECKSUMALGORITHM:: SHA1, checkSumByteCount é 20.</span><span class="sxs-lookup"><span data-stu-id="cf81b-112">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::sha1, checkSumByteCount is 20.</span></span>

<span data-ttu-id="cf81b-113">**checkSumAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="cf81b-113">**checkSumAlgorithm**</span></span>  
<span data-ttu-id="cf81b-114">Especifica o algoritmo usado para gerar a soma de verificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf81b-114">Specifies the algorithm used to generate the checksum of the file.</span></span> <span data-ttu-id="cf81b-115">Os algoritmos com suporte são MD5 e SHA1.</span><span class="sxs-lookup"><span data-stu-id="cf81b-115">Supported algorithms are MD5 and SHA1.</span></span> <span data-ttu-id="cf81b-116">Para obter mais informações, consulte a enumeração CHECKSUMALGORITHM.</span><span class="sxs-lookup"><span data-stu-id="cf81b-116">For more information, see the CHECKSUMALGORITHM enum.</span></span>

<span data-ttu-id="cf81b-117">**checkSumFirstPart**</span><span class="sxs-lookup"><span data-stu-id="cf81b-117">**checkSumFirstPart**</span></span>  
<span data-ttu-id="cf81b-118">A primeira parte de 8 bytes da soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf81b-118">The first 8 byte portion of the checksum.</span></span>

<span data-ttu-id="cf81b-119">**checkSumSecondPart**</span><span class="sxs-lookup"><span data-stu-id="cf81b-119">**checkSumSecondPart**</span></span>  
<span data-ttu-id="cf81b-120">A segunda parte de 8 bytes da soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf81b-120">The second 8 byte portion of the checksum.</span></span>

<span data-ttu-id="cf81b-121">**checkSumThirdPart**</span><span class="sxs-lookup"><span data-stu-id="cf81b-121">**checkSumThirdPart**</span></span>  
<span data-ttu-id="cf81b-122">A terceira parte de 8 bytes da soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf81b-122">The third 8 byte portion of the checksum.</span></span>

<span data-ttu-id="cf81b-123">**checkSumFourthPart**</span><span class="sxs-lookup"><span data-stu-id="cf81b-123">**checkSumFourthPart**</span></span>  
<span data-ttu-id="cf81b-124">A quarta parte de 8 bytes da soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf81b-124">The fourth 8 byte portion of the checksum.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf81b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf81b-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cf81b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf81b-126">Header</span></span></p></td><td><span data-ttu-id="cf81b-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cf81b-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



