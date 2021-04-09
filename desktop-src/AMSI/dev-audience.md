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
# <a name="developer-audience-and-sample-code"></a>Público do desenvolvedor e código de exemplo

A interface de verificação antimalware foi projetada para ser usada por dois grupos de desenvolvedores.

- Desenvolvedores de aplicativos que desejam fazer solicitações para produtos antimalware de dentro de seus aplicativos.
- Criadores de terceiros de produtos antimalware que desejam que seus produtos ofereçam os melhores recursos aos aplicativos.

## <a name="application-developers"></a>Desenvolvedores de aplicativos

O AMSI é projetado especialmente para combater "malware de arquivo". Os tipos de aplicativos que podem aproveitar a tecnologia AMSI de forma ideal incluem mecanismos de script, aplicativos que precisam de buffers de memória a serem verificados antes de usá-los e aplicativos que processam arquivos que podem conter código executável não PE (como macros do Microsoft Word e Excel ou documentos em PDF). No entanto, a utilidade da tecnologia AMSI não está limitada a esses exemplos.

Há duas maneiras pelas quais você pode interagir com AMSI em seu aplicativo.

- Usando as APIs do Win32 AMSI. Consulte [funções da interface de verificação antimalware (AMSI)](/windows/desktop/amsi/antimalware-scan-interface-functions).
- Usando as interfaces COM do AMSI. Consulte a [interface **IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream).

Para obter um exemplo de código que mostra como consumir AMSI em seu aplicativo COM, consulte o [aplicativo de exemplo da interface IAmsiStream](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Criadores de terceiros de produtos Antimalware

Como um criador de produtos Antimalware, você pode optar por criar e registrar seu próprio servidor COM em processo (uma DLL) para funcionar como um provedor AMSI. Esse provedor AMSI deve implementar a [interface **IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)e deve ser executado em processo.

Observe que, após o Windows 10, versão 1709 (a atualização do outono 2017 Creators), sua DLL do provedor AMSI poderá não funcionar se depender de outras DLLs em seu caminho para serem carregadas ao mesmo tempo. Para evitar o seqüestro de DLL, recomendamos que a DLL do provedor carregue suas dependências explicitamente (com um caminho completo) usando chamadas de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) seguras ou equivalentes. Recomendamos isso em vez de depender do comportamento de pesquisa **LoadLibrary** .

A seção a seguir mostra como registrar seu provedor AMSI. Para obter um código de exemplo completo mostrando como criar sua própria DLL do provedor AMSI, consulte o [aplicativo de exemplo da interface IAntimalwareProvider](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Registrar sua DLL de provedor com o AMSI

Para começar, você precisa garantir que essas chaves do registro do Windows existam.

- HKLM\SOFTWARE\Microsoft\AMSI\Providers
- HKLM\SOFTWARE\Classes\CLSID

Um provedor de AMSI é um servidor COM em processo. Consequentemente, ele precisa se registrar com com. As classes COM são registradas no `HKLM\SOFTWARE\Classes\CLSID` .

O código a seguir mostra como registrar um provedor AMSI, cujo GUID (para este exemplo) vamos supor que é `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .

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

Se a DLL implementar a [função DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), como o exemplo acima, você poderá registrá-la usando o executável fornecido pelo Windows `regsvr32.exe` . Em um prompt de comando com privilégios elevados, emita um comando desse formulário.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

Neste exemplo, o comando cria as entradas a seguir.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**Os    REG_SZ implementação de provedor AMSI de exemplo**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**Os    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ ambos**

Além do registro COM regular, você também precisa registrar o provedor com o AMSI. Você faz isso adicionando uma entrada à chave a seguir.

**HKLM\SOFTWARE\Microsoft\AMSI\Providers**

Por exemplo,

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**
