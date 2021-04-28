---
description: Mensagem de SMC_GETOBJECT-solicita um ponteiro para um objeto especificado.
title: Mensagem de SMC_GETOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58741290d741cc18fd788282d0f302ef87bb15dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100434"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="62712-103">Mensagem do SMC \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="62712-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="62712-104">Solicita um ponteiro para um objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="62712-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="62712-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62712-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62712-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="62712-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="62712-107">O IID associado ao objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="62712-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="62712-108">*PV*</span><span class="sxs-lookup"><span data-stu-id="62712-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="62712-109">Um ponteiro void que recebe um ponteiro para a interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="62712-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62712-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="62712-110">Return value</span></span>

<span data-ttu-id="62712-111">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62712-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="62712-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="62712-112">Remarks</span></span>

<span data-ttu-id="62712-113">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="62712-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="62712-114">Crie o objeto solicitado e atribua um ponteiro à interface solicitada para *VP*.</span><span class="sxs-lookup"><span data-stu-id="62712-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="62712-115">As interfaces a seguir podem ser solicitadas.</span><span class="sxs-lookup"><span data-stu-id="62712-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="62712-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="62712-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="62712-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="62712-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="62712-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="62712-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="62712-119">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="62712-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="62712-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62712-120">Requirements</span></span>



| <span data-ttu-id="62712-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="62712-121">Requirement</span></span> | <span data-ttu-id="62712-122">Valor</span><span class="sxs-lookup"><span data-stu-id="62712-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62712-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62712-123">Minimum supported client</span></span><br/> | <span data-ttu-id="62712-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="62712-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="62712-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62712-125">Minimum supported server</span></span><br/> | <span data-ttu-id="62712-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="62712-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62712-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="62712-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="62712-128"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62712-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="62712-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="62712-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62712-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62712-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
