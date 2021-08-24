---
description: A interface IHWEventHandler pode ser registrada na corrompidos (tabela de objetos em execução) para que a execução de aplicativos tenha acesso a eventos de reprodução automática.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Como usar eventos de reprodução automática em aplicativos em execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab30fa020b5501f8832a5b350ad409934ecbb4258d75adf147e908c699516474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714808"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a>Como usar eventos de reprodução automática em aplicativos em execução

A interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) pode ser registrada na corrompidos (tabela de objetos em execução) para que a execução de aplicativos tenha acesso a eventos de reprodução automática.

As instruções a seguir descrevem como usar eventos de reprodução automática em aplicativos em execução.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Crie um novo componente que implemente a interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

### <a name="step-2"></a>Etapa 2:

Inicialize o novo componente com o valor InitCmdLine da entrada do manipulador em particular na chave de **manipuladores** .

Essa etapa é necessária porque a reprodução automática não chama o método Initialize.

### <a name="step-3"></a>Etapa 3:

Chame a função [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) para obter um moniker que representa o componente e o manipulador de eventos que você deseja chamar.

### <a name="step-4"></a>Etapa 4:

Use o parâmetro *ppmoniker* para registrar seu componente no corrompidos.

## <a name="remarks"></a>Comentários

> [!Note]  
> [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode representar riscos de segurança. Consulte a documentação **LoadLibrary** para obter informações sobre como carregar corretamente DLLs com versões diferentes do Windows.

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

A chamada para [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) exige que o componente tenha as seguintes informações de **AppID** no registro.

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a>Tópicos relacionados

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[**CreateHardwareEventMoniker**](createhardwareeventmoniker.md)
