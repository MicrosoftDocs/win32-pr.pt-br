---
title: TCN_GETOBJECT código de notificação (commctrl. h)
description: Enviado por um controle guia quando ele tem o \_ \_ estilo estendido REGISTERDROP de TCS e um objeto é arrastado sobre um item de guia no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750935"
---
# <a name="tcn_getobject-notification-code"></a><span data-ttu-id="9affd-105">Código de notificação do TCN \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="9affd-105">TCN\_GETOBJECT notification code</span></span>

<span data-ttu-id="9affd-106">Enviado por um controle guia quando ele tem o estilo estendido [**\_ \_ REGISTERDROP de TCS**](tab-control-extended-styles.md) e um objeto é arrastado sobre um item de guia no controle.</span><span class="sxs-lookup"><span data-stu-id="9affd-106">Sent by a tab control when it has the [**TCS\_EX\_REGISTERDROP**](tab-control-extended-styles.md) extended style and an object is dragged over a tab item in the control.</span></span> <span data-ttu-id="9affd-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9affd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9affd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9affd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9affd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9affd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9affd-110">Ponteiro para uma estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contém informações sobre o item de guia no qual o objeto é arrastado e recebe dados que o aplicativo retorna em resposta a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="9affd-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the tab item the object is dragged over and receives data the application returns in response to this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9affd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9affd-111">Return value</span></span>

<span data-ttu-id="9affd-112">O aplicativo que processa esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="9affd-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9affd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9affd-113">Requirements</span></span>



| <span data-ttu-id="9affd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9affd-114">Requirement</span></span> | <span data-ttu-id="9affd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9affd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9affd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9affd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9affd-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9affd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9affd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9affd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9affd-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9affd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9affd-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9affd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9affd-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9affd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





