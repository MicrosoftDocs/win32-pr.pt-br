---
title: Mensagem de LVM_GETTILEVIEWINFO (commctrl. h)
description: Recupera informações sobre um controle de exibição de lista no modo de exibição de bloco.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- Controles de LVM_GETTILEVIEWINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe1f34da560d539a9ae12cc7a065b2bf37bc3c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645020"
---
# <a name="lvm_gettileviewinfo-message"></a><span data-ttu-id="e877d-104">\_Mensagem GETTILEVIEWINFO LVM</span><span class="sxs-lookup"><span data-stu-id="e877d-104">LVM\_GETTILEVIEWINFO message</span></span>

<span data-ttu-id="e877d-105">Recupera informações sobre um controle de exibição de lista no modo de exibição de bloco.</span><span class="sxs-lookup"><span data-stu-id="e877d-105">Retrieves information about a list-view control in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="e877d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e877d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e877d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e877d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e877d-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e877d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e877d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e877d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e877d-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> que recebe as informações recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e877d-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e877d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e877d-111">Return value</span></span>

<span data-ttu-id="e877d-112">Valor de retorno não usado.</span><span class="sxs-lookup"><span data-stu-id="e877d-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e877d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e877d-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e877d-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="e877d-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e877d-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e877d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e877d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e877d-116">Requirements</span></span>



| <span data-ttu-id="e877d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e877d-117">Requirement</span></span> | <span data-ttu-id="e877d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e877d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e877d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e877d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e877d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e877d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e877d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e877d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e877d-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e877d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e877d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e877d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e877d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e877d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





