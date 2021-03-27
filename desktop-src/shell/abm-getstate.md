---
description: Recupera os Estados de AutoOcultar e sempre visível da barra de tarefas do Windows.
title: Mensagem de ABM_GETSTATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296223"
---
# <a name="abm_getstate-message"></a><span data-ttu-id="e8d75-103">\_Mensagem GETstate do ABM</span><span class="sxs-lookup"><span data-stu-id="e8d75-103">ABM\_GETSTATE message</span></span>

<span data-ttu-id="e8d75-104">Recupera os Estados de AutoOcultar e sempre visível da barra de tarefas do Windows.</span><span class="sxs-lookup"><span data-stu-id="e8d75-104">Retrieves the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a><span data-ttu-id="e8d75-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8d75-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8d75-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="e8d75-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="e8d75-107">Ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="e8d75-107">Pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="e8d75-108">Você deve especificar o membro **cbSize** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="e8d75-108">You must specify the **cbSize** member when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8d75-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8d75-109">Return value</span></span>

<span data-ttu-id="e8d75-110">Retornará zero se a barra de tarefas não estiver no estado de ocultar automaticamente ou sempre visível.</span><span class="sxs-lookup"><span data-stu-id="e8d75-110">Returns zero if the taskbar is neither in the autohide nor always-on-top state.</span></span> <span data-ttu-id="e8d75-111">Caso contrário, o valor de retorno será um ou ambos os seguintes:</span><span class="sxs-lookup"><span data-stu-id="e8d75-111">Otherwise, the return value is one or both of the following:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8d75-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e8d75-112">Return code</span></span></th>
<th><span data-ttu-id="e8d75-113">Description</span><span class="sxs-lookup"><span data-stu-id="e8d75-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="e8d75-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e8d75-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e8d75-115">A barra de tarefas está no estado sempre visível.</span><span class="sxs-lookup"><span data-stu-id="e8d75-115">The taskbar is in the always-on-top state.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e8d75-116">A partir do Windows 7, ABS_ALWAYSONTOP não é mais retornado porque a barra de tarefas sempre está nesse estado.</span><span class="sxs-lookup"><span data-stu-id="e8d75-116">As of Windows 7, ABS_ALWAYSONTOP is no longer returned because the taskbar is always in that state.</span></span> <span data-ttu-id="e8d75-117">O código mais antigo deve ser atualizado para ignorar a ausência desse valor em não pressupor que o valor de retorno signifique que a barra de tarefas não está no estado sempre visível.</span><span class="sxs-lookup"><span data-stu-id="e8d75-117">Older code should be updated to ignore the absence of this value in not assume that return value to mean that the taskbar is not in the always-on-top state.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e8d75-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e8d75-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e8d75-119">A barra de tarefas está no estado de AutoOcultar.</span><span class="sxs-lookup"><span data-stu-id="e8d75-119">The taskbar is in the autohide state.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="e8d75-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8d75-120">Requirements</span></span>



| <span data-ttu-id="e8d75-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8d75-121">Requirement</span></span> | <span data-ttu-id="e8d75-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e8d75-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d75-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8d75-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d75-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8d75-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e8d75-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8d75-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d75-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8d75-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8d75-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8d75-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8d75-128"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8d75-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




