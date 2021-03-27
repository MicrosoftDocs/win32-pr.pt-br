---
description: Enviado para a função CPlApplet de um aplicativo de painel de controle para recuperar o número de caixas de diálogo com suporte no aplicativo.
title: Mensagem de CPL_GETCOUNT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501435"
---
# <a name="cpl_getcount-message"></a><span data-ttu-id="fcf68-103">\_Mensagem de SQLcount do CPL</span><span class="sxs-lookup"><span data-stu-id="fcf68-103">CPL\_GETCOUNT message</span></span>

<span data-ttu-id="fcf68-104">Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo de painel de controle para recuperar o número de caixas de diálogo com suporte no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fcf68-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to retrieve the number of dialog boxes supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcf68-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcf68-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf68-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcf68-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fcf68-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fcf68-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fcf68-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcf68-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fcf68-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fcf68-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf68-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcf68-110">Return value</span></span>

<span data-ttu-id="fcf68-111">A função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) retorna o número de caixas de diálogo que o aplicativo do painel de controle suporta.</span><span class="sxs-lookup"><span data-stu-id="fcf68-111">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function returns the number of dialog boxes that the Control Panel application supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcf68-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcf68-112">Remarks</span></span>

<span data-ttu-id="fcf68-113">Essa mensagem é enviada imediatamente após a mensagem de [**\_ init de CPL**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="fcf68-113">This message is sent immediately after the [**CPL\_INIT**](cpl-init.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf68-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcf68-114">Requirements</span></span>



| <span data-ttu-id="fcf68-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcf68-115">Requirement</span></span> | <span data-ttu-id="fcf68-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fcf68-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fcf68-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcf68-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf68-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fcf68-118">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fcf68-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcf68-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf68-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fcf68-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fcf68-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fcf68-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcf68-122"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf68-122"><dt>Cpl.h</dt></span></span> </dl> |



 

 
