---
description: As funções a seguir são usadas com a central de segurança do Windows.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Funções da central de segurança do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826112"
---
# <a name="windows-security-center-functions"></a><span data-ttu-id="6b4c5-103">Funções da central de segurança do Windows</span><span class="sxs-lookup"><span data-stu-id="6b4c5-103">Windows Security Center Functions</span></span>

<span data-ttu-id="6b4c5-104">As funções a seguir são usadas com a central de segurança do Windows.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-104">The following functions are used with Windows Security Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b4c5-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6b4c5-105">In this section</span></span>



| <span data-ttu-id="6b4c5-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="6b4c5-106">Topic</span></span>                                                                           | <span data-ttu-id="6b4c5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b4c5-107">Description</span></span>                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b4c5-108">**WscGetSecurityProviderHealth**</span><span class="sxs-lookup"><span data-stu-id="6b4c5-108">**WscGetSecurityProviderHealth**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | <span data-ttu-id="6b4c5-109">Obtém o estado de integridade agregado das categorias de provedor de segurança representadas pelos valores de enumeração do [**\_ \_ provedor de segurança WSC**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) especificado.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-109">Gets the aggregate health state of the security provider categories represented by the specified [**WSC\_SECURITY\_PROVIDER**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) enumeration values.</span></span><br/> |
| [<span data-ttu-id="6b4c5-110">**WscRegisterForChanges**</span><span class="sxs-lookup"><span data-stu-id="6b4c5-110">**WscRegisterForChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | <span data-ttu-id="6b4c5-111">Registra uma função de retorno de chamada a ser executada quando a WSC (central de segurança do Windows) detecta uma alteração que pode afetar a integridade de um dos provedores de segurança.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-111">Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.</span></span><br/>                    |
| [<span data-ttu-id="6b4c5-112">**WscUnRegisterChanges**</span><span class="sxs-lookup"><span data-stu-id="6b4c5-112">**WscUnRegisterChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | <span data-ttu-id="6b4c5-113">Cancela um registro de retorno de chamada que foi feito por uma ligação para a função [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) .</span><span class="sxs-lookup"><span data-stu-id="6b4c5-113">Cancels a callback registration that was made by a call to the [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) function.</span></span><br/>                                               |



 

 

 




