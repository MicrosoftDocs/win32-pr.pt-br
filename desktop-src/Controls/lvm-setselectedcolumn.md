---
title: Mensagem de LVM_SETSELECTEDCOLUMN (commctrl. h)
description: Define o índice da coluna selecionada.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- Controles de LVM_SETSELECTEDCOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824865"
---
# <a name="lvm_setselectedcolumn-message"></a><span data-ttu-id="2a3bf-104">\_Mensagem SETSELECTEDCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="2a3bf-104">LVM\_SETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="2a3bf-105">Define o índice da coluna selecionada.</span><span class="sxs-lookup"><span data-stu-id="2a3bf-105">Sets the index of the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a3bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a3bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a3bf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a3bf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2a3bf-108">Valor do tipo **int** que especifica o índice de coluna.</span><span class="sxs-lookup"><span data-stu-id="2a3bf-108">Value of type **int** that specifies the column index.</span></span></dd> <dt>

<span data-ttu-id="2a3bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a3bf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2a3bf-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2a3bf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a3bf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a3bf-111">Return value</span></span>

<span data-ttu-id="2a3bf-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="2a3bf-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a3bf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a3bf-113">Remarks</span></span>

<span data-ttu-id="2a3bf-114">Os índices de coluna são armazenados em uma matriz **int** .</span><span class="sxs-lookup"><span data-stu-id="2a3bf-114">The column indices are stored in an **int** array.</span></span> <span data-ttu-id="2a3bf-115">Consulte o membro **puColumns** de [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span><span class="sxs-lookup"><span data-stu-id="2a3bf-115">See the **puColumns** member of [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span></span>

> [!Note]  
> <span data-ttu-id="2a3bf-116">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="2a3bf-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2a3bf-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2a3bf-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2a3bf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a3bf-118">Requirements</span></span>



| <span data-ttu-id="2a3bf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a3bf-119">Requirement</span></span> | <span data-ttu-id="2a3bf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2a3bf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3bf-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3bf-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a3bf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a3bf-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3bf-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a3bf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a3bf-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a3bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a3bf-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a3bf-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





