---
description: Solicita se é aceitável descartar um objeto de dados no item especificado pela estrutura SMDATA que o acompanha.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Mensagem de SMC_SFDDRESTRICTED (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968049"
---
# <a name="smc_sfddrestricted-message"></a><span data-ttu-id="31465-103">Mensagem do SMC \_ SFDDRESTRICTED</span><span class="sxs-lookup"><span data-stu-id="31465-103">SMC\_SFDDRESTRICTED message</span></span>

<span data-ttu-id="31465-104">Solicita se é aceitável descartar um objeto de dados no item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="31465-104">Requests whether it is acceptable to drop a data object on the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a><span data-ttu-id="31465-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31465-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31465-106">*pDropTarget*</span><span class="sxs-lookup"><span data-stu-id="31465-106">*pDropTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="31465-107">O endereço de um ponteiro void que recebe um ponteiro para a interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="31465-107">The address of a void pointer that receives a pointer to your [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span> <span data-ttu-id="31465-108">Defina esse valor como **NULL** se você não quiser aceitar o objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="31465-108">Set this value to **NULL** if you do not want to accept the data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31465-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31465-109">Return value</span></span>

<span data-ttu-id="31465-110">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31465-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="31465-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="31465-111">Remarks</span></span>

<span data-ttu-id="31465-112">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="31465-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="31465-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31465-113">Requirements</span></span>



| <span data-ttu-id="31465-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="31465-114">Requirement</span></span> | <span data-ttu-id="31465-115">Valor</span><span class="sxs-lookup"><span data-stu-id="31465-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31465-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31465-116">Minimum supported client</span></span><br/> | <span data-ttu-id="31465-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31465-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31465-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31465-118">Minimum supported server</span></span><br/> | <span data-ttu-id="31465-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31465-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31465-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31465-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="31465-121"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31465-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="31465-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="31465-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31465-123"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31465-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
