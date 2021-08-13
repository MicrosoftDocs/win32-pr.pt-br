---
title: Versões do XInput
description: O XInput é uma API de plataforma cruzada que foi enviada para uso no Xbox e no Windows.
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277712308ca6083147d10138ba4d78e7e0fa086df95a78ab2b8317abca567dba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430769"
---
# <a name="xinput-versions"></a>Versões do XInput

O XInput é uma API de plataforma cruzada que foi enviada para uso no Xbox e no Windows. No Xbox, o XInput é fornecido como uma biblioteca estática que é compilada no executável do jogo principal. no Windows, XInput é fornecido como uma DLL que é instalada nas pastas do sistema do sistema operacional.

Atualmente, há três versões atuais da DLL XInput. escolha a versão apropriada do XInput com base na funcionalidade do XInput que você usa e nas versões do Windows você pretende oferecer suporte.

- XInput 1,4: XInput 1,4 é fornecido como parte do Windows 10. Use esta versão para criar aplicativos UWP.
- XInput 9.1.0: XInput 9.1.0 é fornecido como parte do Windows Vista, Windows 7 e Windows 8. Use esta versão se seu aplicativo de área de trabalho for destinado a executar nessas versões do Windows e você estiver usando a funcionalidade básica de XInput.
- XInput 1,3: XInput 1,3 é fornecido como um componente redistribuível no SDK do DirectX com suporte para Windows Vista, Windows 7 e Windows 8. Use esta versão se seu aplicativo de área de trabalho for destinado a executar nessas versões do Windows e você precisar de uma funcionalidade que não tenha suporte do XInput 9.1.0.

## <a name="xinput-14"></a>XInput 1,4

o XInput 1,4 é fornecido hoje como um componente do sistema em Windows 8 como XINPUT1 \_4.DLL. Ele está disponível "Inbox" e não requer redistribuição com um aplicativo. o SDK (Software Development Kit) do Windows contém o cabeçalho e a biblioteca de importação para vinculação estática com o XINPUT1 \_4.DLL. para baixar o SDK do Windows 8, consulte [Downloads para desenvolver aplicativos da área de trabalho](https://developer.microsoft.com/windows/downloads/).

O XInput 1,4 tem essas vantagens principais em relação a outras versões do XInput:

-   essa é a única versão que pode ser usada em C++/DirectX Windows aplicativos da Store.
-   A nova função [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) fornece uma cadeia de caracteres de ID de dispositivo de áudio que você pode usar para abrir um dispositivo de voz ou áudio de mestre de XAudio2 para um headset anexado a um controlador comum do Xbox. A função [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) não está disponível nesta versão.
-   Fornece recursos aprimorados de relatórios, incluindo XINPUT \_ Caps \_ Wireless, XInput \_ Caps \_ FFB \_ com suporte, XInput \_ Caps \_ PMD \_ com suporte e XInput \_ Caps \_ sem \_ sinalizadores de navegação e relatórios mais precisos de XInput \_ Caps \_ Voice \_ com suporte. Esses sinalizadores são combinados no membro **flags** da estrutura de [**\_ recursos XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) . A função [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) retorna **\_ recursos de XInput**.

### <a name="xinput-910"></a>XInput 9.1.0

como o XInput 1,4, o XInput 9.1.0 é fornecido hoje como um componente do sistema em Windows 10, Windows 8. x, Windows 7 e Windows Vista como XINPUT9 \_ 1 \_0.DLL. Ele é mantido principalmente para compatibilidade com versões anteriores com aplicativos existentes. Ele tem um conjunto de funções reduzido, portanto, recomendamos que você use o XInput 1,4, se possível. mas é conveniente usar para aplicativos que devem ser executados em versões de nível inferior do Windows, mas não precisam da funcionalidade de áudio adicional fornecida pelo XInput 1,4 ou XInput 1,3.

o SDK do Windows contém o cabeçalho e a biblioteca de importação para vinculação estática contra XINPUT9 \_ 1 \_0.DLL.

XInput 9.1.0 tem essas desvantagens em relação a outras versões do XInput:

-   Por motivos de compatibilidade com versões anteriores, o [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) nesta versão do XInput retorna informações de capacidade fixas. Independentemente do dispositivo do controlador comum do Xbox conectado, **XInputGetCapabilities** em XInput 9.1.0 sempre relatará um subtipo de dispositivo do gamepad. Ele não retornará o bit de \_ \_ recurso sem fio do XInput Caps mesmo se um dispositivo sem fio estiver conectado.
-   Você não pode determinar o headset para uma determinada ID de usuário. a função [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) não está disponível e a função [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) não retornará nenhum resultado em Windows 8. x ou Windows 10.
-   As funções [**XInputEnable**](/windows/desktop/api/XInput/nf-xinput-xinputenable), [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)e [**XInputGetKeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) não estão disponíveis.

### <a name="xinput-13"></a>XInput 1,3

Algumas versões anteriores do XInput foram fornecidas como DLLs redistribuíveis no SDK do DirectX. A primeira versão redistribuível do XInput, XInput 1,1, foi fornecida na versão de abril de 2006 do SDK do DirectX. A última versão a ser enviada no SDK do DirectX foi a XInput 1,3, disponível na versão de junho de 2010 do SDK do DirectX herdado. *O SDK do DirectX não está mais disponível nos downloads da Microsoft*.

você pode usar o XInput 1,3 para aplicativos que oferecem suporte a versões de nível inferior do Windows e exigir funcionalidade não fornecida pelo XInput 9.1.0 (ou seja, relatórios de subtipo corretos, suporte a áudio, suporte a relatórios de bateria explícito e assim por diante).
