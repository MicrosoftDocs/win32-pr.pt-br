---
description: Notifica um AppBar quando um aplicativo de tela inteira está abrindo ou fechando. Essa notificação é enviada na forma de uma mensagem definida pelo aplicativo que é definida pela \_ nova mensagem ABM.
title: Mensagem de ABN_FULLSCREENAPP (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090034"
---
# <a name="abn_fullscreenapp-message"></a><span data-ttu-id="96fda-104">\_Mensagem FULLSCREENAPP do ABN</span><span class="sxs-lookup"><span data-stu-id="96fda-104">ABN\_FULLSCREENAPP message</span></span>

<span data-ttu-id="96fda-105">Notifica um AppBar quando um aplicativo de tela inteira está abrindo ou fechando.</span><span class="sxs-lookup"><span data-stu-id="96fda-105">Notifies an appbar when a full-screen application is opening or closing.</span></span> <span data-ttu-id="96fda-106">Essa notificação é enviada na forma de uma mensagem definida pelo aplicativo que é definida pela nova mensagem [**ABM \_**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="96fda-106">This notification is sent in the form of an application-defined message that is set by the [**ABM\_NEW**](abm-new.md) message.</span></span>


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a><span data-ttu-id="96fda-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96fda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96fda-108">*fOpen*</span><span class="sxs-lookup"><span data-stu-id="96fda-108">*fOpen*</span></span> 
</dt> <dd>

<span data-ttu-id="96fda-109">Um sinalizador que especifica se um aplicativo de tela inteira está abrindo ou fechando.</span><span class="sxs-lookup"><span data-stu-id="96fda-109">A flag specifying whether a full-screen application is opening or closing.</span></span> <span data-ttu-id="96fda-110">Esse parâmetro será **true** se o aplicativo estiver sendo aberto ou **false** se estiver fechando.</span><span class="sxs-lookup"><span data-stu-id="96fda-110">This parameter is **TRUE** if the application is opening or **FALSE** if it is closing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96fda-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96fda-111">Return value</span></span>

<span data-ttu-id="96fda-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="96fda-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96fda-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="96fda-113">Remarks</span></span>

<span data-ttu-id="96fda-114">Quando um aplicativo de tela inteira está abrindo, um AppBar deve ser solto na parte inferior da ordem z.</span><span class="sxs-lookup"><span data-stu-id="96fda-114">When a full-screen application is opening, an appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="96fda-115">Quando estiver fechando, o AppBar deverá restaurar sua posição de ordem z.</span><span class="sxs-lookup"><span data-stu-id="96fda-115">When it is closing, the appbar should restore its z-order position.</span></span>

## <a name="requirements"></a><span data-ttu-id="96fda-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96fda-116">Requirements</span></span>



| <span data-ttu-id="96fda-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="96fda-117">Requirement</span></span> | <span data-ttu-id="96fda-118">Valor</span><span class="sxs-lookup"><span data-stu-id="96fda-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96fda-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96fda-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96fda-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="96fda-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96fda-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96fda-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96fda-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96fda-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96fda-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96fda-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="96fda-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="96fda-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




