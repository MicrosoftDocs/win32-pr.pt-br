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
ms.openlocfilehash: 82ec9130a681bdfd36ff6259392c0608e4cde9cf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842277"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="2ddaa-104">\_Mensagem FMEVENT INITMENU</span><span class="sxs-lookup"><span data-stu-id="2ddaa-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="2ddaa-105">Enviado a uma DLL de extensão quando o usuário seleciona o menu para a extensão na barra de menus do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2ddaa-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="2ddaa-106">A extensão pode usar essa notificação para inicializar itens de menu.</span><span class="sxs-lookup"><span data-stu-id="2ddaa-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ddaa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ddaa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddaa-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ddaa-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2ddaa-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2ddaa-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2ddaa-110">*hmenu*</span><span class="sxs-lookup"><span data-stu-id="2ddaa-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="2ddaa-111">Um identificador para a barra de menus do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2ddaa-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddaa-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ddaa-112">Return value</span></span>

<span data-ttu-id="2ddaa-113">Uma DLL de extensão deve retornar zero se ela processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ddaa-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ddaa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ddaa-114">Remarks</span></span>

<span data-ttu-id="2ddaa-115">Uma extensão DLL recebe essa mensagem somente quando o usuário seleciona o menu de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2ddaa-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="2ddaa-116">Se a extensão contiver submenus, ela deverá inicializá-las ao mesmo tempo que inicializar o menu de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2ddaa-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddaa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ddaa-117">Requirements</span></span>



| <span data-ttu-id="2ddaa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ddaa-118">Requirement</span></span> | <span data-ttu-id="2ddaa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2ddaa-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddaa-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ddaa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ddaa-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ddaa-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2ddaa-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ddaa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2ddaa-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ddaa-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2ddaa-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2ddaa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ddaa-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddaa-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ddaa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ddaa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddaa-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="2ddaa-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




