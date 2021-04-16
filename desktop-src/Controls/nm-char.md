---
title: NM_CHAR código de notificação (commctrl. h)
description: O código de notificação do NM \_ Char é enviado por um controle quando uma chave de caractere é processada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750309"
---
# <a name="nm_char-notification-code"></a><span data-ttu-id="b0c70-105">Código de notificação do NM \_ Char</span><span class="sxs-lookup"><span data-stu-id="b0c70-105">NM\_CHAR notification code</span></span>

<span data-ttu-id="b0c70-106">O código de notificação do NM \_ Char é enviado por um controle quando uma chave de caractere é processada.</span><span class="sxs-lookup"><span data-stu-id="b0c70-106">The NM\_CHAR notification code is sent by a control when a character key is processed.</span></span> <span data-ttu-id="b0c70-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b0c70-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b0c70-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0c70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0c70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0c70-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0c70-110">Um ponteiro para uma estrutura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contém informações adicionais sobre o caractere que causou o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="b0c70-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0c70-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0c70-111">Return value</span></span>

<span data-ttu-id="b0c70-112">O valor de retorno é ignorado pela maioria dos controles.</span><span class="sxs-lookup"><span data-stu-id="b0c70-112">The return value is ignored by most controls.</span></span> <span data-ttu-id="b0c70-113">Para obter mais informações, consulte a documentação para os controles individuais.</span><span class="sxs-lookup"><span data-stu-id="b0c70-113">For more information, see the documentation for the individual controls.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0c70-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0c70-114">Requirements</span></span>



| <span data-ttu-id="b0c70-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0c70-115">Requirement</span></span> | <span data-ttu-id="b0c70-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b0c70-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c70-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0c70-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c70-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0c70-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0c70-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0c70-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c70-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0c70-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0c70-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0c70-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0c70-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0c70-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0c70-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0c70-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c70-124">NM \_ Char (barra de ferramentas)</span><span class="sxs-lookup"><span data-stu-id="b0c70-124">NM\_CHAR (toolbar)</span></span>](nm-char-toolbar.md)
</dt> </dl>

 

 





