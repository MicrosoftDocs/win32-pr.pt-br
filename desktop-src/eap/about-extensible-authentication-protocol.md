---
title: Sobre o EAP
description: EAP (Extensible Authentication Protocol), um padrão compatível com muitos componentes de rede da Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocolo de autenticação extensível, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366830"
---
# <a name="about-eap"></a><span data-ttu-id="f6117-104">Sobre o EAP</span><span class="sxs-lookup"><span data-stu-id="f6117-104">About EAP</span></span>

<span data-ttu-id="f6117-105">Este tópico descreve o protocolo EAP (Extensible Authentication Protocol), um padrão compatível com muitos componentes de rede da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f6117-105">This topic describes Extensible Authentication Protocol (EAP), a standard supported by many Microsoft networking components.</span></span>

## <a name="eap-components"></a><span data-ttu-id="f6117-106">Componentes do EAP</span><span class="sxs-lookup"><span data-stu-id="f6117-106">EAP Components</span></span>

<span data-ttu-id="f6117-107">O EAP é crucial para proteger a segurança de LANs sem fio (802.1 X), LANs com fio e dial-up e redes virtuais privadas (VPNs).</span><span class="sxs-lookup"><span data-stu-id="f6117-107">EAP is crucial for protecting the security of wireless (802.1X) LANs, wired LANs, and dial-up and Virtual Private Networks (VPNs).</span></span>

<span data-ttu-id="f6117-108">Os componentes a seguir dão suporte ao protocolo EAP.</span><span class="sxs-lookup"><span data-stu-id="f6117-108">The following components support the EAP protocol.</span></span>

-   <span data-ttu-id="f6117-109">Os clientes e servidores de acesso remoto da Microsoft para dial-up e VPN (PPTP e L2TP/IPSec) implementam o EAP como uma extensão para o PPP.</span><span class="sxs-lookup"><span data-stu-id="f6117-109">Microsoft Remote Access Clients and Servers for both dial-up and VPN (PPTP and L2TP/IPSec) implement EAP as an extension to PPP.</span></span> <span data-ttu-id="f6117-110">Para obter mais informações, consulte [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span><span class="sxs-lookup"><span data-stu-id="f6117-110">For more information, see [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span></span>
-   <span data-ttu-id="f6117-111">Os clientes compatíveis com redes locais com fio e Wireless do Microsoft IEEE 802.1 X e com fio implementam o EAP conforme definido no padrão de rascunho IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="f6117-111">Microsoft IEEE 802.1X compatible wireless and wired LAN clients implement EAP as defined in the IEEE 802.1X draft standard.</span></span>
-   <span data-ttu-id="f6117-112">O servidor RADIUS da Microsoft, chamado IAS (serviço de autenticação da Internet), implementa o EAP conforme definido no [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span><span class="sxs-lookup"><span data-stu-id="f6117-112">Microsoft RADIUS server, called Internet Authentication Service (IAS) implement EAP as defined in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span></span>

<span data-ttu-id="f6117-113">Todos os componentes acima dão suporte a essa arquitetura extensível por meio do SDK (Software Development Kit) do Microsoft Windows, possibilitando a integração de módulos de autenticação de terceiros.</span><span class="sxs-lookup"><span data-stu-id="f6117-113">All of the above components support this extensible architecture through the Microsoft Windows Software Development Kit (SDK), making it possible to integrate third-party authentication modules.</span></span> <span data-ttu-id="f6117-114">Esse mecanismo extensível pode ser usado para dar suporte a placas de token, Kerberos, chave pública e protocolos de autenticação de chave/S.</span><span class="sxs-lookup"><span data-stu-id="f6117-114">This extensible mechanism can be used to support token cards, Kerberos, Public Key, and S/Key authentication protocols.</span></span>

## <a name="protected-extensible-authentication-protocol"></a><span data-ttu-id="f6117-115">Protocolo de autenticação extensível protegida</span><span class="sxs-lookup"><span data-stu-id="f6117-115">Protected Extensible Authentication Protocol</span></span>

<span data-ttu-id="f6117-116">Além do EAP, a implementação sem fio (802.1 X) e o servidor RADIUS também oferecem suporte a um padrão emergente chamado EAP protegido (PEAP).</span><span class="sxs-lookup"><span data-stu-id="f6117-116">In addition to EAP, the wireless (802.1X) implementation and RADIUS server also support an emerging standard called Protected EAP (PEAP).</span></span>

<span data-ttu-id="f6117-117">O PEAP fornece vários serviços importantes para outros protocolos de autenticação EAP, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f6117-117">PEAP provides several key services to other EAP authentication protocols, as follows.</span></span>

-   <span data-ttu-id="f6117-118">O PEAP criptografa pacotes EAP de outros protocolos de autenticação EAP usando o protocolo TLS, uma tecnologia baseada em SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="f6117-118">PEAP encrypts EAP packets of other EAP authentication protocols using Transport Layer Security (TLS), a Secure Socket Layer (SSL) based technology.</span></span> <span data-ttu-id="f6117-119">Para obter mais informações, consulte [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span><span class="sxs-lookup"><span data-stu-id="f6117-119">For more information, see [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span></span>
-   <span data-ttu-id="f6117-120">O PEAP autentica o lado do servidor usando um certificado de servidor, com o servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="f6117-120">PEAP authenticates the server-side using a Server Certificate, with RADIUS server.</span></span>
-   <span data-ttu-id="f6117-121">O PEAP oferece capacidade de reautenticação rápida que dá suporte a roaming eficiente entre dispositivos sem fio.</span><span class="sxs-lookup"><span data-stu-id="f6117-121">PEAP offers fast re-authentication capability that supports efficient roaming between wireless devices.</span></span>
-   <span data-ttu-id="f6117-122">O PEAP gerencia a fragmentação e a remontagem de pacotes EAP.</span><span class="sxs-lookup"><span data-stu-id="f6117-122">PEAP manages the fragmentation and re-assembly of EAP packets.</span></span>
-   <span data-ttu-id="f6117-123">O PEAP gera chaves usadas para criptografar o tráfego sem fio.</span><span class="sxs-lookup"><span data-stu-id="f6117-123">PEAP generates keys used for encrypting wireless traffic.</span></span>

<span data-ttu-id="f6117-124">O PEAP torna muito mais fácil escrever um protocolo EAP, pois o programador não precisa mais resolver esses problemas.</span><span class="sxs-lookup"><span data-stu-id="f6117-124">PEAP makes it much easier to write an EAP protocol because the programmer no longer has to address these issues.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6117-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6117-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6117-126">Sobre o EAP e o EAPHost</span><span class="sxs-lookup"><span data-stu-id="f6117-126">About EAP and EAPHost</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




