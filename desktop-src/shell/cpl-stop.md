---
description: Enviado para a função CPlApplet de um aplicativo de painel de controle quando o controle de aplicativo do painel de controle é fechado. O aplicativo de controle envia a mensagem uma vez para cada caixa de diálogo à qual o aplicativo dá suporte.
title: Mensagem de CPL_STOP (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967347"
---
# <a name="cpl_stop-message"></a><span data-ttu-id="c21b0-104">CPL \_ mensagem de parada</span><span class="sxs-lookup"><span data-stu-id="c21b0-104">CPL\_STOP message</span></span>

<span data-ttu-id="c21b0-105">Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo de painel de controle quando o controle de aplicativo do painel de controle é fechado.</span><span class="sxs-lookup"><span data-stu-id="c21b0-105">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the controlling application of the Control Panel closes.</span></span> <span data-ttu-id="c21b0-106">O aplicativo de controle envia a mensagem uma vez para cada caixa de diálogo à qual o aplicativo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="c21b0-106">The controlling application sends the message once for each dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="c21b0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c21b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c21b0-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="c21b0-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="c21b0-109">O número da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c21b0-109">The dialog box number.</span></span>

</dd> <dt>

<span data-ttu-id="c21b0-110">*lData*</span><span class="sxs-lookup"><span data-stu-id="c21b0-110">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="c21b0-111">O valor que o aplicativo do painel de controle carregou no membro **lpData** da estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c21b0-111">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="c21b0-112">O aplicativo carrega o membro **lpData** em resposta à mensagem [**CPL de \_ consulta**](cpl-inquire.md) ou [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="c21b0-112">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c21b0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c21b0-113">Return value</span></span>

<span data-ttu-id="c21b0-114">Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, ela deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="c21b0-114">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c21b0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c21b0-115">Remarks</span></span>

<span data-ttu-id="c21b0-116">Em resposta a essa mensagem, um aplicativo do painel de controle deve executar a limpeza para a caixa de diálogo especificada.</span><span class="sxs-lookup"><span data-stu-id="c21b0-116">In response to this message, a Control Panel application must perform cleanup for the given dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c21b0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c21b0-117">Requirements</span></span>



| <span data-ttu-id="c21b0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c21b0-118">Requirement</span></span> | <span data-ttu-id="c21b0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c21b0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c21b0-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c21b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c21b0-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c21b0-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c21b0-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c21b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c21b0-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c21b0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c21b0-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c21b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c21b0-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c21b0-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c21b0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c21b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c21b0-127">**CPL de \_ saída**</span><span class="sxs-lookup"><span data-stu-id="c21b0-127">**CPL\_EXIT**</span></span>](cpl-exit.md)
</dt> <dt>

[<span data-ttu-id="c21b0-128">**CPL \_ GETcount**</span><span class="sxs-lookup"><span data-stu-id="c21b0-128">**CPL\_GETCOUNT**</span></span>](cpl-getcount.md)
</dt> </dl>

 

 
