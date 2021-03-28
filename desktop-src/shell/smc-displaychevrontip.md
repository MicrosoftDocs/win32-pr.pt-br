---
description: Notifica que um InfoTip está prestes a ser exibido para a divisa associada ao item especificado pela estrutura SMDATA que o acompanha.
title: Mensagem de SMC_DISPLAYCHEVRONTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461256"
---
# <a name="smc_displaychevrontip-message"></a><span data-ttu-id="81126-103">Mensagem do SMC \_ DISPLAYCHEVRONTIP</span><span class="sxs-lookup"><span data-stu-id="81126-103">SMC\_DISPLAYCHEVRONTIP message</span></span>

<span data-ttu-id="81126-104">Notifica que um InfoTip está prestes a ser exibido para a divisa associada ao item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="81126-104">Notifies you that an infotip is about to be displayed for the chevron associated with the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a><span data-ttu-id="81126-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81126-105">Parameters</span></span>

<span data-ttu-id="81126-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="81126-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81126-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81126-107">Return value</span></span>

<span data-ttu-id="81126-108">Retornar S \_ OK para exibir o InfoTip.</span><span class="sxs-lookup"><span data-stu-id="81126-108">Return S\_OK to display the infotip.</span></span> <span data-ttu-id="81126-109">Retornar S \_ false para impedir que InfoTip seja exibido.</span><span class="sxs-lookup"><span data-stu-id="81126-109">Return S\_FALSE to prevent the infotip from being displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="81126-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="81126-110">Remarks</span></span>

<span data-ttu-id="81126-111">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="81126-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="81126-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81126-112">Requirements</span></span>



| <span data-ttu-id="81126-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="81126-113">Requirement</span></span> | <span data-ttu-id="81126-114">Valor</span><span class="sxs-lookup"><span data-stu-id="81126-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81126-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81126-115">Minimum supported client</span></span><br/> | <span data-ttu-id="81126-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81126-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="81126-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81126-117">Minimum supported server</span></span><br/> | <span data-ttu-id="81126-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81126-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81126-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81126-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="81126-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81126-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="81126-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="81126-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81126-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81126-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




