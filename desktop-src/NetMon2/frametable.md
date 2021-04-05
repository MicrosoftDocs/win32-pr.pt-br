---
description: A estrutura de FRAMEtable, um buffer circular de ponteiros de quadro, é devolvido aos aplicativos anexados à interface ITRC do NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Estrutura de FRAMEtable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089972"
---
# <a name="frametable-structure"></a><span data-ttu-id="2a927-103">Estrutura de quadros</span><span class="sxs-lookup"><span data-stu-id="2a927-103">FRAMETABLE structure</span></span>

<span data-ttu-id="2a927-104">A estrutura de **frametable** , um buffer circular de ponteiros de quadro, é devolvido aos aplicativos anexados à interface **ITRC** do NPP.</span><span class="sxs-lookup"><span data-stu-id="2a927-104">The **FRAMETABLE** structure, a circular buffer of frame pointers, is handed back to applications attached to the **ITRC** interface of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a927-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a927-105">Syntax</span></span>


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a><span data-ttu-id="2a927-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2a927-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a927-107">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="2a927-107">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="2a927-108">O comprimento total da tabela.</span><span class="sxs-lookup"><span data-stu-id="2a927-108">The total length of the table.</span></span>

</dd> <dt>

<span data-ttu-id="2a927-109">**StartIndex**</span><span class="sxs-lookup"><span data-stu-id="2a927-109">**StartIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2a927-110">O primeiro índice na tabela.</span><span class="sxs-lookup"><span data-stu-id="2a927-110">The first index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="2a927-111">**EndIndex**</span><span class="sxs-lookup"><span data-stu-id="2a927-111">**EndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2a927-112">O último índice na tabela.</span><span class="sxs-lookup"><span data-stu-id="2a927-112">The last index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="2a927-113">**FrameCount**</span><span class="sxs-lookup"><span data-stu-id="2a927-113">**FrameCount**</span></span>
</dt> <dd>

<span data-ttu-id="2a927-114">O número de quadros descritos por esta tabela.</span><span class="sxs-lookup"><span data-stu-id="2a927-114">The number of frames described by this table.</span></span>

</dd> <dt>

<span data-ttu-id="2a927-115">**Intervalos**</span><span class="sxs-lookup"><span data-stu-id="2a927-115">**Frames**</span></span>
</dt> <dd>

<span data-ttu-id="2a927-116">A matriz real de descritores de quadros.</span><span class="sxs-lookup"><span data-stu-id="2a927-116">The actual array of frame descriptors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a927-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a927-117">Requirements</span></span>



| <span data-ttu-id="2a927-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a927-118">Requirement</span></span> | <span data-ttu-id="2a927-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2a927-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2a927-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a927-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a927-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a927-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2a927-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a927-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a927-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a927-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2a927-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2a927-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a927-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a927-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




