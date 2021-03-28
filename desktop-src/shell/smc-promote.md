---
description: Promova o item especificado pela estrutura SMDATA que o acompanha.
title: Mensagem de SMC_PROMOTE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b1208673-06b4-42b2-b4ac-872fd22927df
api_name:
- SMC_PROMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 22718e51d6ef1bf7e3c5652741b95cadb4db9937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968050"
---
# <a name="smc_promote-message"></a><span data-ttu-id="a0a70-103">Mensagem de promoção do SMC \_</span><span class="sxs-lookup"><span data-stu-id="a0a70-103">SMC\_PROMOTE message</span></span>

<span data-ttu-id="a0a70-104">Promova o item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="a0a70-104">Promote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_PROMOTE
```



## <a name="parameters"></a><span data-ttu-id="a0a70-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0a70-105">Parameters</span></span>

<span data-ttu-id="a0a70-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a0a70-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0a70-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0a70-107">Return value</span></span>

<span data-ttu-id="a0a70-108">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0a70-108">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a70-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0a70-109">Remarks</span></span>

<span data-ttu-id="a0a70-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="a0a70-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a70-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0a70-111">Requirements</span></span>



| <span data-ttu-id="a0a70-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0a70-112">Requirement</span></span> | <span data-ttu-id="a0a70-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a0a70-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a70-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0a70-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a70-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0a70-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a0a70-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0a70-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a70-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0a70-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0a70-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0a70-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0a70-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0a70-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0a70-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="a0a70-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0a70-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0a70-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




