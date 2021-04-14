---
title: Desenvolvendo aplicativos para versões anteriores do Windows
description: Explica o que fazer para desenvolver aplicativos executados em versões anteriores do Windows e aproveitar a API que tem suporte com a atualização de plataforma para o Windows Vista e a atualização de plataforma para o Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104370836"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a><span data-ttu-id="f6787-103">Desenvolvendo aplicativos para versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="f6787-103">Developing Applications for Previous Versions of Windows</span></span>

<span data-ttu-id="f6787-104">Explica o que fazer para desenvolver aplicativos executados em versões anteriores do Windows e aproveitar a API que tem suporte com a atualização de plataforma para o Windows Vista e a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f6787-104">Explains what to do to develop applications that run on previous versions of Windows and take advantage of the API that are supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

## <a name="required-downloads"></a><span data-ttu-id="f6787-105">Downloads necessários</span><span class="sxs-lookup"><span data-stu-id="f6787-105">Required Downloads</span></span>

<span data-ttu-id="f6787-106">O download e a instalação dos pacotes descritos nas seções a seguir serão necessários se você quiser desenvolver aplicativos que usam a API introduzida com o SDK (Software Development Kit) do Microsoft Windows para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f6787-106">Download and installation of the packages described in the following sections is required if you want to develop applications that use API that are introduced with the Microsoft Windows Software Development Kit (SDK) for Windows 7.</span></span>

### <a name="microsoft-windows-sdk"></a><span data-ttu-id="f6787-107">SDK do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="f6787-107">Microsoft Windows SDK</span></span>

<span data-ttu-id="f6787-108">O SDK do Windows para o Windows 7 é necessário para criar aplicativos que usam APIs com suporte com a atualização de plataforma para Windows Vista e a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f6787-108">The Windows SDK for Windows 7 is required for creating applications that use APIs supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="f6787-109">Para obter acesso a recursos adicionais e informações, como downloads, Postagens de fórum e o blog da equipe SDK do Windows, consulte o [SDK do Windows Developer Center](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f6787-109">For access to additional resources and information, such as downloads, forum posts, and the Windows SDK team blog, see the [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx).</span></span>

### <a name="net-framework"></a><span data-ttu-id="f6787-110">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="f6787-110">.NET Framework</span></span>

<span data-ttu-id="f6787-111">O .NET Framework 3,5 Service Pack 1 é necessário para criar aplicativos que usam APIs com suporte da atualização de plataforma para o Windows Vista e a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f6787-111">The .NET Framework 3.5 Service Pack 1 is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="f6787-112">Para obter recursos adicionais e informações, consulte o [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f6787-112">For additional resources and information, see the [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx).</span></span>

### <a name="directx-sdk-required-when-using-direct3d"></a><span data-ttu-id="f6787-113">SDK do DirectX necessário ao usar o Direct3D</span><span class="sxs-lookup"><span data-stu-id="f6787-113">DirectX SDK Required When Using Direct3D</span></span>

<span data-ttu-id="f6787-114">Se você criar aplicativos que usam o Direct3D, o [SDK do DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) é necessário para criar aplicativos que usam APIs com suporte da atualização da plataforma para o Windows Vista e a atualização da plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f6787-114">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

### <a name="update-your-development-computer"></a><span data-ttu-id="f6787-115">Atualizar seu computador de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="f6787-115">Update Your Development Computer</span></span>

<span data-ttu-id="f6787-116">Verifique se o computador de desenvolvimento tem todas as atualizações mais recentes do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="f6787-116">Ensure that your development computer has all of the latest updates from Windows Update.</span></span>

<span data-ttu-id="f6787-117">Se você estiver desenvolvendo aplicativos em uma versão anterior do Windows, deverá obter a atualização da plataforma para o Windows Vista ou a atualização da plataforma para a atualização do Windows Server 2008 do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="f6787-117">If you are developing applications on a previous version of Windows, you must obtain the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update from Windows Update.</span></span> <span data-ttu-id="f6787-118">A instalação de qualquer uma dessas atualizações permitirá que você aproveite a nova API fornecida pelo SDK do Windows para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f6787-118">Installing either of these updates will enable you to take advantage of the new API provided by the Windows SDK for Windows 7.</span></span>

<span data-ttu-id="f6787-119">Para obter mais informações sobre como obter atualizações do Windows Update consulte o [artigo da base de dados de conhecimento sobre a atualização da plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .</span><span class="sxs-lookup"><span data-stu-id="f6787-119">For more information about how to obtain updates from Windows Update see the [Knowledge Base article about the Platform Update for Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) (https://support.microsoft.com/kb/971644).</span></span>

## <a name="development-environment"></a><span data-ttu-id="f6787-120">Ambiente de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="f6787-120">Development Environment</span></span>

### <a name="set-the-build-target-to-windows-7"></a><span data-ttu-id="f6787-121">Definir o destino da compilação para o Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6787-121">Set the Build Target to Windows 7</span></span>

<span data-ttu-id="f6787-122">Todos os aplicativos que usam bibliotecas na atualização da plataforma para Windows Vista devem ser criados na plataforma de destino do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f6787-122">All applications that use libraries in the Platform Update for Windows Vista must be built against the Windows 7 target platform.</span></span>

<span data-ttu-id="f6787-123">A configuração de WINVER para o valor da plataforma de destino do Windows 7 permite que você desenvolva aplicativos que usam APIs compatíveis com a atualização da plataforma para o Windows Vista ou a atualização da plataforma para o Windows Server 2008 em um computador de desenvolvimento que executa o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f6787-123">Setting WINVER to the Windows 7 target platform value enables you to develop applications that use APIs supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 on a development machine running Windows Vista.</span></span>

<span data-ttu-id="f6787-124">Você pode definir a plataforma de destino para o Windows 7 em seu código-fonte ou usando a opção/D com o compilador do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f6787-124">You can set the target platform to Windows 7 either in your source code or by using the /D option with the Visual Studio compiler.</span></span>

<span data-ttu-id="f6787-125">O exemplo a seguir mostra como definir WINVER em seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="f6787-125">The following example shows how to set WINVER in your source code.</span></span>


```C++
#define WINVER 0x0601
```



<span data-ttu-id="f6787-126">O exemplo a seguir mostra como definir WINVER usando a opção de compilador/D.</span><span class="sxs-lookup"><span data-stu-id="f6787-126">The following example shows how to set WINVER using the /D compiler option.</span></span>

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a><span data-ttu-id="f6787-127">Implantação do aplicativo</span><span class="sxs-lookup"><span data-stu-id="f6787-127">Application Deployment</span></span>

<span data-ttu-id="f6787-128">Se você criar seu aplicativo usando os cabeçalhos e as bibliotecas fornecidos pelo SDK do Windows para o Windows 7, as APIs com suporte serão executadas em qualquer versão do Windows que tenha a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008 instalada.</span><span class="sxs-lookup"><span data-stu-id="f6787-128">If you build your application using the headers and libraries provided by the Windows SDK for Windows 7, supported APIs will run on any Windows version that has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 installed.</span></span>

> [!Note]  
> <span data-ttu-id="f6787-129">O comportamento, o desempenho ou os requisitos para algumas APIs com suporte na atualização da plataforma para o Windows Vista ou a atualização da plataforma para o Windows Server 2008 podem variar em diferentes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="f6787-129">The behavior, performance, or requirements for some APIs that are supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 may vary across different versions of Windows.</span></span> <span data-ttu-id="f6787-130">Para obter detalhes sobre uma API específica com suporte das atualizações, consulte [sobre a atualização de plataforma para o Windows Vista](platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f6787-130">For details about a specific API that is supported by the updates, see [About Platform Update for Windows Vista](platform-update-for-windows-vista-overview.md).</span></span>

 

### <a name="no-redistributable-components"></a><span data-ttu-id="f6787-131">Nenhum componente redistribuível</span><span class="sxs-lookup"><span data-stu-id="f6787-131">No Redistributable Components</span></span>

<span data-ttu-id="f6787-132">Seu aplicativo não precisa instalar componentes redistribuíveis, como DLLs ou outros arquivos de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f6787-132">Your application does not need to install redistributable components, such as DLLs or other run-time files.</span></span>

### <a name="requires-updated-end-user-computer"></a><span data-ttu-id="f6787-133">Requer um computador End-User atualizado</span><span class="sxs-lookup"><span data-stu-id="f6787-133">Requires Updated End-User Computer</span></span>

<span data-ttu-id="f6787-134">Como a atualização de plataforma para o Windows Vista e a atualização de plataforma para Windows Server 2008 são hospedadas pelo Windows Update, os usuários finais com atualizações automáticas habilitadas têm grande probabilidade de já terem essas atualizações, bem como os Service Packs necessários.</span><span class="sxs-lookup"><span data-stu-id="f6787-134">Because Platform Update for Windows Vista and Platform Update for Windows Server 2008 are hosted by Windows Update, end-users with automatic updates enabled are highly likely to already have these updates as well as the required service packs.</span></span>

<span data-ttu-id="f6787-135">Se o computador do usuário final não tiver a atualização de plataforma para Windows Vista ou atualização de plataforma para Windows Server 2008 instalada e seu aplicativo exigir APIs com suporte nessas atualizações, o aplicativo poderá não ser capaz de executar no computador do usuário final ou poderá encontrar erros durante a execução.</span><span class="sxs-lookup"><span data-stu-id="f6787-135">If the end-user's computer does not have Platform Update for Windows Vista or Platform Update for Windows Server 2008 installed and your application requires APIs that are supported with these updates, your application may not be able to run on the end-user's computer or may encounter errors during execution.</span></span>

<span data-ttu-id="f6787-136">Para evitar os problemas que podem ser causados pelo computador do usuário que está desatualizado, você deseja verificar se o computador do usuário tem a atualização da plataforma para o Windows Vista ou a atualização da plataforma para a atualização do Windows Server 2008 durante a instalação do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6787-136">To avoid the problems that could be caused by your user's computer being out-of-date, you want to verify that your user's computer has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update during the installation of your application.</span></span> <span data-ttu-id="f6787-137">Você pode usar a [API do agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client) para verificar se há atualizações instaladas no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="f6787-137">You can use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to check your end-user's computer for installed updates.</span></span> <span data-ttu-id="f6787-138">Você também pode usar a API do agente Windows Update para baixar e instalar as atualizações necessárias durante a instalação do aplicativo se o usuário final ainda não tiver instalado as atualizações.</span><span class="sxs-lookup"><span data-stu-id="f6787-138">You can also use the Windows Update Agent API to download and install required updates during application installation if the end-user has not already installed the updates.</span></span>

<span data-ttu-id="f6787-139">Para obter um exemplo de um instalador que demonstra como usar a [API do agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client), consulte [implantação do Direct3D 11 para desenvolvedores de jogos](../direct3darticles/direct3d11-deployment.md) no SDK do [DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f6787-139">For an example of an installer that demonstrates how to use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client), see [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md) in the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx).</span></span>

<span data-ttu-id="f6787-140">Embora o exemplo do instalador do D3D11InstallHelper que é discutido na [implantação do Direct3D 11 para desenvolvedores de jogos](../direct3darticles/direct3d11-deployment.md), foi escrito para aplicativos que usam o Direct3D 11, ele fornece um bom exemplo de como interagir com a [API do agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client) para iniciar e acompanhar o download e a instalação de atualizações que são hospedadas pelo Windows Update.</span><span class="sxs-lookup"><span data-stu-id="f6787-140">Although the D3D11InstallHelper installer sample that is discussed in [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md), was written for applications that use Direct3D 11, it provides a good example of how to interact with the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to initiate and track the download and installation of updates that are hosted by Windows Update.</span></span> <span data-ttu-id="f6787-141">A compilação deste exemplo pode exigir o SDK do Windows para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f6787-141">Compiling this sample may require the Windows SDK for Windows 7.</span></span> <span data-ttu-id="f6787-142">Para obter informações adicionais sobre o exemplo de D3D11InstallHelper, incluindo problemas conhecidos, consulte o [SDK do DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) notas de versão para agosto de 2009. atualização da plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6787-142">For additional information about the D3D11InstallHelper sample, including known issues, see the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) Release Notes for August 2009.Platform Update for Windows Vista</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6787-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6787-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6787-144">Atualização da plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6787-144">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="f6787-145">**Visões gerais**</span><span class="sxs-lookup"><span data-stu-id="f6787-145">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="f6787-146">Sobre a atualização da plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6787-146">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="f6787-147">Artigo da base de dados de conhecimento sobre a atualização da plataforma para Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="f6787-147">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 