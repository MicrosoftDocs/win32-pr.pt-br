---
title: Alterações de versão do sistema operacional no Windows 8.1 e no Windows Server 2012 R2
description: Alterações de versão do sistema operacional no Windows 8.1 e no Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366633"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a><span data-ttu-id="6a5bb-103">Alterações de versão do sistema operacional no Windows 8.1 e no Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6a5bb-103">Operating system version changes in Windows 8.1 and Windows Server 2012 R2</span></span>

## <a name="platforms"></a><span data-ttu-id="6a5bb-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="6a5bb-104">Platforms</span></span>

<span data-ttu-id="6a5bb-105">**Clientes-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6a5bb-105">**Clients -** Windows 8.1</span></span>

<span data-ttu-id="6a5bb-106">**Servidores-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6a5bb-106">**Servers -** Windows Server 2012 R2</span></span>

## <a name="description"></a><span data-ttu-id="6a5bb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a5bb-107">Description</span></span>

<span data-ttu-id="6a5bb-108">Fizemos algumas alterações significativas em como as APIs GetVersion (ex) funcionam em Windows 8.1 devido a comportamentos indesejáveis do cliente, resultando da forma como as APIs GetVersion (ex) foram usadas no passado.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-108">We have made some significant changes in how the GetVersion(Ex) APIs work in Windows 8.1 due to undesirable customer behaviors resulting from how the GetVersion(Ex) APIs have been used in the past.</span></span>

<span data-ttu-id="6a5bb-109">Nas versões anteriores do Windows, chamar as APIs GetVersion (ex) retornaria a versão real do sistema operacional (SO), a menos que o processo tivesse sido mitigado por um Shim de compatibilidade de aplicativo para dar a ele uma versão diferente.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-109">In previous versions of Windows, calling the GetVersion(Ex) APIs would return the actual version of the operating system (OS), unless the process had been mitigated by an app compat shim to give it a different version.</span></span> <span data-ttu-id="6a5bb-110">Isso foi feito em uma base provisionada e foi relativamente incompleto em termos do número de processos que a Microsoft poderia corrigir razoavelmente em uma versão.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-110">This was done on a provisional basis and was relatively incomplete in terms of the number of processes that Microsoft could reasonably shim in a release.</span></span> <span data-ttu-id="6a5bb-111">Muitos aplicativos passam pelas rachaduras porque não obtiveram corrigido devido a verificações de versão mal projetadas.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-111">Many applications fell through the cracks because they didn’t get shimmed due to poorly designed version checks.</span></span>

<span data-ttu-id="6a5bb-112">O número um motivo para fazer uma verificação de versão é avisar o usuário de que o aplicativo precisa ser executado em uma versão mais recente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-112">The number one reason to do a version check is to warn the user that the application needs to run on a newer version of the OS.</span></span> <span data-ttu-id="6a5bb-113">No entanto, devido a verificações ruins, os aplicativos geralmente avisam que eles precisavam ser executados no Windows XP ou posterior, o que é claro que o sistema operacional mais recente é.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-113">However due to poor checks, apps would often incorrectly warn that they needed to be run on Windows XP or later, which of course the newest OS is.</span></span> <span data-ttu-id="6a5bb-114">Com mais frequência do que não, o sistema operacional mais recente executaria o aplicativo sem nenhum problema se não fosse para essas verificações.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-114">More often than not, the newest OS would run the application without any issues if not for these checks.</span></span>

## <a name="manifestation"></a><span data-ttu-id="6a5bb-115">Manifestação</span><span class="sxs-lookup"><span data-stu-id="6a5bb-115">Manifestation</span></span>

<span data-ttu-id="6a5bb-116">No Windows 8.1, as APIs GetVersion (ex) foram preteridas.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-116">In Windows 8.1, the GetVersion(Ex) APIs have been deprecated.</span></span> <span data-ttu-id="6a5bb-117">Isso significa que, embora você ainda possa chamar essas funções de API, se seu aplicativo não direcionar especificamente Windows 8.1, as funções retornarão a versão do Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="6a5bb-117">That means that while you can still call these API functions, if your app does not specifically target Windows 8.1, the functions will return the Windows 8 version (6.2).</span></span>

## <a name="solution"></a><span data-ttu-id="6a5bb-118">Solução</span><span class="sxs-lookup"><span data-stu-id="6a5bb-118">Solution</span></span>

### <a name="adding-an-app-manifest"></a><span data-ttu-id="6a5bb-119">Adicionando um manifesto de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6a5bb-119">Adding an app manifest</span></span>

<span data-ttu-id="6a5bb-120">Para que seu aplicativo seja direcionado Windows 8.1, você precisará incluir um [manifesto de aplicativo (executável)](/windows/compatibility/application-executable-manifest) para o executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-120">In order for your app to target Windows 8.1, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="6a5bb-121">Em seguida, na [seção **&lt; compatibilidade &gt;**](../SbsCs/application-manifests.md#compatibility) do manifesto, você precisará adicionar um elemento **&lt; supportedOS &gt;** para cada versão do Windows que você deseja declarar para o suporte do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-121">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="6a5bb-122">O exemplo a seguir mostra um arquivo de manifesto de aplicativo para um aplicativo que dá suporte a todas as versões do Windows do Windows Vista para Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="6a5bb-122">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 8.1:</span></span>

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
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
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

<span data-ttu-id="6a5bb-123">A linha acima marcada `* ADD THIS LINE *` mostra como direcionar com precisão seu aplicativo para Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-123">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 8.1.</span></span>

<span data-ttu-id="6a5bb-124">A declaração de suporte para Windows 8.1 em seu manifesto de aplicativo não terá nenhum efeito ao executar seu aplicativo em sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-124">Declaring support for Windows 8.1 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

### <a name="using-versionhelpers-instead-of-getversionex"></a><span data-ttu-id="6a5bb-125">Usando VersionHelpers em vez de GetVersion (ex)</span><span class="sxs-lookup"><span data-stu-id="6a5bb-125">Using VersionHelpers instead of GetVersion(Ex)</span></span>

<span data-ttu-id="6a5bb-126">Windows 8.1 introduz novas funções de API de substituição para GetVersion (ex), conhecidas como VersionHelpers.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-126">Windows 8.1 introduces new replacement API functions for GetVersion(Ex), known as VersionHelpers.</span></span> <span data-ttu-id="6a5bb-127">Eles são extremamente fáceis de usar; Tudo o que você precisa fazer é `#include <VersionHelpers.h>` .</span><span class="sxs-lookup"><span data-stu-id="6a5bb-127">They are extremely easy to use; all you have to do is `#include <VersionHelpers.h>`.</span></span> <span data-ttu-id="6a5bb-128">As funções embutidas disponíveis no arquivo de cabeçalho VersionHelpers. h permitem que seu código pergunte se o sistema operacional é uma determinada versão do Windows ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-128">The inline functions available in the VersionHelpers.h header file allow your code to ask whether the operating system is a given version of Windows or later.</span></span>

<span data-ttu-id="6a5bb-129">**Exemplo** Por exemplo, se seu aplicativo exigir o Windows 8 ou posterior, use o teste a seguir:</span><span class="sxs-lookup"><span data-stu-id="6a5bb-129">**Example** For example, if your application requires Windows 8 or later, use the following test:</span></span>

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

<span data-ttu-id="6a5bb-130">As funções de API do VersionHelper disponíveis são:</span><span class="sxs-lookup"><span data-stu-id="6a5bb-130">The available VersionHelper API functions are:</span></span>

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

<span data-ttu-id="6a5bb-131">Eles retornarão TRUE ou FALSE dependendo da pergunta que você está fazendo e você só precisa definir o sistema operacional de nível mínimo ao qual dá suporte.</span><span class="sxs-lookup"><span data-stu-id="6a5bb-131">They will return TRUE or FALSE depending on the question you are asking, and you only need to define the minimum level operating system that you support.</span></span>

## <a name="resources"></a><span data-ttu-id="6a5bb-132">Recursos</span><span class="sxs-lookup"><span data-stu-id="6a5bb-132">Resources</span></span>

-   [<span data-ttu-id="6a5bb-133">Download do kit de ferramentas de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6a5bb-133">Application Compatibility Toolkit Download</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   <span data-ttu-id="6a5bb-134">[Correções de compatibilidade conhecidas, modos de compatibilidade e mensagens AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6a5bb-134">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="6a5bb-135">APIs do VersionHelpers</span><span class="sxs-lookup"><span data-stu-id="6a5bb-135">VersionHelpers APIs</span></span>](../sysinfo/version-helper-apis.md)