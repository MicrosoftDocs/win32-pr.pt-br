---
title: Método IOrpcDebugNotify ClientFillBuffer
description: Envia dados do depurador do cliente para o depurador do servidor.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- Método COM de ClientFillBuffer
- Método ClientFillBuffer COM, interface IOrpcDebugNotify
- IOrpcDebugNotify interface COM, método ClientFillBuffer
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645201"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a><span data-ttu-id="f9440-106">Método IOrpcDebugNotify:: ClientFillBuffer</span><span class="sxs-lookup"><span data-stu-id="f9440-106">IOrpcDebugNotify::ClientFillBuffer method</span></span>

<span data-ttu-id="f9440-107">Envia dados do depurador do cliente para o depurador do servidor.</span><span class="sxs-lookup"><span data-stu-id="f9440-107">Sends data from the client debugger to the server debugger.</span></span>

> [!Note]  
> <span data-ttu-id="f9440-108">Uma biblioteca de importação que contém a função **ClientFillBuffer** não está incluída no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f9440-108">An import library containing the **ClientFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f9440-109">Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll e fornecer essa função por meio da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f9440-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f9440-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9440-110">Syntax</span></span>


```C++
void ClientFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="f9440-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9440-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9440-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="f9440-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="f9440-113">Um ponteiro para uma estrutura [**ORPC \_ DBG \_ All**](orpc-dbg-all.md) que contém informações específicas de notificação que o sistema RPC com passa para o depurador.</span><span class="sxs-lookup"><span data-stu-id="f9440-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9440-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9440-114">Return value</span></span>

<span data-ttu-id="f9440-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f9440-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9440-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9440-116">Requirements</span></span>



| <span data-ttu-id="f9440-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9440-117">Requirement</span></span> | <span data-ttu-id="f9440-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f9440-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f9440-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9440-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9440-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9440-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="f9440-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9440-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9440-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9440-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f9440-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f9440-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9440-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="f9440-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="f9440-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="f9440-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9440-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="f9440-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9440-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9440-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9440-128">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="f9440-128">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="f9440-129">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="f9440-129">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

