---
title: XInput e DirectInput
description: XInput é uma API que permite que os aplicativos recebam entrada do controlador Xbox para Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcdbc31a66d4928b52ae5d097cab0e877f6f078
ms.sourcegitcommit: 48d4947b16f1ed1eaf6fae2b75954b736dd25450
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/29/2020
ms.locfileid: "103641950"
---
# <a name="xinput-and-directinput"></a><span data-ttu-id="ee97f-103">XInput e DirectInput</span><span class="sxs-lookup"><span data-stu-id="ee97f-103">XInput and DirectInput</span></span>

<span data-ttu-id="ee97f-104">XInput é uma API que permite que os aplicativos recebam entrada do controlador Xbox para Windows.</span><span class="sxs-lookup"><span data-stu-id="ee97f-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="ee97f-105">Este documento descreve as diferenças entre as implementações XInput e [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) do controlador Xbox e como você pode dar suporte a dispositivos XInput e dispositivos DirectInput herdados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="ee97f-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="ee97f-106">O uso de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdado não é recomendado e o DirectInput não está disponível para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="ee97f-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="ee97f-107">O novo padrão: XInput</span><span class="sxs-lookup"><span data-stu-id="ee97f-107">The New Standard: XInput</span></span>

<span data-ttu-id="ee97f-108">O XInput agora está disponível para desenvolvimento de jogos.</span><span class="sxs-lookup"><span data-stu-id="ee97f-108">XInput is now available for game development.</span></span> <span data-ttu-id="ee97f-109">Esse é o novo padrão de entrada para o Xbox e o Windows.</span><span class="sxs-lookup"><span data-stu-id="ee97f-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="ee97f-110">As APIs estão disponíveis por meio do SDK do DirectX e o driver está disponível por meio de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="ee97f-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="ee97f-111">Há várias vantagens em usar o XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="ee97f-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="ee97f-112">O XInput é mais fácil de usar e requer menos configuração do que o [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee97f-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="ee97f-113">A programação do Xbox e do Windows usará os mesmos conjuntos de APIs principais, permitindo que a programação converta várias plataformas de forma muito mais fácil</span><span class="sxs-lookup"><span data-stu-id="ee97f-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="ee97f-114">Haverá uma grande base instalada de controladores do Xbox</span><span class="sxs-lookup"><span data-stu-id="ee97f-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="ee97f-115">Dispositivos XInput (ou seja, os controladores Xbox) terão a funcionalidade de vibração somente ao usar APIs XInput</span><span class="sxs-lookup"><span data-stu-id="ee97f-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="ee97f-116">Controladores futuros lançados para o console do Xbox (ou seja, rodas do direcionamento) também funcionarão no Windows</span><span class="sxs-lookup"><span data-stu-id="ee97f-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="ee97f-117">Usando o controlador Xbox com o DirectInput</span><span class="sxs-lookup"><span data-stu-id="ee97f-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="ee97f-118">O controlador Xbox é enumerado corretamente no [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))e pode ser usado com o DirectInputAPIs.</span><span class="sxs-lookup"><span data-stu-id="ee97f-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="ee97f-119">No entanto, algumas funcionalidades fornecidas pelo XInput estarão faltando na implementação do DirectInput:</span><span class="sxs-lookup"><span data-stu-id="ee97f-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="ee97f-120">Os botões de gatilho à esquerda e à direita funcionarão como um único botão, não de forma independente</span><span class="sxs-lookup"><span data-stu-id="ee97f-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="ee97f-121">Os efeitos de vibração não estarão disponíveis</span><span class="sxs-lookup"><span data-stu-id="ee97f-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="ee97f-122">A consulta de dispositivos Headset não estará disponível</span><span class="sxs-lookup"><span data-stu-id="ee97f-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="ee97f-123">A combinação dos gatilhos esquerdo e direito no [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) é por design.</span><span class="sxs-lookup"><span data-stu-id="ee97f-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="ee97f-124">Os jogos sempre assumiram que os eixos do dispositivo DirectInput estão centralizados quando não há interação do usuário com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee97f-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="ee97f-125">No entanto, o controlador Xbox foi projetado para registrar o valor mínimo, e não o centro, quando os gatilhos não estão sendo mantidos.</span><span class="sxs-lookup"><span data-stu-id="ee97f-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="ee97f-126">Os jogos mais antigos, portanto, assumem a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ee97f-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="ee97f-127">A solução foi combinar os gatilhos, definir um gatilho para uma direção positiva e o outro para uma direção negativa, portanto, nenhuma interação do usuário é indicar ao [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) do "controle" estar no centro.</span><span class="sxs-lookup"><span data-stu-id="ee97f-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="ee97f-128">Para testar os valores do gatilho separadamente, você deve usar XInput.</span><span class="sxs-lookup"><span data-stu-id="ee97f-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="ee97f-129">XInput e DirectInput lado a lado</span><span class="sxs-lookup"><span data-stu-id="ee97f-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="ee97f-130">Ao dar suporte apenas a XInput, seu jogo não funcionará com dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdados.</span><span class="sxs-lookup"><span data-stu-id="ee97f-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="ee97f-131">O XInput não reconhecerá esses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ee97f-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="ee97f-132">Se você quiser que seu jogo dê suporte a dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdados, você poderá usar o DirectInput e o XInput lado a lado.</span><span class="sxs-lookup"><span data-stu-id="ee97f-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="ee97f-133">Ao enumerar seus dispositivos do DirectInput, todos os dispositivos do DirectInput serão enumerados corretamente.</span><span class="sxs-lookup"><span data-stu-id="ee97f-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="ee97f-134">Todos os dispositivos XInput aparecerão como dispositivos XInput e DirectInput, mas eles não devem ser manipulados por meio do DirectInput.</span><span class="sxs-lookup"><span data-stu-id="ee97f-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="ee97f-135">Você precisará determinar quais dos seus dispositivos DirectInput são dispositivos herdados e quais são dispositivos XInput e removê-los da enumeração de dispositivos do DirectInput.</span><span class="sxs-lookup"><span data-stu-id="ee97f-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="ee97f-136">Para fazer isso, insira este código em seu retorno de chamada de enumeração do DirectInput:</span><span class="sxs-lookup"><span data-stu-id="ee97f-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

```cpp
#include <wbemidl.h>
#include <oleauto.h>
#include <wmsstd.h>

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator  = NULL;
    IEnumWbemClassObject*   pEnumDevices   = NULL;
    IWbemClassObject*       pDevices[20]   = {0};
    IWbemServices*          pIWbemServices = NULL;
    BSTR                    bstrNamespace  = NULL;
    BSTR                    bstrDeviceID   = NULL;
    BSTR                    bstrClassName  = NULL;
    DWORD                   uReturned      = 0;
    bool                    bIsXinputDevice= false;
    UINT                    iDevice        = 0;
    VARIANT                 var;
    HRESULT                 hr;

    // CoInit if needed
    hr = CoInitialize(NULL);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance( __uuidof(WbemLocator),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(IWbemLocator),
                           (LPVOID*) &pIWbemLocator);
    if( FAILED(hr) || pIWbemLocator == NULL )
        goto LCleanup;

    bstrNamespace = SysAllocString( L"\\\\.\\root\\cimv2" );if( bstrNamespace == NULL ) goto LCleanup;        
    bstrClassName = SysAllocString( L"Win32_PNPEntity" );   if( bstrClassName == NULL ) goto LCleanup;        
    bstrDeviceID  = SysAllocString( L"DeviceID" );          if( bstrDeviceID == NULL )  goto LCleanup;        
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer( bstrNamespace, NULL, NULL, 0L, 
                                       0L, NULL, NULL, &pIWbemServices );
    if( FAILED(hr) || pIWbemServices == NULL )
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    CoSetProxyBlanket( pIWbemServices, RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, NULL, 
                       RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE );                    

    hr = pIWbemServices->CreateInstanceEnum( bstrClassName, 0, NULL, &pEnumDevices ); 
    if( FAILED(hr) || pEnumDevices == NULL )
        goto LCleanup;

    // Loop over all devices
    for( ;; )
    {
        // Get 20 at a time
        hr = pEnumDevices->Next( 10000, 20, pDevices, &uReturned );
        if( FAILED(hr) )
            goto LCleanup;
        if( uReturned == 0 )
            break;

        for( iDevice=0; iDevice<uReturned; iDevice++ )
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get( bstrDeviceID, 0L, &var, NULL, NULL );
            if( SUCCEEDED( hr ) && var.vt == VT_BSTR && var.bstrVal != NULL )
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                    // This information can not be found from DirectInput 
                if( wcsstr( var.bstrVal, L"IG_" ) )
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr( var.bstrVal, L"VID_" );
                    if( strVid && swscanf( strVid, L"VID_%4X", &dwVid ) != 1 )
                        dwVid = 0;
                    WCHAR* strPid = wcsstr( var.bstrVal, L"PID_" );
                    if( strPid && swscanf( strPid, L"PID_%4X", &dwPid ) != 1 )
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG( dwVid, dwPid );
                    if( dwVidPid == pGuidProductFromDirectInput->Data1 )
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE( pDevices[iDevice] );
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
    for( iDevice=0; iDevice<20; iDevice++ )
        SAFE_RELEASE( pDevices[iDevice] );
    SAFE_RELEASE( pEnumDevices );
    SAFE_RELEASE( pIWbemLocator );
    SAFE_RELEASE( pIWbemServices );

    if( bCleanupCOM )
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
    HRESULT hr;

    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

## <a name="related-topics"></a><span data-ttu-id="ee97f-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee97f-137">Related topics</span></span>

[<span data-ttu-id="ee97f-138">Introdução com XInput</span><span class="sxs-lookup"><span data-stu-id="ee97f-138">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="ee97f-139">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="ee97f-139">Programming Reference</span></span>](programming-reference.md)
