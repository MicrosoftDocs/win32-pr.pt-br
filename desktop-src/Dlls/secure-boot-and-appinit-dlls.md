---
description: A partir do Windows 8, a \_ infraestrutura AppInit DLLs é desabilitada quando a inicialização segura está habilitada.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit DLLs e inicialização segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759423"
---
# <a name="appinit-dlls-and-secure-boot"></a><span data-ttu-id="44588-103">AppInit DLLs e inicialização segura</span><span class="sxs-lookup"><span data-stu-id="44588-103">AppInit DLLs and Secure Boot</span></span>

<span data-ttu-id="44588-104">A partir do Windows 8, a \_ infraestrutura AppInit DLLs é desabilitada quando a inicialização segura está habilitada.</span><span class="sxs-lookup"><span data-stu-id="44588-104">Starting in Windows 8, the AppInit\_DLLs infrastructure is disabled when secure boot is enabled.</span></span>

## <a name="about-appinit_dlls"></a><span data-ttu-id="44588-105">Sobre \_ DLLs AppInit</span><span class="sxs-lookup"><span data-stu-id="44588-105">About AppInit\_DLLs</span></span>

<span data-ttu-id="44588-106">A \_ infraestrutura AppInit DLLs fornece uma maneira fácil de conectar APIs do sistema, permitindo que DLLs personalizadas sejam carregadas no espaço de endereço de cada aplicativo interativo.</span><span class="sxs-lookup"><span data-stu-id="44588-106">The AppInit\_DLLs infrastructure provides an easy way to hook system APIs by allowing custom DLLs to be loaded into the address space of every interactive application.</span></span> <span data-ttu-id="44588-107">Os aplicativos e os softwares mal-intencionados usam DLLs AppInit para o mesmo motivo básico, que é vincular APIs; Depois que a DLL personalizada é carregada, ela pode conectar uma API do sistema conhecida e implementar a funcionalidade alternativa.</span><span class="sxs-lookup"><span data-stu-id="44588-107">Applications and malicious software both use AppInit DLLs for the same basic reason, which is to hook APIs; after the custom DLL is loaded, it can hook a well-known system API and implement alternate functionality.</span></span> <span data-ttu-id="44588-108">Apenas um pequeno conjunto de aplicativos legítimos modernos usa esse mecanismo para carregar DLLs, enquanto um grande conjunto de malwares usa esse mecanismo para comprometer sistemas.</span><span class="sxs-lookup"><span data-stu-id="44588-108">Only a small set of modern legitimate applications use this mechanism to load DLLs, while a large set of malware use this mechanism to compromise systems.</span></span> <span data-ttu-id="44588-109">Até mesmo as DLLs AppInit legítimas \_ podem causar problemas de desempenho e deadlocks do sistema, portanto, o uso de \_ DLLs AppInit não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="44588-109">Even legitimate AppInit\_DLLs can unintentionally cause system deadlocks and performance problems, therefore usage of AppInit\_DLLs is not recommended.</span></span>

## <a name="appinit_dlls-and-secure-boot"></a><span data-ttu-id="44588-110">AppInit \_ DLLs e inicialização segura</span><span class="sxs-lookup"><span data-stu-id="44588-110">AppInit\_DLLs and secure boot</span></span>

<span data-ttu-id="44588-111">O Windows 8 adotou a UEFI e a inicialização segura para melhorar a integridade geral do sistema e para fornecer proteção forte contra ameaças sofisticadas.</span><span class="sxs-lookup"><span data-stu-id="44588-111">Windows 8 adopted UEFI and secure boot to improve the overall system integrity and to provide strong protection against sophisticated threats.</span></span> <span data-ttu-id="44588-112">Quando a inicialização segura está habilitada, o \_ mecanismo de DLLs AppInit é desabilitado como parte de uma abordagem sem comprometimento para proteger os clientes contra malware e ameaças.</span><span class="sxs-lookup"><span data-stu-id="44588-112">When secure boot is enabled, the AppInit\_DLLs mechanism is disabled as part of a no-compromise approach to protect customers against malware and threats.</span></span>

<span data-ttu-id="44588-113">Observe que a inicialização segura é um protocolo UEFI e não um recurso do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="44588-113">Please note that secure boot is a UEFI protocol and not a Windows 8 feature.</span></span> <span data-ttu-id="44588-114">Mais informações sobre a UEFI e a especificação de protocolo de inicialização segura podem ser encontradas em [https://www.uefi.org](https://www.uefi.org/) .</span><span class="sxs-lookup"><span data-stu-id="44588-114">More info on UEFI and the secure boot protocol specification can be found at [https://www.uefi.org](https://www.uefi.org/).</span></span>

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a><span data-ttu-id="44588-115">\_Requisito de certificação AppInit DLLs para aplicativos de área de trabalho do Windows 8</span><span class="sxs-lookup"><span data-stu-id="44588-115">AppInit\_DLLs certification requirement for Windows 8 desktop apps</span></span>

<span data-ttu-id="44588-116">Um dos requisitos de certificação para aplicativos de área de trabalho do Windows 8 é que o aplicativo não deve carregar DLLs arbitrárias para interceptar chamadas à API do Win32 usando o \_ mecanismo AppInit DLLs.</span><span class="sxs-lookup"><span data-stu-id="44588-116">One of the certification requirements for Windows 8 desktop apps is that the app must not load arbitrary DLLs to intercept Win32 API calls using the AppInit\_DLLs mechanism.</span></span> <span data-ttu-id="44588-117">Para obter informações mais detalhadas sobre os requisitos de certificação, consulte a seção 1,1 de [requisitos de certificação para aplicativos de área de trabalho do Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span><span class="sxs-lookup"><span data-stu-id="44588-117">For more detailed information about the certification requirements, refer to section 1.1 of [Certification requirements for Windows 8 desktop apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span></span>

## <a name="summary"></a><span data-ttu-id="44588-118">Resumo</span><span class="sxs-lookup"><span data-stu-id="44588-118">Summary</span></span>

-   <span data-ttu-id="44588-119">O \_ mecanismo de DLLs AppInit não é uma abordagem recomendada para aplicativos legítimos porque pode levar a problemas de desempenho e deadlocks do sistema.</span><span class="sxs-lookup"><span data-stu-id="44588-119">The AppInit\_DLLs mechanism is not a recommended approach for legitimate applications because it can lead to system deadlocks and performance problems.</span></span>
-   <span data-ttu-id="44588-120">O \_ mecanismo AppInit DLLs é desabilitado por padrão quando a inicialização segura está habilitada.</span><span class="sxs-lookup"><span data-stu-id="44588-120">The AppInit\_DLLs mechanism is disabled by default when secure boot is enabled.</span></span>
-   <span data-ttu-id="44588-121">Usar \_ DLLs AppInit em um aplicativo de área de trabalho do Windows 8 é uma falha de certificação de aplicativo de área de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="44588-121">Using AppInit\_DLLs in a Windows 8 desktop app is a Windows desktop app certification failure.</span></span>

<span data-ttu-id="44588-122">Consulte o White Paper a seguir para obter informações sobre DLLs do AppInit \_ no Windows 7 e no Windows server 2008 R2: [AppInit DLLs no Windows 7 e no windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44588-122">See the following whitepaper for info about AppInit\_DLLs on Windows 7 and Windows Server 2008 R2: [AppInit DLLs in Windows 7 and Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span></span>

 

 
