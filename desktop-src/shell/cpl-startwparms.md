---
description: Enviado para notificar CPlApplet que o usuário escolheu o ícone associado a uma determinada caixa de diálogo. CPlApplet deve exibir a caixa de diálogo correspondente e executar qualquer tarefa especificada pelo usuário.
title: Mensagem de CPL_STARTWPARMS (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920752"
---
# <a name="cpl_startwparms-message"></a><span data-ttu-id="d4350-104">CPL \_ mensagem STARTWPARMS</span><span class="sxs-lookup"><span data-stu-id="d4350-104">CPL\_STARTWPARMS message</span></span>

<span data-ttu-id="d4350-105">Enviado para notificar [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que o usuário escolheu o ícone associado a uma determinada caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d4350-105">Sent to notify [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) that the user has chosen the icon associated with a given dialog box.</span></span> <span data-ttu-id="d4350-106">**CPlApplet** deve exibir a caixa de diálogo correspondente e executar qualquer tarefa especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d4350-106">**CPlApplet** should display the corresponding dialog box and carry out any user-specified tasks.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4350-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4350-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4350-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="d4350-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="d4350-109">O número da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d4350-109">The dialog box number.</span></span> <span data-ttu-id="d4350-110">Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**CPL \_ GetCount**](cpl-getcount.md) (CPL \_ GetCount – 1).</span><span class="sxs-lookup"><span data-stu-id="d4350-110">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="d4350-111">*lpszExtra*</span><span class="sxs-lookup"><span data-stu-id="d4350-111">*lpszExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="d4350-112">Uma cadeia de caracteres com direções adicionais para execução.</span><span class="sxs-lookup"><span data-stu-id="d4350-112">A string with additional directions for execution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4350-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4350-113">Return value</span></span>

<span data-ttu-id="d4350-114">Retornará **true** se a mensagem tiver sido tratada ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d4350-114">Returns **TRUE** if the message was handled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4350-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4350-115">Remarks</span></span>

<span data-ttu-id="d4350-116">**CPL \_ STARTWPARMS** é semelhante a [**CPL \_ DBLCLK**](cpl-dblclk.md) , mas permite que você passe uma cadeia de caracteres para [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) em vez de um **int**. Você pode usar essa cadeia de caracteres como uma maneira flexível de fornecer instruções detalhadas para execução.</span><span class="sxs-lookup"><span data-stu-id="d4350-116">**CPL\_STARTWPARMS** is similar to [**CPL\_DBLCLK**](cpl-dblclk.md) but allows you to pass a string to [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) instead of an **int**. You can use this string as a flexible way to provide detailed directions for execution.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4350-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4350-117">Requirements</span></span>



| <span data-ttu-id="d4350-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4350-118">Requirement</span></span> | <span data-ttu-id="d4350-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d4350-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4350-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4350-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d4350-121">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d4350-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="d4350-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4350-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d4350-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4350-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d4350-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4350-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4350-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4350-125"><dt>Cpl.h</dt></span></span> </dl> |



 

 
