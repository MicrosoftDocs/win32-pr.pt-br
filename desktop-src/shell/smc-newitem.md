---
description: Notifica sobre um novo item, conforme especificado pela estrutura SMDATA que o acompanha.
title: Mensagem de SMC_NEWITEM (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e0ccf2db-cb46-469f-bc08-4b5100a410ba
api_name:
- SMC_NEWITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ebd8f1b6454a2fb592374b860811ebfc7a14f09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968052"
---
# <a name="smc_newitem-message"></a><span data-ttu-id="aef5a-103">Mensagem do SMC \_ NEWITEM</span><span class="sxs-lookup"><span data-stu-id="aef5a-103">SMC\_NEWITEM message</span></span>

<span data-ttu-id="aef5a-104">Notifica sobre um novo item, conforme especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="aef5a-104">Notifies you of a new item, as specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_NEWITEM
            
```



## <a name="parameters"></a><span data-ttu-id="aef5a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aef5a-105">Parameters</span></span>

<span data-ttu-id="aef5a-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aef5a-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aef5a-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aef5a-107">Return value</span></span>

<span data-ttu-id="aef5a-108">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aef5a-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="aef5a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="aef5a-109">Remarks</span></span>

<span data-ttu-id="aef5a-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="aef5a-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef5a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aef5a-111">Requirements</span></span>



| <span data-ttu-id="aef5a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="aef5a-112">Requirement</span></span> | <span data-ttu-id="aef5a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="aef5a-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aef5a-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aef5a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="aef5a-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aef5a-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aef5a-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aef5a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="aef5a-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aef5a-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aef5a-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aef5a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="aef5a-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aef5a-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="aef5a-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="aef5a-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aef5a-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aef5a-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




