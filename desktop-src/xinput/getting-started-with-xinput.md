---
title: Introdução com XInput
description: XInput é uma API que permite que os aplicativos recebam entrada do controlador Xbox para Windows. Há suporte para efeitos de Rumble de controlador e entrada e saída de voz.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f590f54bbb2641881cf89cd6d31539d75665c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641189"
---
# <a name="getting-started-with-xinput"></a>Introdução com XInput

XInput é uma API que permite que os aplicativos recebam entrada do controlador Xbox para Windows. Há suporte para efeitos de Rumble de controlador e entrada e saída de voz.

Este tópico fornece uma breve visão geral dos recursos do XInput e como configurá-lo em um aplicativo. Ele inclui o seguinte:

-   [Introdução ao XInput](#introduction-to-xinput)
    -   [O controlador Xbox](#the-xbox-controller)
-   [Usando XInput](#using-xinput)
    -   [Vários controladores](#multiple-controllers)
    -   [Obtendo estado do controlador](#getting-controller-state)
    -   [Zona inoperante](#dead-zone)
    -   [Definindo efeitos de vibração](#setting-vibration-effects)
    -   [Obtendo identificadores de dispositivo de áudio](#getting-audio-device-identifiers)
    -   [Obtendo GUIDs DirectSound (somente SDK do DirectX herdado)](#getting-directsound-guids-legacy-directx-sdk-only)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction-to-xinput"></a>Introdução ao XInput

O console do Xbox usa um controlador de jogo que é compatível com o Windows. Os aplicativos podem usar a API XInput para se comunicar com esses controladores quando estiverem conectados a um computador Windows (até quatro controladores exclusivos podem ser conectados por vez).

Usando essa API, qualquer controlador Xbox conectado pode ser consultado em seu estado e os efeitos de vibração podem ser definidos. Os controladores que têm o headset anexado também podem ser consultados para dispositivos de entrada e saída de som que podem ser usados com o headset para processamento de voz.

### <a name="the-xbox-controller"></a>O controlador Xbox

O controlador Xbox tem dois pentes bidirecionais analógicos, cada um com um botão digital, dois gatilhos analógicos, um painel direcional digital com quatro direções e oito botões digitais. Os Estados de cada uma dessas entradas são retornados na estrutura [**do \_ gamepad do XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) quando a função [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) é chamada.

O controlador também tem dois motores de vibração para fornecer efeitos de feedback forçado ao usuário. As velocidades desses motores são especificadas na estrutura de [**\_ vibração XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que é passada para a função [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) para definir efeitos de vibração.

Opcionalmente, um headset pode ser conectado ao controlador. O headset tem um microfone para entrada de voz e um fone de ouvido para saída de som. Você pode chamar a função [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) ou [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) herdada para obter os identificadores de dispositivo que correspondem aos dispositivos para o microfone e o fone de ouvido. Você pode usar as [APIs de áudio principais](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) para receber entrada de voz e enviar saída de som.

## <a name="using-xinput"></a>Usando XInput

O uso de XInput é tão simples quanto chamar as funções XInput, conforme necessário. Usando as funções XInput, você pode recuperar o estado do controlador, obter as IDs de áudio do headset e definir os efeitos de Rumble do controlador.

### <a name="multiple-controllers"></a>Vários controladores

A API XInput dá suporte a até quatro controladores conectados a qualquer momento. Todas as funções XInput exigem um parâmetro *dwUserIndex* que é passado para identificar o controlador que está sendo definido ou consultado. Essa ID estará no intervalo de 0-3 e será definida automaticamente pelo XInput. O número corresponde à porta em que o controlador está conectado e não é modificável.

Cada controlador exibe qual ID está usando, iluminando um quadrante no "anel de luz" no centro do controlador. Um valor de *dwUserIndex* de 0 corresponde ao quadrante superior esquerdo; a numeração continua em volta do anel na ordem horária.

Os aplicativos devem dar suporte a vários controladores.

### <a name="getting-controller-state"></a>Obtendo estado do controlador

Durante toda a duração de um aplicativo, obter o estado de um controlador provavelmente será feito com mais frequência. Do quadro para o quadro em um aplicativo de jogo, o estado deve ser recuperado e as informações de jogos atualizadas para refletir as alterações do controlador.

Para recuperar o estado, use a função [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :

```cpp
DWORD dwResult;    
for (DWORD i=0; i< XUSER_MAX_COUNT; i++ )
{
    XINPUT_STATE state;
    ZeroMemory( &state, sizeof(XINPUT_STATE) );

    // Simply get the state of the controller from XInput.
    dwResult = XInputGetState( i, &state );

    if( dwResult == ERROR_SUCCESS )
    {
        // Controller is connected
    }
    else
    {
        // Controller is not connected
    }
}
```

Observe que o valor de retorno de [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) pode ser usado para determinar se o controlador está conectado. Os aplicativos devem definir uma estrutura para conter informações internas do controlador; essas informações devem ser comparadas com os resultados de **XInputGetState** para determinar quais alterações, como pressionamentos de botão ou deltas de controlador analógico, foram feitas nesse quadro. No exemplo acima, os *\_ controladores g* representam essa estrutura.

Depois que o estado for recuperado em uma estrutura de [**\_ estado XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , você poderá verificá-lo em busca de alterações e obter informações específicas sobre o estado do controlador.

O membro *dwPacketNumber* da estrutura [**de \_ estado XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) pode ser usado para verificar se o estado do controlador foi alterado desde a última chamada para [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate). Se *dwPacketNumber* não mudar entre duas chamadas sequenciais para **XInputGetState**, não haverá nenhuma alteração no estado. Se for diferente, o aplicativo deverá verificar o membro do *gamepad* da estrutura de **\_ estado XInput** para obter informações de estado mais detalhadas.

Por motivos de desempenho, não chame [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) para um slot de usuário ' empty ' em todos os quadros. É recomendável que o espaçamento das verificações de novos controladores em intervalos de alguns segundos.

### <a name="dead-zone"></a>Zona inoperante

Para que os usuários tenham uma experiência de jogo consistente, seu jogo deve implementar a zona inoperante corretamente. A zona inoperante são valores de "movimento" relatados pelo controlador mesmo quando os Thumbsticks analógicos são intocados e centralizados. Também há uma zona inoperante para os dois gatilhos analógicos.

> [!Note]  
> Os jogos que usam XInput que não filtram a zona inoperante terão um jogo ruim. Observe que alguns controladores são mais sensíveis do que outros, portanto, a zona inoperante pode variar de uma unidade para outra. É recomendável que você teste seus jogos com vários controladores do Xbox em sistemas diferentes.

Os aplicativos devem usar "zonas mortas" em entradas analógicas (gatilhos, pentes) para indicar quando um movimento foi feito suficientemente no pente ou gatilho para ser considerado válido.

Seu aplicativo deve verificar se há zonas mortas e responder appopriately, como neste exemplo:

```cpp
XINPUT_STATE state = g_Controllers[i].state;

float LX = state.Gamepad.sThumbLX;
float LY = state.Gamepad.sThumbLY;

//determine how far the controller is pushed
float magnitude = sqrt(LX*LX + LY*LY);

//determine the direction the controller is pushed
float normalizedLX = LX / magnitude;
float normalizedLY = LY / magnitude;

float normalizedMagnitude = 0;

//check if the controller is outside a circular dead zone
if (magnitude > INPUT_DEADZONE)
{
    //clip the magnitude at its expected maximum value
    if (magnitude > 32767) magnitude = 32767;

    //adjust magnitude relative to the end of the dead zone
    magnitude -= INPUT_DEADZONE;

    //optionally normalize the magnitude with respect to its expected range
    //giving a magnitude value of 0.0 to 1.0
    normalizedMagnitude = magnitude / (32767 - INPUT_DEADZONE);
}
else //if the controller is in the deadzone zero out the magnitude
{
    magnitude = 0.0;
    normalizedMagnitude = 0.0;
}

//repeat for right thumb stick
```

Este exemplo calcula o vetor de direção do controlador e o quanto ao longo do vetor o controlador foi enviado por push. Isso permite a imposição de um deadzone circular simplesmente verificando se a magnitude do controlador é maior que o valor de deadzone. Além disso, o código normaliza a magnitude do controlador, que pode então ser multiplicado por um fator específico do jogo para converter a posição do controlador em unidades relevantes para o jogo.

Observe que você pode definir suas próprias zonas mortas para os pentes e gatilhos (em qualquer lugar de 0-65534) ou pode usar o deadzones fornecido definido como XINPUT \_ gamepad \_ esquerdo \_ Thumb \_ DEADZONE, XInput \_ gamepad \_ Right \_ Thumb \_ DEADZONE e \_ o \_ \_ limite de gatilho de gamepad XInput em XInput. h:

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

Depois que o deadzone for imposto, você poderá achar útil dimensionar o intervalo resultante \[ 0,0.. 1.0 \] ponto flutuante (como no exemplo acima) e, opcionalmente, aplicar uma transformação não linear.

Por exemplo, com a condução de jogos, pode ser útil para o cubo o resultado fornecer uma melhor ideia para a condução de carros usando um gamepad, pois cubing o resultado lhe dá mais precisão nos intervalos inferiores, o que é desejável, pois os jogadores normalmente aplicam a força sutil para obter um movimento Suti ou aplicar força complexa em uma direção para obter a resposta da RD.

### <a name="setting-vibration-effects"></a>Definindo efeitos de vibração

Além de obter o estado do controlador, você também pode enviar dados de vibração para o controlador para alterar os comentários fornecidos ao usuário do controlador. O controlador contém dois motores de Rumble que podem ser controlados de forma independente passando valores para a função [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .

A velocidade de cada motor pode ser especificada usando um valor de palavra na estrutura de [**\_ vibração XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que é passada para a função [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) da seguinte maneira:

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

Observe que o motor certo é o motor de alta frequência, o motor esquerdo é o motor de baixa frequência. Eles nem sempre precisam ser definidos com o mesmo valor, pois fornecem efeitos diferentes.

### <a name="getting-audio-device-identifiers"></a>Obtendo identificadores de dispositivo de áudio

O headset de um controlador Xbox tem estas funções:

-   Gravar som usando um microfone
-   Reproduzir som usando um fone de ouvido

Use este código para obter os identificadores de dispositivo para o headset:

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

Depois de obter os identificadores de dispositivo, você pode criar as interfaces apropriadas. Por exemplo, se você usar o XAudio 2,8, use este código para criar uma voz de mestre para este dispositivo:

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

Para obter informações sobre como usar o identificador de dispositivo capturaid, consulte [capturando um fluxo](/windows/desktop/CoreAudio/capturing-a-stream).

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>Obtendo GUIDs DirectSound (somente SDK do DirectX herdado)

O headset que pode ser conectado a um controlador Xbox tem duas funções: ele pode gravar som usando um microfone e pode reproduzir som usando um fone de ouvido. Na API do XInput, essas funções são realizadas por meio do [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), usando as interfaces **IDirectSound8** e **IDirectSoundCapture8** .

Para associar o microfone do headset e o fone de ouvido às interfaces [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) apropriadas, você deve obter o DirectSoundGUIDs para os dispositivos de captura e renderização chamando [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).

> [!Note]  
> O uso do [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) herdado não é recomendado e não está disponível em aplicativos da Windows Store. As informações nesta seção se aplicam somente à versão SDK do DirectX do XInput (XInput 1,3). A versão do Windows 8 do XInput (XInput 1,4) usa exclusivamente os identificadores de dispositivo da API de sessão de áudio do Windows (WASAPI) que são obtidos por meio do [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

Depois de recuperar os GUIDs, você pode criar as interfaces apropriadas chamando DirectSoundCreate8 e DirectSoundCaptureCreate8 da seguinte maneira:

```cpp
// Create IDirectSound8 using the controller's render device
if( FAILED( hr = DirectSoundCreate8( &dsRenderGuid, &pDS, NULL ) ) )
   return hr;

// Set coop level to DSSCL_PRIORITY
if( FAILED( hr = pDS->SetCooperativeLevel( hWnd, DSSCL_NORMAL ) ) )
   return hr;

// Create IDirectSoundCapture using the controller's capture device
if( FAILED( hr = DirectSoundCaptureCreate8( &dsCaptureGuid, &pDSCapture, NULL ) ) )
   return hr;
```

## <a name="related-topics"></a>Tópicos relacionados

[Referência de programação](programming-reference.md)