---
title: Diretriz de segurança
description: É importante manter o usuário informado sobre possíveis problemas de segurança.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084778"
---
# <a name="security-guideline"></a><span data-ttu-id="5a9b6-103">Diretriz de segurança</span><span class="sxs-lookup"><span data-stu-id="5a9b6-103">Security Guideline</span></span>

<span data-ttu-id="5a9b6-104">É importante manter o usuário informado sobre possíveis problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="5a9b6-104">It is important to keep the user informed about possible security issues.</span></span>

## <a name="notify-the-user-of-security-related-events"></a><span data-ttu-id="5a9b6-105">Notificar o usuário sobre eventos de Security-Related</span><span class="sxs-lookup"><span data-stu-id="5a9b6-105">Notify the User of Security-Related Events</span></span>

<span data-ttu-id="5a9b6-106">Sempre notifique o usuário sobre qualquer alteração na segurança, seja um erro relacionado à segurança, como uma falha de certificado, ou uma alteração na segurança do protocolo subjacente, como alterar de um site HTTPS para um site HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a9b6-106">Always notify the user of any change in security, whether it is a security-related error such as a certificate failure, or a change in the security of the underlying protocol, such as change from an HTTPS site to an HTTP site.</span></span>

## <a name="notify-the-user-of-security-related-errors"></a><span data-ttu-id="5a9b6-107">Notificar o usuário sobre erros de Security-Related</span><span class="sxs-lookup"><span data-stu-id="5a9b6-107">Notify the User of Security-Related Errors</span></span>

<span data-ttu-id="5a9b6-108">Quando seu aplicativo recebe uma mensagem de erro que pode indicar um problema de segurança, a função **InternetErrorDlg** fornece uma interface padrão e familiar para notificar o usuário na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="5a9b6-108">When your application receives an error message that may indicate a security problem, the **InternetErrorDlg** function provides a standard, familiar interface for notifying the user in most cases.</span></span>

<span data-ttu-id="5a9b6-109">Entre os erros que se enquadram nessa categoria estão:</span><span class="sxs-lookup"><span data-stu-id="5a9b6-109">Among the errors that fall in this category are:</span></span>

<span data-ttu-id="5a9b6-110">**ERRO \_ \_ de http \_ da Internet para \_ https \_ no \_ REDIR**</span><span class="sxs-lookup"><span data-stu-id="5a9b6-110">**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>

<span data-ttu-id="5a9b6-111">**ERRO \_ de \_ AC inválida \_ da Internet**</span><span class="sxs-lookup"><span data-stu-id="5a9b6-111">**ERROR\_INTERNET\_INVALID\_CA**</span></span>

<span data-ttu-id="5a9b6-112">**ERRO \_ a \_ postagem na Internet \_ \_ não é \_ segura**</span><span class="sxs-lookup"><span data-stu-id="5a9b6-112">**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>

<span data-ttu-id="5a9b6-113">**\_erros de certificados da Internet \_ SEC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5a9b6-113">**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>

<span data-ttu-id="5a9b6-114">**ERRO \_ CN do certificado da Internet \_ SEC \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="5a9b6-114">**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>

<span data-ttu-id="5a9b6-115">**ERRO de data de CERT. de \_ Internet \_ \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="5a9b6-115">**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>

<span data-ttu-id="5a9b6-116">Uma falha ao notificar o usuário sobre erros como esses podem expor o usuário a vários tipos de violações de segurança, incluindo ataques de falsificação ou divulgação involuntária de informações.</span><span class="sxs-lookup"><span data-stu-id="5a9b6-116">A failure to notify the user of errors such as these can expose the user to various sorts of security breaches, including spoofing attacks or involuntary information disclosure.</span></span>

## <a name="notify-the-user-when-connection-security-changes"></a><span data-ttu-id="5a9b6-117">Notificar o usuário quando a segurança da conexão for alterada</span><span class="sxs-lookup"><span data-stu-id="5a9b6-117">Notify the User When Connection Security Changes</span></span>

<span data-ttu-id="5a9b6-118">Sempre notifique o usuário quando a segurança da conexão for alterada, por exemplo, de HTTPS para HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a9b6-118">Always notify the user when the security of the connection changes, for example from HTTPS to HTTP.</span></span> <span data-ttu-id="5a9b6-119">Caso contrário, a menos que o usuário tenha optado explicitamente por não ser notificado sobre tais alterações, você está ocultando os riscos da divulgação involuntária de informações.</span><span class="sxs-lookup"><span data-stu-id="5a9b6-119">Otherwise, unless the user has explicitly chosen not to be notified of such changes, you are concealing the risks of involuntary information disclosure.</span></span>

<span data-ttu-id="5a9b6-120">Entre as funções que relatam tal alteração na segurança da conexão estão a função de retorno de chamada **InternetStatusCallback** e a função **InternetConfirmZoneCrossing** .</span><span class="sxs-lookup"><span data-stu-id="5a9b6-120">Among the functions that report such a change in connection security are the **InternetStatusCallback** callback function and the **InternetConfirmZoneCrossing** function.</span></span>

> [!Note]  
> <span data-ttu-id="5a9b6-121">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="5a9b6-121">WinINet does not support server implementations.</span></span> <span data-ttu-id="5a9b6-122">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="5a9b6-122">In addition, it should not be used from a service.</span></span> <span data-ttu-id="5a9b6-123">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="5a9b6-123">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 