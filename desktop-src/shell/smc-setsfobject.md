---
description: Notifica você para salvar o objeto passado.
title: Mensagem de SMC_SETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170312"
---
# <a name="smc_setsfobject-message"></a><span data-ttu-id="ebf18-103">Mensagem do SMC \_ SETSFOBJECT</span><span class="sxs-lookup"><span data-stu-id="ebf18-103">SMC\_SETSFOBJECT message</span></span>

<span data-ttu-id="ebf18-104">Notifica você para salvar o objeto passado.</span><span class="sxs-lookup"><span data-stu-id="ebf18-104">Notifies you to save the passed object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="ebf18-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebf18-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf18-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="ebf18-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf18-107">O IID associado ao objeto.</span><span class="sxs-lookup"><span data-stu-id="ebf18-107">The IID associated with the object.</span></span>

</dd> <dt>

<span data-ttu-id="ebf18-108">*PV*</span><span class="sxs-lookup"><span data-stu-id="ebf18-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf18-109">Um ponteiro da interface no objeto especificado por *IID*.</span><span class="sxs-lookup"><span data-stu-id="ebf18-109">A pointer the interface on the object specified by *iid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf18-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebf18-110">Return value</span></span>

<span data-ttu-id="ebf18-111">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ebf18-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf18-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebf18-112">Remarks</span></span>

<span data-ttu-id="ebf18-113">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="ebf18-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

<span data-ttu-id="ebf18-114">A notificação do **SMC \_ SETSFOBJECT** é usada com o fluxo de IID \_ .</span><span class="sxs-lookup"><span data-stu-id="ebf18-114">The **SMC\_SETSFOBJECT** notification is used with IID\_Stream.</span></span> <span data-ttu-id="ebf18-115">O objeto é salvo em um formulário persistente no registro e nada é feito com a contagem de referência no objeto passado.</span><span class="sxs-lookup"><span data-stu-id="ebf18-115">The object is saved into a persisted form in the registry and nothing is done with the reference count on the object passed in.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf18-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebf18-116">Requirements</span></span>



| <span data-ttu-id="ebf18-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebf18-117">Requirement</span></span> | <span data-ttu-id="ebf18-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ebf18-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf18-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf18-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf18-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ebf18-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ebf18-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf18-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf18-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ebf18-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ebf18-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ebf18-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebf18-124"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf18-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebf18-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="ebf18-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ebf18-126"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ebf18-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




