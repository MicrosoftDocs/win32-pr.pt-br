---
title: TTN_LINKCLICK código de notificação (commctrl. h)
description: Enviado quando um link de texto dentro de uma dica de ferramenta de balão é clicado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753563"
---
# <a name="ttn_linkclick-notification-code"></a><span data-ttu-id="db9f8-105">Código de notificação do TTN \_ LINKCLICK</span><span class="sxs-lookup"><span data-stu-id="db9f8-105">TTN\_LINKCLICK notification code</span></span>

<span data-ttu-id="db9f8-106">Enviado quando um link de texto dentro de uma dica de ferramenta de balão é clicado.</span><span class="sxs-lookup"><span data-stu-id="db9f8-106">Sent when a text link inside a balloon tooltip is clicked.</span></span> <span data-ttu-id="db9f8-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="db9f8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a><span data-ttu-id="db9f8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db9f8-108">Parameters</span></span>

<span data-ttu-id="db9f8-109">Este código de notificação não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="db9f8-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db9f8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db9f8-110">Return value</span></span>

<span data-ttu-id="db9f8-111">Valor de retorno não usado.</span><span class="sxs-lookup"><span data-stu-id="db9f8-111">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9f8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="db9f8-112">Remarks</span></span>

<span data-ttu-id="db9f8-113">Veja a seguir um exemplo de quando essa notificação é enviada.</span><span class="sxs-lookup"><span data-stu-id="db9f8-113">Following is an example of when this notification is sent.</span></span> <span data-ttu-id="db9f8-114">Suponha que a dica de ferramenta de balão contenha o seguinte texto, "Este é um <A>link</A>".</span><span class="sxs-lookup"><span data-stu-id="db9f8-114">Assume that your balloon tooltip contains the following text, "This is a <A>link</A>".</span></span> <span data-ttu-id="db9f8-115">Quando o "link" é clicado, o controle ToolTip envia um \_ código de notificação TTN LINKCLICK.</span><span class="sxs-lookup"><span data-stu-id="db9f8-115">When "link" is clicked, the tooltip control sends a TTN\_LINKCLICK notification code.</span></span>

> [!Note]  
> <span data-ttu-id="db9f8-116">Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="db9f8-116">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="db9f8-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="db9f8-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db9f8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db9f8-118">Requirements</span></span>



| <span data-ttu-id="db9f8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="db9f8-119">Requirement</span></span> | <span data-ttu-id="db9f8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="db9f8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db9f8-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db9f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="db9f8-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db9f8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db9f8-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db9f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="db9f8-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db9f8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db9f8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db9f8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9f8-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db9f8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





