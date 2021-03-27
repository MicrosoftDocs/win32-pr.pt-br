---
description: Este tópico mostra como criar um atalho para seu aplicativo, atribuí-lo a um AppUserModelID e instalá-lo na tela inicial.
title: Como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: bd02a0ec6512aa7637f0d6b2b281e1b862e61d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967726"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a><span data-ttu-id="634f7-103">Como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="634f7-103">How to enable desktop toast notifications through an AppUserModelID</span></span>

<span data-ttu-id="634f7-104">Este tópico mostra como criar um atalho para seu aplicativo, atribuí-lo a um [AppUserModelID](appids.md)e instalá-lo na tela inicial.</span><span class="sxs-lookup"><span data-stu-id="634f7-104">This topic shows you how to create a shortcut for your app, assign it an [AppUserModelID](appids.md), and install it in the Start screen.</span></span> <span data-ttu-id="634f7-105">É altamente recomendável que você faça isso na Windows Installer em vez de no código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="634f7-105">We strongly recommend that you do this in the Windows Installer rather than in your app's code.</span></span> <span data-ttu-id="634f7-106">Sem um atalho válido instalado na tela inicial ou em **todos os programas**, você não pode gerar uma notificação do sistema de um aplicativo de desktop.</span><span class="sxs-lookup"><span data-stu-id="634f7-106">Without a valid shortcut installed in the Start screen or in **All Programs**, you cannot raise a toast notification from a desktop app.</span></span>

> [!Note]  
> <span data-ttu-id="634f7-107">Os métodos de exemplo usados neste tópico são extraídos do [exemplo de notificação do sistema de área de trabalho](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span><span class="sxs-lookup"><span data-stu-id="634f7-107">The example methods used in this topic are taken from the [Desktop toast sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="634f7-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="634f7-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="634f7-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="634f7-109">Technologies</span></span>

-   <span data-ttu-id="634f7-110">COM</span><span class="sxs-lookup"><span data-stu-id="634f7-110">COM</span></span>

### <a name="prerequisites"></a><span data-ttu-id="634f7-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="634f7-111">Prerequisites</span></span>

-   <span data-ttu-id="634f7-112">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="634f7-112">Libraries</span></span>
    -   <span data-ttu-id="634f7-113">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="634f7-113">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="634f7-114">C \# : Windows. Winmd</span><span class="sxs-lookup"><span data-stu-id="634f7-114">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="634f7-115">C \# : pacote de códigos da API do Windows para Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="634f7-115">C\#: Windows API Code Pack for Microsoft .NET Framework</span></span>
-   <span data-ttu-id="634f7-116">Uma versão do Microsoft Visual Studio que oferece suporte a pelo menos o Windows 8</span><span class="sxs-lookup"><span data-stu-id="634f7-116">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="634f7-117">Instruções</span><span class="sxs-lookup"><span data-stu-id="634f7-117">Instructions</span></span>

### <a name="step-1-prepare-the-shortcut-to-be-created"></a><span data-ttu-id="634f7-118">Etapa 1: preparar o atalho a ser criado</span><span class="sxs-lookup"><span data-stu-id="634f7-118">Step 1: Prepare the shortcut to be created</span></span>

<span data-ttu-id="634f7-119">Este exemplo primeiro determina o caminho da pasta de dados de aplicativo do usuário por meio da função [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) .</span><span class="sxs-lookup"><span data-stu-id="634f7-119">This example first determines the path of the user's app data folder through the [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) function.</span></span> <span data-ttu-id="634f7-120">Em seguida, ele compõe o caminho completo para o atalho, determina que um atalho desse nome ainda não existe nesse local e passa essas informações para outro método que cria e instala o atalho.</span><span class="sxs-lookup"><span data-stu-id="634f7-120">It then composes the full path to the shortcut, determines that a shortcut of that name does not already exist at that location, and passes that information to another method which creates and installs the shortcut.</span></span>

<span data-ttu-id="634f7-121">Observe que o atalho pode ser implantado por usuário ou por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="634f7-121">Note that the shortcut can be deployed per-user or per-app.</span></span>


```C++
HRESULT DesktopToastsApp::TryCreateShortcut()
{
    wchar_t shortcutPath[MAX_PATH];
    DWORD charWritten = GetEnvironmentVariable(L"APPDATA", shortcutPath, MAX_PATH);
    HRESULT hr = charWritten > 0 ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        errno_t concatError = wcscat_s(shortcutPath, ARRAYSIZE(shortcutPath), L"\\Microsoft\\Windows\\Start Menu\\Programs\\Desktop Toasts App.lnk");
 
        hr = concatError == 0 ? S_OK : E_INVALIDARG;
        if (SUCCEEDED(hr))
        {
            DWORD attributes = GetFileAttributes(shortcutPath);
            bool fileExists = attributes < 0xFFFFFFF;

            if (!fileExists)
            {
                hr = InstallShortcut(shortcutPath);  // See step 2.
            }
            else
            {
                hr = S_FALSE;
            }
        }
    }
    return hr;
}
```



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a><span data-ttu-id="634f7-122">Etapa 2: criar o atalho e instalá-lo na tela inicial</span><span class="sxs-lookup"><span data-stu-id="634f7-122">Step 2: Create the shortcut and install it in the Start screen</span></span>

<span data-ttu-id="634f7-123">Este exemplo também recupera o repositório de propriedades do atalho e define a propriedade [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) necessária de uma variável definida anteriormente, `AppID` .</span><span class="sxs-lookup"><span data-stu-id="634f7-123">This example also retrieves the shortcut's property store and sets the required [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property from a previously defined variable, `AppID`.</span></span>


```C++
HRESULT DesktopToastsApp::InstallShortcut(_In_z_ wchar_t *shortcutPath)
{
    wchar_t exePath[MAX_PATH];
    
    DWORD charWritten = GetModuleFileNameEx(GetCurrentProcess(), nullptr, exePath, ARRAYSIZE(exePath));

    HRESULT hr = charWritten > 0 ? S_OK : E_FAIL;
    
    if (SUCCEEDED(hr))
    {
        ComPtr<IShellLink> shellLink;
        hr = CoCreateInstance(CLSID_ShellLink, nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink));

        if (SUCCEEDED(hr))
        {
            hr = shellLink->SetPath(exePath);
            if (SUCCEEDED(hr))
            {
                hr = shellLink->SetArguments(L"");
                if (SUCCEEDED(hr))
                {
                    ComPtr<IPropertyStore> propertyStore;

                    hr = shellLink.As(&propertyStore);
                    if (SUCCEEDED(hr))
                    {
                        PROPVARIANT appIdPropVar;
                        hr = InitPropVariantFromString(AppId, &appIdPropVar);
                        if (SUCCEEDED(hr))
                        {
                            hr = propertyStore->SetValue(PKEY_AppUserModel_ID, appIdPropVar);
                            if (SUCCEEDED(hr))
                            {
                                hr = propertyStore->Commit();
                                if (SUCCEEDED(hr))
                                {
                                    ComPtr<IPersistFile> persistFile;
                                    hr = shellLink.As(&persistFile);
                                    if (SUCCEEDED(hr))
                                    {
                                        hr = persistFile->Save(shortcutPath, TRUE);
                                    }
                                }
                            }
                            PropVariantClear(&appIdPropVar);
                        }
                    }
                }
            }
        }
    }
    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="634f7-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="634f7-124">Remarks</span></span>

<span data-ttu-id="634f7-125">Como alternativa à abordagem mostrada neste tópico, você pode usar uma estrutura como o Windows Installer XML (WiX) para gerar o atalho e implantá-lo como parte do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="634f7-125">As an alternative to the approach shown in this topic, you can use a framework such as the Windows Installer XML (WiX) to generate the shortcut and deploy it as part of the Windows Installer.</span></span> <span data-ttu-id="634f7-126">Nesse caso, esse código deve ser incluído no MSI em vez de no código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="634f7-126">In that case, this code should be included in the MSI rather than in the app's code.</span></span> <span data-ttu-id="634f7-127">Para obter mais informações, consulte o arquivo de configuração do WiX de exemplo incluído com o exemplo [enviar notificações do sistema de aplicativos da área de trabalho](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) .</span><span class="sxs-lookup"><span data-stu-id="634f7-127">For more information, see the sample WiX configuration file included with the [Sending toast notifications from desktop apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="634f7-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="634f7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="634f7-129">Início rápido: enviando uma notificação do sistema da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="634f7-129">Quickstart: Sending a toast notification from the desktop</span></span>](quickstart-sending-desktop-toast.md)
</dt> <dt>

<span data-ttu-id="634f7-130">[Enviando notificações do sistema de exemplo de aplicativos da área de trabalho](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="634f7-130">[Sending toast notifications from desktop apps sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span></span>
</dt> <dt>

[<span data-ttu-id="634f7-131">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="634f7-131">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> <dt>

<span data-ttu-id="634f7-132">[Como instalar as ferramentas do Windows Installer XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-132">[How to: Install the Windows Installer XML (WiX) Tools](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="634f7-133">Esquema XML do sistema</span><span class="sxs-lookup"><span data-stu-id="634f7-133">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="634f7-134">[Visão geral da notificação do sistema](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-134">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="634f7-135">[Início rápido: enviando uma notificação do sistema](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-135">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="634f7-136">[Início rápido: enviando uma notificação por push do sistema](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-136">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="634f7-137">Diretrizes e lista de verificação para notificações do sistema</span><span class="sxs-lookup"><span data-stu-id="634f7-137">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[<span data-ttu-id="634f7-138">Como adicionar imagens a um modelo do sistema</span><span class="sxs-lookup"><span data-stu-id="634f7-138">How to add images to a toast template</span></span>](/previous-versions/windows/)
</dt> <dt>

[<span data-ttu-id="634f7-139">Como verificar as configurações de notificação do sistema</span><span class="sxs-lookup"><span data-stu-id="634f7-139">How to check toast notification settings</span></span>](/previous-versions/windows/)
</dt> <dt>

<span data-ttu-id="634f7-140">[Como escolher e usar um modelo de notificação do sistema](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-140">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="634f7-141">[Como lidar com a ativação de uma notificação do sistema](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-141">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="634f7-142">[Como aceitar notificações do sistema](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-142">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="634f7-143">[Escolhendo um modelo de notificação do sistema](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-143">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="634f7-144">[Opções de áudio do sistema](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="634f7-144">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
