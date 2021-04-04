---
title: Mensagem de LVM_SETTILEVIEWINFO (commctrl. h)
description: Define informações que um controle de exibição de lista usa no modo de exibição de bloco.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- Controles de LVM_SETTILEVIEWINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085399"
---
# <a name="lvm_settileviewinfo-message"></a><span data-ttu-id="6f2da-104">\_Mensagem SETTILEVIEWINFO LVM</span><span class="sxs-lookup"><span data-stu-id="6f2da-104">LVM\_SETTILEVIEWINFO message</span></span>

<span data-ttu-id="6f2da-105">Define informações que um controle de exibição de lista usa no modo de exibição de bloco.</span><span class="sxs-lookup"><span data-stu-id="6f2da-105">Sets information that a list-view control uses in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f2da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f2da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f2da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f2da-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f2da-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6f2da-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f2da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f2da-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6f2da-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> que contém as informações a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="6f2da-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f2da-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f2da-111">Return value</span></span>

<span data-ttu-id="6f2da-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6f2da-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f2da-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f2da-113">Remarks</span></span>

<span data-ttu-id="6f2da-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="6f2da-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6f2da-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6f2da-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f2da-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f2da-116">Requirements</span></span>



| <span data-ttu-id="6f2da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f2da-117">Requirement</span></span> | <span data-ttu-id="6f2da-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6f2da-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f2da-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f2da-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f2da-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f2da-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f2da-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f2da-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f2da-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6f2da-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f2da-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f2da-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f2da-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f2da-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





