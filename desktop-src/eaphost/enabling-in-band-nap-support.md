---
title: Implementando o suporte do In-Band NAP para métodos EAP
description: Pode ser habilitado para métodos de EAP do EAPHost que dão suporte à transmissão de TLVs (objetos de valor-tamanho-de-tipo).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642928"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a><span data-ttu-id="5da35-103">Implementando o suporte do In-Band NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="5da35-103">Implementing In-Band NAP Support for EAP Methods</span></span>

<span data-ttu-id="5da35-104">O suporte à NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ) em banda para um método EAP pode ser habilitado para métodos de EAP do EAPHost que dão suporte à transmissão de TLVs (objetos de valor-comprimento).</span><span class="sxs-lookup"><span data-stu-id="5da35-104">In-band [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) support for an EAP method can be enabled for EAPHost EAP methods that support the transmission of type-length-value objects (TLVs).</span></span> <span data-ttu-id="5da35-105">Quando o suporte a NAP em banda está habilitado, os pacotes NAP são transportados dentro de pacotes de método EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-105">When in-band NAP support is enabled, NAP packets are transported inside EAP method packets.</span></span>

<span data-ttu-id="5da35-106">Por outro lado, quando o suporte a NAP fora de banda está habilitado, a troca de soh ( [instrução NAP de integridade](https://go.microsoft.com/fwlink/p/?linkid=83917) ) ocorre por meio de meios diferentes dos pacotes de método EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-106">In contrast, when out-of-band NAP support is enabled, the NAP [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange occurs through means other than internal to EAP method packets.</span></span>

<span data-ttu-id="5da35-107">Todos os TLVs são específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="5da35-107">All TLVs are vendor specific.</span></span>

## <a name="implementing-nap-support-on-eap-peer-methods"></a><span data-ttu-id="5da35-108">Implementando o suporte a NAP em métodos de pares EAP</span><span class="sxs-lookup"><span data-stu-id="5da35-108">Implementing NAP Support on EAP Peer Methods</span></span>

<span data-ttu-id="5da35-109">A implementação do método EAP peer recebe um TLV que contém o TLV de solicitação soh ( [declaração de integridade](https://go.microsoft.com/fwlink/p/?linkid=83917) ) de um servidor EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-109">The EAP peer method implementation receives a TLV containing the [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) request TLV from an EAP server.</span></span>

<span data-ttu-id="5da35-110">Em seguida, a implementação do método EAP peer passa o TLV que contém o TLV de solicitação SoH para EAPHost da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5da35-110">The EAP peer method implementation then passes the TLV containing the SoH request TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="5da35-111">A implementação do método EAP peer retorna o código de ação [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) para EAPHost no retorno de [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span><span class="sxs-lookup"><span data-stu-id="5da35-111">The EAP peer method implementation returns the action code [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) to EAPHost on return from [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span></span>
-   <span data-ttu-id="5da35-112">O EAPHost chama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) da implementação do método EAP peer.</span><span class="sxs-lookup"><span data-stu-id="5da35-112">EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) from the EAP peer method implementation.</span></span> <span data-ttu-id="5da35-113">Os atributos são passados no processo.</span><span class="sxs-lookup"><span data-stu-id="5da35-113">The attributes are passed in the process.</span></span>
-   <span data-ttu-id="5da35-114">A implementação do método EAP peer retorna o TLV que contém o TLV de solicitação SoH em [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="5da35-114">The EAP peer method implementation returns the TLV containing the SoH request TLV in [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes).</span></span> <span data-ttu-id="5da35-115">Os atributos são recebidos no processo.</span><span class="sxs-lookup"><span data-stu-id="5da35-115">The attributes are received in the process.</span></span>

<span data-ttu-id="5da35-116">A implementação do método EAP peer recebe um TLV que contém um TLV SoH do EAPHost da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5da35-116">The EAP peer method implementation receives a TLV containing an SoH TLV from EAPHost as follows.</span></span>

-   <span data-ttu-id="5da35-117">O EAPHost chama [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) da implementação do método EAP peer.</span><span class="sxs-lookup"><span data-stu-id="5da35-117">EAPHost calls [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) from the EAP peer method implementation.</span></span> <span data-ttu-id="5da35-118">**EapPeerSetResponseAttributes** contém um TLV que hospeda um TLV soh.</span><span class="sxs-lookup"><span data-stu-id="5da35-118">**EapPeerSetResponseAttributes** contains a TLV that houses an SoH TLV.</span></span>
-   <span data-ttu-id="5da35-119">A implementação do método EAP peer envia o TLV SoH para o servidor EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-119">The EAP peer method implementation sends the SoH TLV to the EAP server.</span></span>
-   <span data-ttu-id="5da35-120">A implementação do método EAP peer recebe um TLV que contém um TLV de resposta SoH do servidor EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-120">The EAP peer method implementation receives a TLV containing an SoH response TLV from the EAP server.</span></span>

<span data-ttu-id="5da35-121">A implementação do método EAP peer passa o TLV que contém o TLV de resposta SoH para EAPHost da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5da35-121">The EAP peer method implementation passes the TLV containing the SoH response TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="5da35-122">A implementação do método EAP peer retorna o código de ação **EapPeerMethodResponseActionRespond** para EAPHost no retorno de [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span><span class="sxs-lookup"><span data-stu-id="5da35-122">The EAP peer method implementation returns the action code **EapPeerMethodResponseActionRespond** to EAPHost on return from [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span></span>
-   <span data-ttu-id="5da35-123">O EAPHost chama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) das implementações do método EAP peer.</span><span class="sxs-lookup"><span data-stu-id="5da35-123">EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) from the EAP peer method implementations.</span></span> <span data-ttu-id="5da35-124">A estrutura de [**\_ atributos EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) é passada no processo.</span><span class="sxs-lookup"><span data-stu-id="5da35-124">The [**EAP\_ATTRIBUTES**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) structure is passed in the process.</span></span>
-   <span data-ttu-id="5da35-125">A implementação do método EAP peer retorna o TLV que contém o TLV de resposta SoH em [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="5da35-125">The EAP peer method implementation returns the TLV containing the SoH response TLV in [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).</span></span>

> [!Note]  
> <span data-ttu-id="5da35-126">O membro **eapType** da estrutura [**de \_ atributo do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sempre será definido como **eatEAPTLV** e o **membro de nome da série** apontará para o primeiro byte do TLV que contém o TLV de resposta soh.</span><span class="sxs-lookup"><span data-stu-id="5da35-126">The **eapType** member of the [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure will always be set to **eatEAPTLV** and the **pValue** member will point to the first byte of the TLV that contains the SoH response TLV.</span></span>

 

### <a name="implementing-nap-support-on-eap-server-methods"></a><span data-ttu-id="5da35-127">Implementando o suporte a NAP em métodos de servidor EAP</span><span class="sxs-lookup"><span data-stu-id="5da35-127">Implementing NAP Support on EAP Server Methods</span></span>

<span data-ttu-id="5da35-128">A implementação do método de servidor EAP constrói um TLV que contém um TLV de solicitação SoH.</span><span class="sxs-lookup"><span data-stu-id="5da35-128">The EAP server method implementation constructs a TLV containing an SoH request TLV.</span></span> <span data-ttu-id="5da35-129">A implementação do método de servidor EAP envia esse TLV contendo o TLV de solicitação SoH para o par EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-129">The EAP server method implementation sends this TLV containing the SoH Request TLV to the EAP peer.</span></span> <span data-ttu-id="5da35-130">A implementação do método de servidor EAP recebe o TLV do ponto EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-130">The EAP server method implementation receives the TLV from the EAP peer.</span></span>

<span data-ttu-id="5da35-131">A implementação do método de servidor EAP passa o TLV que contém um TLV SoH para o EAPHost da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5da35-131">The EAP server method implementation passes the TLV containing an SoH TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="5da35-132">A implementação do método do servidor EAP retorna a **resposta do autenticador do método EAP do código de ação \_ \_ \_ \_ responderá** a EAPHost no retorno de [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).</span><span class="sxs-lookup"><span data-stu-id="5da35-132">The EAP server method implementation returns the action code **EAP\_METHOD\_AUTHENTICATOR\_RESPONSE\_RESPOND** to EAPHost on return from [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).</span></span>
-   <span data-ttu-id="5da35-133">O EAPHost chama [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) da implementação do método de servidor EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-133">EAPHost calls [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) from the EAP server method implementation.</span></span>
-   <span data-ttu-id="5da35-134">A implementação do método de servidor EAP retorna o TLV que contém o TLV SoH em [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).</span><span class="sxs-lookup"><span data-stu-id="5da35-134">The EAP server method implementation returns the TLV containing the SoH TLV in [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).</span></span>

<span data-ttu-id="5da35-135">A implementação do método de servidor EAP recebe um TLV que contém um TLV de resposta SoH do EAPHost da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5da35-135">The EAP server method implementation receives a TLV containing an SoH response TLV from EAPHost as follows.</span></span>

-   <span data-ttu-id="5da35-136">O EAPHost chama [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) da implementação do método de servidor EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-136">EAPHost calls [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) from the EAP server method implementation.</span></span>
-   <span data-ttu-id="5da35-137">O TLV que contém o TLV de resposta SoH é retornado em [ **EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)</span><span class="sxs-lookup"><span data-stu-id="5da35-137">The TLV containing the SoH response TLV is returned in [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)</span></span>
-   <span data-ttu-id="5da35-138">A implementação do método de servidor EAP envia o TLV que contém o TLV de resposta SoH.</span><span class="sxs-lookup"><span data-stu-id="5da35-138">The EAP server method implementation sends the TLV containing the SoH response TLV.</span></span>

> [!Note]  
> <span data-ttu-id="5da35-139">O membro **eapType** da estrutura [**de \_ atributo do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sempre será definido como **eatEAPTLV** e o **membro de nome da série** apontará para o primeiro byte do TLV que contém o TLV de resposta soh.</span><span class="sxs-lookup"><span data-stu-id="5da35-139">The **eapType** member of the [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure will always be set to **eatEAPTLV** and the **pValue** member will point to the first byte of the TLV that contains the SoH response TLV.</span></span>

 

### <a name="messages"></a><span data-ttu-id="5da35-140">Mensagens</span><span class="sxs-lookup"><span data-stu-id="5da35-140">Messages</span></span>

<span data-ttu-id="5da35-141">O TLV de SoH EAP é usado para encapsular o protocolo SoH para transmissão por meio de um método EAP.</span><span class="sxs-lookup"><span data-stu-id="5da35-141">The EAP SoH TLV is used to encapsulate the SoH protocol for transmission via an EAP method.</span></span> <span data-ttu-id="5da35-142">Todos os TLVs de SoH do EAP têm a mesma estrutura, diferente somente na ID da mensagem e na parte de dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5da35-142">All EAP SoH TLVs have the same structure, differing only on the message ID and data portion of the message.</span></span>

<span data-ttu-id="5da35-143">Para obter mais informações, consulte [mensagens de soh (proteção de acesso à rede)](https://go.microsoft.com/fwlink/p/?linkid=83918).</span><span class="sxs-lookup"><span data-stu-id="5da35-143">For more information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5da35-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5da35-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5da35-145">Configurando a interface do usuário do método EAP</span><span class="sxs-lookup"><span data-stu-id="5da35-145">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="5da35-146">Habilitando Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="5da35-146">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="5da35-147">Implementando o suporte a NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="5da35-147">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="5da35-148">Transferindo dados entre os métodos suplicante e EAP</span><span class="sxs-lookup"><span data-stu-id="5da35-148">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="5da35-149">Suplicantes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="5da35-149">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 