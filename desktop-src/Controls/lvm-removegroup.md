---
title: Mensagem de LVM_REMOVEGROUP (commctrl. h)
description: Remove um grupo de um controle de exibição de lista.
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- Controles de LVM_REMOVEGROUP de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa631593e791f90c76a9f74aa1d967d9678540f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918702"
---
# <a name="lvm_removegroup-message"></a><span data-ttu-id="0b870-104">\_Mensagem de REmovimentação do LVM</span><span class="sxs-lookup"><span data-stu-id="0b870-104">LVM\_REMOVEGROUP message</span></span>

<span data-ttu-id="0b870-105">Remove um grupo de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="0b870-105">Removes a group from a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b870-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b870-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b870-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b870-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0b870-108">ID que especifica o grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0b870-108">ID that specifies the group to remove.</span></span></dd> <dt>

<span data-ttu-id="0b870-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b870-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b870-110">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0b870-110">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b870-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b870-111">Return value</span></span>

<span data-ttu-id="0b870-112">Retorna o índice do grupo se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0b870-112">Returns the index of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b870-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b870-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b870-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="0b870-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0b870-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0b870-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b870-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b870-116">Requirements</span></span>



| <span data-ttu-id="0b870-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b870-117">Requirement</span></span> | <span data-ttu-id="0b870-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0b870-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b870-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b870-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b870-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b870-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b870-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b870-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b870-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b870-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b870-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b870-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b870-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b870-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





