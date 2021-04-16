---
title: Classe CSecureChannelClient
description: Classe CSecureChannelClient
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Gerenciador de Dispositivos, classe CSecureChannelClient
- Gerenciador de Dispositivos, classe CSecureChannelClient
- aplicativos de área de trabalho, classe CSecureChannelClient
- referência de programação, classe CSecureChannelClient
- referência para Windows Media Gerenciador de Dispositivos, classe CSecureChannelClient
- Classe CSecureChannelClient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789594"
---
# <a name="csecurechannelclient-class"></a><span data-ttu-id="90749-109">Classe CSecureChannelClient</span><span class="sxs-lookup"><span data-stu-id="90749-109">CSecureChannelClient Class</span></span>

<span data-ttu-id="90749-110">A classe **CSecureChannelClient** é uma classe auxiliar (não uma interface) que permite que os aplicativos se autentiquem, criptografem e descriptografem dados e criem Macs.</span><span class="sxs-lookup"><span data-stu-id="90749-110">The **CSecureChannelClient** class is a helper class (not an interface) that enables applications to authenticate themselves, encrypt and decrypt data, and create MACs.</span></span>

<span data-ttu-id="90749-111">A classe **CSecureChannelClient** expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="90749-111">The **CSecureChannelClient** class exposes the following methods.</span></span>



| <span data-ttu-id="90749-112">Método</span><span class="sxs-lookup"><span data-stu-id="90749-112">Method</span></span>                                                            | <span data-ttu-id="90749-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="90749-113">Description</span></span>                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90749-114">[**Autenticação**](/previous-versions/ms983906(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="90749-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span></span>         | <span data-ttu-id="90749-115">Dispara a troca de certificados entre componentes para estabelecer confiança.</span><span class="sxs-lookup"><span data-stu-id="90749-115">Triggers the exchange of certificates between components to establish trust.</span></span>                                              |
| <span data-ttu-id="90749-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90749-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span></span>         | <span data-ttu-id="90749-117">Descriptografa os dados recebidos por meio de um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="90749-117">Decrypts data received through a parameter.</span></span>                                                                               |
| <span data-ttu-id="90749-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90749-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span></span>         | <span data-ttu-id="90749-119">Criptografa os dados sendo enviados por meio de um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="90749-119">Encrypts data being sent out through a parameter.</span></span>                                                                         |
| <span data-ttu-id="90749-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="90749-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span></span> | <span data-ttu-id="90749-121">Verifica se um canal de autenticação segura foi estabelecido com êxito.</span><span class="sxs-lookup"><span data-stu-id="90749-121">Verifies that a secure authentication channel has been successfully established.</span></span> <span data-ttu-id="90749-122">Esse método não é usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="90749-122">This method is not used by applications.</span></span> |
| <span data-ttu-id="90749-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="90749-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span></span>               | <span data-ttu-id="90749-124">Recupera os níveis de segurança do aplicativo dos componentes locais e remotos.</span><span class="sxs-lookup"><span data-stu-id="90749-124">Retrieves the application security levels of the local and remote components.</span></span>                                             |
| <span data-ttu-id="90749-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90749-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span></span>       | <span data-ttu-id="90749-126">Recupera a chave de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="90749-126">Retrieves the current session key.</span></span> <span data-ttu-id="90749-127">Esse método não é usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="90749-127">This method is not used by applications.</span></span>                                               |
| <span data-ttu-id="90749-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90749-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span></span>                 | <span data-ttu-id="90749-129">Libera o canal do código de autenticação de mensagem (MAC) e recupera um valor MAC final.</span><span class="sxs-lookup"><span data-stu-id="90749-129">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>                                   |
| <span data-ttu-id="90749-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90749-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span></span>                   | <span data-ttu-id="90749-131">Adquire um canal MAC (código de autenticação de mensagens).</span><span class="sxs-lookup"><span data-stu-id="90749-131">Acquires a message authentication code (MAC) channel.</span></span>                                                                     |
| <span data-ttu-id="90749-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90749-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span></span>               | <span data-ttu-id="90749-133">Adiciona um valor a um MAC (código de autenticação de mensagem).</span><span class="sxs-lookup"><span data-stu-id="90749-133">Adds a value to a message authentication code (MAC).</span></span>                                                                      |
| <span data-ttu-id="90749-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="90749-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span></span>     | <span data-ttu-id="90749-135">Especifica o certificado e a chave privada do cliente do (a) canal autenticado seguro (SAC).</span><span class="sxs-lookup"><span data-stu-id="90749-135">Specifies the certificate and private key of the secure authenticated channel (SAC) client.</span></span>                               |
| <span data-ttu-id="90749-136">[**Setinterface**](/previous-versions/bb231595(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90749-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span></span>         | <span data-ttu-id="90749-137">Seleciona a interface usada para comunicações de canal autenticado seguro (SAC).</span><span class="sxs-lookup"><span data-stu-id="90749-137">Selects the interface used for secure authenticated channel (SAC) communications.</span></span>                                         |
| <span data-ttu-id="90749-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="90749-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span></span>       | <span data-ttu-id="90749-139">Define a chave de sessão que é usada para se comunicar com outro componente.</span><span class="sxs-lookup"><span data-stu-id="90749-139">Sets the session key that is used to communicate with another component.</span></span> <span data-ttu-id="90749-140">Esse método não é usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="90749-140">This method is not used by applications.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="90749-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90749-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90749-142">**Classe CSecureChannelServer**</span><span class="sxs-lookup"><span data-stu-id="90749-142">**CSecureChannelServer Class**</span></span>](csecurechannelserver-class.md)
</dt> <dt>

[<span data-ttu-id="90749-143">**Interface IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="90749-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="90749-144">**Interfaces para aplicativos**</span><span class="sxs-lookup"><span data-stu-id="90749-144">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> </dl>

 

 