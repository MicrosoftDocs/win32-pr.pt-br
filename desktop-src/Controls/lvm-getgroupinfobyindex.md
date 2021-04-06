---
title: Mensagem de LVM_GETGROUPINFOBYINDEX (commctrl. h)
description: Obtém informações sobre um grupo especificado. Envie essa mensagem explicitamente ou usando a \_ macro GetGroupInfoByIndex do ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- Controles de LVM_GETGROUPINFOBYINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085815"
---
# <a name="lvm_getgroupinfobyindex-message"></a><span data-ttu-id="20901-105">\_Mensagem GETGROUPINFOBYINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="20901-105">LVM\_GETGROUPINFOBYINDEX message</span></span>

<span data-ttu-id="20901-106">Obtém informações sobre um grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="20901-106">Gets information on a specified group.</span></span> <span data-ttu-id="20901-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetGroupInfoByIndex do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .</span><span class="sxs-lookup"><span data-stu-id="20901-107">Send this message explicitly or by using the [**ListView\_GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="20901-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20901-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20901-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20901-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20901-110">O índice do grupo.</span><span class="sxs-lookup"><span data-stu-id="20901-110">The index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="20901-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="20901-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="20901-112">Um ponteiro para uma estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) para receber informações sobre o grupo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="20901-112">A pointer to an [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="20901-113">O processo de chamada é responsável por alocar memória para a estrutura e quaisquer buffers na estrutura, como aquele apontado pelo membro **pszHeader** .</span><span class="sxs-lookup"><span data-stu-id="20901-113">The calling process is responsible for allocating memory for the structure and any buffers in the structure, such as the one pointed to by the **pszHeader** member.</span></span> <span data-ttu-id="20901-114">Defina quaisquer membros contingentes da estrutura, como **cchHeader** o tamanho do buffer apontado por **pszHeader** em **WCHAR** , incluindo o **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="20901-114">Set any contingent members of the structure, such as **cchHeader** the size of the buffer pointed to by **pszHeader** in **WCHARs** including the terminating **NULL**.</span></span> <span data-ttu-id="20901-115">Defina **cbSize** como sizeof (LVGROUP).</span><span class="sxs-lookup"><span data-stu-id="20901-115">Set **cbSize** to sizeof(LVGROUP).</span></span>

<span data-ttu-id="20901-116">O receptor da mensagem é responsável por definir os membros da estrutura com informações para o grupo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="20901-116">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20901-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20901-117">Return value</span></span>

<span data-ttu-id="20901-118">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="20901-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="20901-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20901-119">Requirements</span></span>



| <span data-ttu-id="20901-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="20901-120">Requirement</span></span> | <span data-ttu-id="20901-121">Valor</span><span class="sxs-lookup"><span data-stu-id="20901-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20901-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20901-122">Minimum supported client</span></span><br/> | <span data-ttu-id="20901-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20901-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20901-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20901-124">Minimum supported server</span></span><br/> | <span data-ttu-id="20901-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20901-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20901-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20901-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="20901-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="20901-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





