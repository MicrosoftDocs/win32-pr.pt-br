---
description: Representa uma descrição de um formato de textura.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixEngineTextureFormatDesc
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919946"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span data-ttu-id="29939-103"><span id="vspixengine.pixenginetextureformatdesc"></span>Estrutura PixEngineTextureFormatDesc</span><span class="sxs-lookup"><span data-stu-id="29939-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc structure</span></span>

<span data-ttu-id="29939-104">Representa uma descrição de um formato de textura.</span><span class="sxs-lookup"><span data-stu-id="29939-104">Represents a description of a texture format.</span></span>

## <a name="syntax"></a><span data-ttu-id="29939-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29939-105">Syntax</span></span>


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a><span data-ttu-id="29939-106">Membros</span><span class="sxs-lookup"><span data-stu-id="29939-106">Members</span></span>

<span data-ttu-id="29939-107">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="29939-107">**dxgiFormat**</span></span>  
<span data-ttu-id="29939-108">O formato DXGI da textura.</span><span class="sxs-lookup"><span data-stu-id="29939-108">The DXGI format of the texture.</span></span>

<span data-ttu-id="29939-109">**Formato de DataFormat**</span><span class="sxs-lookup"><span data-stu-id="29939-109">**dataFormat**</span></span>  
<span data-ttu-id="29939-110">O formato de dados da textura.</span><span class="sxs-lookup"><span data-stu-id="29939-110">The data format of the texture.</span></span>

<span data-ttu-id="29939-111">**blockBytes**</span><span class="sxs-lookup"><span data-stu-id="29939-111">**blockBytes**</span></span>  
<span data-ttu-id="29939-112">O número de bytes em um bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="29939-112">The number of bytes in a data block.</span></span>

<span data-ttu-id="29939-113">**blockHeight**</span><span class="sxs-lookup"><span data-stu-id="29939-113">**blockHeight**</span></span>  
<span data-ttu-id="29939-114">A altura (exemplos de número no eixo Y) do bloco.</span><span class="sxs-lookup"><span data-stu-id="29939-114">The height (number samples in the Y axis) of the block.</span></span>

<span data-ttu-id="29939-115">**blockWidth**</span><span class="sxs-lookup"><span data-stu-id="29939-115">**blockWidth**</span></span>  
<span data-ttu-id="29939-116">A largura (número de amostras no eixo X) do bloco.</span><span class="sxs-lookup"><span data-stu-id="29939-116">The width (number of samples in the X axis) of the block.</span></span>

<span data-ttu-id="29939-117">**channelX**</span><span class="sxs-lookup"><span data-stu-id="29939-117">**channelX**</span></span>  
<span data-ttu-id="29939-118">Descreve as propriedades do canal X.</span><span class="sxs-lookup"><span data-stu-id="29939-118">Describes properties of the X channel.</span></span> <span data-ttu-id="29939-119">Para obter mais informações, consulte a estrutura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="29939-119">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="29939-120">**canal**</span><span class="sxs-lookup"><span data-stu-id="29939-120">**channelY**</span></span>  
<span data-ttu-id="29939-121">Descreve as propriedades do canal Y.</span><span class="sxs-lookup"><span data-stu-id="29939-121">Describes properties of the Y channel.</span></span> <span data-ttu-id="29939-122">Para obter mais informações, consulte a estrutura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="29939-122">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="29939-123">**channelZ**</span><span class="sxs-lookup"><span data-stu-id="29939-123">**channelZ**</span></span>  
<span data-ttu-id="29939-124">Descreve as propriedades do canal Z.</span><span class="sxs-lookup"><span data-stu-id="29939-124">Describes properties of the Z channel.</span></span> <span data-ttu-id="29939-125">Para obter mais informações, consulte a estrutura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="29939-125">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="29939-126">**channelW**</span><span class="sxs-lookup"><span data-stu-id="29939-126">**channelW**</span></span>  
<span data-ttu-id="29939-127">Descreve as propriedades do canal W.</span><span class="sxs-lookup"><span data-stu-id="29939-127">Describes properties of the W channel.</span></span> <span data-ttu-id="29939-128">Para obter mais informações, consulte a estrutura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="29939-128">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="29939-129">**swizzle**</span><span class="sxs-lookup"><span data-stu-id="29939-129">**swizzle**</span></span>  
<span data-ttu-id="29939-130">Descreve o swizzle (troca de canal) aplicado ao exemplo.</span><span class="sxs-lookup"><span data-stu-id="29939-130">Describes the swizzle (channel-swapping) applied to the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="29939-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29939-131">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="29939-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29939-132">Header</span></span></p></td><td><span data-ttu-id="29939-133">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="29939-133">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



