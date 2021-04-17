---
title: Autenticação (Windows Media Format 11 SDK)
description: Autenticação
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- SDK do Windows Media Format, autenticação
- SDK do Windows Media Format, autenticação de rede
- ASF (Advanced Systems Format), autenticação
- ASF (formato de sistemas avançados), autenticação
- ASF (Advanced Systems Format), autenticação de rede
- ASF (formato de sistemas avançados), autenticação de rede
- autenticação
- autenticação de rede, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105798390"
---
# <a name="authentication-windows-media-format-11-sdk"></a><span data-ttu-id="da8a2-111">Autenticação (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="da8a2-111">Authentication (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="da8a2-112">O objeto leitor pode lidar com desafios de autenticação de rede, incluindo autenticação Digest e autenticação NTLM.</span><span class="sxs-lookup"><span data-stu-id="da8a2-112">The reader object can handle network authentication challenges, including digest authentication and NTLM authentication.</span></span> <span data-ttu-id="da8a2-113">Em alguns casos, o aplicativo deve fornecer as credenciais do usuário por meio de uma interface de retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="da8a2-113">In some cases the application must provide the user's credentials through a callback interface:</span></span>

-   <span data-ttu-id="da8a2-114">Autenticação Digest: o aplicativo deve implementar a interface **IWMCredentialCallback** , conforme descrito posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="da8a2-114">Digest authentication: The application must implement the **IWMCredentialCallback** interface, as described later in this topic.</span></span>
-   <span data-ttu-id="da8a2-115">Autenticação NTLM: o leitor responde automaticamente com as credenciais de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="da8a2-115">NTLM authentication: The reader automatically responds with the user's logon credentials.</span></span> <span data-ttu-id="da8a2-116">Se o usuário atual estiver autorizado a fazer logon no servidor, o aplicativo não precisará fazer nada.</span><span class="sxs-lookup"><span data-stu-id="da8a2-116">If the current user is authorized to log on to the server, the application does not have to do anything.</span></span> <span data-ttu-id="da8a2-117">Se o usuário não tiver autorização, o aplicativo deverá implementar a interface **IWMCredentialCallback** .</span><span class="sxs-lookup"><span data-stu-id="da8a2-117">If the user does not have authorization, the application must implement the **IWMCredentialCallback** interface.</span></span>

    > [!Note]  
    > <span data-ttu-id="da8a2-118">O Windows Media Services versão 4,1 não oferece suporte à autenticação NTLM por meio de um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="da8a2-118">Windows Media Services version 4.1 does not support NTLM authentication through a proxy server.</span></span> <span data-ttu-id="da8a2-119">A autenticação NTLM requer várias trocas de cliente/servidor na mesma conexão, e a versão 4,1 não mantém uma conexão persistente com o proxy.</span><span class="sxs-lookup"><span data-stu-id="da8a2-119">NTLM authentication requires several client-server exchanges on the same connection, and version 4.1 does not keep a persistent connection with the proxy.</span></span> <span data-ttu-id="da8a2-120">O Windows Media Services 9 Series no Microsoft Windows Server 2003 dá suporte à autenticação NTLM por meio de um servidor proxy, desde que o proxy dê suporte a conexões Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="da8a2-120">Windows Media Services 9 Series in Microsoft Windows Server 2003 supports NTLM authentication through a proxy server, as long as the proxy supports keep-alive connections.</span></span>

     

<span data-ttu-id="da8a2-121">Como observado, em alguns casos, o aplicativo deve fornecer as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="da8a2-121">As noted, in some cases the application must provide the user's credentials.</span></span> <span data-ttu-id="da8a2-122">Isso ocorre por meio da interface **IWMCredentialCallback** , que tem um único método, **AcquireCredentials**.</span><span class="sxs-lookup"><span data-stu-id="da8a2-122">This occurs through the **IWMCredentialCallback** interface, which has a single method, **AcquireCredentials**.</span></span> <span data-ttu-id="da8a2-123">Para dar suporte à autenticação, implemente essa interface em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="da8a2-123">To support authentication, implement this interface in your application.</span></span> <span data-ttu-id="da8a2-124">O objeto de leitor consulta essa interface chamando **QueryInterface** no ponteiro [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) recebido do aplicativo no método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="da8a2-124">The reader object queries for this interface by calling **QueryInterface** on the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) pointer that it received from the application in the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span> <span data-ttu-id="da8a2-125">Se o objeto do leitor precisar obter as credenciais do usuário, ele chamará o método **AcquireCredentials** do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="da8a2-125">If the reader object needs to get the user's credentials, it calls the application's **AcquireCredentials** method.</span></span>

<span data-ttu-id="da8a2-126">Se as credenciais forem enviadas pela rede sem criptografia, o leitor definirá o sinalizador de \_ texto não criptografado da credencial WMT \_ \_ no parâmetro *pdwFlags* .</span><span class="sxs-lookup"><span data-stu-id="da8a2-126">If the credentials will be sent over the network without encryption, the reader sets the WMT\_CREDENTIAL\_CLEAR\_TEXT flag in the *pdwFlags* parameter.</span></span> <span data-ttu-id="da8a2-127">Isso dá ao aplicativo uma oportunidade de avisar ao usuário que suas credenciais serão enviadas em texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="da8a2-127">This gives the application an opportunity to warn the user that his or her credentials will be sent in plain text.</span></span>

<span data-ttu-id="da8a2-128">Caso contrário, o objeto leitor criptografará automaticamente as credenciais antes de enviá-las pela rede.</span><span class="sxs-lookup"><span data-stu-id="da8a2-128">Otherwise, the reader object automatically encrypts the credentials before sending them over the network.</span></span> <span data-ttu-id="da8a2-129">O aplicativo pode retorná-los ao objeto leitor em texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="da8a2-129">The application can return them to the reader object in plain text.</span></span> <span data-ttu-id="da8a2-130">Além disso, se o objeto do leitor definir o \_ sinalizador de criptografia de credencial WMT \_ , isso significará que o leitor dá suporte a obter credenciais criptografadas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="da8a2-130">In addition, if the reader object sets the WMT\_CREDENTIAL\_ENCRYPT flag, it means the reader supports getting encrypted credentials from the application.</span></span> <span data-ttu-id="da8a2-131">Nesse caso, o aplicativo pode retornar as credenciais em texto sem formatação ou, caso contrário, criptografá-las usando a função **CryptProtectData** , que é descrita na documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="da8a2-131">In that case, the application can either return the credentials in plain text, or else encrypt them itself using the **CryptProtectData** function, which is described in the Platform SDK documentation.</span></span> <span data-ttu-id="da8a2-132">Se o aplicativo criptografar as credenciais, ele deverá definir o \_ sinalizador de criptografia de credencial WMT \_ no parâmetro *pdwFlags* antes que o método retorne.</span><span class="sxs-lookup"><span data-stu-id="da8a2-132">If the application encrypts the credentials, it must set the WMT\_CREDENTIAL\_ENCRYPT flag in the *pdwFlags* parameter before the method returns.</span></span>

<span data-ttu-id="da8a2-133">Em geral, não é necessário criptografar os dados, pois o objeto leitor criptografa os dados, se necessário.</span><span class="sxs-lookup"><span data-stu-id="da8a2-133">Generally, it is not necessary to encrypt the data, because the reader object encrypts the data if necessary.</span></span> <span data-ttu-id="da8a2-134">No entanto, a criptografia poderá ser útil se o aplicativo mantiver o nome de usuário e a senha na memória, pois impede que um invasor Inspecione um despejo de memória do processo.</span><span class="sxs-lookup"><span data-stu-id="da8a2-134">However, encryption might be useful if the application keeps the user name and password in memory, because it prevents an attacker from inspecting a memory dump of the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da8a2-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da8a2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da8a2-136">**Interface IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="da8a2-136">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[<span data-ttu-id="da8a2-137">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="da8a2-137">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




