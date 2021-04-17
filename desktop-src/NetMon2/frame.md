---
description: Um quadro real do driver.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Estrutura do quadro (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766364"
---
# <a name="frame-structure"></a><span data-ttu-id="dfe2d-103">Estrutura do quadro</span><span class="sxs-lookup"><span data-stu-id="dfe2d-103">FRAME structure</span></span>

<span data-ttu-id="dfe2d-104">A estrutura do **quadro** é um quadro real do driver.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-104">The **FRAME** structure is an actual frame from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe2d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfe2d-105">Syntax</span></span>


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a><span data-ttu-id="dfe2d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="dfe2d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dfe2d-107">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="dfe2d-107">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="dfe2d-108">Tempo decorrido, em microssegundos, entre o início da captura e a hora em que o quadro foi capturado.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-108">Elapsed time, in microseconds, between the start of the capture and the time when the frame was captured.</span></span>

</dd> <dt>

<span data-ttu-id="dfe2d-109">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="dfe2d-109">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="dfe2d-110">Tamanho do quadro MAC.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-110">MAC frame length.</span></span>

</dd> <dt>

<span data-ttu-id="dfe2d-111">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="dfe2d-111">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="dfe2d-112">Tamanho de quadro real copiado.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-112">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="dfe2d-113">**MacFrame**</span><span class="sxs-lookup"><span data-stu-id="dfe2d-113">**MacFrame**</span></span>
</dt> <dd>

<span data-ttu-id="dfe2d-114">Dados do quadro.</span><span class="sxs-lookup"><span data-stu-id="dfe2d-114">Frame data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfe2d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfe2d-115">Requirements</span></span>



| <span data-ttu-id="dfe2d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfe2d-116">Requirement</span></span> | <span data-ttu-id="dfe2d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dfe2d-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe2d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfe2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dfe2d-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dfe2d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dfe2d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfe2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dfe2d-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dfe2d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dfe2d-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dfe2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfe2d-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfe2d-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




