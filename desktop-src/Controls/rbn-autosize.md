---
title: RBN_AUTOSIZE código de notificação (commctrl. h)
description: Enviado por um controle rebar criado com o estilo de AUTOSIZE do RBS \_ quando o rebar é redimensionado automaticamente. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749072"
---
# <a name="rbn_autosize-notification-code"></a><span data-ttu-id="aee52-105">Código de notificação do RBN \_ AUTOSIZE</span><span class="sxs-lookup"><span data-stu-id="aee52-105">RBN\_AUTOSIZE notification code</span></span>

<span data-ttu-id="aee52-106">Enviado por um controle rebar criado com o estilo de [**\_ AUTOSIZE do RBS**](rebar-control-styles.md) quando o rebar é redimensionado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="aee52-106">Sent by a rebar control created with the [**RBS\_AUTOSIZE**](rebar-control-styles.md) style when the rebar automatically resizes itself.</span></span> <span data-ttu-id="aee52-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aee52-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="aee52-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aee52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee52-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aee52-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aee52-110">Ponteiro para uma estrutura [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) que contém informações sobre a operação de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="aee52-110">Pointer to an [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) structure that contains information about the resize operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aee52-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aee52-111">Return value</span></span>

<span data-ttu-id="aee52-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="aee52-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee52-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aee52-113">Requirements</span></span>



| <span data-ttu-id="aee52-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee52-114">Requirement</span></span> | <span data-ttu-id="aee52-115">Valor</span><span class="sxs-lookup"><span data-stu-id="aee52-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aee52-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee52-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aee52-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aee52-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aee52-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee52-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aee52-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aee52-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aee52-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aee52-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee52-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aee52-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





