---
title: DTN_FORMATQUERY código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) para recuperar o tamanho máximo permitido da cadeia de caracteres que será exibida em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918037"
---
# <a name="dtn_formatquery-notification-code"></a><span data-ttu-id="2d641-105">Código de notificação do DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="2d641-105">DTN\_FORMATQUERY notification code</span></span>

<span data-ttu-id="2d641-106">Enviado por um controle do seletor de data e hora (DTP) para recuperar o tamanho máximo permitido da cadeia de caracteres que será exibida em um campo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="2d641-106">Sent by a date and time picker (DTP) control to retrieve the maximum allowable size of the string that will be displayed in a callback field.</span></span> <span data-ttu-id="2d641-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2d641-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2d641-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d641-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d641-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d641-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d641-110">Um ponteiro para uma estrutura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) que contém informações sobre o campo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="2d641-110">A pointer to an [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure containing information about the callback field.</span></span> <span data-ttu-id="2d641-111">A estrutura contém uma subcadeia de caracteres que define um campo de retorno de chamada e recebe o tamanho máximo permitido da cadeia de caracteres que será exibida no campo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="2d641-111">The structure contains a substring that defines a callback field and receives the maximum allowable size of the string that will be displayed in the callback field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d641-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d641-112">Return value</span></span>

<span data-ttu-id="2d641-113">O proprietário do controle deve calcular a largura máxima possível do texto que será exibido no campo de retorno de chamada, definir o membro **szMax** da estrutura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) e retornar zero.</span><span class="sxs-lookup"><span data-stu-id="2d641-113">The owner of the control must calculate the maximum possible width of the text that will be displayed in the callback field, set the **szMax** member of the [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure, and return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d641-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d641-114">Remarks</span></span>

<span data-ttu-id="2d641-115">Manipular esse código de notificação prepara o controle para ajustar o tamanho máximo da cadeia de caracteres que será exibida em um campo de retorno de chamada específico.</span><span class="sxs-lookup"><span data-stu-id="2d641-115">Handling this notification code prepares the control to adjust for the maximum size of the string that will be displayed in a particular callback field.</span></span> <span data-ttu-id="2d641-116">Isso permite que o controle exiba corretamente a saída em todos os momentos, reduzindo a cintilação dentro da exibição do controle.</span><span class="sxs-lookup"><span data-stu-id="2d641-116">This enables the control to properly display output at all times, reducing flicker within the control's display.</span></span> <span data-ttu-id="2d641-117">(Para obter informações adicionais sobre campos de retorno de chamada, consulte [campos de retorno de chamada](date-and-time-picker-controls.md).)</span><span class="sxs-lookup"><span data-stu-id="2d641-117">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="2d641-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d641-118">Requirements</span></span>



| <span data-ttu-id="2d641-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d641-119">Requirement</span></span> | <span data-ttu-id="2d641-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2d641-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d641-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d641-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2d641-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d641-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d641-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d641-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2d641-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d641-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d641-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d641-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d641-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d641-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2d641-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2d641-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2d641-128">**DTN \_ FORMATQUERYW** (Unicode) e **DTN \_ FORMATQUERYA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2d641-128">**DTN\_FORMATQUERYW** (Unicode) and **DTN\_FORMATQUERYA** (ANSI)</span></span><br/>           |



 

 





