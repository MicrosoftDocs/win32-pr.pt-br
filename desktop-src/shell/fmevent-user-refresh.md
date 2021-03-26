---
description: Enviado a uma DLL de extensão quando o usuário escolhe o comando Atualizar no menu Exibir no Gerenciador de arquivos. A extensão pode usar essa notificação para atualizar seu menu.
title: Mensagem de FMEVENT_USER_REFRESH (Wfext. h)
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
ms.openlocfilehash: c3c4596b0ea589545c6e59953b9c7b5977e07b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967938"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="c27af-104">FMEVENT \_ mensagem de atualização do usuário \_</span><span class="sxs-lookup"><span data-stu-id="c27af-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="c27af-105">Enviado a uma DLL de extensão quando o usuário escolhe o comando **Atualizar** no menu **Exibir** no Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c27af-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="c27af-106">A extensão pode usar essa notificação para atualizar seu menu.</span><span class="sxs-lookup"><span data-stu-id="c27af-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="c27af-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c27af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c27af-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c27af-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c27af-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c27af-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c27af-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c27af-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c27af-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c27af-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c27af-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c27af-112">Return value</span></span>

<span data-ttu-id="c27af-113">Uma DLL de extensão deve retornar zero se ela processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c27af-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c27af-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c27af-114">Requirements</span></span>



| <span data-ttu-id="c27af-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c27af-115">Requirement</span></span> | <span data-ttu-id="c27af-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c27af-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c27af-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c27af-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c27af-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c27af-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c27af-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c27af-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c27af-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c27af-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c27af-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c27af-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c27af-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="c27af-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c27af-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c27af-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c27af-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="c27af-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




