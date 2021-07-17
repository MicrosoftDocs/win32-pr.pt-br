---
title: XInput e DirectInput
description: XInput é uma API que permite que os aplicativos recebam entrada do controlador Xbox para Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58339616f1e9e3a43529b6853bfc193d359ef11e
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373192"
---
# <a name="xinput-and-directinput"></a><span data-ttu-id="06493-103">XInput e DirectInput</span><span class="sxs-lookup"><span data-stu-id="06493-103">XInput and DirectInput</span></span>

<span data-ttu-id="06493-104">XInput é uma API que permite que os aplicativos recebam entrada do controlador Xbox para Windows.</span><span class="sxs-lookup"><span data-stu-id="06493-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="06493-105">Este documento descreve as diferenças entre as implementações XInput e [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) do controlador Xbox e como você pode dar suporte a dispositivos XInput e dispositivos DirectInput herdados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="06493-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="06493-106">o uso de [directinput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdado não é recomendado e o directinput não está disponível para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="06493-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="06493-107">O novo padrão: XInput</span><span class="sxs-lookup"><span data-stu-id="06493-107">The New Standard: XInput</span></span>

<span data-ttu-id="06493-108">O XInput agora está disponível para desenvolvimento de jogos.</span><span class="sxs-lookup"><span data-stu-id="06493-108">XInput is now available for game development.</span></span> <span data-ttu-id="06493-109">Esse é o novo padrão de entrada para o Xbox e o Windows.</span><span class="sxs-lookup"><span data-stu-id="06493-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="06493-110">as APIs estão disponíveis por meio do SDK do DirectX e o driver está disponível por meio de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="06493-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="06493-111">Há várias vantagens em usar o XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="06493-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="06493-112">O XInput é mais fácil de usar e requer menos configuração do que o [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06493-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="06493-113">o Xbox e a programação de Windows usarão os mesmos conjuntos de APIs principais, permitindo que a programação converta várias plataformas de forma muito mais fácil</span><span class="sxs-lookup"><span data-stu-id="06493-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="06493-114">Haverá uma grande base instalada de controladores do Xbox</span><span class="sxs-lookup"><span data-stu-id="06493-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="06493-115">Dispositivos XInput (ou seja, os controladores Xbox) terão a funcionalidade de vibração somente ao usar APIs XInput</span><span class="sxs-lookup"><span data-stu-id="06493-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="06493-116">Controladores futuros lançados para o console do Xbox (ou seja, rodas de direcionamento) também funcionarão em Windows</span><span class="sxs-lookup"><span data-stu-id="06493-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="06493-117">Usando o controlador Xbox com o DirectInput</span><span class="sxs-lookup"><span data-stu-id="06493-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="06493-118">O controlador Xbox é enumerado corretamente no [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))e pode ser usado com o DirectInputAPIs.</span><span class="sxs-lookup"><span data-stu-id="06493-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="06493-119">No entanto, algumas funcionalidades fornecidas pelo XInput estarão faltando na implementação do DirectInput:</span><span class="sxs-lookup"><span data-stu-id="06493-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="06493-120">Os botões de gatilho à esquerda e à direita funcionarão como um único botão, não de forma independente</span><span class="sxs-lookup"><span data-stu-id="06493-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="06493-121">Os efeitos de vibração não estarão disponíveis</span><span class="sxs-lookup"><span data-stu-id="06493-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="06493-122">A consulta de dispositivos Headset não estará disponível</span><span class="sxs-lookup"><span data-stu-id="06493-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="06493-123">A combinação dos gatilhos esquerdo e direito no [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) é por design.</span><span class="sxs-lookup"><span data-stu-id="06493-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="06493-124">Os jogos sempre assumiram que os eixos do dispositivo DirectInput estão centralizados quando não há interação do usuário com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06493-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="06493-125">No entanto, o controlador Xbox foi projetado para registrar o valor mínimo, e não o centro, quando os gatilhos não estão sendo mantidos.</span><span class="sxs-lookup"><span data-stu-id="06493-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="06493-126">Os jogos mais antigos, portanto, assumem a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="06493-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="06493-127">A solução foi combinar os gatilhos, definir um gatilho para uma direção positiva e o outro para uma direção negativa, portanto, nenhuma interação do usuário é indicar ao [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) do "controle" estar no centro.</span><span class="sxs-lookup"><span data-stu-id="06493-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="06493-128">Para testar os valores do gatilho separadamente, você deve usar XInput.</span><span class="sxs-lookup"><span data-stu-id="06493-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="06493-129">XInput e DirectInput lado a lado</span><span class="sxs-lookup"><span data-stu-id="06493-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="06493-130">Ao dar suporte apenas a XInput, seu jogo não funcionará com dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdados.</span><span class="sxs-lookup"><span data-stu-id="06493-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="06493-131">O XInput não reconhecerá esses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="06493-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="06493-132">Se você quiser que seu jogo dê suporte a dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdados, você poderá usar o DirectInput e o XInput lado a lado.</span><span class="sxs-lookup"><span data-stu-id="06493-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="06493-133">Ao enumerar seus dispositivos do DirectInput, todos os dispositivos do DirectInput serão enumerados corretamente.</span><span class="sxs-lookup"><span data-stu-id="06493-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="06493-134">Todos os dispositivos XInput aparecerão como dispositivos XInput e DirectInput, mas eles não devem ser manipulados por meio do DirectInput.</span><span class="sxs-lookup"><span data-stu-id="06493-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="06493-135">Você precisará determinar quais dos seus dispositivos DirectInput são dispositivos herdados e quais são dispositivos XInput e removê-los da enumeração de dispositivos do DirectInput.</span><span class="sxs-lookup"><span data-stu-id="06493-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="06493-136">Para fazer isso, insira este código em seu retorno de chamada de enumeração do DirectInput:</span><span class="sxs-lookup"><span data-stu-id="06493-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

```cpp
#include <wbemidl.h>
#include <oleauto.h>

#ifndef SAFE_RELEASE
#define SAFE_RELEASE(p) { if (p) { (p)->Release(); (p) = nullptr; } }
#endif

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator = nullptr;
    IEnumWbemClassObject*   pEnumDevices = nullptr;
    IWbemClassObject*       pDevices[20] = {};
    IWbemServices*          pIWbemServices = nullptr;
    BSTR                    bstrNamespace = nullptr;
    BSTR                    bstrDeviceID = nullptr;
    BSTR                    bstrClassName = nullptr;
    bool                    bIsXinputDevice = false;
    
    // CoInit if needed
    HRESULT hr = CoInitialize(nullptr);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VARIANT var = {};
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance(__uuidof(WbemLocator),
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWbemLocator),
        (LPVOID*)&pIWbemLocator);
    if (FAILED(hr) || pIWbemLocator == nullptr)
        goto LCleanup;

    bstrNamespace = SysAllocString(L"\\\\.\\root\\cimv2");  if (bstrNamespace == nullptr) goto LCleanup;
    bstrClassName = SysAllocString(L"Win32_PNPEntity");     if (bstrClassName == nullptr) goto LCleanup;
    bstrDeviceID = SysAllocString(L"DeviceID");             if (bstrDeviceID == nullptr)  goto LCleanup;
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer(bstrNamespace, nullptr, nullptr, 0L,
        0L, nullptr, nullptr, &pIWbemServices);
    if (FAILED(hr) || pIWbemServices == nullptr)
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    hr = CoSetProxyBlanket(pIWbemServices,
        RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, nullptr,
        RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE,
        nullptr, EOAC_NONE);
    if ( FAILED(hr) )
        goto LCleanup;

    hr = pIWbemServices->CreateInstanceEnum(bstrClassName, 0, nullptr, &pEnumDevices);
    if (FAILED(hr) || pEnumDevices == nullptr)
        goto LCleanup;

    // Loop over all devices
    for (;;)
    {
        ULONG uReturned = 0;
        hr = pEnumDevices->Next(10000, _countof(pDevices), pDevices, &uReturned);
        if (FAILED(hr))
            goto LCleanup;
        if (uReturned == 0)
            break;

        for (size_t iDevice = 0; iDevice < uReturned; ++iDevice)
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get(bstrDeviceID, 0L, &var, nullptr, nullptr);
            if (SUCCEEDED(hr) && var.vt == VT_BSTR && var.bstrVal != nullptr)
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                // This information can not be found from DirectInput 
                if (wcsstr(var.bstrVal, L"IG_"))
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr(var.bstrVal, L"VID_");
                    if (strVid && swscanf_s(strVid, L"VID_%4X", &dwVid) != 1)
                        dwVid = 0;
                    WCHAR* strPid = wcsstr(var.bstrVal, L"PID_");
                    if (strPid && swscanf_s(strPid, L"PID_%4X", &dwPid) != 1)
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG(dwVid, dwPid);
                    if (dwVidPid == pGuidProductFromDirectInput->Data1)
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE(pDevices[iDevice]);
        }
    }

LCleanup:
    VariantClear(&var);
    
    if(bstrNamespace)
        SysFreeString(bstrNamespace);
    if(bstrDeviceID)
        SysFreeString(bstrDeviceID);
    if(bstrClassName)
        SysFreeString(bstrClassName);
        
    for (size_t iDevice = 0; iDevice < _countof(pDevices); ++iDevice)
        SAFE_RELEASE(pDevices[iDevice]);

    SAFE_RELEASE(pEnumDevices);
    SAFE_RELEASE(pIWbemLocator);
    SAFE_RELEASE(pIWbemServices);

    if(bCleanupCOM)
        CoUninitialize();

    return bIsXinputDevice;
}


//-----------------------------------------------------------------------------
// Name: EnumJoysticksCallback()
// Desc: Called once for each enumerated joystick. If we find one, create a
//       device interface on it so we can play with it.
//-----------------------------------------------------------------------------
BOOL CALLBACK EnumJoysticksCallback( const DIDEVICEINSTANCE* pdidInstance,
                                     VOID* pContext )
{
    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

> <span data-ttu-id="06493-137">Uma versão ligeiramente aprimorada desse código está no exemplo de [Joystick](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) do DirectInput herdado.</span><span class="sxs-lookup"><span data-stu-id="06493-137">A slightly improved version of this code is in the legacy DirectInput [Joystick](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06493-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06493-138">Related topics</span></span>

[<span data-ttu-id="06493-139">Introdução com XInput</span><span class="sxs-lookup"><span data-stu-id="06493-139">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="06493-140">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="06493-140">Programming Reference</span></span>](programming-reference.md)
