---
description: A interface IHWEventHandler pode ser registrada na corrompidos (tabela de objetos em execução) para que a execução de aplicativos tenha acesso a eventos de reprodução automática.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Como usar eventos de reprodução automática em aplicativos em execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51795a3992bdb40dde833bb3e352905efaa2be63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921667"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a><span data-ttu-id="fac7b-103">Como usar eventos de reprodução automática em aplicativos em execução</span><span class="sxs-lookup"><span data-stu-id="fac7b-103">How to Use AutoPlay Events in Running Applications</span></span>

<span data-ttu-id="fac7b-104">A interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) pode ser registrada na corrompidos (tabela de objetos em execução) para que a execução de aplicativos tenha acesso a eventos de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="fac7b-104">The [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface can be registered in the running object table (ROT) so that running applications have access to AutoPlay events.</span></span>

<span data-ttu-id="fac7b-105">As instruções a seguir descrevem como usar eventos de reprodução automática em aplicativos em execução.</span><span class="sxs-lookup"><span data-stu-id="fac7b-105">The following instructions describe how to use AutoPlay events in running applications.</span></span>

## <a name="instructions"></a><span data-ttu-id="fac7b-106">Instruções</span><span class="sxs-lookup"><span data-stu-id="fac7b-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="fac7b-107">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="fac7b-107">Step 1:</span></span>

<span data-ttu-id="fac7b-108">Crie um novo componente que implemente a interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="fac7b-108">Create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="fac7b-109">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="fac7b-109">Step 2:</span></span>

<span data-ttu-id="fac7b-110">Inicialize o novo componente com o valor InitCmdLine da entrada do manipulador em particular na chave de **manipuladores** .</span><span class="sxs-lookup"><span data-stu-id="fac7b-110">Initialize the new component with the InitCmdLine value from the particular handler's entry under the **Handlers** key.</span></span>

<span data-ttu-id="fac7b-111">Essa etapa é necessária porque a reprodução automática não chama o método Initialize.</span><span class="sxs-lookup"><span data-stu-id="fac7b-111">This step is required because Autoplay does not call the Initialize method.</span></span>

### <a name="step-3"></a><span data-ttu-id="fac7b-112">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="fac7b-112">Step 3:</span></span>

<span data-ttu-id="fac7b-113">Chame a função [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) para obter um moniker que representa o componente e o manipulador de eventos que você deseja chamar.</span><span class="sxs-lookup"><span data-stu-id="fac7b-113">Call the [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) function to get a moniker that represents your component and the event handler that you want to call.</span></span>

### <a name="step-4"></a><span data-ttu-id="fac7b-114">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="fac7b-114">Step 4:</span></span>

<span data-ttu-id="fac7b-115">Use o parâmetro *ppmoniker* para registrar seu componente no corrompidos.</span><span class="sxs-lookup"><span data-stu-id="fac7b-115">Use the *ppmoniker* parameter to register your component in the ROT.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac7b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fac7b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fac7b-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode representar riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="fac7b-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) can pose security risks.</span></span> <span data-ttu-id="fac7b-118">Consulte a documentação de **LoadLibrary** para obter informações sobre como carregar DLLs corretamente com diferentes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="fac7b-118">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

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

<span data-ttu-id="fac7b-119">A chamada para [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) exige que o componente tenha as seguintes informações de **AppID** no registro.</span><span class="sxs-lookup"><span data-stu-id="fac7b-119">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that the component have the following **AppID** information in the registry.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="fac7b-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fac7b-120">Related topics</span></span>

[<span data-ttu-id="fac7b-121">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="fac7b-121">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[<span data-ttu-id="fac7b-122">**CreateHardwareEventMoniker**</span><span class="sxs-lookup"><span data-stu-id="fac7b-122">**CreateHardwareEventMoniker**</span></span>](createhardwareeventmoniker.md)
