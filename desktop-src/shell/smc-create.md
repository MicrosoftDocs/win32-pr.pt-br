---
description: Notifica que uma banda de menu foi criada.
title: Mensagem de SMC_CREATE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 59219f376288431fa20e198d8c427ff40c7fba62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989029"
---
# <a name="smc_create-message"></a><span data-ttu-id="f6c4f-103">\_Criar mensagem do SMC</span><span class="sxs-lookup"><span data-stu-id="f6c4f-103">SMC\_CREATE message</span></span>

<span data-ttu-id="f6c4f-104">Notifica que uma banda de menu foi criada.</span><span class="sxs-lookup"><span data-stu-id="f6c4f-104">Notifies you that a menu band has been created.</span></span>


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a><span data-ttu-id="f6c4f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6c4f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c4f-106">*psmd*</span><span class="sxs-lookup"><span data-stu-id="f6c4f-106">*psmd*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c4f-107">Um ponteiro para o membro **pvUserData** de uma estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="f6c4f-107">A pointer to the **pvUserData** member of an [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c4f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6c4f-108">Return value</span></span>

<span data-ttu-id="f6c4f-109">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f6c4f-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c4f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6c4f-110">Remarks</span></span>

<span data-ttu-id="f6c4f-111">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="f6c4f-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c4f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6c4f-112">Requirements</span></span>



| <span data-ttu-id="f6c4f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c4f-113">Requirement</span></span> | <span data-ttu-id="f6c4f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f6c4f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c4f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c4f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c4f-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6c4f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f6c4f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c4f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c4f-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6c4f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f6c4f-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f6c4f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c4f-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6c4f-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6c4f-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="f6c4f-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6c4f-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6c4f-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




