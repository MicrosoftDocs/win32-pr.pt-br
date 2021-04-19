---
description: Lista as constantes usadas para APIs de autenticação da Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Constantes de autenticação (autenticação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748468"
---
# <a name="authentication-constants-authentication"></a><span data-ttu-id="0c481-103">Constantes de autenticação (autenticação)</span><span class="sxs-lookup"><span data-stu-id="0c481-103">Authentication Constants (Authentication)</span></span>

## <a name="credentials-management-constants"></a><span data-ttu-id="0c481-104">Constantes de gerenciamento de credenciais</span><span class="sxs-lookup"><span data-stu-id="0c481-104">Credentials Management Constants</span></span>

<span data-ttu-id="0c481-105">O gerenciamento de credenciais usa as seguintes constantes para especificar tamanhos máximos de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0c481-105">Credentials Management uses the following constants to specify maximum string sizes.</span></span>



| <span data-ttu-id="0c481-106">Constante</span><span class="sxs-lookup"><span data-stu-id="0c481-106">Constant</span></span>                                        | <span data-ttu-id="0c481-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c481-107">Description</span></span>                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c481-108">\_comprimento máximo da \_ mensagem \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="0c481-108">CREDUI\_MAX\_MESSAGE\_LENGTH</span></span><br/>         | <span data-ttu-id="0c481-109">Número máximo de caracteres para o membro **pszMessageText** de uma estrutura de [**\_ informações de CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="0c481-109">Maximum number of characters for the **pszMessageText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="0c481-110">CREDUI \_ tamanho máximo da \_ legenda \_</span><span class="sxs-lookup"><span data-stu-id="0c481-110">CREDUI\_MAX\_CAPTION\_LENGTH</span></span><br/>         | <span data-ttu-id="0c481-111">Número máximo de caracteres para o membro **pszCaptionText** de uma estrutura de [**\_ informações de CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="0c481-111">Maximum number of characters for the **pszCaptionText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="0c481-112">\_comprimento de \_ \_ destino genérico CREDUI máximo \_</span><span class="sxs-lookup"><span data-stu-id="0c481-112">CREDUI\_MAX\_GENERIC\_TARGET\_LENGTH</span></span><br/> | <span data-ttu-id="0c481-113">Número máximo de caracteres em uma cadeia de caracteres que especifica um nome de destino.</span><span class="sxs-lookup"><span data-stu-id="0c481-113">Maximum number of characters in a string that specifies a target name.</span></span><br/>                                             |
| <span data-ttu-id="0c481-114">\_comprimento máximo \_ de \_ destino de domínio \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="0c481-114">CREDUI\_MAX\_DOMAIN\_TARGET\_LENGTH</span></span><br/>  | <span data-ttu-id="0c481-115">Número máximo de caracteres em uma cadeia de caracteres que especifica um nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="0c481-115">Maximum number of characters in a string that specifies a domain name.</span></span><br/>                                             |
| <span data-ttu-id="0c481-116">CREDUI \_ tamanho máximo do \_ nome de usuário \_</span><span class="sxs-lookup"><span data-stu-id="0c481-116">CREDUI\_MAX\_USERNAME\_LENGTH</span></span><br/>        | <span data-ttu-id="0c481-117">Número máximo de caracteres em uma cadeia de caracteres que especifica um nome de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="0c481-117">Maximum number of characters in a string that specifies a user account name.</span></span><br/>                                       |
| <span data-ttu-id="0c481-118">\_comprimento máximo da \_ senha \_ do CREDUI</span><span class="sxs-lookup"><span data-stu-id="0c481-118">CREDUI\_MAX\_PASSWORD\_LENGTH</span></span><br/>        | <span data-ttu-id="0c481-119">Número máximo de caracteres em uma cadeia de caracteres que especifica uma senha.</span><span class="sxs-lookup"><span data-stu-id="0c481-119">Maximum number of characters in a string that specifies a password.</span></span><br/>                                                |



 

## <a name="gina-defined-values"></a><span data-ttu-id="0c481-120">Valores definidos da Gina</span><span class="sxs-lookup"><span data-stu-id="0c481-120">Gina Defined Values</span></span>

<span data-ttu-id="0c481-121">As funções de interface [*Gina*](/windows/desktop/SecGloss/g-gly) e de suporte do [*Winlogon*](/windows/desktop/SecGloss/w-gly) usam os valores definidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c481-121">[*GINA*](/windows/desktop/SecGloss/g-gly) interface functions and [*Winlogon*](/windows/desktop/SecGloss/w-gly) support functions use the following defined values.</span></span>

> [!Note]  
> <span data-ttu-id="0c481-122">As DLLs GINAs são ignoradas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0c481-122">GINA DLLs are ignored in Windows Vista.</span></span>

 



| <span data-ttu-id="0c481-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0c481-123">Value</span></span>                                                              | <span data-ttu-id="0c481-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c481-124">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c481-125">**opção de logon do WLX \_ \_ \_ xxx**</span><span class="sxs-lookup"><span data-stu-id="0c481-125">**WLX\_LOGON\_OPTION\_XXX**</span></span>](wlx-logon-option-xxx.md)<br/> | <span data-ttu-id="0c481-126">Contém opções de logon predefinidas.</span><span class="sxs-lookup"><span data-stu-id="0c481-126">Contains predefined logon options.</span></span> <span data-ttu-id="0c481-127">Ele é usado pelo parâmetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="0c481-127">It is used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span><br/> |
| [<span data-ttu-id="0c481-128">**WLX \_ SAS \_ Type \_ xxx**</span><span class="sxs-lookup"><span data-stu-id="0c481-128">**WLX\_SAS\_TYPE\_XXX**</span></span>](wlx-sas-type-xxx.md)<br/>         | <span data-ttu-id="0c481-129">Define um tipo SAS específico.</span><span class="sxs-lookup"><span data-stu-id="0c481-129">Defines a specific SAS type.</span></span><br/>                                                                                              |



 

 

