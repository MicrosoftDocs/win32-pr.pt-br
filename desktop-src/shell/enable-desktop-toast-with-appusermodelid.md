---
description: Este tópico mostra como criar um atalho para seu aplicativo, atribuí-lo a um AppUserModelID e instalá-lo no tela inicial.
title: Como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 517c2b72e830c00b105048adc63923291f896cd5d0d77569c91b1aa12e034e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459788"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a>Como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID

Este tópico mostra como criar um atalho para seu aplicativo, atribuí-lo a [um AppUserModelID](appids.md)e instalá-lo no tela inicial. É fortemente recomendável que você faça isso no Windows instalador em vez de no código do aplicativo. Sem um atalho válido instalado no tela inicial ou em Todos os Programas **,** você não pode auar uma notificação do sistema de um aplicativo da área de trabalho.

> [!Note]  
> Os métodos de exemplo usados neste tópico são retirados do exemplo [de sistema de área de trabalho](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).

 

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   COM

### <a name="prerequisites"></a>Pré-requisitos

-   Bibliotecas
    -   C++: Runtime.object.lib
    -   C: \# Windows. Winmd
-   C: \# Windows code pack de API para Microsoft .NET Framework
-   Uma versão do Microsoft Visual Studio que dá suporte a pelo menos Windows 8

## <a name="instructions"></a>Instruções

### <a name="step-1-prepare-the-shortcut-to-be-created"></a>Etapa 1: Preparar o atalho a ser criado

Este exemplo primeiro determina o caminho da pasta de dados do aplicativo do usuário por meio da [**função GetEnvironmentVariable.**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) Em seguida, ele compõe o caminho completo para o atalho, determina que um atalho desse nome ainda não existe nesse local e passa essas informações para outro método que cria e instala o atalho.

Observe que o atalho pode ser implantado por usuário ou por aplicativo.


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



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a>Etapa 2: Criar o atalho e instalá-lo no tela inicial

Este exemplo também recupera o armazenamento de propriedades do atalho e define a propriedade [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) necessária de uma variável definida anteriormente, `AppID` .


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



## <a name="remarks"></a>Comentários

Como alternativa à abordagem mostrada neste tópico, você pode usar uma estrutura como o WiX (XML do instalador do Windows) para gerar o atalho e implantá-lo como parte do instalador Windows. Nesse caso, esse código deve ser incluído na MSI em vez de no código do aplicativo. Para obter mais informações, consulte o arquivo de configuração WiX de exemplo incluído com o exemplo [Enviar notificações do sistema de aplicativos da área de](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) trabalho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Início Rápido: Enviar uma notificação do sistema da área de trabalho](quickstart-sending-desktop-toast.md)
</dt> <dt>

[Exemplo de envio de notificações do sistema de aplicativos da área de trabalho](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))
</dt> <dt>

[IDs de modelo de usuário do aplicativo (AppUserModelIDs)](appids.md)
</dt> <dt>

[Como instalar as ferramentas Windows XML (WiX) do Windows Installer](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))
</dt> <dt>

[Esquema XML do toast](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Visão geral da notificação do toast](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Início Rápido: Enviar uma notificação do toast](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Início Rápido: Enviar uma notificação por push do toast](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Diretrizes e lista de verificação para notificações do toast](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Como adicionar imagens a um modelo de toast](/previous-versions/windows/)
</dt> <dt>

[Como verificar as configurações de notificação do toast](/previous-versions/windows/)
</dt> <dt>

[Como escolher e usar um modelo de sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Como lidar com a ativação de uma notificação do sistema](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Como optar por notificações do toast](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Escolhendo um modelo de sistema](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opções de áudio do sistema](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
