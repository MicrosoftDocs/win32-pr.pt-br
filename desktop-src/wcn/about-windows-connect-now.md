---
title: Sobre o Windows Connect agora
description: O WCN (Windows Connect Now) fornece um mecanismo simples e seguro para dispositivos e pontos de acesso à rede (como impressoras, câmera e computadores) para conexão e troca de configurações.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084816"
---
# <a name="about-windows-connect-now"></a><span data-ttu-id="ce824-103">Sobre o Windows Connect agora</span><span class="sxs-lookup"><span data-stu-id="ce824-103">About Windows Connect Now</span></span>

<span data-ttu-id="ce824-104">O WCN (Windows Connect Now) fornece um mecanismo simples e seguro para dispositivos e pontos de acesso à rede (como impressoras, câmera e computadores) para conexão e troca de configurações.</span><span class="sxs-lookup"><span data-stu-id="ce824-104">Windows Connect Now (WCN) provides a simple and secure mechanism for network access points and devices (like printers, camera, and PCs) to connect and exchange settings.</span></span> <span data-ttu-id="ce824-105">Essa API é a implementação da Microsoft do protocolo/Wi-Fi (configuração protegida Wi-Fi) (WSC), que foi criado pela Aliança de Wi-Fi como uma solução para redes domésticas e pequenas empresas.</span><span class="sxs-lookup"><span data-stu-id="ce824-105">This API is the Microsoft implementation of the Wi-Fi Protected Setup (WPS)/Wi-Fi Simple Configuration (WSC) protocol, which was created by the Wi-Fi Alliance as a solution for home networking and small businesses.</span></span> <span data-ttu-id="ce824-106">Essa tecnologia não se destina a cenários empresariais.</span><span class="sxs-lookup"><span data-stu-id="ce824-106">This technology is not intended for enterprise scenarios.</span></span>

> [!Note]  
> <span data-ttu-id="ce824-107">O nome da especificação foi alterado entre a versão 1.0 h e a versão 2.</span><span class="sxs-lookup"><span data-stu-id="ce824-107">The specification name changed between version 1.0h and version 2.</span></span> <span data-ttu-id="ce824-108">A especificação da versão 1.0 h foi denominada Wi-Fi configuração protegida (WPS).</span><span class="sxs-lookup"><span data-stu-id="ce824-108">The version 1.0h specification was named Wi-Fi Protected Setup (WPS).</span></span> <span data-ttu-id="ce824-109">A partir da especificação da versão 2, a especificação é chamada de Wi-Fi configuração simples (WSC).</span><span class="sxs-lookup"><span data-stu-id="ce824-109">Starting with version 2 specification, the specification is named Wi-Fi Simple Configuration (WSC).</span></span> <span data-ttu-id="ce824-110">Em nossa documentação, os termos WPS e WSC são usados de maneira intercambiável, a menos que sejam indicados.</span><span class="sxs-lookup"><span data-stu-id="ce824-110">In our documentation, the terms WPS and WSC are used interchangeably unless noted.</span></span>

 

<span data-ttu-id="ce824-111">Agora, o Windows Connect permite que os aplicativos pesquisem dispositivos compatíveis com WCN usando a [API de descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal).</span><span class="sxs-lookup"><span data-stu-id="ce824-111">Windows Connect Now enables applications to search for WCN-capable devices using the [Function Discovery API](/previous-versions/windows/desktop/fundisc/fd-portal).</span></span> <span data-ttu-id="ce824-112">O escopo de uma pesquisa pode ser limitado a um SSID, estado, categoria ou até mesmo ampliado para incluir todos os dispositivos compatíveis com o WCN.</span><span class="sxs-lookup"><span data-stu-id="ce824-112">The scope of a search can be narrowed down to a specific SSID, state, category, or even broadened to include all WCN-capable devices.</span></span> <span data-ttu-id="ce824-113">Depois que os dispositivos são localizados, a API WCN permite a comunicação com o dispositivo compatível com WCN para facilitar a configuração ou a conectividade.</span><span class="sxs-lookup"><span data-stu-id="ce824-113">Once devices are located, the WCN API allows communication with the WCN-capable device in order to facilitate configuration or connectivity.</span></span>

 

 