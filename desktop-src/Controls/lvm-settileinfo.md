---
title: Mensagem de LVM_SETTILEINFO (commctrl. h)
description: Define informações para um bloco existente de um controle de exibição de lista.
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- Controles de LVM_SETTILEINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085400"
---
# <a name="lvm_settileinfo-message"></a><span data-ttu-id="28219-104">\_Mensagem SETTILEINFO LVM</span><span class="sxs-lookup"><span data-stu-id="28219-104">LVM\_SETTILEINFO message</span></span>

<span data-ttu-id="28219-105">Define informações para um bloco existente de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="28219-105">Sets information for an existing tile of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="28219-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28219-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28219-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28219-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="28219-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="28219-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="28219-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28219-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="28219-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> que contém as informações a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="28219-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28219-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28219-111">Return value</span></span>

<span data-ttu-id="28219-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="28219-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="28219-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="28219-113">Remarks</span></span>

<span data-ttu-id="28219-114">**LVM \_** Não há suporte para SETTILEINFO no estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="28219-114">**LVM\_SETTILEINFO** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="28219-115">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="28219-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="28219-116">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="28219-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="28219-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28219-117">Requirements</span></span>



| <span data-ttu-id="28219-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="28219-118">Requirement</span></span> | <span data-ttu-id="28219-119">Valor</span><span class="sxs-lookup"><span data-stu-id="28219-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28219-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28219-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28219-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28219-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28219-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28219-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28219-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28219-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28219-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28219-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="28219-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28219-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





