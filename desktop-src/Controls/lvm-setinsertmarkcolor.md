---
title: Mensagem de LVM_SETINSERTMARKCOLOR (commctrl. h)
description: Define a cor do ponto de inserção.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- Controles de LVM_SETINSERTMARKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917990"
---
# <a name="lvm_setinsertmarkcolor-message"></a><span data-ttu-id="76d9e-104">\_Mensagem SETINSERTMARKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="76d9e-104">LVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="76d9e-105">Define a cor do ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="76d9e-105">Sets the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="76d9e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76d9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d9e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76d9e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="76d9e-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="76d9e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="76d9e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76d9e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="76d9e-110">Estrutura **COLORREF** que especifica a cor para definir o ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="76d9e-110">**COLORREF** structure that specifies the color to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d9e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76d9e-111">Return value</span></span>

<span data-ttu-id="76d9e-112">Retorna a estrutura **COLORREF** definida como a cor anterior.</span><span class="sxs-lookup"><span data-stu-id="76d9e-112">Returns **COLORREF** structure set to the previous color.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d9e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="76d9e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="76d9e-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="76d9e-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="76d9e-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="76d9e-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="76d9e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76d9e-116">Requirements</span></span>



| <span data-ttu-id="76d9e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="76d9e-117">Requirement</span></span> | <span data-ttu-id="76d9e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="76d9e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76d9e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76d9e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="76d9e-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76d9e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76d9e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76d9e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="76d9e-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76d9e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76d9e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76d9e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d9e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76d9e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





