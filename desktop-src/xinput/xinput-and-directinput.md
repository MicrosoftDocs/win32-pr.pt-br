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
# <a name="xinput-and-directinput"></a>XInput e DirectInput

XInput é uma API que permite que os aplicativos recebam entrada do controlador Xbox para Windows. Este documento descreve as diferenças entre as implementações XInput e [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) do controlador Xbox e como você pode dar suporte a dispositivos XInput e dispositivos DirectInput herdados ao mesmo tempo.

> [!Note]  
> O uso de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdado não é recomendado e o DirectInput não está disponível para aplicativos da Windows Store.

## <a name="the-new-standard-xinput"></a>O novo padrão: XInput

O XInput agora está disponível para desenvolvimento de jogos. Esse é o novo padrão de entrada para o Xbox e o Windows. As APIs estão disponíveis por meio do SDK do DirectX e o driver está disponível por meio de Windows Update.

Há várias vantagens em usar o XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):

-   O XInput é mais fácil de usar e requer menos configuração do que o [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   A programação do Xbox e do Windows usará os mesmos conjuntos de APIs principais, permitindo que a programação converta várias plataformas de forma muito mais fácil
-   Haverá uma grande base instalada de controladores do Xbox
-   Dispositivos XInput (ou seja, os controladores Xbox) terão a funcionalidade de vibração somente ao usar APIs XInput
-   Controladores futuros lançados para o console do Xbox (ou seja, rodas do direcionamento) também funcionarão no Windows

### <a name="using-the-xbox-controller-with-directinput"></a>Usando o controlador Xbox com o DirectInput

O controlador Xbox é enumerado corretamente no [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))e pode ser usado com o DirectInputAPIs. No entanto, algumas funcionalidades fornecidas pelo XInput estarão faltando na implementação do DirectInput:

-   Os botões de gatilho à esquerda e à direita funcionarão como um único botão, não de forma independente
-   Os efeitos de vibração não estarão disponíveis
-   A consulta de dispositivos Headset não estará disponível

A combinação dos gatilhos esquerdo e direito no [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) é por design. Os jogos sempre assumiram que os eixos do dispositivo DirectInput estão centralizados quando não há interação do usuário com o dispositivo. No entanto, o controlador Xbox foi projetado para registrar o valor mínimo, e não o centro, quando os gatilhos não estão sendo mantidos. Os jogos mais antigos, portanto, assumem a interação do usuário.

A solução foi combinar os gatilhos, definir um gatilho para uma direção positiva e o outro para uma direção negativa, portanto, nenhuma interação do usuário é indicar ao [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) do "controle" estar no centro.

Para testar os valores do gatilho separadamente, você deve usar XInput.

## <a name="xinput-and-directinput-side-by-side"></a>XInput e DirectInput lado a lado

Ao dar suporte apenas a XInput, seu jogo não funcionará com dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdados. O XInput não reconhecerá esses dispositivos.

Se você quiser que seu jogo dê suporte a dispositivos [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) herdados, você poderá usar o DirectInput e o XInput lado a lado. Ao enumerar seus dispositivos do DirectInput, todos os dispositivos do DirectInput serão enumerados corretamente. Todos os dispositivos XInput aparecerão como dispositivos XInput e DirectInput, mas eles não devem ser manipulados por meio do DirectInput. Você precisará determinar quais dos seus dispositivos DirectInput são dispositivos herdados e quais são dispositivos XInput e removê-los da enumeração de dispositivos do DirectInput.

Para fazer isso, insira este código em seu retorno de chamada de enumeração do DirectInput:

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

## <a name="related-topics"></a>Tópicos relacionados

[Introdução com XInput](getting-started-with-xinput.md)

[Referência de programação](programming-reference.md)
