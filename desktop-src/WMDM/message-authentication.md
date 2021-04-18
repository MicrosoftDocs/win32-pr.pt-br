---
title: Autenticação de mensagens
description: Autenticação de mensagens
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Windows Media Gerenciador de Dispositivos, autenticação de mensagem
- Gerenciador de Dispositivos, autenticação de mensagem
- aplicativos de desktop, autenticação de mensagens
- provedores de serviços, autenticação de mensagens
- Guia de programação, autenticação de mensagens
- autenticação de mensagens
- código de autenticação de mensagem (MAC)
- MAC (código de autenticação de mensagem)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763391"
---
# <a name="message-authentication"></a><span data-ttu-id="284af-111">Autenticação de mensagens</span><span class="sxs-lookup"><span data-stu-id="284af-111">Message Authentication</span></span>

<span data-ttu-id="284af-112">A autenticação de mensagens é um processo que permite que aplicativos e provedores de serviços verifiquem se os dados passados entre eles não foram adulterados.</span><span class="sxs-lookup"><span data-stu-id="284af-112">Message authentication is a process that enables applications and service providers to verify that data passed between them has not been tampered with.</span></span> <span data-ttu-id="284af-113">O Windows Media Gerenciador de Dispositivos permite que aplicativos e provedores de serviço executem a autenticação de mensagens usando MACs (códigos de autenticação de mensagens).</span><span class="sxs-lookup"><span data-stu-id="284af-113">Windows Media Device Manager allows applications and service providers to perform message authentication by using message authentication codes (MACs).</span></span> <span data-ttu-id="284af-114">Veja como funciona a autenticação MAC:</span><span class="sxs-lookup"><span data-stu-id="284af-114">Here is how MAC authentication works:</span></span>

<span data-ttu-id="284af-115">O remetente dos dados, geralmente o provedor de serviços, passa uma ou mais partes de dados por meio de uma função criptográfica unidirecional que produz uma única assinatura, o MAC, para todos os dados.</span><span class="sxs-lookup"><span data-stu-id="284af-115">The data sender, usually the service provider, passes one or more pieces of data through a one-way cryptographic function that produces a single signature, the MAC, for all the data.</span></span> <span data-ttu-id="284af-116">O remetente envia, então, todos os pedaços de dados assinados com o MAC para o receptor (geralmente o aplicativo).</span><span class="sxs-lookup"><span data-stu-id="284af-116">The sender then sends all the signed pieces of data together with the MAC to the receiver (usually the application).</span></span> <span data-ttu-id="284af-117">O receptor passa os dados por meio da mesma função criptográfica para gerar um MAC e o compara com o MAC que foi enviado.</span><span class="sxs-lookup"><span data-stu-id="284af-117">The receiver passes the data through the same cryptographic function to generate a MAC and compares it to the MAC that was sent.</span></span> <span data-ttu-id="284af-118">Se o MAC corresponder, os dados não foram modificados.</span><span class="sxs-lookup"><span data-stu-id="284af-118">If the MAC matches, the data has not been modified.</span></span>

<span data-ttu-id="284af-119">Para executar a autenticação MAC, o aplicativo ou o provedor de serviços requer uma chave de criptografia e um certificado correspondente.</span><span class="sxs-lookup"><span data-stu-id="284af-119">To perform MAC authentication, the application or service provider requires an encryption key and a matching certificate.</span></span> <span data-ttu-id="284af-120">Para obter informações sobre onde obter esses, consulte [ferramentas para desenvolvimento](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="284af-120">For information on where to get these, see [Tools for Development](tools-for-development.md).</span></span>

<span data-ttu-id="284af-121">As etapas a seguir descrevem como os dados são assinados pelo remetente e, posteriormente, verificados pelo receptor.</span><span class="sxs-lookup"><span data-stu-id="284af-121">The following steps describe how data is signed by the sender, and later checked by the receiver.</span></span> <span data-ttu-id="284af-122">No Windows Media Gerenciador de Dispositivos, o provedor de serviços usa a classe [CSecureChannelServer](csecurechannelserver-class.md) para gerar Macs e o aplicativo usa a classe [CSecureChannelClient](csecurechannelclient-class.md) .</span><span class="sxs-lookup"><span data-stu-id="284af-122">In Windows Media Device Manager, the service provider uses the [CSecureChannelServer](csecurechannelserver-class.md) class to generate MACs, and the application uses the [CSecureChannelClient](csecurechannelclient-class.md) class.</span></span> <span data-ttu-id="284af-123">Ambas as classes fornecem funções idênticas com parâmetros idênticos, portanto, as etapas a seguir se aplicam a ambas as classes.</span><span class="sxs-lookup"><span data-stu-id="284af-123">Both classes provide identical functions with identical parameters, so the following steps apply to both classes.</span></span>

<span data-ttu-id="284af-124">O remetente (normalmente o provedor de serviços):</span><span class="sxs-lookup"><span data-stu-id="284af-124">The sender (typically the service provider):</span></span>

1.  <span data-ttu-id="284af-125">Obter os dados a serem assinados.</span><span class="sxs-lookup"><span data-stu-id="284af-125">Get the data to be signed.</span></span>
2.  <span data-ttu-id="284af-126">Crie um novo identificador de MAC chamando **MACInit**.</span><span class="sxs-lookup"><span data-stu-id="284af-126">Create a new MAC handle by calling **MACInit**.</span></span>
3.  <span data-ttu-id="284af-127">Adicione uma parte dos dados a serem assinados para o identificador chamando **MACUpdate**.</span><span class="sxs-lookup"><span data-stu-id="284af-127">Add a piece of data to be signed to the handle by calling **MACUpdate**.</span></span> <span data-ttu-id="284af-128">Essa função aceita o identificador criado anteriormente, além de uma parte dos dados que devem ser assinados.</span><span class="sxs-lookup"><span data-stu-id="284af-128">This function accepts the previously created handle, plus a piece of data that must be signed.</span></span>
4.  <span data-ttu-id="284af-129">Repita a etapa 3 com cada parte adicional dos dados que devem ser assinados.</span><span class="sxs-lookup"><span data-stu-id="284af-129">Repeat step 3 with each additional piece of data that must be signed.</span></span> <span data-ttu-id="284af-130">Não importa quais dados de ordem são adicionados ao MAC.</span><span class="sxs-lookup"><span data-stu-id="284af-130">It does not matter in what order data is added to the MAC.</span></span>
5.  <span data-ttu-id="284af-131">Copie o MAC do identificador para um novo buffer de bytes chamando **MACFinal**.</span><span class="sxs-lookup"><span data-stu-id="284af-131">Copy the MAC from the handle to a new byte buffer by calling **MACFinal**.</span></span> <span data-ttu-id="284af-132">Essa função aceita o identificador de MAC e um buffer que você aloca e copia o MAC do identificador para o buffer fornecido.</span><span class="sxs-lookup"><span data-stu-id="284af-132">This function accepts the MAC handle and a buffer that you allocate, and copies the MAC from the handle into the provided buffer.</span></span>

<span data-ttu-id="284af-133">Ao executar a autenticação MAC, é importante que o remetente e o destinatário estejam colocando os mesmos dados no MAC.</span><span class="sxs-lookup"><span data-stu-id="284af-133">When performing MAC authentication, it is important that both the sender and the receiver are putting the same data into the MAC.</span></span> <span data-ttu-id="284af-134">Para os métodos de aplicativo que fornecem um MAC, normalmente todos os parâmetros são incluídos no valor de MAC (exceto para o próprio MAC, é claro).</span><span class="sxs-lookup"><span data-stu-id="284af-134">For the application methods that provide a MAC, typically all parameters are included in the MAC value (except for the MAC itself, of course).</span></span> <span data-ttu-id="284af-135">Por exemplo, considere o método **IWMDMOperation:: TransferObjectData** :</span><span class="sxs-lookup"><span data-stu-id="284af-135">For example, consider the **IWMDMOperation::TransferObjectData** method:</span></span>

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

<span data-ttu-id="284af-136">Nesse método, o MAC inclui *pData* e *pdwSize*.</span><span class="sxs-lookup"><span data-stu-id="284af-136">In this method, the MAC would include *pData* and *pdwSize*.</span></span> <span data-ttu-id="284af-137">Se você não incluir os dois parâmetros, o MAC que você criar não corresponderá ao MAC passado para *abMac*.</span><span class="sxs-lookup"><span data-stu-id="284af-137">If you do not include both the parameters, the MAC you create will not match the MAC passed to *abMac*.</span></span> <span data-ttu-id="284af-138">Um provedor de serviços deve ter certeza de colocar todos os parâmetros necessários no método de aplicativo no valor MAC.</span><span class="sxs-lookup"><span data-stu-id="284af-138">A service provider must be sure to put all the required parameters in the application method into the MAC value.</span></span>

<span data-ttu-id="284af-139">O código C++ a seguir demonstra como criar um MAC na implementação de um provedor de serviço de [**IMDSPStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span><span class="sxs-lookup"><span data-stu-id="284af-139">The following C++ code demonstrates creating a MAC in a service provider's implementation of [**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span></span>


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



<span data-ttu-id="284af-140">O receptor (normalmente o aplicativo):</span><span class="sxs-lookup"><span data-stu-id="284af-140">The receiver (typically the application):</span></span>

<span data-ttu-id="284af-141">Se o receptor não tiver implementado a interface [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , ele deverá executar as mesmas etapas que o remetente e, em seguida, comparar os dois valores Mac.</span><span class="sxs-lookup"><span data-stu-id="284af-141">If the receiver has not implemented the [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) interface, it should perform the same steps as the sender, and then compare the two MAC values.</span></span> <span data-ttu-id="284af-142">O exemplo de código C++ a seguir mostra como um aplicativo verificaria o MAC recebido em uma chamada para [**IWMDMStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) para garantir que o número de série não foi violado em trânsito.</span><span class="sxs-lookup"><span data-stu-id="284af-142">The following C++ code example shows how an application would check the MAC received in a call to [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) to ensure that the serial number was not tampered with in transit.</span></span>


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="284af-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="284af-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="284af-144">**Usando canais autenticados seguros**</span><span class="sxs-lookup"><span data-stu-id="284af-144">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




