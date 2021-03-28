---
description: Enviado a uma DLL de extensão quando o usuário seleciona o menu para a extensão na barra de menus do Gerenciador de arquivos. A extensão pode usar essa notificação para inicializar itens de menu.
title: Mensagem de FMEVENT_INITMENU (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 4bbb959feeb2c1bf99eaa999b4c51b69b0d0cf63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164181"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="b3b09-104">\_Mensagem FMEVENT INITMENU</span><span class="sxs-lookup"><span data-stu-id="b3b09-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="b3b09-105">Enviado a uma DLL de extensão quando o usuário seleciona o menu para a extensão na barra de menus do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b3b09-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="b3b09-106">A extensão pode usar essa notificação para inicializar itens de menu.</span><span class="sxs-lookup"><span data-stu-id="b3b09-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3b09-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3b09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3b09-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3b09-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b3b09-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b3b09-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b3b09-110">*hmenu*</span><span class="sxs-lookup"><span data-stu-id="b3b09-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="b3b09-111">Um identificador para a barra de menus do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b3b09-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3b09-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3b09-112">Return value</span></span>

<span data-ttu-id="b3b09-113">Uma DLL de extensão deve retornar zero se ela processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="b3b09-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b09-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3b09-114">Remarks</span></span>

<span data-ttu-id="b3b09-115">Uma extensão DLL recebe essa mensagem somente quando o usuário seleciona o menu de nível superior.</span><span class="sxs-lookup"><span data-stu-id="b3b09-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="b3b09-116">Se a extensão contiver submenus, ela deverá inicializá-las ao mesmo tempo que inicializar o menu de nível superior.</span><span class="sxs-lookup"><span data-stu-id="b3b09-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3b09-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3b09-117">Requirements</span></span>



| <span data-ttu-id="b3b09-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b09-118">Requirement</span></span> | <span data-ttu-id="b3b09-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b3b09-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b09-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3b09-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3b09-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3b09-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b3b09-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3b09-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3b09-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3b09-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b3b09-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3b09-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3b09-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3b09-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3b09-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3b09-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b09-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="b3b09-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




