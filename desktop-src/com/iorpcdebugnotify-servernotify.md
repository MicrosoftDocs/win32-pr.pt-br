---
title: Método IOrpcDebugNotify ServerNotify
description: Informa ao servidor de uma solicitação de entrada do depurador do cliente.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- Método COM de ServerNotify
- Método ServerNotify COM, interface IOrpcDebugNotify
- IOrpcDebugNotify interface COM, método ServerNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6dab7cf68b305e83212045851a88e1cdecdde9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919130"
---
# <a name="iorpcdebugnotifyservernotify-method"></a><span data-ttu-id="488ed-106">Método IOrpcDebugNotify:: ServerNotify</span><span class="sxs-lookup"><span data-stu-id="488ed-106">IOrpcDebugNotify::ServerNotify method</span></span>

<span data-ttu-id="488ed-107">Informa ao servidor de uma solicitação de entrada do depurador do cliente.</span><span class="sxs-lookup"><span data-stu-id="488ed-107">Informs the server of an incoming debugger request from the client.</span></span>

> [!Note]  
> <span data-ttu-id="488ed-108">Uma biblioteca de importação que contém a função **ServerNotify** não está incluída no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="488ed-108">An import library containing the **ServerNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="488ed-109">Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll e fornecer essa função por meio da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="488ed-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="488ed-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="488ed-110">Syntax</span></span>


```C++
void ServerNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="488ed-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="488ed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="488ed-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="488ed-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="488ed-113">Um ponteiro para uma estrutura [**ORPC \_ DBG \_ All**](orpc-dbg-all.md) que contém informações específicas de notificação que o sistema RPC com passa para o depurador.</span><span class="sxs-lookup"><span data-stu-id="488ed-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="488ed-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="488ed-114">Return value</span></span>

<span data-ttu-id="488ed-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="488ed-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="488ed-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="488ed-116">Requirements</span></span>



| <span data-ttu-id="488ed-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="488ed-117">Requirement</span></span> | <span data-ttu-id="488ed-118">Valor</span><span class="sxs-lookup"><span data-stu-id="488ed-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="488ed-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="488ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="488ed-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="488ed-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="488ed-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="488ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="488ed-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="488ed-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="488ed-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="488ed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="488ed-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="488ed-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="488ed-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="488ed-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="488ed-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="488ed-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="488ed-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="488ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488ed-128">**\_argumentos de inicialização ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="488ed-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="488ed-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="488ed-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="488ed-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="488ed-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

