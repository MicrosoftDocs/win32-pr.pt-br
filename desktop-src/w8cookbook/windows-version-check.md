---
title: Verificação de versão do Windows
description: A versão do sistema operacional foi incrementada com a versão do sistema operacional Windows 10.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea1e65ed97859486bdd0a18fe53ee44a653faf
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104084969"
---
# <a name="windows-version-check"></a><span data-ttu-id="55a76-103">Verificação de versão do Windows</span><span class="sxs-lookup"><span data-stu-id="55a76-103">Windows version check</span></span>

<span data-ttu-id="55a76-104">A versão do sistema operacional foi incrementada com a versão do sistema operacional Windows 10.</span><span class="sxs-lookup"><span data-stu-id="55a76-104">The OS version has been incremented with the Windows 10 OS release.</span></span> <span data-ttu-id="55a76-105">Isso significa que o número de versão interno para o Windows 10 também foi alterado para 10,0.</span><span class="sxs-lookup"><span data-stu-id="55a76-105">This means that the internal version number for Windows 10 has also been changed to 10.0.</span></span> <span data-ttu-id="55a76-106">Como sempre, não medimos esforços para manter a compatibilidade de aplicativos e dispositivos após uma mudança de versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="55a76-106">As in the past, we go to great lengths to maintain application and device compatibility after an OS version change.</span></span> <span data-ttu-id="55a76-107">Para a maioria das categorias de aplicativo (sem nenhuma dependência de kernel), a alteração não afetará negativamente a funcionalidade do aplicativo e os aplicativos existentes continuarão funcionando bem no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="55a76-107">For most app categories (without any kernel dependencies) the change will not negatively impact app functionality, and existing apps will continue to work fine on Windows 10.</span></span>

## <a name="manifestations"></a><span data-ttu-id="55a76-108">Manifestações</span><span class="sxs-lookup"><span data-stu-id="55a76-108">Manifestations</span></span>

<span data-ttu-id="55a76-109">A manifestação dessa alteração é específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55a76-109">The manifestation of this change is app-specific.</span></span> <span data-ttu-id="55a76-110">Isso significa que qualquer aplicativo que verifica especificamente para a versão do sistema operacional obterá um número de versão superior, que pode levar a uma ou mais das seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="55a76-110">This means any app that specifically checks for the OS version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="55a76-111">Os instaladores de aplicativos podem não ser capazes de instalar o aplicativo e os aplicativos talvez não consigam iniciar.</span><span class="sxs-lookup"><span data-stu-id="55a76-111">App installers might not be able to install the app, and apps might not be able to start.</span></span>
-   <span data-ttu-id="55a76-112">Os aplicativos podem ficar instáveis ou falhar.</span><span class="sxs-lookup"><span data-stu-id="55a76-112">Apps might become unstable or crash.</span></span>
-   <span data-ttu-id="55a76-113">Os aplicativos podem gerar mensagens de erro, mas continuar funcionando adequadamente.</span><span class="sxs-lookup"><span data-stu-id="55a76-113">Apps might generate error messages, but continue to function properly.</span></span>

<span data-ttu-id="55a76-114">Alguns aplicativos realizam uma verificação de versão e simplesmente passam um aviso para os usuários.</span><span class="sxs-lookup"><span data-stu-id="55a76-114">Some apps perform a version check and simply pass a warning to users.</span></span> <span data-ttu-id="55a76-115">No entanto, há aplicativos associados rigidamente a uma verificação de versão (nos drivers ou no modo de kernel para evitar a detecção).</span><span class="sxs-lookup"><span data-stu-id="55a76-115">However, there are apps that are bound very tightly to a version check (in the drivers, or in kernel mode to avoid detection).</span></span> <span data-ttu-id="55a76-116">Nesses casos, o aplicativo falhará se for encontrada uma versão incorreta.</span><span class="sxs-lookup"><span data-stu-id="55a76-116">In these cases, the app will fail if an incorrect version is found.</span></span> <span data-ttu-id="55a76-117">Em vez de uma verificação de versão, recomendamos um dos procedimentos a seguir:</span><span class="sxs-lookup"><span data-stu-id="55a76-117">Rather than a version check, we recommend one of the following approaches:</span></span>

-   <span data-ttu-id="55a76-118">Se o aplicativo for dependente da funcionalidade de uma API específica, selecione a versão correta da API.</span><span class="sxs-lookup"><span data-stu-id="55a76-118">If the app is dependent on specific API functionality, ensure you target the correct API version.</span></span>
-   <span data-ttu-id="55a76-119">O número de versão do NTDDI (NT Device Driver interface) será incrementado somente se a funcionalidade de destino na API for alterada.</span><span class="sxs-lookup"><span data-stu-id="55a76-119">NTDDI (NT device driver interface) version number will increment only if target functionality in the API changes.</span></span> <span data-ttu-id="55a76-120">Certifique-se de detectar a alteração via APISet ou outra API exposta, conforme criado pela equipe de recursos, e não use a versão como um proxy para algum recurso ou correção.</span><span class="sxs-lookup"><span data-stu-id="55a76-120">Ensure you detect the change via APISet or other exposed API as created by the feature team, and do not use the version as a proxy for some feature or fix.</span></span> <span data-ttu-id="55a76-121">Se houver alterações da falha e uma seleção adequada não for exposta, então isso será um bug.</span><span class="sxs-lookup"><span data-stu-id="55a76-121">If there are breaking changes and a proper check is not exposed, then that is a bug.</span></span>
-   <span data-ttu-id="55a76-122">Verifique se o aplicativo não verifica a versão de maneiras estranhas, como por meio do registro, versões de arquivo, deslocamentos, modo kernel, drivers ou outros meios.</span><span class="sxs-lookup"><span data-stu-id="55a76-122">Ensure the app does NOT check for version in odd ways, such as via the registry, file versions, offsets, kernel mode, drivers or other means.</span></span> <span data-ttu-id="55a76-123">Se o aplicativo precisar verificar a versão, use as APIs GetVersion, que devem retornar o número principal, secundário e de Build.</span><span class="sxs-lookup"><span data-stu-id="55a76-123">If the app absolutely needs to check the version, use the GetVersion APIs, which should return the major, minor and build number.</span></span>
-   <span data-ttu-id="55a76-124">Se você estiver usando a API GetVersion ou outras funções auxiliares de versão, como [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), lembre-se de que o comportamento dessa API foi alterado a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="55a76-124">If you are using the GetVersion API or other Version Helper functions such as [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), remember that the behavior of this API has changed starting with Windows 8.1.</span></span> <span data-ttu-id="55a76-125">Consulte [a documentação da API](../SysInfo/version-helper-apis.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="55a76-125">Please refer to [the API documentation](../SysInfo/version-helper-apis.md) for more details.</span></span>
-   <span data-ttu-id="55a76-126">Se você possui aplicativos como Antimalware ou firewall, você deve trabalhar com seus canais de comentários usuais e por meio do programa Windows Insider.</span><span class="sxs-lookup"><span data-stu-id="55a76-126">If you own apps such as antimalware or firewall, you should work through your usual feedback channels and via the Windows Insider program.</span></span>

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a><span data-ttu-id="55a76-127">Declarando a compatibilidade do Windows 10 com um manifesto de aplicativo</span><span class="sxs-lookup"><span data-stu-id="55a76-127">Declaring Windows 10 Compatibility With An App Manifest</span></span>

<span data-ttu-id="55a76-128">Se seu aplicativo for compatível com o Windows 10, ele poderá declarar esse fato no [manifesto do aplicativo (executável)](/windows/compatibility/application-executable-manifest) para o executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55a76-128">If your app is compatible with Windows 10, it can declare this fact in the [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="55a76-129">Isso informa ao sistema que seu aplicativo entende o número de versão do sistema do Windows 10 de 10,0 (para que a API GetVersion não retorne uma versão anterior) e também permite que o sistema desative outros comportamentos de compatibilidade aplicados a aplicativos que não declaram a compatibilidade com o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="55a76-129">This tells the system that your app understands Windows 10's system version number of 10.0 (so the GetVersion API does not return an earlier version), and also lets the system turn off other compatibility behaviors applied to apps that don't declare Windows 10 compatibility.</span></span>

<span data-ttu-id="55a76-130">Para declarar a compatibilidade do Windows 10 em um manifesto de aplicativo, você precisará adicionar uma seção de [ **&lt; compatibilidade &gt;**](../SbsCs/application-manifests.md#compatibility) do manifesto, caso ainda não exista, e, em seguida, adicionar elementos **&lt; supportedOS &gt;** ao Windows 10 e a todas as outras versões do Windows que você deseja declarar para as quais seu aplicativo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="55a76-130">To declare Windows 10 compatibility in an app manifest, you'll need to add a [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest if one does not already exist, and then add **&lt;supportedOS&gt;** elements for Windows 10 and every other Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="55a76-131">O exemplo a seguir mostra um arquivo de manifesto de aplicativo para um aplicativo que dá suporte a todas as versões do Windows do Windows Vista para o Windows 10:</span><span class="sxs-lookup"><span data-stu-id="55a76-131">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

<span data-ttu-id="55a76-132">A linha acima marcada `* ADD THIS LINE *` mostra como direcionar com precisão seu aplicativo para o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="55a76-132">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 10.</span></span>

<span data-ttu-id="55a76-133">A declaração de suporte para Windows 10 em seu manifesto de aplicativo não terá nenhum efeito ao executar seu aplicativo em sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="55a76-133">Declaring support for Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="55a76-134">Recursos</span><span class="sxs-lookup"><span data-stu-id="55a76-134">Resources</span></span>

-   [<span data-ttu-id="55a76-135">Download do kit de ferramentas de compatibilidade de aplicativos: Baixe o Windows ADK para Windows 10</span><span class="sxs-lookup"><span data-stu-id="55a76-135">Application Compatibility Toolkit Download: Download the Windows ADK for Windows 10</span></span>](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   <span data-ttu-id="55a76-136">[Correções de compatibilidade conhecidas, modos de compatibilidade e mensagens AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="55a76-136">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="55a76-137">API de auxiliares de versão</span><span class="sxs-lookup"><span data-stu-id="55a76-137">Version Helpers API</span></span>](../sysinfo/version-helper-apis.md)