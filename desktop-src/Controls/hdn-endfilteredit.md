---
title: HDN_ENDFILTEREDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que uma edição de filtro terminou. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d3832875-4cde-4d8a-b3a4-a8dae0742c56
keywords:
- HDN_ENDFILTEREDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ENDFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a557278598600f1bd11ebfbe791691de954a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645277"
---
# <a name="hdn_endfilteredit-notification-code"></a><span data-ttu-id="43a7e-105">Código de notificação do HDN \_ ENDFILTEREDIT</span><span class="sxs-lookup"><span data-stu-id="43a7e-105">HDN\_ENDFILTEREDIT notification code</span></span>

<span data-ttu-id="43a7e-106">Notifica uma janela pai do controle de cabeçalho que uma edição de filtro terminou.</span><span class="sxs-lookup"><span data-stu-id="43a7e-106">Notifies a header control's parent window that a filter edit has ended.</span></span> <span data-ttu-id="43a7e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="43a7e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="43a7e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43a7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a7e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43a7e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43a7e-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações adicionais sobre o filtro que está sendo editado.</span><span class="sxs-lookup"><span data-stu-id="43a7e-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a7e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43a7e-111">Return value</span></span>

<span data-ttu-id="43a7e-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="43a7e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a7e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a7e-113">Requirements</span></span>



| <span data-ttu-id="43a7e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a7e-114">Requirement</span></span> | <span data-ttu-id="43a7e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="43a7e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43a7e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a7e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43a7e-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43a7e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43a7e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a7e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43a7e-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43a7e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43a7e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43a7e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a7e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a7e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





