---
title: Estrutura de ORPC_INIT_ARGS
description: A \_ estrutura ORPC Init \_ args contém informações usadas para inicializar a depuração remota usando a interface IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- COM ORPC_INIT_ARGS estrutura COM
- COM ponteiro de estrutura de LPORPC_INIT_ARGS COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085351"
---
# <a name="orpc_init_args-structure"></a><span data-ttu-id="67845-105">\_Estrutura de \_ argumentos init ORPC</span><span class="sxs-lookup"><span data-stu-id="67845-105">ORPC\_INIT\_ARGS structure</span></span>

<span data-ttu-id="67845-106">A estrutura **ORPC \_ init \_ args** contém informações usadas para inicializar a depuração remota usando a interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="67845-106">The **ORPC\_INIT\_ARGS** structure contains information used to initialize remote debugging using the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="67845-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67845-107">Syntax</span></span>


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a><span data-ttu-id="67845-108">Membros</span><span class="sxs-lookup"><span data-stu-id="67845-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="67845-109">**lpIntfOrpcDebug**</span><span class="sxs-lookup"><span data-stu-id="67845-109">**lpIntfOrpcDebug**</span></span>
</dt> <dd>

<span data-ttu-id="67845-110">Um ponteiro para a interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) para uso por depuradores em processo.</span><span class="sxs-lookup"><span data-stu-id="67845-110">A pointer to the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface for use by in-process debuggers.</span></span> <span data-ttu-id="67845-111">Se o depurador não estiver em processo ou for um sistema Macintosh, esse campo deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="67845-111">If the debugger is not in-process or is a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="67845-112">**pvPSN**</span><span class="sxs-lookup"><span data-stu-id="67845-112">**pvPSN**</span></span>
</dt> <dd>

<span data-ttu-id="67845-113">Um ponteiro para o número de série do processo do Macintosh do processo do depurador.</span><span class="sxs-lookup"><span data-stu-id="67845-113">A pointer to the Macintosh process serial number of the debuggee's process.</span></span> <span data-ttu-id="67845-114">Se o depurado não for um sistema Macintosh, esse campo deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="67845-114">If the debuggee is not a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="67845-115">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="67845-115">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="67845-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="67845-116">Reserved.</span></span> <span data-ttu-id="67845-117">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="67845-117">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="67845-118">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="67845-118">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="67845-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="67845-119">Reserved.</span></span> <span data-ttu-id="67845-120">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="67845-120">Must be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67845-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67845-121">Requirements</span></span>



| <span data-ttu-id="67845-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="67845-122">Requirement</span></span> | <span data-ttu-id="67845-123">Valor</span><span class="sxs-lookup"><span data-stu-id="67845-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="67845-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67845-124">Minimum supported client</span></span><br/> | <span data-ttu-id="67845-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="67845-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="67845-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67845-126">Minimum supported server</span></span><br/> | <span data-ttu-id="67845-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="67845-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="67845-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="67845-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="67845-129"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="67845-129"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67845-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="67845-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67845-131">**ORPC \_ DBG \_ All**</span><span class="sxs-lookup"><span data-stu-id="67845-131">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="67845-132">**\_buffer de DBG ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="67845-132">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="67845-133">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="67845-133">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="67845-134">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="67845-134">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





