---
description: Observe que essa API foi preterida. Novos aplicativos não devem usá-lo. O tipo de dados MSPID identifica a finalidade de um fluxo de mídia.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (Mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758836"
---
# <a name="mspid"></a><span data-ttu-id="581a3-105">MSPID</span><span class="sxs-lookup"><span data-stu-id="581a3-105">MSPID</span></span>

> [!Note]  
> <span data-ttu-id="581a3-106">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="581a3-106">This API is deprecated.</span></span> <span data-ttu-id="581a3-107">Novos aplicativos não devem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="581a3-107">New applications should not use it.</span></span>

 

<span data-ttu-id="581a3-108">O tipo de dados **MSPID** identifica a finalidade de um fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="581a3-108">The **MSPID** data type identifies the purpose of a media steam.</span></span>


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a><span data-ttu-id="581a3-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="581a3-109">Remarks</span></span>

<span data-ttu-id="581a3-110">**MSPID** é simplesmente um TYPEDEF para GUID.</span><span class="sxs-lookup"><span data-stu-id="581a3-110">**MSPID** is simply a typedef for GUID.</span></span> <span data-ttu-id="581a3-111">Os MSPIDs a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="581a3-111">The following MSPIDs are defined.</span></span>



| <span data-ttu-id="581a3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="581a3-112">Value</span></span>               | <span data-ttu-id="581a3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="581a3-113">Description</span></span>           |
|---------------------|-----------------------|
| <span data-ttu-id="581a3-114">MSPID \_ PrimaryVideo</span><span class="sxs-lookup"><span data-stu-id="581a3-114">MSPID\_PrimaryVideo</span></span> | <span data-ttu-id="581a3-115">Fluxo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="581a3-115">Primary video stream.</span></span> |
| <span data-ttu-id="581a3-116">MSPID \_ PrimaryAudio</span><span class="sxs-lookup"><span data-stu-id="581a3-116">MSPID\_PrimaryAudio</span></span> | <span data-ttu-id="581a3-117">Fluxo de áudio primário.</span><span class="sxs-lookup"><span data-stu-id="581a3-117">Primary audio stream.</span></span> |



 

<span data-ttu-id="581a3-118">O tipo **REFMSPID** define uma referência a um **MSPID**.</span><span class="sxs-lookup"><span data-stu-id="581a3-118">The **REFMSPID** type defines a reference to an **MSPID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="581a3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="581a3-119">Requirements</span></span>



| <span data-ttu-id="581a3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="581a3-120">Requirement</span></span> | <span data-ttu-id="581a3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="581a3-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="581a3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="581a3-122">Header</span></span><br/> | <dl> <span data-ttu-id="581a3-123"><dt>Mmstream. h</dt></span><span class="sxs-lookup"><span data-stu-id="581a3-123"><dt>Mmstream.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="581a3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="581a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581a3-125">Tipos de dados de streaming de multimídia</span><span class="sxs-lookup"><span data-stu-id="581a3-125">Multimedia Streaming Data Types</span></span>](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




