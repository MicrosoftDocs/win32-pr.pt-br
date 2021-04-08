---
title: Mensagem de LVM_GETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Obtém os estilos estendidos que estão em uso no momento para um determinado controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetExtendedListViewStyle do ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- Controles de LVM_GETEXTENDEDLISTVIEWSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008863"
---
# <a name="lvm_getextendedlistviewstyle-message"></a><span data-ttu-id="ca09c-105">\_Mensagem GETEXTENDEDLISTVIEWSTYLE LVM</span><span class="sxs-lookup"><span data-stu-id="ca09c-105">LVM\_GETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="ca09c-106">Obtém os estilos estendidos que estão em uso no momento para um determinado controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="ca09c-106">Gets the extended styles that are currently in use for a given list-view control.</span></span> <span data-ttu-id="ca09c-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetExtendedListViewStyle do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .</span><span class="sxs-lookup"><span data-stu-id="ca09c-107">You can send this message explicitly or use the [**ListView\_GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca09c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca09c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca09c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca09c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ca09c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ca09c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ca09c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca09c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ca09c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ca09c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca09c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca09c-113">Return value</span></span>

<span data-ttu-id="ca09c-114">Retorna um **DWORD** que representa os estilos atualmente em uso para um determinado controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="ca09c-114">Returns a **DWORD** that represents the styles currently in use for a given list-view control.</span></span> <span data-ttu-id="ca09c-115">Esse valor pode ser uma combinação de [estilos de List-View estendidos](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="ca09c-115">This value can be a combination of [Extended List-View Styles](extended-list-view-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca09c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca09c-116">Requirements</span></span>



| <span data-ttu-id="ca09c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca09c-117">Requirement</span></span> | <span data-ttu-id="ca09c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ca09c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca09c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca09c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ca09c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca09c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca09c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca09c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ca09c-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca09c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca09c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca09c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca09c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca09c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





