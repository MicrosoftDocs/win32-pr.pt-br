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
# <a name="message-authentication"></a>Autenticação de mensagens

A autenticação de mensagens é um processo que permite que aplicativos e provedores de serviços verifiquem se os dados passados entre eles não foram adulterados. O Windows Media Gerenciador de Dispositivos permite que aplicativos e provedores de serviço executem a autenticação de mensagens usando MACs (códigos de autenticação de mensagens). Veja como funciona a autenticação MAC:

O remetente dos dados, geralmente o provedor de serviços, passa uma ou mais partes de dados por meio de uma função criptográfica unidirecional que produz uma única assinatura, o MAC, para todos os dados. O remetente envia, então, todos os pedaços de dados assinados com o MAC para o receptor (geralmente o aplicativo). O receptor passa os dados por meio da mesma função criptográfica para gerar um MAC e o compara com o MAC que foi enviado. Se o MAC corresponder, os dados não foram modificados.

Para executar a autenticação MAC, o aplicativo ou o provedor de serviços requer uma chave de criptografia e um certificado correspondente. Para obter informações sobre onde obter esses, consulte [ferramentas para desenvolvimento](tools-for-development.md).

As etapas a seguir descrevem como os dados são assinados pelo remetente e, posteriormente, verificados pelo receptor. No Windows Media Gerenciador de Dispositivos, o provedor de serviços usa a classe [CSecureChannelServer](csecurechannelserver-class.md) para gerar Macs e o aplicativo usa a classe [CSecureChannelClient](csecurechannelclient-class.md) . Ambas as classes fornecem funções idênticas com parâmetros idênticos, portanto, as etapas a seguir se aplicam a ambas as classes.

O remetente (normalmente o provedor de serviços):

1.  Obter os dados a serem assinados.
2.  Crie um novo identificador de MAC chamando **MACInit**.
3.  Adicione uma parte dos dados a serem assinados para o identificador chamando **MACUpdate**. Essa função aceita o identificador criado anteriormente, além de uma parte dos dados que devem ser assinados.
4.  Repita a etapa 3 com cada parte adicional dos dados que devem ser assinados. Não importa quais dados de ordem são adicionados ao MAC.
5.  Copie o MAC do identificador para um novo buffer de bytes chamando **MACFinal**. Essa função aceita o identificador de MAC e um buffer que você aloca e copia o MAC do identificador para o buffer fornecido.

Ao executar a autenticação MAC, é importante que o remetente e o destinatário estejam colocando os mesmos dados no MAC. Para os métodos de aplicativo que fornecem um MAC, normalmente todos os parâmetros são incluídos no valor de MAC (exceto para o próprio MAC, é claro). Por exemplo, considere o método **IWMDMOperation:: TransferObjectData** :

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

Nesse método, o MAC inclui *pData* e *pdwSize*. Se você não incluir os dois parâmetros, o MAC que você criar não corresponderá ao MAC passado para *abMac*. Um provedor de serviços deve ter certeza de colocar todos os parâmetros necessários no método de aplicativo no valor MAC.

O código C++ a seguir demonstra como criar um MAC na implementação de um provedor de serviço de [**IMDSPStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).


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



O receptor (normalmente o aplicativo):

Se o receptor não tiver implementado a interface [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , ele deverá executar as mesmas etapas que o remetente e, em seguida, comparar os dois valores Mac. O exemplo de código C++ a seguir mostra como um aplicativo verificaria o MAC recebido em uma chamada para [**IWMDMStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) para garantir que o número de série não foi violado em trânsito.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando canais autenticados seguros**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




