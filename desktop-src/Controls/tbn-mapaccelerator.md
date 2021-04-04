---
title: TBN_MAPACCELERATOR código de notificação (commctrl. h)
description: Solicita o índice do botão na barra de ferramentas correspondente ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917980"
---
# <a name="tbn_mapaccelerator-notification-code"></a><span data-ttu-id="e4a65-105">Código de notificação do TBN \_ MAPACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="e4a65-105">TBN\_MAPACCELERATOR notification code</span></span>

<span data-ttu-id="e4a65-106">Solicita o índice do botão na barra de ferramentas correspondente ao caractere de acelerador especificado.</span><span class="sxs-lookup"><span data-stu-id="e4a65-106">Requests the index of the button in the toolbar corresponding to the specified accelerator character.</span></span> <span data-ttu-id="e4a65-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e4a65-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e4a65-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4a65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4a65-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4a65-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4a65-110">Um ponteiro para uma estrutura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contém o caractere de tecla acelerador e que recebe o índice do botão correspondente.</span><span class="sxs-lookup"><span data-stu-id="e4a65-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains the accelerator key character and that receives the index of the corresponding button.</span></span> <span data-ttu-id="e4a65-111">O campo **dwItemNext** será-1 se o acelerador não corresponder a um comando.</span><span class="sxs-lookup"><span data-stu-id="e4a65-111">The **dwItemNext** field is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4a65-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4a65-112">Return value</span></span>

<span data-ttu-id="e4a65-113">TRUE se **NMCHAR. dwItemNext** for definido como um valor.</span><span class="sxs-lookup"><span data-stu-id="e4a65-113">TRUE if **NMCHAR.dwItemNext** is set to a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a65-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4a65-114">Requirements</span></span>



| <span data-ttu-id="e4a65-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4a65-115">Requirement</span></span> | <span data-ttu-id="e4a65-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e4a65-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a65-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a65-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a65-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4a65-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4a65-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a65-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a65-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4a65-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4a65-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4a65-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a65-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a65-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





