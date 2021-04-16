---
title: Mensagem de HDN_ITEMSTATEICONCLICK (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário clicou no ícone de estado de um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- Controles de HDN_ITEMSTATEICONCLICK de mensagens do Windows
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455961"
---
# <a name="hdn_itemstateiconclick-message"></a><span data-ttu-id="de381-105">\_Mensagem HDN ITEMSTATEICONCLICK</span><span class="sxs-lookup"><span data-stu-id="de381-105">HDN\_ITEMSTATEICONCLICK message</span></span>

<span data-ttu-id="de381-106">Notifica uma janela pai do controle de cabeçalho que o usuário clicou no ícone de estado de um item.</span><span class="sxs-lookup"><span data-stu-id="de381-106">Notifies a header control's parent window that the user clicked an item's state icon.</span></span> <span data-ttu-id="de381-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="de381-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="de381-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de381-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de381-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de381-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de381-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações adicionais sobre o ícone de estado que foi clicado.</span><span class="sxs-lookup"><span data-stu-id="de381-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the state icon that was clicked on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de381-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de381-111">Return value</span></span>

<span data-ttu-id="de381-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="de381-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="de381-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de381-113">Requirements</span></span>



| <span data-ttu-id="de381-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de381-114">Requirement</span></span> | <span data-ttu-id="de381-115">Valor</span><span class="sxs-lookup"><span data-stu-id="de381-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de381-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de381-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de381-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de381-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de381-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de381-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de381-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de381-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de381-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de381-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de381-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de381-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





