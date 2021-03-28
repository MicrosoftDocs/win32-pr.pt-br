---
description: Rebaixar o item especificado pela estrutura SMDATA que o acompanha.
title: Mensagem de SMC_DEMOTE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 46e5505571402feec24d81a9184b713e1c61ae0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989027"
---
# <a name="smc_demote-message"></a><span data-ttu-id="1e160-103">\_Mensagem de rebaixamento do SMC</span><span class="sxs-lookup"><span data-stu-id="1e160-103">SMC\_DEMOTE message</span></span>

<span data-ttu-id="1e160-104">Rebaixar o item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="1e160-104">Demote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a><span data-ttu-id="1e160-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e160-105">Parameters</span></span>

<span data-ttu-id="1e160-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1e160-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e160-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e160-107">Return value</span></span>

<span data-ttu-id="1e160-108">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e160-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e160-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e160-109">Remarks</span></span>

<span data-ttu-id="1e160-110">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="1e160-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e160-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e160-111">Requirements</span></span>



| <span data-ttu-id="1e160-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e160-112">Requirement</span></span> | <span data-ttu-id="1e160-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1e160-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e160-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e160-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1e160-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e160-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1e160-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e160-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1e160-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e160-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e160-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1e160-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e160-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e160-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e160-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="1e160-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e160-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e160-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




