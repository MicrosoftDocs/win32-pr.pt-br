---
title: Determinando suas necessidades de segurança
description: A maneira como você configura a segurança COM para seu aplicativo depende de qual tipo de segurança seu aplicativo precisa. Há várias situações comuns que determinam o que você deve fazer.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637213"
---
# <a name="determining-your-security-needs"></a><span data-ttu-id="9dcc1-104">Determinando suas necessidades de segurança</span><span class="sxs-lookup"><span data-stu-id="9dcc1-104">Determining Your Security Needs</span></span>

<span data-ttu-id="9dcc1-105">A maneira como você configura a segurança COM para seu aplicativo depende de qual tipo de segurança seu aplicativo precisa.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-105">How you set up COM security for your application depends on what kind of security your application needs.</span></span> <span data-ttu-id="9dcc1-106">Há várias situações comuns que determinam o que você deve fazer.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-106">There are several common situations that determine what you should do.</span></span>

<span data-ttu-id="9dcc1-107">Se você decidir usar os padrões de segurança COM, não precisará fazer anythingâ € "COM tudo isso.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-107">If you decide to use the COM security defaults, you do not have to do anythingâ€”COM handles it all.</span></span> <span data-ttu-id="9dcc1-108">Para obter informações sobre o que são essas configurações padrão, consulte [padrões de segurança com](com-security-defaults.md).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-108">For information on what these default settings are, see [COM Security Defaults](com-security-defaults.md).</span></span>

<span data-ttu-id="9dcc1-109">Você também pode impedir qualquer chamada remota em seu computador desabilitando totalmente o DCOM (COM entre computadores remotos).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-109">You can also prevent any remote calls into your machine by disabling DCOM altogether (COM between remote computers).</span></span> <span data-ttu-id="9dcc1-110">Para obter mais informações, consulte [definindo System-Wide segurança usando DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-110">For more information, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="9dcc1-111">Para aplicativos herdados ou novos, você pode definir a segurança de todo o processo no registro.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-111">For legacy or new applications, you can set process-wide security in the registry.</span></span> <span data-ttu-id="9dcc1-112">Para obter mais informações, consulte [Configurando a segurança do processwide por meio do registro](setting-processwide-security-through-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-112">For more information, see [Setting Processwide Security Through the Registry](setting-processwide-security-through-the-registry.md).</span></span>

<span data-ttu-id="9dcc1-113">Você também pode substituir as configurações de segurança padrão para chamadas para determinadas interfaces no processo ao definir a segurança padrão para o restante do processo (para permitir que o COM manipule os casos gerais).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-113">You can also override default security settings for calls to certain interfaces in the process while setting default security for the remainder of the process (to allow COM to handle the general cases).</span></span> <span data-ttu-id="9dcc1-114">Para obter mais informações, consulte [definindo a segurança no nível de proxy da interface](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-114">For more information, see [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="9dcc1-115">Para requisitos de segurança complexos, você pode manipular toda a segurança programaticamente, em vez de permitir que o COM a manipule para você.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-115">For complex security requirements, you can handle all security programmatically rather than allowing COM to handle it for you.</span></span> <span data-ttu-id="9dcc1-116">Para fazer isso, chame [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para desabilitar a autenticação automática e, em seguida, controle todas as configurações de segurança definindo a segurança em uma base proxy por interface.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-116">To do this, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to disable automatic authentication, and then control all the security settings by setting security on a per-interface proxy basis.</span></span> <span data-ttu-id="9dcc1-117">Para obter mais informações, consulte [definindo a segurança do processwide com CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) e [definindo a segurança no nível do proxy da interface](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-117">For more information, see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) and [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="9dcc1-118">Em alguns cenários, talvez você queira desativar completamente a segurança.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-118">In some scenarios, you might want to turn off security completely.</span></span> <span data-ttu-id="9dcc1-119">Você pode decidir que seu aplicativo não precisa de segurança, ou talvez você queira desabilitar a segurança durante o tempo de desenvolvimento para que você possa habilitar os recursos de segurança individualmente.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-119">You might decide that your application does not need any security, or you might want to disable security during development time so that you can enable security features individually.</span></span> <span data-ttu-id="9dcc1-120">Para saber como desabilitar a segurança COM, consulte [desativando a segurança](turning-off-security.md).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-120">To learn how to disable COM security, see [Turning Off Security](turning-off-security.md).</span></span>

<span data-ttu-id="9dcc1-121">A segurança em COM conta COM os serviços de autenticação administrados por pacotes de segurança.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-121">Security in COM relies on authentication services administered by security packages.</span></span> <span data-ttu-id="9dcc1-122">O NTLMSSP funciona bem para muitos aplicativos, mas não fornece a segurança mais robusta oferecida por outros pacotes.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-122">NTLMSSP works well for many applications but does not provide the more robust security offered by other packages.</span></span> <span data-ttu-id="9dcc1-123">Portanto, o COM dá suporte ao pacote de segurança Schannel e ao protocolo de segurança Kerberos v5.</span><span class="sxs-lookup"><span data-stu-id="9dcc1-123">Therefore, COM supports the Schannel security package and the Kerberos v5 security protocol.</span></span> <span data-ttu-id="9dcc1-124">Para obter mais detalhes sobre como usar esses pacotes de segurança, consulte [pacotes de segurança e com](com-and-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="9dcc1-124">For more details on using these security packages, see [COM and Security Packages](com-and-security-packages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dcc1-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9dcc1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dcc1-126">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="9dcc1-126">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




