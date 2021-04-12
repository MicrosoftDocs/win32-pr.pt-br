---
description: Os valores são usados pelo parâmetro dwOptions de WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297076"
---
# <a name="wlx_logon_option_xxx"></a><span data-ttu-id="92aee-103">opção de logon do WLX \_ \_ \_ xxx</span><span class="sxs-lookup"><span data-stu-id="92aee-103">WLX\_LOGON\_OPTION\_XXX</span></span>

<span data-ttu-id="92aee-104">\[A \_ constante da opção de logon WLX \_ \_ xxx não está mais disponível para uso a partir do Windows Server 2008 e do Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="92aee-104">\[The WLX\_LOGON\_OPTION\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="92aee-105">Os valores da **\_ opção de logon WLX \_ \_ xxx** são usados pelo parâmetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="92aee-105">The **WLX\_LOGON\_OPTION\_XXX** values are used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span>

> [!Note]  
> <span data-ttu-id="92aee-106">As DLLs GINAs são ignoradas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92aee-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="92aee-107">Após um logon bem-sucedido, sua DLL GINA pode usar esse valor para especificar a opção a seguir.</span><span class="sxs-lookup"><span data-stu-id="92aee-107">Upon a successful logon, your GINA DLL can use this value to specify the following option.</span></span>



| <span data-ttu-id="92aee-108">Constante</span><span class="sxs-lookup"><span data-stu-id="92aee-108">Constant</span></span>                                                                                                                                                                                          | <span data-ttu-id="92aee-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="92aee-109">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <span data-ttu-id="92aee-110"><dt>**\_ \_ \_ não aceitar \_ perfil de logon WLX**</dt></span><span class="sxs-lookup"><span data-stu-id="92aee-110"><dt>**WLX\_LOGON\_OPT\_NO\_PROFILE**</dt></span></span> </dl> | <span data-ttu-id="92aee-111">Especifica que o Winlogon não deve carregar um perfil para o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="92aee-111">Specifies that Winlogon must not load a profile for the logged-on user.</span></span> <span data-ttu-id="92aee-112">Nesse caso, sua DLL GINA carregará o perfil ou o usuário não precisará de um perfil.</span><span class="sxs-lookup"><span data-stu-id="92aee-112">In this case, either your GINA DLL will load the profile or the user does not need a profile.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="92aee-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92aee-113">Requirements</span></span>



| <span data-ttu-id="92aee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="92aee-114">Requirement</span></span> | <span data-ttu-id="92aee-115">Valor</span><span class="sxs-lookup"><span data-stu-id="92aee-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="92aee-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92aee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="92aee-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="92aee-117">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="92aee-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92aee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="92aee-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92aee-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="92aee-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="92aee-120">End of client support</span></span><br/>    | <span data-ttu-id="92aee-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="92aee-121">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="92aee-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="92aee-122">End of server support</span></span><br/>    | <span data-ttu-id="92aee-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92aee-123">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="92aee-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92aee-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="92aee-125"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="92aee-125"><dt>Winwlx.h</dt></span></span> </dl> |



 

 




