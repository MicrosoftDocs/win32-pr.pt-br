---
description: Envia a notificação de que os menus foram completamente atualizados e você pode redefinir seu estado.
title: Mensagem de SMC_REFRESH (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aab18245c6502d4d3424e6ed6727eceb5a329d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829099"
---
# <a name="smc_refresh-message"></a><span data-ttu-id="99e7d-103">Mensagem de atualização do SMC \_</span><span class="sxs-lookup"><span data-stu-id="99e7d-103">SMC\_REFRESH message</span></span>

<span data-ttu-id="99e7d-104">Envia a notificação de que os menus foram completamente atualizados e você pode redefinir seu estado.</span><span class="sxs-lookup"><span data-stu-id="99e7d-104">Sends notification that the menus have completely refreshed and you can reset your state.</span></span>


```C++
SMC_REFRESH
            
```



## <a name="parameters"></a><span data-ttu-id="99e7d-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99e7d-105">Parameters</span></span>

<span data-ttu-id="99e7d-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="99e7d-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99e7d-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99e7d-107">Return value</span></span>

<span data-ttu-id="99e7d-108">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99e7d-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e7d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="99e7d-109">Remarks</span></span>

<span data-ttu-id="99e7d-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="99e7d-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="99e7d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99e7d-111">Requirements</span></span>



| <span data-ttu-id="99e7d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="99e7d-112">Requirement</span></span> | <span data-ttu-id="99e7d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="99e7d-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99e7d-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99e7d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="99e7d-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99e7d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="99e7d-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99e7d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="99e7d-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99e7d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99e7d-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99e7d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="99e7d-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99e7d-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="99e7d-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="99e7d-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99e7d-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99e7d-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




