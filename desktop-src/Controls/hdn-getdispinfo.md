---
title: HDN_GETDISPINFO código de notificação (commctrl. h)
description: Enviado ao proprietário de um controle de cabeçalho quando o controle precisa de informações sobre um item de cabeçalho de retorno de chamada. Esse código de notificação é enviado como uma \_ mensagem de notificação do WM.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008941"
---
# <a name="hdn_getdispinfo-notification-code"></a><span data-ttu-id="9752d-105">Código de notificação do HDN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="9752d-105">HDN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="9752d-106">Enviado ao proprietário de um controle de cabeçalho quando o controle precisa de informações sobre um item de cabeçalho de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9752d-106">Sent to the owner of a header control when the control needs information about a callback header item.</span></span> <span data-ttu-id="9752d-107">Esse código de notificação é enviado como uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9752d-107">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9752d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9752d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9752d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9752d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9752d-110">Um ponteiro para uma estrutura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9752d-110">A pointer to an [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure.</span></span> <span data-ttu-id="9752d-111">Na entrada, os campos da estrutura especificam quais informações são necessárias e o item de interesse.</span><span class="sxs-lookup"><span data-stu-id="9752d-111">On input, the fields of the structure specify what information is required and the item of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9752d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9752d-112">Return value</span></span>

<span data-ttu-id="9752d-113">Retorna um LRESULT.</span><span class="sxs-lookup"><span data-stu-id="9752d-113">Returns an LRESULT.</span></span>

## <a name="remarks"></a><span data-ttu-id="9752d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9752d-114">Remarks</span></span>

<span data-ttu-id="9752d-115">Preencha os membros apropriados da estrutura para retornar as informações solicitadas ao controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9752d-115">Fill the appropriate members of the structure to return the requested information to the header control.</span></span> <span data-ttu-id="9752d-116">Se o manipulador de mensagens definir o membro **Mask** da estrutura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) para HDI \_ di \_ SETITEM, o controle de cabeçalho armazenará as informações e não a solicitará novamente.</span><span class="sxs-lookup"><span data-stu-id="9752d-116">If your message handler sets the **mask** member of the [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure to HDI\_DI\_SETITEM, the header control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="9752d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9752d-117">Requirements</span></span>



| <span data-ttu-id="9752d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9752d-118">Requirement</span></span> | <span data-ttu-id="9752d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9752d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9752d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9752d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9752d-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9752d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9752d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9752d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9752d-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9752d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9752d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9752d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9752d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9752d-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9752d-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9752d-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9752d-127">**HDN \_ GETDISPINFOW** (Unicode) e **HDN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9752d-127">**HDN\_GETDISPINFOW** (Unicode) and **HDN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





