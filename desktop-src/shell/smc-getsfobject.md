---
description: Solicita um ponteiro para um objeto especificado.
title: Mensagem de SMC_GETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c7fb57ea8e3f02ce4e773e187310530c14d65515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170314"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="95a4f-103">Mensagem do SMC \_ GETSFOBJECT</span><span class="sxs-lookup"><span data-stu-id="95a4f-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="95a4f-104">Solicita um ponteiro para um objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="95a4f-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="95a4f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95a4f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95a4f-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="95a4f-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="95a4f-107">O IID associado ao objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="95a4f-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="95a4f-108">*PV*</span><span class="sxs-lookup"><span data-stu-id="95a4f-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="95a4f-109">Um ponteiro void que recebe um ponteiro para a interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="95a4f-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95a4f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95a4f-110">Return value</span></span>

<span data-ttu-id="95a4f-111">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95a4f-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="95a4f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="95a4f-112">Remarks</span></span>

<span data-ttu-id="95a4f-113">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="95a4f-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="95a4f-114">É semelhante ao [**SMC \_ GetObject**](smc-getobject.md) , mas usado para itens de pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="95a4f-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="95a4f-115">Crie o objeto solicitado e atribua um ponteiro à interface solicitada para *VP*.</span><span class="sxs-lookup"><span data-stu-id="95a4f-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="95a4f-116">As interfaces a seguir podem ser solicitadas.</span><span class="sxs-lookup"><span data-stu-id="95a4f-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="95a4f-117">**IStream**</span><span class="sxs-lookup"><span data-stu-id="95a4f-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="95a4f-118">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="95a4f-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="95a4f-119">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="95a4f-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="95a4f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a4f-120">Requirements</span></span>



| <span data-ttu-id="95a4f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a4f-121">Requirement</span></span> | <span data-ttu-id="95a4f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="95a4f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95a4f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95a4f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95a4f-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95a4f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="95a4f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95a4f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95a4f-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95a4f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95a4f-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="95a4f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="95a4f-128"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95a4f-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="95a4f-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="95a4f-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95a4f-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95a4f-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
