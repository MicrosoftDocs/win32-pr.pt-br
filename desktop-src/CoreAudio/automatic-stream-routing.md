---
description: Este artigo descreve como atualizar uma implementação do WASAPI para tirar proveito do roteamento automático de fluxo.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Roteamento de fluxo automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920568"
---
# <a name="automatic-stream-routing"></a>Roteamento de fluxo automático

Este artigo descreve como atualizar uma implementação do WASAPI para tirar proveito do roteamento automático de fluxo.

A partir do Windows 7, sempre que o dispositivo de áudio padrão for alterado, o fluxo de reprodução de áudio de um aplicativo será transferido diretamente do dispositivo de áudio padrão anterior para o novo dispositivo de áudio padrão. Essa transferência ocorre automaticamente sem qualquer código de aplicativo adicional. No entanto, antes do Windows 10, a versão 1607, os aplicativos que usaram a API de sessão de áudio do Windows (WASAPI) de baixo nível não podiam participar dessa funcionalidade de roteamento de fluxo automatizado. Aplicativos que usam WASAPI eram necessários para implementar sua própria forma de roteamento de fluxo, adicionando código adicional para detectar a chegada e a remoção de dispositivos de áudio e alternar o fluxo para esses dispositivos, conforme apropriado. Aplicativos que usam WASAPI que não implementaram seu próprio mecanismo de roteamento de fluxo na chegada ou remoção do dispositivo, fornecendo uma experiência do usuário menos do que o ideal.

A partir do Windows 10, versão 1607, os aplicativos que usam o WASAPI podem aproveitar o roteamento automático de fluxo. Se seu aplicativo usar WASAPI, é altamente recomendável que você atualize seu aplicativo para aproveitar essa nova funcionalidade usando as seguintes etapas:

1.  O Windows 10, versão 1607, define dois novos GUIDs que podem ser usados para ativar uma interface de renderização ou captura de áudio com roteamento automático de fluxo, [ \_ \_ processamento de áudio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids) e [ \_ \_ captura de áudio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids). Obtenha uma representação de cadeia de caracteres dessas GUIDs chamando [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid). O exemplo a seguir mostra essa chamada para o GUID de renderização de áudio.

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  Ative o ponto de extremidade de áudio passando a cadeia de caracteres do identificador para a função WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) . O exemplo a seguir passa o identificador de renderização de áudio obtido na etapa 1:

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  Libere a memória alocada para manter o identificador do ponto de extremidade:

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

Depois de modificar seu aplicativo para ativar a interface de áudio da maneira descrita acima, ele participará do recurso de roteamento de fluxo automático.

Para demonstrar o roteamento automático de fluxo, use um laptop ou Tablet equipado com alto-falantes internos para reproduzir áudio. Você deve ouvir o áudio passando pelos alto-falantes internos do dispositivo. Enquanto o áudio estiver em execução, conecte um par de fones de ouvido. Agora você deve ouvir áudio passando pelos fones de ouvido. Em seguida, desconecte os fones de ouvido e o áudio deve rotear automaticamente de volta para os alto-falantes internos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Roteamento de fluxo](stream-routing.md)
</dt> <dt>

[**MediaDevice.GetDefaultAudioRenderId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**MediaDevice.GetDefaultAudioCaptureId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
