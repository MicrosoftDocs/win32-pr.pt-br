---
description: Notifica você para inicializar a banda do menu.
title: Mensagem de SMC_INITMENU (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 415ee805-2b57-4f8f-85d9-2b38cd05998d
api_name:
- SMC_INITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ed7f7be1786192fb2be42f6d36cfb4bf222136fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170313"
---
# <a name="smc_initmenu-message"></a><span data-ttu-id="6e6f9-103">Mensagem do SMC \_ INITMENU</span><span class="sxs-lookup"><span data-stu-id="6e6f9-103">SMC\_INITMENU message</span></span>

<span data-ttu-id="6e6f9-104">Notifica você para inicializar a banda do menu.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-104">Notifies you to initialize the menu band.</span></span>


```C++
SMC_INITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="6e6f9-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e6f9-105">Parameters</span></span>

<span data-ttu-id="6e6f9-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e6f9-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e6f9-107">Return value</span></span>

<span data-ttu-id="6e6f9-108">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e6f9-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e6f9-109">Remarks</span></span>

<span data-ttu-id="6e6f9-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="6e6f9-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e6f9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e6f9-111">Requirements</span></span>



| <span data-ttu-id="6e6f9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e6f9-112">Requirement</span></span> | <span data-ttu-id="6e6f9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6e6f9-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6f9-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e6f9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6e6f9-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e6f9-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6e6f9-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e6f9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6e6f9-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e6f9-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e6f9-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e6f9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e6f9-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e6f9-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e6f9-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="6e6f9-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e6f9-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e6f9-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




