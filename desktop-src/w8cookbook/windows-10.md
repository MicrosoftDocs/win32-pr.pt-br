---
title: Windows 10
description: Este manual fornece informações para desenvolvedores sobre alterações de plataforma para os sistemas operacionais Windows 10 (SO).
ms.assetid: bf8d7d10-bab6-4711-b65f-5393d906e47b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03fce627969573deb395fda356564a85a3573682
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366555"
---
# <a name="windows-10"></a><span data-ttu-id="7361e-103">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7361e-103">Windows 10</span></span>

<span data-ttu-id="7361e-104">Este manual fornece informações para desenvolvedores sobre alterações de plataforma para os sistemas operacionais Windows 10 (SO).</span><span class="sxs-lookup"><span data-stu-id="7361e-104">This Cookbook provides info for developers about platform changes to the Windows 10 operating systems (OS).</span></span> <span data-ttu-id="7361e-105">Também fornecemos diretrizes para verificar a compatibilidade de seus aplicativos existentes e planejados com a versão mais recente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7361e-105">We also provide guidelines for you to verify the compatibility of your existing and planned apps with the latest version of the OS.</span></span> <span data-ttu-id="7361e-106">Supomos que você esteja familiarizado com as versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="7361e-106">We assume that you are familiar with previous versions of Windows.</span></span>

<span data-ttu-id="7361e-107">O conteúdo se aplica a: Windows 10</span><span class="sxs-lookup"><span data-stu-id="7361e-107">The content applies to: Windows 10</span></span>

<span data-ttu-id="7361e-108">O manual é para desenvolvedores de aplicativos e dispositivos de terceiros que são projetados para serem usados no ambiente do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7361e-108">The Cookbook is for third party developers of apps and devices that are designed to be used in the Microsoft Windows environment.</span></span>

## <a name="introduction"></a><span data-ttu-id="7361e-109">Introdução</span><span class="sxs-lookup"><span data-stu-id="7361e-109">Introduction</span></span>

<span data-ttu-id="7361e-110">O Windows 10 apresenta a tecnologia de so mais recente e as plataformas de desenvolvimento de software para uso por desenvolvedores de aplicativos e de drivers e empresas em todo o mundo.</span><span class="sxs-lookup"><span data-stu-id="7361e-110">Windows 10 introduces the latest OS technology and software development platforms for use by app and driver developers and enterprises worldwide.</span></span> <span data-ttu-id="7361e-111">Para aprimorar ainda mais a segurança, a confiabilidade, o desempenho e a experiência do usuário do Windows, a Microsoft introduziu muitos recursos novos, aprimorou os recursos existentes e removeu outros.</span><span class="sxs-lookup"><span data-stu-id="7361e-111">To further enhance the security, reliability, performance, and user experience of Windows, Microsoft has introduced many new features, improved existing features, and removed others.</span></span>

<span data-ttu-id="7361e-112">Embora o objetivo do Windows 10 seja manter a compatibilidade com aplicativos escritos para versões lançadas anteriormente do sistema operacional Windows, algumas quebras de compatibilidade são inevitáveis devido a inovações, segurança rígida e maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="7361e-112">While the goal of Windows 10 is to maintain compatibility with apps written for previously released versions of the Windows OS, some compatibility breaks are inevitable due to innovations, tightened security, and increased reliability.</span></span> <span data-ttu-id="7361e-113">De modo geral, a compatibilidade da versão mais recente do sistema operacional Windows com aplicativos e dispositivos existentes é alta.</span><span class="sxs-lookup"><span data-stu-id="7361e-113">Overall, the compatibility of the latest version of the Windows OS with existing apps and devices is high.</span></span>

<span data-ttu-id="7361e-114">Este documento mostra como verificar se seus aplicativos e dispositivos são compatíveis com a versão mais recente do sistema operacional e fornece uma visão geral dos problemas conhecidos de incompatibilidade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7361e-114">This document shows you how to verify that your apps and devices are compatible with the latest version of the OS and provides an overview of known app incompatibility issues.</span></span>

<span data-ttu-id="7361e-115">Convidamos você a conferir esses tópicos para aprender a otimizar seus aplicativos e aproveitar o que essa versão mais recente do Windows tem a oferecer.</span><span class="sxs-lookup"><span data-stu-id="7361e-115">We invite you to check out these topics to learn how to optimize your apps and take advantage of what this newest release of Windows has to offer.</span></span>

## <a name="contents"></a><span data-ttu-id="7361e-116">Sumário</span><span class="sxs-lookup"><span data-stu-id="7361e-116">Contents</span></span>

-   [<span data-ttu-id="7361e-117">Principais alterações desde o Windows 7 para garantir a compatibilidade</span><span class="sxs-lookup"><span data-stu-id="7361e-117">Key changes since Windows 7 to ensure compatibility</span></span>](key-changes-since-windows-7-to-ensure-compatibility.md)
-   [<span data-ttu-id="7361e-118">Como podemos garantir a compatibilidade do ecossistema combinado</span><span class="sxs-lookup"><span data-stu-id="7361e-118">How we can ensure compatibility of the combined ecosystem</span></span>](how-we-can-ensure-compatibility-of-the-combined-ecosystem.md)
    -   [<span data-ttu-id="7361e-119">Verificação de versão do Windows</span><span class="sxs-lookup"><span data-stu-id="7361e-119">Windows version check</span></span>](windows-version-check.md)
    -   [<span data-ttu-id="7361e-120">APIs não documentadas</span><span class="sxs-lookup"><span data-stu-id="7361e-120">Undocumented APIs</span></span>](undocumented-apis.md)
    -   [<span data-ttu-id="7361e-121">Desenvolver aplicativos UWP e de ponte de desktop</span><span class="sxs-lookup"><span data-stu-id="7361e-121">Develop UWP and Desktop Bridge apps</span></span>](/windows/desktop/w8cookbook/develop-universal-windows-platform-apps)
    -   [<span data-ttu-id="7361e-122">A funcionalidade moderna do aplicativo de área de trabalho será afetada se não for executada no modo de janela</span><span class="sxs-lookup"><span data-stu-id="7361e-122">Modern Desktop App functionality is impacted if not run in Windowed Mode</span></span>](modern-desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode.md)
    -   [<span data-ttu-id="7361e-123">Disponibilidade de drivers gráficos aplicáveis no Windows Update</span><span class="sxs-lookup"><span data-stu-id="7361e-123">Availability of applicable graphics drivers on Windows Update</span></span>](availability-of-applicable-graphics-drivers-on-windows-update.md)
    -   [<span data-ttu-id="7361e-124">Migração de driver de gráficos para o Windows 10</span><span class="sxs-lookup"><span data-stu-id="7361e-124">Graphics driver migration to Windows 10</span></span>](graphics-driver-migration-to-windows-10.md)
    -   [<span data-ttu-id="7361e-125">Drivers Bluetooth</span><span class="sxs-lookup"><span data-stu-id="7361e-125">Bluetooth drivers</span></span>](bluetooth-drivers.md)

## <a name="download-the-cookbook"></a><span data-ttu-id="7361e-126">Baixe o manual</span><span class="sxs-lookup"><span data-stu-id="7361e-126">Download the cookbook</span></span>

<span data-ttu-id="7361e-127">Para obter uma referência rápida a todas essas informações, bem como informações sobre o Windows como serviço, suporte a aplicativos no Windows e estratégias otimizadas para testar seu aplicativo, [Baixe o manual de compatibilidade do Windows 10](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span><span class="sxs-lookup"><span data-stu-id="7361e-127">For a quick reference to all this information, as well as information on Windows as a service, supporting apps in Windows, and optimized strategies for testing your app, [download the Windows 10 Compatibility Cookbook](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span></span>

## <a name="see-also"></a><span data-ttu-id="7361e-128">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7361e-128">See Also</span></span>

-   <span data-ttu-id="7361e-129">[Windows como serviço](/windows/deployment/update/), para obter informações sobre os tipos de versão do Windows 10 e o suporte a aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7361e-129">[Windows as a service](/windows/deployment/update/), for information about Windows 10 release types and app support.</span></span>
-   <span data-ttu-id="7361e-130">[Windows Insider](https://insider.windows.com/), para acessar versões prévias, teste e forneça comentários.</span><span class="sxs-lookup"><span data-stu-id="7361e-130">[Windows Insider](https://insider.windows.com/), to access preview builds, test, and provide feedback.</span></span>
-   <span data-ttu-id="7361e-131">[Pronto para o Windows 10](https://www.readyfor10.com/), para enviar as informações da sua empresa a um recurso para gerentes de ti.</span><span class="sxs-lookup"><span data-stu-id="7361e-131">[Ready for Windows 10](https://www.readyfor10.com/), to submit your company's information to a resource for IT managers.</span></span>

 

 