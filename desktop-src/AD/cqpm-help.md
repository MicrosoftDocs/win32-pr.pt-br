---
title: Mensagem de CQPM_HELP (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta para permitir que a extensão de página exiba a ajuda contextual para a página.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_HELP Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085256"
---
# <a name="cqpm_help-message"></a><span data-ttu-id="32b10-104">Mensagem de ajuda do CQPM \_</span><span class="sxs-lookup"><span data-stu-id="32b10-104">CQPM\_HELP message</span></span>

<span data-ttu-id="32b10-105">A mensagem de **\_ ajuda do CQPM** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão do formulário de consulta para permitir que a extensão de página exiba a ajuda contextual para a página.</span><span class="sxs-lookup"><span data-stu-id="32b10-105">The **CQPM\_HELP** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page extension to display context-sensitive help for the page.</span></span> <span data-ttu-id="32b10-106">Se possível, a extensão de página de consulta deve exibir a ajuda contextual em resposta a esse evento.</span><span class="sxs-lookup"><span data-stu-id="32b10-106">If possible, the query page extension should display context-sensitive help in response to this event.</span></span>

## <a name="parameters"></a><span data-ttu-id="32b10-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32b10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b10-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32b10-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32b10-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="32b10-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="32b10-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32b10-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32b10-111">Ponteiro para uma estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contém dados adicionais sobre o item de menu, controle, caixa de diálogo ou janela para o qual a ajuda contextual é solicitada.</span><span class="sxs-lookup"><span data-stu-id="32b10-111">Pointer to a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains additional data about the menu item, control, dialog box, or window for which context-sensitive help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b10-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32b10-112">Return value</span></span>

<span data-ttu-id="32b10-113">O valor de retorno para essa mensagem é ignorado.</span><span class="sxs-lookup"><span data-stu-id="32b10-113">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b10-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32b10-114">Requirements</span></span>



| <span data-ttu-id="32b10-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="32b10-115">Requirement</span></span> | <span data-ttu-id="32b10-116">Valor</span><span class="sxs-lookup"><span data-stu-id="32b10-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32b10-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32b10-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32b10-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32b10-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="32b10-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32b10-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32b10-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32b10-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="32b10-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32b10-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32b10-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="32b10-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b10-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="32b10-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b10-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="32b10-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="32b10-125">**HELPINFO**</span><span class="sxs-lookup"><span data-stu-id="32b10-125">**HELPINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

