---
title: Versões do XInput
description: O XInput é uma API de plataforma cruzada que foi enviada para uso no Xbox e Windows.
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

O XInput é uma API de plataforma cruzada que foi enviada para uso no Xbox e Windows. No Xbox, o XInput é lançado como uma biblioteca estática que é compilada no executável do jogo principal. No Windows, o XInput é fornecido como uma DLL instalada nas pastas do sistema do sistema operacional.

Há três versões atuais da DLL XInput atualmente. Escolha a versão apropriada do XInput com base na funcionalidade do XInput usada e nas versões do Windows que você pretende dar suporte.

- XInput 1.4: O XInput 1.4 é Windows 10. Use esta versão para criar aplicativos UWP.
- XInput 9.1.0: XInput 9.1.0 é Windows vista, Windows 7 e Windows 8. Use esta versão se o aplicativo da área de trabalho for executado nessas versões do Windows e você estiver usando a funcionalidade básica do XInput.
- XInput 1.3: O XInput 1.3 é um componente redistribuível no SDK do DirectX com suporte para Windows Vista, Windows 7 e Windows 8. Use esta versão se o aplicativo da área de trabalho for executado nessas versões do Windows e você precisar de funcionalidades que não têm suporte no XInput 9.1.0.

## <a name="xinput-14"></a>XInput 1.4

O XInput 1.4 é hoje um componente do sistema no Windows 8 como XINPUT1 \_4.DLL. Ele está disponível como "caixa de entrada" e não requer redistribuição com um aplicativo. O Windows SDK (Software Development Kit) contém o título e a biblioteca de importação para vinculação estaticamente ao XINPUT1 \_4.DLL. Para baixar o SDK Windows 8, consulte [Downloads para desenvolver aplicativos da área de trabalho](https://developer.microsoft.com/windows/downloads/).

O XInput 1.4 tem essas principais vantagens em relação a outras versões do XInput:

-   Essa é a única versão que pode ser usada em aplicativos C++/DirectX Windows Store.
-   A nova [**função XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) fornece uma cadeia de caracteres de ID do dispositivo de áudio que você pode usar para abrir um dispositivo de voz ou áudio de mestre XAudio2 para um headset anexado a um controlador comum do Xbox. A [**função XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) não está disponível nesta versão.
-   Fornece relatórios de recursos de dispositivo aprimorados, incluindo \_ \_ XINPUT CAPS WIRELESS, \_ XINPUT CAPS \_ FFB \_ SUPPORTED, XINPUT CAPS PMD SUPPORTD e XINPUT CAPS NO NAVIGATION flags e relatórios mais precisos de \_ \_ \_ \_ \_ \_ XINPUT \_ CAPS VOICE \_ \_ SUPPORTED. Esses sinalizadores são **combinados** no membro Flags da estrutura [**XINPUT \_ CAPABILITIES.**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) A [**função XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) retorna **XINPUT \_ CAPABILITIES.**

### <a name="xinput-910"></a>XInput 9.1.0

Assim como o XInput 1.4, o XInput 9.1.0 é hoje um componente do sistema no Windows 10, Windows 8.x, Windows 7 e Windows Vista como XINPUT9 \_ 1 \_0.DLL. Ele é mantido principalmente para compatibilidade com aplicativos existentes. Ele tem um conjunto de funções reduzido, portanto, recomendamos que você use xInput 1.4, se possível. Mas é conveniente usar para aplicativos que devem ser executados em versões de nível inferior do Windows, mas não precisam da funcionalidade de áudio adicional fornecida pelo XInput 1.4 ou XInput 1.3.

O Windows SDK contém o título e a biblioteca de importação para vinculação estaticamente ao XINPUT9 \_ 1 \_0.DLL.

O XInput 9.1.0 tem essas desvantagens em relação a outras versões do XInput:

-   Por motivos de compatibilidade com versões atrás, [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) nesta versão do XInput retorna informações de funcionalidade fixas. Independentemente do dispositivo do controlador comum do Xbox anexado, **XInputGetCapabilities** no XInput 9.1.0 sempre relatará um subtipo de dispositivo gamepad. Ele não retornará o bit de funcionalidade XINPUT \_ CAPS WIRELESS mesmo se um dispositivo sem fio estiver \_ conectado.
-   Não é possível determinar o headset para uma determinada ID de usuário. A [**função XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) não está disponível e a função [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) não retornará nenhum resultado em Windows 8.x ou Windows 10.
-   As [**funções XInputEnable,**](/windows/desktop/api/XInput/nf-xinput-xinputenable) [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)e [**XInputGetKeystrake**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) não estão disponíveis.

### <a name="xinput-13"></a>XInput 1.3

Algumas versões anteriores do XInput foram fornecidas como DLLs redistribuíveis no SDK do DirectX. A primeira versão redistribuível do XInput, XInput 1.1, enviada na versão de abril de 2006 do SDK do DirectX. A última versão a ser disponibilizada no SDK do DirectX foi o XInput 1.3, disponível na versão de junho de 2010 do SDK do DirectX herdado. *O SDK do DirectX não está mais disponível nos Downloads da Microsoft.*

Você pode usar o XInput 1.3 para aplicativos que suportam versões de nível inferior do Windows e exigem funcionalidade não fornecida pelo XInput 9.1.0 (ou seja, relatórios de subtipo corretos, suporte a áudio, suporte explícito a relatórios de bateria e assim por diante).
