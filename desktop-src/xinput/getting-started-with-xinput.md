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
# <a name="getting-started-with-xinput"></a><span data-ttu-id="077d6-104">Introdução com XInput</span><span class="sxs-lookup"><span data-stu-id="077d6-104">Getting Started With XInput</span></span>

<span data-ttu-id="077d6-105">XInput é uma API que permite que os aplicativos recebam entrada do controlador Xbox para Windows.</span><span class="sxs-lookup"><span data-stu-id="077d6-105">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="077d6-106">Há suporte para efeitos de Rumble de controlador e entrada e saída de voz.</span><span class="sxs-lookup"><span data-stu-id="077d6-106">Controller rumble effects and voice input and output are supported.</span></span>

<span data-ttu-id="077d6-107">Este tópico fornece uma breve visão geral dos recursos do XInput e como configurá-lo em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="077d6-107">This topic provides a brief overview of the capabilities of XInput and how to set it up in an application.</span></span> <span data-ttu-id="077d6-108">Ele inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="077d6-108">It includes the following:</span></span>

-   [<span data-ttu-id="077d6-109">Introdução ao XInput</span><span class="sxs-lookup"><span data-stu-id="077d6-109">Introduction to XInput</span></span>](#introduction-to-xinput)
    -   [<span data-ttu-id="077d6-110">O controlador Xbox</span><span class="sxs-lookup"><span data-stu-id="077d6-110">The Xbox Controller</span></span>](#the-xbox-controller)
-   [<span data-ttu-id="077d6-111">Usando XInput</span><span class="sxs-lookup"><span data-stu-id="077d6-111">Using XInput</span></span>](#using-xinput)
    -   [<span data-ttu-id="077d6-112">Vários controladores</span><span class="sxs-lookup"><span data-stu-id="077d6-112">Multiple Controllers</span></span>](#multiple-controllers)
    -   [<span data-ttu-id="077d6-113">Obtendo estado do controlador</span><span class="sxs-lookup"><span data-stu-id="077d6-113">Getting Controller State</span></span>](#getting-controller-state)
    -   [<span data-ttu-id="077d6-114">Zona inoperante</span><span class="sxs-lookup"><span data-stu-id="077d6-114">Dead Zone</span></span>](#dead-zone)
    -   [<span data-ttu-id="077d6-115">Definindo efeitos de vibração</span><span class="sxs-lookup"><span data-stu-id="077d6-115">Setting Vibration Effects</span></span>](#setting-vibration-effects)
    -   [<span data-ttu-id="077d6-116">Obtendo identificadores de dispositivo de áudio</span><span class="sxs-lookup"><span data-stu-id="077d6-116">Getting Audio Device Identifiers</span></span>](#getting-audio-device-identifiers)
    -   [<span data-ttu-id="077d6-117">Obtendo GUIDs DirectSound (somente SDK do DirectX herdado)</span><span class="sxs-lookup"><span data-stu-id="077d6-117">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>](#getting-directsound-guids-legacy-directx-sdk-only)
-   [<span data-ttu-id="077d6-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="077d6-118">Related topics</span></span>](#related-topics)

## <a name="introduction-to-xinput"></a><span data-ttu-id="077d6-119">Introdução ao XInput</span><span class="sxs-lookup"><span data-stu-id="077d6-119">Introduction to XInput</span></span>

<span data-ttu-id="077d6-120">O console do Xbox usa um controlador de jogo que é compatível com o Windows.</span><span class="sxs-lookup"><span data-stu-id="077d6-120">The Xbox console uses a gaming controller that is compatible with Windows.</span></span> <span data-ttu-id="077d6-121">Os aplicativos podem usar a API XInput para se comunicar com esses controladores quando estiverem conectados a um computador Windows (até quatro controladores exclusivos podem ser conectados por vez).</span><span class="sxs-lookup"><span data-stu-id="077d6-121">Applications can use the XInput API to communicate with these controllers when they are plugged into a Windows PC (up to four unique controllers can be plugged in at a time).</span></span>

<span data-ttu-id="077d6-122">Usando essa API, qualquer controlador Xbox conectado pode ser consultado em seu estado e os efeitos de vibração podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="077d6-122">Using this API, any connected Xbox Controller can be queried for its state, and vibration effects can be set.</span></span> <span data-ttu-id="077d6-123">Os controladores que têm o headset anexado também podem ser consultados para dispositivos de entrada e saída de som que podem ser usados com o headset para processamento de voz.</span><span class="sxs-lookup"><span data-stu-id="077d6-123">Controllers that have the headset attached can also be queried for sound input and output devices that can be used with the headset for voice processing.</span></span>

### <a name="the-xbox-controller"></a><span data-ttu-id="077d6-124">O controlador Xbox</span><span class="sxs-lookup"><span data-stu-id="077d6-124">The Xbox Controller</span></span>

<span data-ttu-id="077d6-125">O controlador Xbox tem dois pentes bidirecionais analógicos, cada um com um botão digital, dois gatilhos analógicos, um painel direcional digital com quatro direções e oito botões digitais.</span><span class="sxs-lookup"><span data-stu-id="077d6-125">The Xbox Controller has two analog directional sticks, each with a digital button, two analog triggers, a digital directional pad with four directions, and eight digital buttons.</span></span> <span data-ttu-id="077d6-126">Os Estados de cada uma dessas entradas são retornados na estrutura [**do \_ gamepad do XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) quando a função [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) é chamada.</span><span class="sxs-lookup"><span data-stu-id="077d6-126">The states of each of these inputs are returned in the [**XINPUT\_GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) structure when the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function is called.</span></span>

<span data-ttu-id="077d6-127">O controlador também tem dois motores de vibração para fornecer efeitos de feedback forçado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="077d6-127">The controller also has two vibration motors to supply force feedback effects to the user.</span></span> <span data-ttu-id="077d6-128">As velocidades desses motores são especificadas na estrutura de [**\_ vibração XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que é passada para a função [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) para definir efeitos de vibração.</span><span class="sxs-lookup"><span data-stu-id="077d6-128">The speeds of these motors are specified in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function to set vibration effects.</span></span>

<span data-ttu-id="077d6-129">Opcionalmente, um headset pode ser conectado ao controlador.</span><span class="sxs-lookup"><span data-stu-id="077d6-129">Optionally, a headset can be connected to the controller.</span></span> <span data-ttu-id="077d6-130">O headset tem um microfone para entrada de voz e um fone de ouvido para saída de som.</span><span class="sxs-lookup"><span data-stu-id="077d6-130">The headset has a microphone for voice input, and a headphone for sound output.</span></span> <span data-ttu-id="077d6-131">Você pode chamar a função [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) ou [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) herdada para obter os identificadores de dispositivo que correspondem aos dispositivos para o microfone e o fone de ouvido.</span><span class="sxs-lookup"><span data-stu-id="077d6-131">You can call the [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) or legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) function to obtain the device identifiers that correspond to the devices for the microphone and headphone.</span></span> <span data-ttu-id="077d6-132">Você pode usar as [APIs de áudio principais](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) para receber entrada de voz e enviar saída de som.</span><span class="sxs-lookup"><span data-stu-id="077d6-132">You can then use the [Core Audio APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) to receive voice input and send sound output.</span></span>

## <a name="using-xinput"></a><span data-ttu-id="077d6-133">Usando XInput</span><span class="sxs-lookup"><span data-stu-id="077d6-133">Using XInput</span></span>

<span data-ttu-id="077d6-134">O uso de XInput é tão simples quanto chamar as funções XInput, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="077d6-134">Using XInput is as simple as calling the XInput functions as required.</span></span> <span data-ttu-id="077d6-135">Usando as funções XInput, você pode recuperar o estado do controlador, obter as IDs de áudio do headset e definir os efeitos de Rumble do controlador.</span><span class="sxs-lookup"><span data-stu-id="077d6-135">Using the XInput functions, you can retrieve controller state, get headset audio IDs, and set controller rumble effects.</span></span>

### <a name="multiple-controllers"></a><span data-ttu-id="077d6-136">Vários controladores</span><span class="sxs-lookup"><span data-stu-id="077d6-136">Multiple Controllers</span></span>

<span data-ttu-id="077d6-137">A API XInput dá suporte a até quatro controladores conectados a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="077d6-137">The XInput API supports up to four controllers connected at any time.</span></span> <span data-ttu-id="077d6-138">Todas as funções XInput exigem um parâmetro *dwUserIndex* que é passado para identificar o controlador que está sendo definido ou consultado.</span><span class="sxs-lookup"><span data-stu-id="077d6-138">The XInput functions all require a *dwUserIndex* parameter that is passed in to identify the controller being set or queried.</span></span> <span data-ttu-id="077d6-139">Essa ID estará no intervalo de 0-3 e será definida automaticamente pelo XInput.</span><span class="sxs-lookup"><span data-stu-id="077d6-139">This ID will be in the range of 0-3 and is set automatically by XInput.</span></span> <span data-ttu-id="077d6-140">O número corresponde à porta em que o controlador está conectado e não é modificável.</span><span class="sxs-lookup"><span data-stu-id="077d6-140">The number corresponds to the port that the controller is plugged into, and is not modifiable.</span></span>

<span data-ttu-id="077d6-141">Cada controlador exibe qual ID está usando, iluminando um quadrante no "anel de luz" no centro do controlador.</span><span class="sxs-lookup"><span data-stu-id="077d6-141">Each controller displays which ID it is using by lighting up a quadrant on the "ring of light" in the center of the controller.</span></span> <span data-ttu-id="077d6-142">Um valor de *dwUserIndex* de 0 corresponde ao quadrante superior esquerdo; a numeração continua em volta do anel na ordem horária.</span><span class="sxs-lookup"><span data-stu-id="077d6-142">A *dwUserIndex* value of 0 corresponds to the top-left quadrant; the numbering proceeds around the ring in clockwise order.</span></span>

<span data-ttu-id="077d6-143">Os aplicativos devem dar suporte a vários controladores.</span><span class="sxs-lookup"><span data-stu-id="077d6-143">Applications should support multiple controllers.</span></span>

### <a name="getting-controller-state"></a><span data-ttu-id="077d6-144">Obtendo estado do controlador</span><span class="sxs-lookup"><span data-stu-id="077d6-144">Getting Controller State</span></span>

<span data-ttu-id="077d6-145">Durante toda a duração de um aplicativo, obter o estado de um controlador provavelmente será feito com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="077d6-145">Throughout the duration of an application, getting state from a controller will probably be done most often.</span></span> <span data-ttu-id="077d6-146">Do quadro para o quadro em um aplicativo de jogo, o estado deve ser recuperado e as informações de jogos atualizadas para refletir as alterações do controlador.</span><span class="sxs-lookup"><span data-stu-id="077d6-146">From frame to frame in a game application, state should be retrieved and game information updated to reflect the controller changes.</span></span>

<span data-ttu-id="077d6-147">Para recuperar o estado, use a função [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :</span><span class="sxs-lookup"><span data-stu-id="077d6-147">To retrieve state, use the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function:</span></span>

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

<span data-ttu-id="077d6-148">Observe que o valor de retorno de [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) pode ser usado para determinar se o controlador está conectado.</span><span class="sxs-lookup"><span data-stu-id="077d6-148">Note that the return value of [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) can be used to determine if the controller is connected.</span></span> <span data-ttu-id="077d6-149">Os aplicativos devem definir uma estrutura para conter informações internas do controlador; essas informações devem ser comparadas com os resultados de **XInputGetState** para determinar quais alterações, como pressionamentos de botão ou deltas de controlador analógico, foram feitas nesse quadro.</span><span class="sxs-lookup"><span data-stu-id="077d6-149">Applications should define a structure to hold internal controller information; this information should be compared against the results of **XInputGetState** to determine what changes, such as button presses or analog controller deltas, were made that frame.</span></span> <span data-ttu-id="077d6-150">No exemplo acima, os *\_ controladores g* representam essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="077d6-150">In the above example, *g\_Controllers* represents such a structure.</span></span>

<span data-ttu-id="077d6-151">Depois que o estado for recuperado em uma estrutura de [**\_ estado XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , você poderá verificá-lo em busca de alterações e obter informações específicas sobre o estado do controlador.</span><span class="sxs-lookup"><span data-stu-id="077d6-151">Once the state has been retrieved in a [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure, you can check it for changes and get specific information about controller state.</span></span>

<span data-ttu-id="077d6-152">O membro *dwPacketNumber* da estrutura [**de \_ estado XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) pode ser usado para verificar se o estado do controlador foi alterado desde a última chamada para [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span><span class="sxs-lookup"><span data-stu-id="077d6-152">The *dwPacketNumber* member of the [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure can be used to check if the state of the controller has changed since the last call to [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span></span> <span data-ttu-id="077d6-153">Se *dwPacketNumber* não mudar entre duas chamadas sequenciais para **XInputGetState**, não haverá nenhuma alteração no estado.</span><span class="sxs-lookup"><span data-stu-id="077d6-153">If *dwPacketNumber* does not change between two sequential calls to **XInputGetState**, then there has been no change in state.</span></span> <span data-ttu-id="077d6-154">Se for diferente, o aplicativo deverá verificar o membro do *gamepad* da estrutura de **\_ estado XInput** para obter informações de estado mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="077d6-154">If it differs, then the application should check the *Gamepad* member of the **XINPUT\_STATE** structure to get more detailed state information.</span></span>

<span data-ttu-id="077d6-155">Por motivos de desempenho, não chame [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) para um slot de usuário ' empty ' em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="077d6-155">For performance reasons, don't call [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) for an 'empty' user slot every frame.</span></span> <span data-ttu-id="077d6-156">É recomendável que o espaçamento das verificações de novos controladores em intervalos de alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="077d6-156">We recommend that you space out checks for new controllers every few seconds instead.</span></span>

### <a name="dead-zone"></a><span data-ttu-id="077d6-157">Zona inoperante</span><span class="sxs-lookup"><span data-stu-id="077d6-157">Dead Zone</span></span>

<span data-ttu-id="077d6-158">Para que os usuários tenham uma experiência de jogo consistente, seu jogo deve implementar a zona inoperante corretamente.</span><span class="sxs-lookup"><span data-stu-id="077d6-158">In order for users to have a consistent gameplay experience, your game must implement dead zone correctly.</span></span> <span data-ttu-id="077d6-159">A zona inoperante são valores de "movimento" relatados pelo controlador mesmo quando os Thumbsticks analógicos são intocados e centralizados.</span><span class="sxs-lookup"><span data-stu-id="077d6-159">The dead zone is "movement" values reported by the controller even when the analog thumbsticks are untouched and centered.</span></span> <span data-ttu-id="077d6-160">Também há uma zona inoperante para os dois gatilhos analógicos.</span><span class="sxs-lookup"><span data-stu-id="077d6-160">There is also a dead zone for the 2 analog triggers.</span></span>

> [!Note]  
> <span data-ttu-id="077d6-161">Os jogos que usam XInput que não filtram a zona inoperante terão um jogo ruim.</span><span class="sxs-lookup"><span data-stu-id="077d6-161">Games that use XInput that do not filter dead zone at all will experience poor gameplay.</span></span> <span data-ttu-id="077d6-162">Observe que alguns controladores são mais sensíveis do que outros, portanto, a zona inoperante pode variar de uma unidade para outra.</span><span class="sxs-lookup"><span data-stu-id="077d6-162">Please note that some controllers are more sensitive than others, thus the dead zone may vary from unit to unit.</span></span> <span data-ttu-id="077d6-163">É recomendável que você teste seus jogos com vários controladores do Xbox em sistemas diferentes.</span><span class="sxs-lookup"><span data-stu-id="077d6-163">It is recommended that you test your games with several Xbox controllers on different systems.</span></span>

<span data-ttu-id="077d6-164">Os aplicativos devem usar "zonas mortas" em entradas analógicas (gatilhos, pentes) para indicar quando um movimento foi feito suficientemente no pente ou gatilho para ser considerado válido.</span><span class="sxs-lookup"><span data-stu-id="077d6-164">Applications should use "dead zones" on analog inputs (triggers, sticks) to indicate when a movement has been made sufficiently on the stick or trigger to be considered valid.</span></span>

<span data-ttu-id="077d6-165">Seu aplicativo deve verificar se há zonas mortas e responder appopriately, como neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="077d6-165">Your application should check for dead zones and respond appopriately, as in this example:</span></span>

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

<span data-ttu-id="077d6-166">Este exemplo calcula o vetor de direção do controlador e o quanto ao longo do vetor o controlador foi enviado por push.</span><span class="sxs-lookup"><span data-stu-id="077d6-166">This example calculates the controller's direction vector and how far along the vector the controller has been pushed.</span></span> <span data-ttu-id="077d6-167">Isso permite a imposição de um deadzone circular simplesmente verificando se a magnitude do controlador é maior que o valor de deadzone.</span><span class="sxs-lookup"><span data-stu-id="077d6-167">This allows enforcement of a circular deadzone by simply checking whether the controller's magnitude is greater than the deadzone value.</span></span> <span data-ttu-id="077d6-168">Além disso, o código normaliza a magnitude do controlador, que pode então ser multiplicado por um fator específico do jogo para converter a posição do controlador em unidades relevantes para o jogo.</span><span class="sxs-lookup"><span data-stu-id="077d6-168">In addition the code normalizes the controller's magnitude which can then be multiplied by a game specific factor to convert the controller's position to units relevant to the game.</span></span>

<span data-ttu-id="077d6-169">Observe que você pode definir suas próprias zonas mortas para os pentes e gatilhos (em qualquer lugar de 0-65534) ou pode usar o deadzones fornecido definido como XINPUT \_ gamepad \_ esquerdo \_ Thumb \_ DEADZONE, XInput \_ gamepad \_ Right \_ Thumb \_ DEADZONE e \_ o \_ \_ limite de gatilho de gamepad XInput em XInput. h:</span><span class="sxs-lookup"><span data-stu-id="077d6-169">Note that you may define your own dead zones for the sticks and triggers (anywhere from 0-65534), or you may use the provided deadzones defined as XINPUT\_GAMEPAD\_LEFT\_THUMB\_DEADZONE, XINPUT\_GAMEPAD\_RIGHT\_THUMB\_DEADZONE, and XINPUT\_GAMEPAD\_TRIGGER\_THRESHOLD in XInput.h:</span></span>

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

<span data-ttu-id="077d6-170">Depois que o deadzone for imposto, você poderá achar útil dimensionar o intervalo resultante \[ 0,0.. 1.0 \] ponto flutuante (como no exemplo acima) e, opcionalmente, aplicar uma transformação não linear.</span><span class="sxs-lookup"><span data-stu-id="077d6-170">Once the deadzone is enforced, you may find it useful to scale the resulting range \[0.0..1.0\] floating point (as in the example above), and optionally apply a non-linear transform.</span></span>

<span data-ttu-id="077d6-171">Por exemplo, com a condução de jogos, pode ser útil para o cubo o resultado fornecer uma melhor ideia para a condução de carros usando um gamepad, pois cubing o resultado lhe dá mais precisão nos intervalos inferiores, o que é desejável, pois os jogadores normalmente aplicam a força sutil para obter um movimento Suti ou aplicar força complexa em uma direção para obter a resposta da RD.</span><span class="sxs-lookup"><span data-stu-id="077d6-171">For example, with driving games, it may be helpful to cube the result to provide a better feel to driving the cars using a gamepad, as cubing the result gives you more precision in the lower ranges, which is desirable, since gamers typically either apply soft force to get subtle movement or apply hard force all the way in one direction to get rd response.</span></span>

### <a name="setting-vibration-effects"></a><span data-ttu-id="077d6-172">Definindo efeitos de vibração</span><span class="sxs-lookup"><span data-stu-id="077d6-172">Setting Vibration Effects</span></span>

<span data-ttu-id="077d6-173">Além de obter o estado do controlador, você também pode enviar dados de vibração para o controlador para alterar os comentários fornecidos ao usuário do controlador.</span><span class="sxs-lookup"><span data-stu-id="077d6-173">In addition to getting the state of the controller, you may also send vibration data to the controller to alter the feedback provided to the user of the controller.</span></span> <span data-ttu-id="077d6-174">O controlador contém dois motores de Rumble que podem ser controlados de forma independente passando valores para a função [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .</span><span class="sxs-lookup"><span data-stu-id="077d6-174">The controller contains two rumble motors that can be independently controlled by passing values to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function.</span></span>

<span data-ttu-id="077d6-175">A velocidade de cada motor pode ser especificada usando um valor de palavra na estrutura de [**\_ vibração XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que é passada para a função [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="077d6-175">The speed of each motor can be specified using a WORD value in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function as follows:</span></span>

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

<span data-ttu-id="077d6-176">Observe que o motor certo é o motor de alta frequência, o motor esquerdo é o motor de baixa frequência.</span><span class="sxs-lookup"><span data-stu-id="077d6-176">Note that the right motor is the high-frequency motor, the left motor is the low-frequency motor.</span></span> <span data-ttu-id="077d6-177">Eles nem sempre precisam ser definidos com o mesmo valor, pois fornecem efeitos diferentes.</span><span class="sxs-lookup"><span data-stu-id="077d6-177">They do not always need to be set to the same amount, as they provide different effects.</span></span>

### <a name="getting-audio-device-identifiers"></a><span data-ttu-id="077d6-178">Obtendo identificadores de dispositivo de áudio</span><span class="sxs-lookup"><span data-stu-id="077d6-178">Getting Audio Device Identifiers</span></span>

<span data-ttu-id="077d6-179">O headset de um controlador Xbox tem estas funções:</span><span class="sxs-lookup"><span data-stu-id="077d6-179">The headset for an Xbox Controller has these functions:</span></span>

-   <span data-ttu-id="077d6-180">Gravar som usando um microfone</span><span class="sxs-lookup"><span data-stu-id="077d6-180">Record sound using a microphone</span></span>
-   <span data-ttu-id="077d6-181">Reproduzir som usando um fone de ouvido</span><span class="sxs-lookup"><span data-stu-id="077d6-181">Play back sound using a headphone</span></span>

<span data-ttu-id="077d6-182">Use este código para obter os identificadores de dispositivo para o headset:</span><span class="sxs-lookup"><span data-stu-id="077d6-182">Use this code to obtain the device identifiers for the headset:</span></span>

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

<span data-ttu-id="077d6-183">Depois de obter os identificadores de dispositivo, você pode criar as interfaces apropriadas.</span><span class="sxs-lookup"><span data-stu-id="077d6-183">After you obtain the device identifiers, you can create the appropriate interfaces.</span></span> <span data-ttu-id="077d6-184">Por exemplo, se você usar o XAudio 2,8, use este código para criar uma voz de mestre para este dispositivo:</span><span class="sxs-lookup"><span data-stu-id="077d6-184">For example, if you use XAudio 2.8, use this code to create a mastering voice for this device:</span></span>

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

<span data-ttu-id="077d6-185">Para obter informações sobre como usar o identificador de dispositivo capturaid, consulte [capturando um fluxo](/windows/desktop/CoreAudio/capturing-a-stream).</span><span class="sxs-lookup"><span data-stu-id="077d6-185">For info about how to use the captureId device identifier, see [Capturing a Stream](/windows/desktop/CoreAudio/capturing-a-stream).</span></span>

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a><span data-ttu-id="077d6-186">Obtendo GUIDs DirectSound (somente SDK do DirectX herdado)</span><span class="sxs-lookup"><span data-stu-id="077d6-186">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>

<span data-ttu-id="077d6-187">O headset que pode ser conectado a um controlador Xbox tem duas funções: ele pode gravar som usando um microfone e pode reproduzir som usando um fone de ouvido.</span><span class="sxs-lookup"><span data-stu-id="077d6-187">The headset that can be connected to an Xbox Controller has two functions: it can record sound using a microphone, and it can play back sound using a headphone.</span></span> <span data-ttu-id="077d6-188">Na API do XInput, essas funções são realizadas por meio do [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), usando as interfaces **IDirectSound8** e **IDirectSoundCapture8** .</span><span class="sxs-lookup"><span data-stu-id="077d6-188">In the XInput API, these functions are accomplished through [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), using the **IDirectSound8** and **IDirectSoundCapture8** interfaces.</span></span>

<span data-ttu-id="077d6-189">Para associar o microfone do headset e o fone de ouvido às interfaces [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) apropriadas, você deve obter o DirectSoundGUIDs para os dispositivos de captura e renderização chamando [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span><span class="sxs-lookup"><span data-stu-id="077d6-189">To associate the headset microphone and headphone with their appropriate [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) interfaces, you must get the DirectSoundGUIDs for the capture and render devices by calling [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span></span>

> [!Note]  
> <span data-ttu-id="077d6-190">O uso do [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) herdado não é recomendado e não está disponível em aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="077d6-190">Use of the legacy [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) is not recommended, and is not available in Windows Store apps.</span></span> <span data-ttu-id="077d6-191">As informações nesta seção se aplicam somente à versão SDK do DirectX do XInput (XInput 1,3).</span><span class="sxs-lookup"><span data-stu-id="077d6-191">The info in this section only applies to the DirectX SDK version of XInput (XInput 1.3).</span></span> <span data-ttu-id="077d6-192">A versão do Windows 8 do XInput (XInput 1,4) usa exclusivamente os identificadores de dispositivo da API de sessão de áudio do Windows (WASAPI) que são obtidos por meio do [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span><span class="sxs-lookup"><span data-stu-id="077d6-192">The Windows 8 version of XInput (XInput 1.4) exclusively uses Windows Audio Session API (WASAPI) device identifiers that are obtained through [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span></span>

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

<span data-ttu-id="077d6-193">Depois de recuperar os GUIDs, você pode criar as interfaces apropriadas chamando DirectSoundCreate8 e DirectSoundCaptureCreate8 da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="077d6-193">Once you have retrieved the GUIDs you can create the appropriate interfaces by calling DirectSoundCreate8 and DirectSoundCaptureCreate8 like this:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="077d6-194">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="077d6-194">Related topics</span></span>

[<span data-ttu-id="077d6-195">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="077d6-195">Programming Reference</span></span>](programming-reference.md)