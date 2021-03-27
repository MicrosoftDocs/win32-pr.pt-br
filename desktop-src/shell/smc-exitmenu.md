---
description: Notifica que o menu está sendo recolhido.
title: Mensagem de SMC_EXITMENU (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 868b4819-1dbf-497a-9c79-5935f503969a
api_name:
- SMC_EXITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9a8680617a17ce0069a8633e1c70ff6b32a4be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922065"
---
# <a name="smc_exitmenu-message"></a><span data-ttu-id="111bb-103">Mensagem do SMC \_ EXITMENU</span><span class="sxs-lookup"><span data-stu-id="111bb-103">SMC\_EXITMENU message</span></span>

<span data-ttu-id="111bb-104">Notifica que o menu está sendo recolhido.</span><span class="sxs-lookup"><span data-stu-id="111bb-104">Notifies you that the menu is collapsing.</span></span>


```C++
SMC_EXITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="111bb-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="111bb-105">Parameters</span></span>

<span data-ttu-id="111bb-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="111bb-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="111bb-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="111bb-107">Return value</span></span>

<span data-ttu-id="111bb-108">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="111bb-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="111bb-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="111bb-109">Remarks</span></span>

<span data-ttu-id="111bb-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="111bb-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="111bb-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="111bb-111">Requirements</span></span>



| <span data-ttu-id="111bb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="111bb-112">Requirement</span></span> | <span data-ttu-id="111bb-113">Valor</span><span class="sxs-lookup"><span data-stu-id="111bb-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="111bb-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="111bb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="111bb-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="111bb-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="111bb-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="111bb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="111bb-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="111bb-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="111bb-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="111bb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="111bb-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="111bb-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="111bb-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="111bb-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="111bb-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="111bb-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




