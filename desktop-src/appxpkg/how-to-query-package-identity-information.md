---
title: Consultar informações de manifesto do pacote de aplicativo (C++)
description: Saiba como obter informações do manifesto do pacote do aplicativo para um aplicativo do Windows usando a API de empacotamento.
ms.assetid: A29986F9-C620-48CD-87F8-525DFA076AAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9940f92a4412be7731db2454d68b4429522b63f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007370"
---
# <a name="query-app-package-manifest-info-c"></a><span data-ttu-id="bc017-103">Consultar informações de manifesto do pacote de aplicativo (C++)</span><span class="sxs-lookup"><span data-stu-id="bc017-103">Query app package manifest info (C++)</span></span>

<span data-ttu-id="bc017-104">Saiba como obter informações do manifesto do pacote do aplicativo para um aplicativo do Windows usando a [API de empacotamento](interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="bc017-104">Learn how to get info from the app package manifest for a Windows app using the [packaging API](interfaces.md).</span></span>

### <a name="create-a-package-manifest-reader"></a><span data-ttu-id="bc017-105">Criar um leitor de manifesto de pacote</span><span class="sxs-lookup"><span data-stu-id="bc017-105">Create a package manifest reader</span></span>

<span data-ttu-id="bc017-106">Para criar um leitor de manifesto de pacote, chame [**IAppxFactory:: CreatePackageReader**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) para criar um leitor de pacote.</span><span class="sxs-lookup"><span data-stu-id="bc017-106">To create a package manifest reader, call [**IAppxFactory::CreatePackageReader**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) to create a package reader.</span></span> <span data-ttu-id="bc017-107">O primeiro parâmetro é um fluxo de entrada para o pacote (arquivo. AppX).</span><span class="sxs-lookup"><span data-stu-id="bc017-107">The first parameter is an input stream for the package (.appx file).</span></span> <span data-ttu-id="bc017-108">O segundo parâmetro é um parâmetro de saída que recebe um ponteiro para um ponteiro [**IAppxPackageReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) .</span><span class="sxs-lookup"><span data-stu-id="bc017-108">The second parameter is an output parameter that receives a pointer to an [**IAppxPackageReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) pointer.</span></span> <span data-ttu-id="bc017-109">Em seguida, chame [**IAppxPackageReader:: getmanifest**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getmanifest) para obter o leitor de manifesto.</span><span class="sxs-lookup"><span data-stu-id="bc017-109">Next, call [**IAppxPackageReader::GetManifest**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getmanifest) to get the manifest reader.</span></span> <span data-ttu-id="bc017-110">O parâmetro é um parâmetro de saída que recebe um ponteiro para um ponteiro [**IAppxManifestReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader) .</span><span class="sxs-lookup"><span data-stu-id="bc017-110">The parameter is an output parameter that receives a pointer to an [**IAppxManifestReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader) pointer.</span></span>


```C++
int wmain(
    _In_ int argc,
    _In_reads_(argc) wchar_t** argv)
{
    HRESULT hr = S_OK;
 
    if (argc != 2)
    {
        wprintf(L"Usage: DescribeAppx.exe inputFile\n");
        wprintf(L"       inputFile: Path to the app package to read\n");
        return 2;
    }

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        IAppxPackageReader* packageReader = NULL;
        IAppxManifestReader* manifestReader = NULL;

        // Create a package reader using the file name given in command line
        hr = GetPackageReader(argv[1], &packageReader);

        // Get manifest reader for the package and read from the manifest
        if (SUCCEEDED(hr))
        {
            hr = packageReader->GetManifest(&manifestReader);
        }
        if (SUCCEEDED(hr))
        {
            hr = ReadManifest(manifestReader);
        }
    }
}

//
// Creates an app package reader.
//
// Parameters:
//   inputFileName 
//     Fully qualified name of the app package (.appx file) to be opened.
//   reader 
//     On success, receives the created instance of IAppxPackageReader.
//
HRESULT GetPackageReader(
    _In_ LPCWSTR inputFileName,
    _Outptr_ IAppxPackageReader** reader)
{
    HRESULT hr = S_OK;
    IAppxFactory* appxFactory = NULL;
    IStream* inputStream = NULL;

    // Create a new factory
    hr = CoCreateInstance(
            __uuidof(AppxFactory),
            NULL,
            CLSCTX_INPROC_SERVER,
            __uuidof(IAppxFactory),
            (LPVOID*)(&appxFactory));

    // Create a stream over the input app package
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                inputFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0, // default file attributes
                FALSE, // do not create new file
                NULL, // no template
                &inputStream);
    }

    // Create a new package reader using the factory.  For 
    // simplicity, we don't verify the digital signature of the package.
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageReader(
                inputStream,
                reader);
    }

    // Clean up allocated resources
    if (inputStream != NULL)
    {
        inputStream->Release();
        inputStream = NULL;
    }
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    return hr;
}
```



### <a name="read-package-identity-info"></a><span data-ttu-id="bc017-111">Ler informações de identidade do pacote</span><span class="sxs-lookup"><span data-stu-id="bc017-111">Read package identity info</span></span>

<span data-ttu-id="bc017-112">A identificação do pacote é especificada usando o elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) no manifesto.</span><span class="sxs-lookup"><span data-stu-id="bc017-112">Package identify is specified using the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the manifest.</span></span> <span data-ttu-id="bc017-113">Use [**IAppxManifestReader:: Getpackageid**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getpackageid) para obter um [**IAppxManifestPackageId**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestpackageid) para ler informações de identidade do pacote, como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="bc017-113">Use [**IAppxManifestReader::GetPackageId**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getpackageid) to get an [**IAppxManifestPackageId**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestpackageid) to read package identity info, as shown here.</span></span>

<span data-ttu-id="bc017-114">Esse código usa [**IAppxManifestPackageId:: GetPackageFullName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getpackagefullname) para obter o nome completo do pacote, [**IAppxManifestPackageId:: GetName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getname) para obter o nome do pacote e [**IAppxManifestPackageId:: GetVersion**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getversion) para obter a versão do pacote.</span><span class="sxs-lookup"><span data-stu-id="bc017-114">This code uses [**IAppxManifestPackageId::GetPackageFullName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getpackagefullname) to get the package full name, [**IAppxManifestPackageId::GetName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getname) to get the package name, and [**IAppxManifestPackageId::GetVersion**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getversion) to get the package version.</span></span>


```C++
//
// Reads a subset of the manifest Identity element.
//
//
HRESULT ReadManifestPackageId(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestPackageId* packageId = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetPackageId(&packageId);
    if (SUCCEEDED(hr))
    {
        LPWSTR packageFullName = NULL;
        LPWSTR packageName = NULL;
        UINT64 packageVersion = 0;

        hr = packageId->GetPackageFullName(&packageFullName);

        if (SUCCEEDED(hr))
        {
            hr = packageId->GetName(&packageName);
        }
        if (SUCCEEDED(hr))
        {
            hr = packageId->GetVersion(&packageVersion);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package full name: %s\n", packageFullName);
            wprintf(L"Package name: %s\n", packageName);
            wprintf(L"Package version: ");

            // Convert version number from 64-bit integer to dot-quad form
            for (int bitPosition = 0x30; bitPosition >= 0; bitPosition -= 0x10)
            {
                UINT64 versionWord = (packageVersion >> bitPosition) & 0xFFFF;
                wprintf(L"%llu.", versionWord);
            }
            wprintf(L"\n");
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(packageFullName);
        CoTaskMemFree(packageName);
    }

    // Clean up allocated resources
    if (packageId != NULL)
    {
        packageId->Release();
        packageId = NULL;
    }
     
    return hr;
}
```



### <a name="read-metadata-that-describes-the-package-to-users"></a><span data-ttu-id="bc017-115">Ler metadados que descrevem o pacote para os usuários</span><span class="sxs-lookup"><span data-stu-id="bc017-115">Read metadata that describes the package to users</span></span>

<span data-ttu-id="bc017-116">As propriedades são especificadas usando o elemento [**Properties**](/uwp/schemas/appxpackage/appxmanifestschema/element-properties) no manifesto.</span><span class="sxs-lookup"><span data-stu-id="bc017-116">Properties are specified using the [**Properties**](/uwp/schemas/appxpackage/appxmanifestschema/element-properties) element in the manifest.</span></span> <span data-ttu-id="bc017-117">Use [**IAppxManifestReader:: GetProperties**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getproperties) para obter um [**IAppxManifestProperties**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestproperties) para ler este nó, como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="bc017-117">Use [**IAppxManifestReader::GetProperties**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getproperties) to get an [**IAppxManifestProperties**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestproperties) to read this node, as shown here.</span></span>

<span data-ttu-id="bc017-118">Esse código usa [**IAppxManifestProperties:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue) para obter o nome de exibição do pacote e a descrição do pacote.</span><span class="sxs-lookup"><span data-stu-id="bc017-118">This code uses [**IAppxManifestProperties::GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue) to get the package display name and package description.</span></span>


```C++
//
// Reads a subset of the manifest Properties element.
//
//
HRESULT ReadManifestProperties(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestProperties* properties = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetProperties(&properties);
    if (SUCCEEDED(hr))
    {
        LPWSTR displayName = NULL;
        LPWSTR description = NULL;

        hr = properties->GetStringValue(L"DisplayName", &displayName);

        if (SUCCEEDED(hr))
        {
            hr = properties->GetStringValue(L"Description", &description);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package display name: %s\n", displayName);
            wprintf(L"Package description:  %s\n", description);
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(displayName);
        CoTaskMemFree(description);
    }
    // Clean up allocated resources
    if (properties != NULL)
    {
        properties->Release();
        properties = NULL;
    }

    return hr;
}
```



### <a name="read-metadata-about-the-apps-included-in-the-package"></a><span data-ttu-id="bc017-119">Ler metadados sobre os aplicativos incluídos no pacote</span><span class="sxs-lookup"><span data-stu-id="bc017-119">Read metadata about the apps included in the package</span></span>

<span data-ttu-id="bc017-120">Os aplicativos são especificados usando o elemento [**Applications**](/uwp/schemas/appxpackage/appxmanifestschema/element-applications) no manifesto.</span><span class="sxs-lookup"><span data-stu-id="bc017-120">Apps are specified using the [**Applications**](/uwp/schemas/appxpackage/appxmanifestschema/element-applications) element in the manifest.</span></span> <span data-ttu-id="bc017-121">Use [**IAppxManifestReader:: GetApplications**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getapplications) para obter um [**IAppxManifestApplicationsEnumerator**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator) para ler este nó.</span><span class="sxs-lookup"><span data-stu-id="bc017-121">Use [**IAppxManifestReader::GetApplications**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getapplications) to get an [**IAppxManifestApplicationsEnumerator**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator) to read this node.</span></span> <span data-ttu-id="bc017-122">Use [**IAppxManifestApplicationsEnumerator:: GetCurrent**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent) e [**IAppxManifestApplicationsEnumerator:: MoveNext**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext) para obter um [**IAppxManifestApplication**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplication) para cada aplicativo no pacote.</span><span class="sxs-lookup"><span data-stu-id="bc017-122">Use [**IAppxManifestApplicationsEnumerator::GetCurrent**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent) and [**IAppxManifestApplicationsEnumerator::MoveNext**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext) to get an [**IAppxManifestApplication**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplication) for each app in the package.</span></span>

<span data-ttu-id="bc017-123">Esse código usa [**IAppxManifestApplication:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue) para obter o nome de exibição de cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc017-123">This code uses [**IAppxManifestApplication::GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue) to get the display name for each app.</span></span>


```C++
//
// Reads a subset of the manifest Applications element.
//
//
HRESULT ReadManifestApplications(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;
    BOOL hasCurrent = FALSE;
    UINT32 applicationsCount = 0;

    IAppxManifestApplicationsEnumerator* applications = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetApplications(&applications);
    if (SUCCEEDED(hr))
    {
        hr = applications->GetHasCurrent(&hasCurrent);

        while (SUCCEEDED(hr) && hasCurrent)
        {
            IAppxManifestApplication* application = NULL;
            LPWSTR applicationName = NULL;

            hr = applications->GetCurrent(&application);
            if (SUCCEEDED(hr))
            {
                application->GetStringValue(L"DisplayName", &applicationName);
            }
            if (SUCCEEDED(hr))
            {
                applicationsCount++;
                wprintf(L"App #%u: %s\n", applicationsCount, applicationName);
            }

            if (SUCCEEDED(hr))
            {
                hr = applications->MoveNext(&hasCurrent);
            }
            if (application != NULL)
            {
                application->Release();
                application = NULL;
            }
            CoTaskMemFree(applicationName);
        }

        wprintf(L"Count of apps in the package: %u\n", applicationsCount);
    }

    // Clean up allocated resources
    if (applications != NULL)
    {
        applications->Release();
        applications = NULL;
    }

    return hr;
}
```



### <a name="clean-up-the-package-manifest-reader"></a><span data-ttu-id="bc017-124">Limpar o leitor de manifesto de pacote</span><span class="sxs-lookup"><span data-stu-id="bc017-124">Clean up the package manifest reader</span></span>

<span data-ttu-id="bc017-125">Antes de retornar da `wmain` função, chame o método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) para limpar o leitor de manifesto de pacote e chamar a função [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="bc017-125">Before returning from the `wmain` function, call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method to clean up the package manifest reader and call the [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
// Clean up allocated resources
if (manifestReader != NULL)
{
    manifestReader->Release();
    manifestReader = NULL;
}
if (packageReader != NULL)
{
    packageReader->Release();
    packageReader = NULL;
}

CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="bc017-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc017-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc017-127">**Amostras**</span><span class="sxs-lookup"><span data-stu-id="bc017-127">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="bc017-128">Exemplo de pacote do aplicativo de consulta e manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="bc017-128">Query app package and app manifest sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx)
</dt> <dt>

<span data-ttu-id="bc017-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bc017-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc017-130">**IAppxManifestReader**</span><span class="sxs-lookup"><span data-stu-id="bc017-130">**IAppxManifestReader**</span></span>](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader)
</dt> </dl>

 

 