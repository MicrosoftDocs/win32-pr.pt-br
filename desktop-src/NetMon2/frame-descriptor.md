---
description: A \_ estrutura do descritor de quadros fornece informações descritivas sobre quadros brutos.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Estrutura de FRAME_DESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782303"
---
# <a name="frame_descriptor-structure"></a><span data-ttu-id="51f19-103">\_Estrutura do descritor de quadros</span><span class="sxs-lookup"><span data-stu-id="51f19-103">FRAME\_DESCRIPTOR structure</span></span>

<span data-ttu-id="51f19-104">A estrutura do **\_ descritor de quadros** fornece informações descritivas sobre quadros brutos.</span><span class="sxs-lookup"><span data-stu-id="51f19-104">The **FRAME\_DESCRIPTOR** structure provides descriptive information about raw frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51f19-105">Syntax</span></span>


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="51f19-106">Membros</span><span class="sxs-lookup"><span data-stu-id="51f19-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="51f19-107">**FramePointer**</span><span class="sxs-lookup"><span data-stu-id="51f19-107">**FramePointer**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-108">Ponteiro para dados de quadro.</span><span class="sxs-lookup"><span data-stu-id="51f19-108">Pointer to frame data.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-109">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="51f19-109">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-110">Hora do sistema, em microssegundos, quando o quadro foi capturado.</span><span class="sxs-lookup"><span data-stu-id="51f19-110">System time, in microseconds, when the frame was captured.</span></span> <span data-ttu-id="51f19-111">Esse tempo normalmente é usado para determinar o intervalo entre os tempos em que dois quadros foram capturados.</span><span class="sxs-lookup"><span data-stu-id="51f19-111">This time is typically used to determine the interval between the times two frames were captured.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-112">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="51f19-112">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-113">Comprimento do quadro.</span><span class="sxs-lookup"><span data-stu-id="51f19-113">Length of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-114">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="51f19-114">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-115">Tamanho de quadro real copiado.</span><span class="sxs-lookup"><span data-stu-id="51f19-115">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-116">**ETYPE**</span><span class="sxs-lookup"><span data-stu-id="51f19-116">**Etype**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-117">Nome do ETYPE.</span><span class="sxs-lookup"><span data-stu-id="51f19-117">Etype name.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-118">**SAP**</span><span class="sxs-lookup"><span data-stu-id="51f19-118">**Sap**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-119">Valor SAP.</span><span class="sxs-lookup"><span data-stu-id="51f19-119">SAP value.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-120">**LowProtocol**</span><span class="sxs-lookup"><span data-stu-id="51f19-120">**LowProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-121">Índice do protocolo encontrado.</span><span class="sxs-lookup"><span data-stu-id="51f19-121">Index of protocol found.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-122">**LowProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="51f19-122">**LowProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-123">Deslocamento para os dados de protocolo obtidos de **LowProtocol**.</span><span class="sxs-lookup"><span data-stu-id="51f19-123">Offset to protocol data obtained from **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-124">**HighPort**</span><span class="sxs-lookup"><span data-stu-id="51f19-124">**HighPort**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-125">Porta de protocolo alto identificado em **LowProtocol**.</span><span class="sxs-lookup"><span data-stu-id="51f19-125">Port of high protocol identified in **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="51f19-126">**HighProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="51f19-126">**HighProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="51f19-127">Deslocamento para os dados de protocolo obtidos de **HighPort**.</span><span class="sxs-lookup"><span data-stu-id="51f19-127">Offset to protocol data obtained from **HighPort**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51f19-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51f19-128">Requirements</span></span>



| <span data-ttu-id="51f19-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="51f19-129">Requirement</span></span> | <span data-ttu-id="51f19-130">Valor</span><span class="sxs-lookup"><span data-stu-id="51f19-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="51f19-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51f19-131">Minimum supported client</span></span><br/> | <span data-ttu-id="51f19-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51f19-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="51f19-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51f19-133">Minimum supported server</span></span><br/> | <span data-ttu-id="51f19-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51f19-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="51f19-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="51f19-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="51f19-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="51f19-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




