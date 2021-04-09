---
title: Mensagem de LVM_GETTILEINFO (commctrl. h)
description: Recupera informações sobre um bloco em um controle de exibição de lista.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- Controles de LVM_GETTILEINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009647"
---
# <a name="lvm_gettileinfo-message"></a><span data-ttu-id="8b2f6-104">\_Mensagem GETTILEINFO LVM</span><span class="sxs-lookup"><span data-stu-id="8b2f6-104">LVM\_GETTILEINFO message</span></span>

<span data-ttu-id="8b2f6-105">Recupera informações sobre um bloco em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="8b2f6-105">Retrieves information about a tile in a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b2f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b2f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b2f6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b2f6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8b2f6-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8b2f6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8b2f6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b2f6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8b2f6-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> que recebe as informações recuperadas.</span><span class="sxs-lookup"><span data-stu-id="8b2f6-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b2f6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b2f6-111">Return value</span></span>

<span data-ttu-id="8b2f6-112">Valor de retorno não usado.</span><span class="sxs-lookup"><span data-stu-id="8b2f6-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b2f6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b2f6-113">Remarks</span></span>

<span data-ttu-id="8b2f6-114">A exibição de bloco é uma nova maneira de organizar e exibir itens em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="8b2f6-114">Tile view is a new way of arranging and displaying items in a list-view control.</span></span> <span data-ttu-id="8b2f6-115">As outras exibições são ícone, ícone pequeno, detalhes e lista.</span><span class="sxs-lookup"><span data-stu-id="8b2f6-115">The other views are icon, small icon, details, and list.</span></span>

> [!Note]  
> <span data-ttu-id="8b2f6-116">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="8b2f6-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8b2f6-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8b2f6-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b2f6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b2f6-118">Requirements</span></span>



| <span data-ttu-id="8b2f6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b2f6-119">Requirement</span></span> | <span data-ttu-id="8b2f6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8b2f6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2f6-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b2f6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8b2f6-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b2f6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b2f6-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b2f6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8b2f6-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b2f6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b2f6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b2f6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b2f6-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b2f6-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





