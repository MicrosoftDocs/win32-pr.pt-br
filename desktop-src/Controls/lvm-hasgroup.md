---
title: Mensagem de LVM_HASGROUP (commctrl. h)
description: Determina se o controle de exibição de lista tem um grupo especificado.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- Controles de LVM_HASGROUP de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455741"
---
# <a name="lvm_hasgroup-message"></a><span data-ttu-id="6e660-104">\_Mensagem HASGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="6e660-104">LVM\_HASGROUP message</span></span>

<span data-ttu-id="6e660-105">Determina se o controle de exibição de lista tem um grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="6e660-105">Determines whether the list-view control has a specified group.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e660-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e660-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e660-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e660-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e660-108">ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="6e660-108">ID of the group.</span></span></dd> <dt>

<span data-ttu-id="6e660-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e660-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6e660-110">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6e660-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e660-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e660-111">Return value</span></span>

<span data-ttu-id="6e660-112">Retornará **true** se o controle de exibição de lista tiver o grupo especificado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6e660-112">Returns **TRUE** if the list-view control has the specified group, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e660-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e660-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6e660-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="6e660-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6e660-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6e660-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6e660-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e660-116">Requirements</span></span>



| <span data-ttu-id="6e660-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e660-117">Requirement</span></span> | <span data-ttu-id="6e660-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6e660-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e660-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e660-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6e660-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e660-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e660-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e660-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6e660-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e660-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e660-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e660-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e660-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e660-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





