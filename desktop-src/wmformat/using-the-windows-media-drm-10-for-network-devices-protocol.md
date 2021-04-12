---
title: Usando o protocolo Windows Media DRM 10 para dispositivos de rede
description: Usando o protocolo Windows Media DRM 10 para dispositivos de rede
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- SDK do Windows Media Format, Windows Media DRM 10 para dispositivos de rede
- SDK do Windows Media Format, DRM 10 para dispositivos de rede
- ASF (Advanced Systems Format), Windows Media DRM 10 para dispositivos de rede
- ASF (formato de sistemas avançados), Windows Media DRM 10 para dispositivos de rede
- Formato de sistema avançado (ASF), DRM 10 para dispositivos de rede
- Formato ASF 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows Media DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows Media DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- Windows Media DRM 10 para dispositivos de rede, protocolos
- DRM 10 para dispositivos de rede, protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292112"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a>Usando o protocolo Windows Media DRM 10 para dispositivos de rede

O Windows Media Format SDK fornece alguns recursos para dar suporte ao protocolo de dispositivo de rede seguro, Windows Media DRM 10 para dispositivos de rede. Esse protocolo define as mensagens enviadas entre um dispositivo de reprodução de mídia digital, como um player de vídeo de conjunto superior e o computador que atende aos dados para o dispositivo. Os dados de mídia enviados entre o servidor e o dispositivo são criptografados para protegê-lo da interceptação.

A comunicação entre o aplicativo e os dispositivos que dão suporte ao Windows Media DRM 10 para dispositivos de rede pode usar quaisquer protocolos de rede que você preferir. O Windows Media Format SDK não fornece nenhum objeto que execute as comunicações de rede para você. Em vez disso, os objetos desse SDK processam algumas mensagens do Windows Media DRM 10 para dispositivos de rede depois que seu aplicativo as recebeu.

Os recursos que dão suporte ao Windows Media DRM 10 para dispositivos de rede são o registro de dispositivo, a detecção de proximidade e a conversão de arquivos protegidos por DRM. Esses recursos são descritos nas seções a seguir.



| Seção                                                                                                                                                                          | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Registro de dispositivo](device-registration.md)                                                                                                                                   | Descreve como processar mensagens de solicitação de registro de dispositivos.                                                                       |
| [Executando detecção de proximidade](performing-proximity-detection.md)                                                                                                             | Descreve o processo de detecção de proximidade.                                                                                                 |
| [Convertendo um arquivo de DRM-Protected em um fluxo do Windows Media DRM 10 para dispositivos de rede](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | Descreve como converter um arquivo protegido por DRM em um fluxo que pode ser enviado para um dispositivo que usa o Windows Media DRM 10 para dispositivos de rede. |



 

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




