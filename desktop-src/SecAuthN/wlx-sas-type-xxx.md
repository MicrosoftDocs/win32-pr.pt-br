---
description: Os valores definem um tipo SAS específico.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749683"
---
# <a name="wlx_sas_type_xxx"></a><span data-ttu-id="ba627-103">WLX \_ SAS \_ Type \_ xxx</span><span class="sxs-lookup"><span data-stu-id="ba627-103">WLX\_SAS\_TYPE\_XXX</span></span>

<span data-ttu-id="ba627-104">\[A \_ constante do tipo WLX SAS \_ \_ xxx não está mais disponível para uso a partir do Windows Server 2008 e do Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="ba627-104">\[The WLX\_SAS\_TYPE\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="ba627-105">Os **valores \_ \_ \_ xxx do tipo SAS do WLX** definem um tipo SAS específico.</span><span class="sxs-lookup"><span data-stu-id="ba627-105">The **WLX\_SAS\_TYPE\_XXX** values define a specific SAS type.</span></span>

> [!Note]  
> <span data-ttu-id="ba627-106">As DLLs GINAs são ignoradas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ba627-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="ba627-107">Todos os valores de zero a 127 são reservados para tipos definidos pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ba627-107">All values from zero to 127 are reserved for Microsoft-defined types.</span></span> <span data-ttu-id="ba627-108">Os valores acima de 127 estão disponíveis para tipos definidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="ba627-108">Values above 127 are available for customer-defined types.</span></span> <span data-ttu-id="ba627-109">Os tipos a seguir são passados para funções que têm um parâmetro *dwSasType* .</span><span class="sxs-lookup"><span data-stu-id="ba627-109">The following types are passed to functions that have a *dwSasType* parameter.</span></span>



| <span data-ttu-id="ba627-110">Constante</span><span class="sxs-lookup"><span data-stu-id="ba627-110">Constant</span></span>                                                                                                                                                                                                         | <span data-ttu-id="ba627-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba627-111">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <span data-ttu-id="ba627-112"><dt>**\_tipo de SAS WLX \_ \_ Ctrl \_ ALT \_ del**</dt></span><span class="sxs-lookup"><span data-stu-id="ba627-112"><dt>**WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL**</dt></span></span> </dl>            | <span data-ttu-id="ba627-113">Indica que um usuário digitou a SAS CTRL + ALT + DEL padrão.</span><span class="sxs-lookup"><span data-stu-id="ba627-113">Indicates a user has typed the standard CTRL+ALT+DEL SAS.</span></span><br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <span data-ttu-id="ba627-114"><dt>**WLX \_ SAS \_ tipo \_ sc \_ Insert**</dt></span><span class="sxs-lookup"><span data-stu-id="ba627-114"><dt>**WLX\_SAS\_TYPE\_SC\_INSERT**</dt></span></span> </dl>                      | <span data-ttu-id="ba627-115">Indica que um [*cartão inteligente*](../secgloss/s-gly.md) foi inserido em um dispositivo compatível.</span><span class="sxs-lookup"><span data-stu-id="ba627-115">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span><br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <span data-ttu-id="ba627-116"><dt>**WLX \_ SAS \_ tipo \_ sc \_ Remove**</dt></span><span class="sxs-lookup"><span data-stu-id="ba627-116"><dt>**WLX\_SAS\_TYPE\_SC\_REMOVE**</dt></span></span> </dl>                      | <span data-ttu-id="ba627-117">Indica que um cartão inteligente foi removido de um dispositivo compatível.</span><span class="sxs-lookup"><span data-stu-id="ba627-117">Indicates that a smart card has been removed from a compatible device.</span></span><br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <span data-ttu-id="ba627-118"><dt>**\_ \_ atividade SCRNSVR do tipo SAS \_ do \_ WLX**</dt></span><span class="sxs-lookup"><span data-stu-id="ba627-118"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_ACTIVITY**</dt></span></span> </dl> | <span data-ttu-id="ba627-119">Indica que a atividade do teclado ou do mouse ocorreu enquanto uma proteção de tela segura estava ativa.</span><span class="sxs-lookup"><span data-stu-id="ba627-119">Indicates that keyboard or mouse activity occurred while a secure screen saver was active.</span></span><br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <span data-ttu-id="ba627-120"><dt>**WLX \_ SAS \_ tipo \_ SCRNSVR \_ Timeout**</dt></span><span class="sxs-lookup"><span data-stu-id="ba627-120"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT**</dt></span></span> </dl>    | <span data-ttu-id="ba627-121">Indica que a ativação da proteção de tela ocorreu devido à inatividade do teclado e do mouse.</span><span class="sxs-lookup"><span data-stu-id="ba627-121">Indicates that screen saver activation has occurred due to keyboard and mouse inactivity.</span></span><br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <span data-ttu-id="ba627-122"><dt>**\_ \_ tempo limite de tipo SAS WLX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba627-122"><dt>**WLX\_SAS\_TYPE\_TIMEOUT**</dt></span></span> </dl>                             | <span data-ttu-id="ba627-123">Indica que nenhuma entrada de usuário foi recebida dentro do período de tempo limite especificado.</span><span class="sxs-lookup"><span data-stu-id="ba627-123">Indicates that no user input was received within the specified time-out period.</span></span><br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <span data-ttu-id="ba627-124"><dt>**\_logoff do \_ usuário do tipo SAS \_ WLX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba627-124"><dt>**WLX\_SAS\_TYPE\_USER\_LOGOFF**</dt></span></span> </dl>                | <span data-ttu-id="ba627-125">Indica que o usuário está sendo desconectado do sistema.</span><span class="sxs-lookup"><span data-stu-id="ba627-125">Indicates the user is being logged off the system.</span></span><br/>                                                                                            |



## <a name="requirements"></a><span data-ttu-id="ba627-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba627-126">Requirements</span></span>



| <span data-ttu-id="ba627-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba627-127">Requirement</span></span> | <span data-ttu-id="ba627-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ba627-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ba627-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba627-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ba627-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ba627-130">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ba627-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba627-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ba627-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba627-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ba627-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ba627-133">End of client support</span></span><br/>    | <span data-ttu-id="ba627-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba627-134">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="ba627-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ba627-135">End of server support</span></span><br/>    | <span data-ttu-id="ba627-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba627-136">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="ba627-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba627-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba627-138"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba627-138"><dt>Winwlx.h</dt></span></span> </dl> |



 

 
