---
title: Mensagem de LVM_ISGROUPVIEWENABLED (commctrl. h)
description: Verifica se o controle de exibição de lista tem a exibição de grupo habilitada.
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- Controles de LVM_ISGROUPVIEWENABLED de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f7af79a1b0594ba6ebb100c1c975f09898d35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918961"
---
# <a name="lvm_isgroupviewenabled-message"></a><span data-ttu-id="22b16-104">\_Mensagem ISGROUPVIEWENABLED LVM</span><span class="sxs-lookup"><span data-stu-id="22b16-104">LVM\_ISGROUPVIEWENABLED message</span></span>

<span data-ttu-id="22b16-105">Verifica se o controle de exibição de lista tem a exibição de grupo habilitada.</span><span class="sxs-lookup"><span data-stu-id="22b16-105">Checks whether the list-view control has group view enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="22b16-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22b16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b16-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22b16-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="22b16-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="22b16-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="22b16-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22b16-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="22b16-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="22b16-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b16-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22b16-111">Return value</span></span>

<span data-ttu-id="22b16-112">Retornará **true** se a exibição de grupo estiver habilitada ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="22b16-112">Returns **TRUE** if group view is enabled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="22b16-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="22b16-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="22b16-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="22b16-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="22b16-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22b16-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22b16-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22b16-116">Requirements</span></span>



| <span data-ttu-id="22b16-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="22b16-117">Requirement</span></span> | <span data-ttu-id="22b16-118">Valor</span><span class="sxs-lookup"><span data-stu-id="22b16-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22b16-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22b16-119">Minimum supported client</span></span><br/> | <span data-ttu-id="22b16-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22b16-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22b16-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22b16-121">Minimum supported server</span></span><br/> | <span data-ttu-id="22b16-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22b16-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22b16-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22b16-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="22b16-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b16-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





