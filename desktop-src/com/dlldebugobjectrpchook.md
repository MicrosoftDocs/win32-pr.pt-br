---
title: Função DllDebugObjectRPCHook
description: Exportado por DLLs COM para habilitar a depuração remota.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- COM função DllDebugObjectRPCHook
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812261"
---
# <a name="dlldebugobjectrpchook-function"></a><span data-ttu-id="f1588-104">Função DllDebugObjectRPCHook</span><span class="sxs-lookup"><span data-stu-id="f1588-104">DllDebugObjectRPCHook function</span></span>

<span data-ttu-id="f1588-105">Exportado por DLLs COM para habilitar a depuração remota.</span><span class="sxs-lookup"><span data-stu-id="f1588-105">Exported by COM DLLs to enable remote debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1588-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1588-106">Syntax</span></span>


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a><span data-ttu-id="f1588-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1588-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1588-108">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="f1588-108">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="f1588-109">Se for **true**, a depuração remota será habilitada.</span><span class="sxs-lookup"><span data-stu-id="f1588-109">If **TRUE**, remote debugging is enabled.</span></span> <span data-ttu-id="f1588-110">Se for **false**, a depuração remota não estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="f1588-110">If **FALSE**, remote debugging is not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="f1588-111">*lpOrpcInitArgs*</span><span class="sxs-lookup"><span data-stu-id="f1588-111">*lpOrpcInitArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="f1588-112">Um ponteiro para uma estrutura [**ORPC \_ init \_ args**](orpc-init-args.md) .</span><span class="sxs-lookup"><span data-stu-id="f1588-112">A pointer to an [**ORPC\_INIT\_ARGS**](orpc-init-args.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1588-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1588-113">Return value</span></span>

<span data-ttu-id="f1588-114">**True** se for bem-sucedido; caso contrário, **false**</span><span class="sxs-lookup"><span data-stu-id="f1588-114">**TRUE** if successful, **FALSE** otherwise</span></span>

## <a name="requirements"></a><span data-ttu-id="f1588-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1588-115">Requirements</span></span>



| <span data-ttu-id="f1588-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1588-116">Requirement</span></span> | <span data-ttu-id="f1588-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f1588-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1588-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1588-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f1588-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1588-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f1588-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1588-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f1588-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1588-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f1588-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f1588-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1588-123"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="f1588-123"><dt>N/A</dt></span></span> </dl>       |
| <span data-ttu-id="f1588-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1588-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1588-125"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1588-125"><dt>Ole32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f1588-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f1588-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1588-127"><dt>Ole32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1588-127"><dt>Ole32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1588-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1588-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1588-129">**ORPC \_ DBG \_ All**</span><span class="sxs-lookup"><span data-stu-id="f1588-129">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="f1588-130">**\_buffer de DBG ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="f1588-130">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="f1588-131">**\_argumentos de inicialização ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="f1588-131">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="f1588-132">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="f1588-132">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





