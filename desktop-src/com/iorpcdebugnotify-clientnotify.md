---
title: Método IOrpcDebugNotify ClientNotify
description: Informa ao cliente uma solicitação de depuração de saída para o servidor.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Método COM de ClientNotify
- Método ClientNotify COM, interface IOrpcDebugNotify
- IOrpcDebugNotify interface COM, método ClientNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455971"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a><span data-ttu-id="4c90f-106">Método IOrpcDebugNotify:: ClientNotify</span><span class="sxs-lookup"><span data-stu-id="4c90f-106">IOrpcDebugNotify::ClientNotify method</span></span>

<span data-ttu-id="4c90f-107">Informa ao cliente uma solicitação de depuração de saída para o servidor.</span><span class="sxs-lookup"><span data-stu-id="4c90f-107">Informs the client of an outgoing debugger request to the server.</span></span>

> [!Note]  
> <span data-ttu-id="4c90f-108">Uma biblioteca de importação que contém a função **ClientNotify** não está incluída no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4c90f-108">An import library containing the **ClientNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4c90f-109">Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll e fornecer essa função por meio da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="4c90f-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4c90f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c90f-110">Syntax</span></span>


```C++
void ClientNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="4c90f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c90f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c90f-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="4c90f-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="4c90f-113">Um ponteiro para uma estrutura [**ORPC \_ DBG \_ All**](orpc-dbg-all.md) que contém informações específicas de notificação que o sistema RPC com passa para o depurador.</span><span class="sxs-lookup"><span data-stu-id="4c90f-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c90f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c90f-114">Return value</span></span>

<span data-ttu-id="4c90f-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4c90f-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c90f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c90f-116">Requirements</span></span>



| <span data-ttu-id="4c90f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c90f-117">Requirement</span></span> | <span data-ttu-id="4c90f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4c90f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="4c90f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c90f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c90f-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c90f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="4c90f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c90f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4c90f-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c90f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4c90f-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4c90f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c90f-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="4c90f-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="4c90f-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="4c90f-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c90f-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="4c90f-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c90f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c90f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c90f-128">**\_argumentos de inicialização ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="4c90f-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="4c90f-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="4c90f-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="4c90f-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="4c90f-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

