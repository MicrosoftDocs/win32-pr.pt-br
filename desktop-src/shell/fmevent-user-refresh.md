---
description: Enviado para uma DLL de extensão quando o usuário escolhe o comando Atualizar no menu Exibir no Gerenciador de Arquivos. A extensão pode usar essa notificação para atualizar seu menu.
title: FMEVENT_USER_REFRESH mensagem (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: 16f75f562149b50237a6b41bf2023d1f694741e3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841257"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="e7809-104">Mensagem FMEVENT \_ USER \_ REFRESH</span><span class="sxs-lookup"><span data-stu-id="e7809-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="e7809-105">Enviado para uma DLL de extensão quando o usuário escolhe o **comando Atualizar** no menu **Exibir** no Gerenciador de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="e7809-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="e7809-106">A extensão pode usar essa notificação para atualizar seu menu.</span><span class="sxs-lookup"><span data-stu-id="e7809-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7809-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7809-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7809-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7809-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e7809-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e7809-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e7809-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7809-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e7809-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e7809-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7809-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7809-112">Return value</span></span>

<span data-ttu-id="e7809-113">Uma DLL de extensão deverá retornar zero se ela processa essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="e7809-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7809-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7809-114">Requirements</span></span>



| <span data-ttu-id="e7809-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7809-115">Requirement</span></span> | <span data-ttu-id="e7809-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e7809-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7809-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7809-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7809-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7809-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e7809-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7809-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7809-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7809-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e7809-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7809-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7809-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="e7809-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7809-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7809-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7809-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="e7809-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




