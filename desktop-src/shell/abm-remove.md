---
description: Cancela o registro de um AppBar removendo-o da lista interna do sistema. O sistema não envia mais mensagens de notificação para o AppBar ou impede que outros aplicativos usem a área de tela usada pelo AppBar.
title: Mensagem de ABM_REMOVE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826899"
---
# <a name="abm_remove-message"></a><span data-ttu-id="cf120-104">ABM \_ remover mensagem</span><span class="sxs-lookup"><span data-stu-id="cf120-104">ABM\_REMOVE message</span></span>

<span data-ttu-id="cf120-105">Cancela o registro de um AppBar removendo-o da lista interna do sistema.</span><span class="sxs-lookup"><span data-stu-id="cf120-105">Unregisters an appbar by removing it from the system's internal list.</span></span> <span data-ttu-id="cf120-106">O sistema não envia mais mensagens de notificação para o AppBar ou impede que outros aplicativos usem a área de tela usada pelo AppBar.</span><span class="sxs-lookup"><span data-stu-id="cf120-106">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span>


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a><span data-ttu-id="cf120-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf120-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf120-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="cf120-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="cf120-109">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contém o identificador para o AppBar para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="cf120-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the handle to the appbar to unregister.</span></span> <span data-ttu-id="cf120-110">Você deve especificar os membros **cbSize** e **HWND** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="cf120-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf120-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf120-111">Return value</span></span>

<span data-ttu-id="cf120-112">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="cf120-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf120-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf120-113">Remarks</span></span>

<span data-ttu-id="cf120-114">Essa mensagem faz com que o sistema envie a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) para todos os appbars.</span><span class="sxs-lookup"><span data-stu-id="cf120-114">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf120-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf120-115">Requirements</span></span>



| <span data-ttu-id="cf120-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf120-116">Requirement</span></span> | <span data-ttu-id="cf120-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cf120-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf120-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf120-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cf120-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cf120-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cf120-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf120-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cf120-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf120-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf120-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cf120-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf120-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf120-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




