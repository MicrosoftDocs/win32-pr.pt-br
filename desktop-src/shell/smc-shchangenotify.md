---
description: Notifica-o de que uma alteração foi feita.
title: Mensagem de SMC_SHCHANGENOTIFY (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 258a885ddaf61b45df1cfff9f9c77ce37a233dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967963"
---
# <a name="smc_shchangenotify-message"></a><span data-ttu-id="08ed3-103">Mensagem do SMC \_ SHCHANGENOTIFY</span><span class="sxs-lookup"><span data-stu-id="08ed3-103">SMC\_SHCHANGENOTIFY message</span></span>

<span data-ttu-id="08ed3-104">Notifica-o de que uma alteração foi feita.</span><span class="sxs-lookup"><span data-stu-id="08ed3-104">Notifies you that a change has taken place.</span></span>


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a><span data-ttu-id="08ed3-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08ed3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ed3-106">*psmc*</span><span class="sxs-lookup"><span data-stu-id="08ed3-106">*psmc*</span></span> 
</dt> <dd>

<span data-ttu-id="08ed3-107">Um ponteiro para uma estrutura [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) com informações sobre a alteração.</span><span class="sxs-lookup"><span data-stu-id="08ed3-107">A pointer to an [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) structure with information on the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ed3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08ed3-108">Return value</span></span>

<span data-ttu-id="08ed3-109">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08ed3-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="08ed3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="08ed3-110">Remarks</span></span>

<span data-ttu-id="08ed3-111">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="08ed3-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="08ed3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08ed3-112">Requirements</span></span>



| <span data-ttu-id="08ed3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="08ed3-113">Requirement</span></span> | <span data-ttu-id="08ed3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="08ed3-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08ed3-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08ed3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="08ed3-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="08ed3-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="08ed3-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08ed3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="08ed3-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="08ed3-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08ed3-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="08ed3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="08ed3-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08ed3-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="08ed3-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="08ed3-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="08ed3-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08ed3-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




