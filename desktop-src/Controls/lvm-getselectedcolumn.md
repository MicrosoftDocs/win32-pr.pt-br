---
title: Mensagem de LVM_GETSELECTEDCOLUMN (commctrl. h)
description: Recupera um inteiro que especifica a coluna selecionada.
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- Controles de LVM_GETSELECTEDCOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ffae9a9c7812f025241f5b46f3b1ea61bb88bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295848"
---
# <a name="lvm_getselectedcolumn-message"></a><span data-ttu-id="7effa-104">\_Mensagem GETSELECTEDCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="7effa-104">LVM\_GETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="7effa-105">Recupera um inteiro que especifica a coluna selecionada.</span><span class="sxs-lookup"><span data-stu-id="7effa-105">Retrieves an integer that specifies the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="7effa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7effa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7effa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7effa-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7effa-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7effa-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7effa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7effa-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7effa-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7effa-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7effa-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7effa-111">Return value</span></span>

<span data-ttu-id="7effa-112">Retorna um **uint** que especifica a coluna selecionada.</span><span class="sxs-lookup"><span data-stu-id="7effa-112">Returns an **UINT** that specifies the selected column.</span></span>

## <a name="remarks"></a><span data-ttu-id="7effa-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7effa-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7effa-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="7effa-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7effa-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7effa-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7effa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7effa-116">Requirements</span></span>



| <span data-ttu-id="7effa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7effa-117">Requirement</span></span> | <span data-ttu-id="7effa-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7effa-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7effa-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7effa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7effa-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7effa-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7effa-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7effa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7effa-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7effa-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7effa-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7effa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7effa-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7effa-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





