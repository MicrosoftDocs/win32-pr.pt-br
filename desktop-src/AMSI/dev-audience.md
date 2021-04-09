---
title: Público do desenvolvedor e código de exemplo
description: Este tópico descreve os grupos de desenvolvedores para os quais a interface de verificação antimalware foi projetada.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 22cf1156a8fa0aedc212b2ab70e34b984d13470f
ms.sourcegitcommit: 272ba17a215d0d27bb7918fee1192d4954ccc576
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/30/2020
ms.locfileid: "104007035"
---
# <a name="developer-audience-and-sample-code"></a><span data-ttu-id="d44c5-103">Público do desenvolvedor e código de exemplo</span><span class="sxs-lookup"><span data-stu-id="d44c5-103">Developer audience, and sample code</span></span>

<span data-ttu-id="d44c5-104">A interface de verificação antimalware foi projetada para ser usada por dois grupos de desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="d44c5-104">The Antimalware Scan Interface is designed for use by two groups of developers.</span></span>

- <span data-ttu-id="d44c5-105">Desenvolvedores de aplicativos que desejam fazer solicitações para produtos antimalware de dentro de seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d44c5-105">Application developers who want to make requests to antimalware products from within their apps.</span></span>
- <span data-ttu-id="d44c5-106">Criadores de terceiros de produtos antimalware que desejam que seus produtos ofereçam os melhores recursos aos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d44c5-106">Third-party creators of antimalware products who want their products to offer the best features to applications.</span></span>

## <a name="application-developers"></a><span data-ttu-id="d44c5-107">Desenvolvedores de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d44c5-107">Application developers</span></span>

<span data-ttu-id="d44c5-108">O AMSI é projetado especialmente para combater "malware de arquivo".</span><span class="sxs-lookup"><span data-stu-id="d44c5-108">AMSI is designed in particular to combat "fileless malware".</span></span> <span data-ttu-id="d44c5-109">Os tipos de aplicativos que podem aproveitar a tecnologia AMSI de forma ideal incluem mecanismos de script, aplicativos que precisam de buffers de memória a serem verificados antes de usá-los e aplicativos que processam arquivos que podem conter código executável não PE (como macros do Microsoft Word e Excel ou documentos em PDF).</span><span class="sxs-lookup"><span data-stu-id="d44c5-109">Application types that can optimally leverage AMSI technology include script engines, applications that need memory buffers to be scanned before using them, and applications that process files that can contain non-PE executable code (such as Microsoft Word and Excel macros, or PDF documents).</span></span> <span data-ttu-id="d44c5-110">No entanto, a utilidade da tecnologia AMSI não está limitada a esses exemplos.</span><span class="sxs-lookup"><span data-stu-id="d44c5-110">However, the usefulness of AMSI technology is not limited to those examples.</span></span>

<span data-ttu-id="d44c5-111">Há duas maneiras pelas quais você pode interagir com AMSI em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d44c5-111">There are two ways in which you can interface with AMSI in your application.</span></span>

- <span data-ttu-id="d44c5-112">Usando as APIs do Win32 AMSI.</span><span class="sxs-lookup"><span data-stu-id="d44c5-112">By using the AMSI Win32 APIs.</span></span> <span data-ttu-id="d44c5-113">Consulte [funções da interface de verificação antimalware (AMSI)](/windows/desktop/amsi/antimalware-scan-interface-functions).</span><span class="sxs-lookup"><span data-stu-id="d44c5-113">See [Antimalware Scan Interface (AMSI) functions](/windows/desktop/amsi/antimalware-scan-interface-functions).</span></span>
- <span data-ttu-id="d44c5-114">Usando as interfaces COM do AMSI.</span><span class="sxs-lookup"><span data-stu-id="d44c5-114">By using the AMSI COM interfaces.</span></span> <span data-ttu-id="d44c5-115">Consulte a [interface **IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span><span class="sxs-lookup"><span data-stu-id="d44c5-115">See [**IAmsiStream** interface](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span></span>

<span data-ttu-id="d44c5-116">Para obter um exemplo de código que mostra como consumir AMSI em seu aplicativo COM, consulte o [aplicativo de exemplo da interface IAmsiStream](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span><span class="sxs-lookup"><span data-stu-id="d44c5-116">For sample code showing how to consume AMSI within your COM application, see the [IAmsiStream interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span></span>

## <a name="third-party-creators-of-antimalware-products"></a><span data-ttu-id="d44c5-117">Criadores de terceiros de produtos Antimalware</span><span class="sxs-lookup"><span data-stu-id="d44c5-117">Third-party creators of antimalware products</span></span>

<span data-ttu-id="d44c5-118">Como um criador de produtos Antimalware, você pode optar por criar e registrar seu próprio servidor COM em processo (uma DLL) para funcionar como um provedor AMSI.</span><span class="sxs-lookup"><span data-stu-id="d44c5-118">As a creator of antimalware products, you can choose to author and register your own in-process COM server (a DLL) to function as an AMSI provider.</span></span> <span data-ttu-id="d44c5-119">Esse provedor AMSI deve implementar a [interface **IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)e deve ser executado em processo.</span><span class="sxs-lookup"><span data-stu-id="d44c5-119">That AMSI provider must implement the [**IAntimalwareProvider** interface](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), and it must run in-process.</span></span>

<span data-ttu-id="d44c5-120">Observe que, após o Windows 10, versão 1709 (a atualização do outono 2017 Creators), sua DLL do provedor AMSI poderá não funcionar se depender de outras DLLs em seu caminho para serem carregadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d44c5-120">Note that, after Windows 10, version 1709 (the Fall 2017 Creators' Update), your AMSI provider DLL may not work if it depends upon other DLLs in its path to be loaded at the same time.</span></span> <span data-ttu-id="d44c5-121">Para evitar o seqüestro de DLL, recomendamos que a DLL do provedor carregue suas dependências explicitamente (com um caminho completo) usando chamadas de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) seguras ou equivalentes.</span><span class="sxs-lookup"><span data-stu-id="d44c5-121">To prevent DLL hijacking, we recommend that your provider DLL load its dependencies explicitly (with a full path) using secure [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) calls, or equivalent.</span></span> <span data-ttu-id="d44c5-122">Recomendamos isso em vez de depender do comportamento de pesquisa **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="d44c5-122">We recommend this instead of relying on the **LoadLibrary** search behavior.</span></span>

<span data-ttu-id="d44c5-123">A seção a seguir mostra como registrar seu provedor AMSI.</span><span class="sxs-lookup"><span data-stu-id="d44c5-123">The section below shows how to register your AMSI provider.</span></span> <span data-ttu-id="d44c5-124">Para obter um código de exemplo completo mostrando como criar sua própria DLL do provedor AMSI, consulte o [aplicativo de exemplo da interface IAntimalwareProvider](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span><span class="sxs-lookup"><span data-stu-id="d44c5-124">For full sample code showing how to author your own AMSI provider DLL, see the [IAntimalwareProvider interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span></span>

### <a name="register-your-provider-dll-with-amsi"></a><span data-ttu-id="d44c5-125">Registrar sua DLL de provedor com o AMSI</span><span class="sxs-lookup"><span data-stu-id="d44c5-125">Register your provider DLL with AMSI</span></span>

<span data-ttu-id="d44c5-126">Para começar, você precisa garantir que essas chaves do registro do Windows existam.</span><span class="sxs-lookup"><span data-stu-id="d44c5-126">To begin with, you need to ensure that these Windows Registry keys exist.</span></span>

- <span data-ttu-id="d44c5-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span><span class="sxs-lookup"><span data-stu-id="d44c5-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span></span>
- <span data-ttu-id="d44c5-128">HKLM\SOFTWARE\Classes\CLSID</span><span class="sxs-lookup"><span data-stu-id="d44c5-128">HKLM\SOFTWARE\Classes\CLSID</span></span>

<span data-ttu-id="d44c5-129">Um provedor de AMSI é um servidor COM em processo.</span><span class="sxs-lookup"><span data-stu-id="d44c5-129">An AMSI provider is an in-process COM server.</span></span> <span data-ttu-id="d44c5-130">Consequentemente, ele precisa se registrar com com.</span><span class="sxs-lookup"><span data-stu-id="d44c5-130">Consequently, it needs to register itself with COM.</span></span> <span data-ttu-id="d44c5-131">As classes COM são registradas no `HKLM\SOFTWARE\Classes\CLSID` .</span><span class="sxs-lookup"><span data-stu-id="d44c5-131">COM classes are registered in `HKLM\SOFTWARE\Classes\CLSID`.</span></span>

<span data-ttu-id="d44c5-132">O código a seguir mostra como registrar um provedor AMSI, cujo GUID (para este exemplo) vamos supor que é `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .</span><span class="sxs-lookup"><span data-stu-id="d44c5-132">The code below shows how to register an AMSI provider, whose GUID (for this example) we will assume is `2E5D8A62-77F9-4F7B-A90C-2744820139B2`.</span></span>

```cpp
#include <strsafe.h>
...
HRESULT SetKeyStringValue(_In_ HKEY key, _In_opt_ PCWSTR subkey, _In_opt_ PCWSTR valueName, _In_ PCWSTR stringValue)
{
    LONG status = RegSetKeyValue(key, subkey, valueName, REG_SZ, stringValue, (wcslen(stringValue) + 1) * sizeof(wchar_t));
    return HRESULT_FROM_WIN32(status);
}

STDAPI DllRegisterServer()
{
    wchar_t modulePath[MAX_PATH];
    if (GetModuleFileName(g_currentModule, modulePath, ARRAYSIZE(modulePath)) >= ARRAYSIZE(modulePath))
    {
        return E_UNEXPECTED;
    }

    // Create a standard COM registration for our CLSID.
    // The class must be registered as "Both" threading model,
    // and support multithreaded access.
    wchar_t clsidString[40];
    if (StringFromGUID2(__uuidof(SampleAmsiProvider), clsidString, ARRAYSIZE(clsidString)) == 0)
    {
        return E_UNEXPECTED;
    }

    wchar_t keyPath[200];
    HRESULT hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls\\InProcServer32", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, modulePath);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, L"ThreadingModel", L"Both");
    if (FAILED(hr)) return hr;

    // Register this CLSID as an anti-malware provider.
    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Microsoft\\AMSI\\Providers\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    return S_OK;
}
```

<span data-ttu-id="d44c5-133">Se a DLL implementar a [função DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), como o exemplo acima, você poderá registrá-la usando o executável fornecido pelo Windows `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="d44c5-133">If your DLL implements the [DllRegisterServer function](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), as the example above does, then you can register it by using the Windows-supplied executable `regsvr32.exe`.</span></span> <span data-ttu-id="d44c5-134">Em um prompt de comando com privilégios elevados, emita um comando desse formulário.</span><span class="sxs-lookup"><span data-stu-id="d44c5-134">From an elevated command prompt, issue a command of this form.</span></span>

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

<span data-ttu-id="d44c5-135">Neste exemplo, o comando cria as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d44c5-135">In this example, the command creates the following entries.</span></span>

<span data-ttu-id="d44c5-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="d44c5-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>

<span data-ttu-id="d44c5-137">&nbsp;&nbsp;&nbsp;&nbsp;**Os    REG_SZ implementação de provedor AMSI de exemplo**</span><span class="sxs-lookup"><span data-stu-id="d44c5-137">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_SZ    Sample AMSI Provider implementation**</span></span>


<span data-ttu-id="d44c5-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="d44c5-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**</span></span>

<span data-ttu-id="d44c5-139">&nbsp;&nbsp;&nbsp;&nbsp;**Os    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**</span><span class="sxs-lookup"><span data-stu-id="d44c5-139">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_EXPAND_SZ    %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**</span></span>

<span data-ttu-id="d44c5-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ ambos**</span><span class="sxs-lookup"><span data-stu-id="d44c5-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel    REG_SZ    Both**</span></span>

<span data-ttu-id="d44c5-141">Além do registro COM regular, você também precisa registrar o provedor com o AMSI.</span><span class="sxs-lookup"><span data-stu-id="d44c5-141">In addition to regular COM registration, you also need to enroll the provider with AMSI.</span></span> <span data-ttu-id="d44c5-142">Você faz isso adicionando uma entrada à chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="d44c5-142">You do that by adding an entry to the following key.</span></span>

<span data-ttu-id="d44c5-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span><span class="sxs-lookup"><span data-stu-id="d44c5-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span></span>

<span data-ttu-id="d44c5-144">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="d44c5-144">For example,</span></span>

<span data-ttu-id="d44c5-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="d44c5-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>
