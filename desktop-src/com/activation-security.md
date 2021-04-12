---
title: Segurança de ativação
description: Segurança de ativação
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454387"
---
# <a name="activation-security"></a><span data-ttu-id="27e8e-103">Segurança de ativação</span><span class="sxs-lookup"><span data-stu-id="27e8e-103">Activation Security</span></span>

<span data-ttu-id="27e8e-104">A segurança de ativação (também chamada de segurança de inicialização) ajuda a controlar quem pode iniciar um servidor.</span><span class="sxs-lookup"><span data-stu-id="27e8e-104">Activation security (also called launch security) helps control who can launch a server.</span></span> <span data-ttu-id="27e8e-105">A segurança de ativação é aplicada automaticamente pelo SCM (Gerenciador de controle de serviço) de um computador específico.</span><span class="sxs-lookup"><span data-stu-id="27e8e-105">Activation security is automatically applied by the service control manager (SCM) of a particular computer.</span></span> <span data-ttu-id="27e8e-106">Após o recebimento de uma solicitação de um cliente para ativar um objeto (conforme descrito em [funções auxiliares de criação de instância](instance-creation-helper-functions.md)), o SCM verifica a solicitação em relação às informações de segurança de ativação armazenadas em seu registro.</span><span class="sxs-lookup"><span data-stu-id="27e8e-106">Upon receipt of a request from a client to activate an object (as described in [Instance Creation Helper Functions](instance-creation-helper-functions.md)), the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="27e8e-107">(A segurança de ativação também é verificada para ativações de mesmo computador.)</span><span class="sxs-lookup"><span data-stu-id="27e8e-107">(Activation security is also checked for same-computer activations.)</span></span>

<span data-ttu-id="27e8e-108">Ao determinar a identidade do cliente, a ativação examina o sinalizador de encobrimento definido na chamada do cliente para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="27e8e-108">When determining the identity of the client, activation examines the cloaking flag set in the client's call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="27e8e-109">Se o sinalizador de encobrimento for definido (para o encobrimento dinâmico ou estático), o token de thread será usado, se presente, para determinar a identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="27e8e-109">If the cloaking flag is set (for either dynamic or static cloaking), the thread token is used, if present, to determine the identity of the client.</span></span> <span data-ttu-id="27e8e-110">Se nenhum encobrimento estiver definido, o token de processo será usado em vez do token de thread.</span><span class="sxs-lookup"><span data-stu-id="27e8e-110">If no cloaking is set, the process token is used instead of the thread token.</span></span>

<span data-ttu-id="27e8e-111">Para obter mais informações sobre segurança de ativação, consulte [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) e [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span><span class="sxs-lookup"><span data-stu-id="27e8e-111">For more information about activation security, see [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) and [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="27e8e-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27e8e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27e8e-113">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="27e8e-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 