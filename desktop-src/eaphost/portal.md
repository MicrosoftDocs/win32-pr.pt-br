---
title: Host do protocolo de autenticação extensível
description: Saiba mais sobre o host EAP (Extensible Authentication Protocol). Consulte requisitos de tempo de execução e exiba recursos adicionais disponíveis.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104085020"
---
# <a name="extensible-authentication-protocol-host"></a><span data-ttu-id="1f0a7-104">Host do protocolo de autenticação extensível</span><span class="sxs-lookup"><span data-stu-id="1f0a7-104">Extensible Authentication Protocol Host</span></span>

## <a name="purpose"></a><span data-ttu-id="1f0a7-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="1f0a7-105">Purpose</span></span>


<span data-ttu-id="1f0a7-106">O EAPHost é um componente de rede do Microsoft Windows que fornece uma infraestrutura EAP (Extensible Authentication Protocol) para a autenticação de implementações de protocolo "suplicante", como [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) e [ponto a ponto](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span><span class="sxs-lookup"><span data-stu-id="1f0a7-106">EAPHost is a Microsoft Windows Networking component that provides an Extensible Authentication Protocol (EAP) infrastructure for the authentication of "supplicant" protocol implementations such as [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) and [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span></span> <span data-ttu-id="1f0a7-107">Ele também permite a autenticação com tecnologias "autenticador", como o Microsoft Network Policy Server (NPS).</span><span class="sxs-lookup"><span data-stu-id="1f0a7-107">It also allows for authentication with "authenticator" technologies such as the Microsoft network policy server (NPS).</span></span> <span data-ttu-id="1f0a7-108">Ao contrário do servidor IAS anterior ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), o NPS dá suporte à NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ).</span><span class="sxs-lookup"><span data-stu-id="1f0a7-108">Unlike the previous IAS Server ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS supports [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span></span>


<span data-ttu-id="1f0a7-109">As APIs do EAPHost permitem que os aplicativos se autentiquem usando o serviço EAPHost e forneçam um modelo para o desenvolvimento de métodos de autenticação em conformidade para uso com o EAPHost.</span><span class="sxs-lookup"><span data-stu-id="1f0a7-109">The EAPHost APIs enable applications to authenticate using the EAPHost service, and provide a template for the development of conformant authentication methods for use with EAPHost.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1f0a7-110">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="1f0a7-110">Run-time requirements</span></span>

<span data-ttu-id="1f0a7-111">As APIs do EAPHost têm suporte apenas no Windows Vista e sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="1f0a7-111">The EAPHost APIs are supported only in Windows Vista and later operating systems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f0a7-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f0a7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f0a7-113">Sobre o EAPHost</span><span class="sxs-lookup"><span data-stu-id="1f0a7-113">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="1f0a7-114">Usando o EAPHost</span><span class="sxs-lookup"><span data-stu-id="1f0a7-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="1f0a7-115">Referência da API EAPHost</span><span class="sxs-lookup"><span data-stu-id="1f0a7-115">EAPHost API Reference</span></span>](eaphost-api-reference.md)
</dt> </dl>

 

 