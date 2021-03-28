---
description: O usuário clicou em uma divisa para expandir o item especificado pela estrutura SMDATA que o acompanha.
title: Mensagem de SMC_CHEVRONEXPAND (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6ecf8f86e111326b3f37f3111c382d2d04ef2fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170318"
---
# <a name="smc_chevronexpand-message"></a><span data-ttu-id="968d8-103">Mensagem do SMC \_ CHEVRONEXPAND</span><span class="sxs-lookup"><span data-stu-id="968d8-103">SMC\_CHEVRONEXPAND message</span></span>

<span data-ttu-id="968d8-104">O usuário clicou em uma divisa para expandir o item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="968d8-104">The user has clicked a chevron to expand the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a><span data-ttu-id="968d8-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="968d8-105">Parameters</span></span>

<span data-ttu-id="968d8-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="968d8-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="968d8-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="968d8-107">Return value</span></span>

<span data-ttu-id="968d8-108">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="968d8-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="968d8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="968d8-109">Remarks</span></span>

<span data-ttu-id="968d8-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="968d8-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="968d8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="968d8-111">Requirements</span></span>



| <span data-ttu-id="968d8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="968d8-112">Requirement</span></span> | <span data-ttu-id="968d8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="968d8-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="968d8-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="968d8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="968d8-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="968d8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="968d8-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="968d8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="968d8-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="968d8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="968d8-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="968d8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="968d8-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="968d8-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="968d8-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="968d8-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="968d8-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="968d8-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




