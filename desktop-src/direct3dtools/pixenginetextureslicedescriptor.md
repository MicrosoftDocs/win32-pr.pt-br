---
description: Representa uma descrição de uma fatia de textura.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixEngineTextureSliceDescriptor
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087426"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span data-ttu-id="d9718-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>Estrutura PixEngineTextureSliceDescriptor</span><span class="sxs-lookup"><span data-stu-id="d9718-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor structure</span></span>

<span data-ttu-id="d9718-104">Representa uma descrição de uma fatia de textura.</span><span class="sxs-lookup"><span data-stu-id="d9718-104">Represents a description of a texture slice.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9718-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9718-105">Syntax</span></span>


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a><span data-ttu-id="d9718-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d9718-106">Members</span></span>

<span data-ttu-id="d9718-107">**width**</span><span class="sxs-lookup"><span data-stu-id="d9718-107">**width**</span></span>  
<span data-ttu-id="d9718-108">A largura (número de amostras no eixo X) da fatia.</span><span class="sxs-lookup"><span data-stu-id="d9718-108">The width (number of samples in the X axis) of the slice.</span></span>

<span data-ttu-id="d9718-109">**altura**</span><span class="sxs-lookup"><span data-stu-id="d9718-109">**height**</span></span>  
<span data-ttu-id="d9718-110">A altura (número de amostras no eixo Y) da fatia.</span><span class="sxs-lookup"><span data-stu-id="d9718-110">The height (number of samples in the Y axis) of the slice.</span></span>

<span data-ttu-id="d9718-111">**blockRowBytes**</span><span class="sxs-lookup"><span data-stu-id="d9718-111">**blockRowBytes**</span></span>  
<span data-ttu-id="d9718-112">O número de bytes por linha em cada bloco.</span><span class="sxs-lookup"><span data-stu-id="d9718-112">The number of bytes per row in each block.</span></span>

<span data-ttu-id="d9718-113">**offset**</span><span class="sxs-lookup"><span data-stu-id="d9718-113">**offset**</span></span>  
<span data-ttu-id="d9718-114">O deslocamento da fatia dentro da textura inteira.</span><span class="sxs-lookup"><span data-stu-id="d9718-114">The offset of the slice within the whole texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9718-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9718-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d9718-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9718-116">Header</span></span></p></td><td><span data-ttu-id="d9718-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d9718-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



