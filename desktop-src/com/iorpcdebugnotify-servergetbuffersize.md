---
title: Método IOrpcDebugNotify ServerGetBufferSize
description: Recupera o tamanho do buffer RPC do depurador do lado do servidor.
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- Método COM de ServerGetBufferSize
- Método ServerGetBufferSize COM, interface IOrpcDebugNotify
- IOrpcDebugNotify interface COM, método ServerGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d461670cc65f5cfcb433a52529e724a1c54bede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919180"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a><span data-ttu-id="b5519-106">Método IOrpcDebugNotify:: ServerGetBufferSize</span><span class="sxs-lookup"><span data-stu-id="b5519-106">IOrpcDebugNotify::ServerGetBufferSize method</span></span>

<span data-ttu-id="b5519-107">Recupera o tamanho do buffer RPC do depurador do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="b5519-107">Retrieves the RPC buffer size from the server-side debugger.</span></span>

> [!Note]  
> <span data-ttu-id="b5519-108">Uma biblioteca de importação que contém a função **ServerGetBufferSize** não está incluída no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b5519-108">An import library containing the **ServerGetBufferSize** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b5519-109">Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll e fornecer essa função por meio da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="b5519-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b5519-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5519-110">Syntax</span></span>


```C++
void ServerGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="b5519-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5519-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5519-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="b5519-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="b5519-113">Um ponteiro para uma estrutura [**ORPC \_ DBG \_ All**](orpc-dbg-all.md) que contém informações específicas de notificação que o sistema RPC com passa para o depurador.</span><span class="sxs-lookup"><span data-stu-id="b5519-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5519-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5519-114">Return value</span></span>

<span data-ttu-id="b5519-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b5519-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5519-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5519-116">Requirements</span></span>



| <span data-ttu-id="b5519-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5519-117">Requirement</span></span> | <span data-ttu-id="b5519-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b5519-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b5519-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5519-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5519-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5519-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="b5519-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5519-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5519-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5519-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b5519-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b5519-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5519-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="b5519-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="b5519-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="b5519-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5519-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="b5519-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5519-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5519-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5519-128">**\_argumentos de inicialização ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="b5519-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="b5519-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="b5519-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="b5519-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="b5519-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

