---
title: Classe CSecureChannelServer
description: Classe CSecureChannelServer
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Gerenciador de Dispositivos, classe CSecureChannelServer
- Gerenciador de Dispositivos, classe CSecureChannelServer
- provedores de serviço, classe CSecureChannelServer
- referência de programação, classe CSecureChannelServer
- referência para Windows Media Gerenciador de Dispositivos, classe CSecureChannelServer
- Classe CSecureChannelServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641244"
---
# <a name="csecurechannelserver-class"></a><span data-ttu-id="d86a2-109">Classe CSecureChannelServer</span><span class="sxs-lookup"><span data-stu-id="d86a2-109">CSecureChannelServer Class</span></span>

<span data-ttu-id="d86a2-110">A classe **CSecureChannelServer** é uma classe auxiliar (não uma interface) que permite que um provedor de serviços ou provedor de conteúdo seguro autentique um aplicativo usando a interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) , para criptografar e descriptografar dados e para criar assinaturas Mac.</span><span class="sxs-lookup"><span data-stu-id="d86a2-110">The **CSecureChannelServer** class is a helper class (not an interface) that enables a service provider or secure content provider to authenticate an application using the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface, to encrypt and decrypt data, and to create MAC signatures.</span></span> <span data-ttu-id="d86a2-111">O processo de autenticação requer que o aplicativo crie um objeto **CSecureChannelClient** e que o provedor de serviços Crie um objeto **CSecureChannelServer** .</span><span class="sxs-lookup"><span data-stu-id="d86a2-111">The authentication process requires that the application create a **CSecureChannelClient** object and that the service provider create a **CSecureChannelServer** object.</span></span> <span data-ttu-id="d86a2-112">As classes **CSecureChannelClient** e **CSecureChannelServer** são declaradas na biblioteca de links estáticos, Mssachlp. lib.</span><span class="sxs-lookup"><span data-stu-id="d86a2-112">The **CSecureChannelClient** and **CSecureChannelServer** classes are declared in the static link library, Mssachlp.lib.</span></span> <span data-ttu-id="d86a2-113">Todos os métodos de Gerenciador de Dispositivos de mídia do Windows, provedor de serviços e interfaces de provedor de conteúdo seguro podem retornar WMDM \_ E \_ não certificados para indicar que o chamador não foi autenticado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d86a2-113">All methods of Windows Media Device Manager, service provider, and secure content provider interfaces can return WMDM\_E\_NOTCERTIFIED to indicate that the caller has not authenticated successfully.</span></span>

<span data-ttu-id="d86a2-114">A classe **CSecureChannelServer** expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d86a2-114">The **CSecureChannelServer** class exposes the following methods.</span></span>



| <span data-ttu-id="d86a2-115">Método</span><span class="sxs-lookup"><span data-stu-id="d86a2-115">Method</span></span>                                                            | <span data-ttu-id="d86a2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d86a2-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86a2-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d86a2-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span></span>         | <span data-ttu-id="d86a2-118">Descriptografa os dados contidos em um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d86a2-118">Decrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="d86a2-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d86a2-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span></span>         | <span data-ttu-id="d86a2-120">Criptografa os dados contidos em um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d86a2-120">Encrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="d86a2-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d86a2-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span></span> | <span data-ttu-id="d86a2-122">Verifica se um canal de autenticação segura foi estabelecido com êxito.</span><span class="sxs-lookup"><span data-stu-id="d86a2-122">Verifies that a secure authentication channel has been successfully established.</span></span>            |
| <span data-ttu-id="d86a2-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d86a2-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span></span>               | <span data-ttu-id="d86a2-124">Recupera os níveis de segurança do aplicativo dos componentes locais e remotos.</span><span class="sxs-lookup"><span data-stu-id="d86a2-124">Retrieves the application security levels of the local and remote components.</span></span>               |
| <span data-ttu-id="d86a2-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d86a2-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span></span>       | <span data-ttu-id="d86a2-126">Recupera a chave de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="d86a2-126">Retrieves the current session key.</span></span>                                                          |
| <span data-ttu-id="d86a2-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d86a2-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span></span>                 | <span data-ttu-id="d86a2-128">Libera o canal do código de autenticação de mensagem (MAC) e recupera um valor MAC final.</span><span class="sxs-lookup"><span data-stu-id="d86a2-128">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>     |
| <span data-ttu-id="d86a2-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d86a2-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span></span>                   | <span data-ttu-id="d86a2-130">Adquire um canal MAC (código de autenticação de mensagens).</span><span class="sxs-lookup"><span data-stu-id="d86a2-130">Acquires a message authentication code (MAC) channel.</span></span>                                       |
| <span data-ttu-id="d86a2-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d86a2-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span></span>               | <span data-ttu-id="d86a2-132">Atualiza o valor do código de autenticação de mensagem (MAC) com um valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d86a2-132">Updates the message authentication code (MAC) value with a parameter value.</span></span>                 |
| <span data-ttu-id="d86a2-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d86a2-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span></span>                   | <span data-ttu-id="d86a2-134">Estabelece um canal autenticado seguro entre componentes.</span><span class="sxs-lookup"><span data-stu-id="d86a2-134">Establishes a secure authenticated channel between components.</span></span>                              |
| <span data-ttu-id="d86a2-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d86a2-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span></span>   | <span data-ttu-id="d86a2-136">Relata os protocolos com suporte por um componente.</span><span class="sxs-lookup"><span data-stu-id="d86a2-136">Reports the protocols supported by a component.</span></span>                                             |
| <span data-ttu-id="d86a2-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d86a2-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span></span>     | <span data-ttu-id="d86a2-138">Especifica o certificado e a chave privada do servidor do (a) canal autenticado seguro (SAC).</span><span class="sxs-lookup"><span data-stu-id="d86a2-138">Specifies the certificate and private key of the secure authenticated channel (SAC) server.</span></span> |
| <span data-ttu-id="d86a2-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d86a2-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span></span>       | <span data-ttu-id="d86a2-140">Define a chave de sessão que é usada para se comunicar com outro componente.</span><span class="sxs-lookup"><span data-stu-id="d86a2-140">Sets the session key that is used to communicate with another component.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="d86a2-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d86a2-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d86a2-142">**Classe CSecureChannelClient**</span><span class="sxs-lookup"><span data-stu-id="d86a2-142">**CSecureChannelClient Class**</span></span>](csecurechannelclient-class.md)
</dt> <dt>

[<span data-ttu-id="d86a2-143">**Interface IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="d86a2-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="d86a2-144">**Interfaces para provedores de serviços**</span><span class="sxs-lookup"><span data-stu-id="d86a2-144">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> <dt>

[<span data-ttu-id="d86a2-145">**Usando canais autenticados seguros**</span><span class="sxs-lookup"><span data-stu-id="d86a2-145">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 