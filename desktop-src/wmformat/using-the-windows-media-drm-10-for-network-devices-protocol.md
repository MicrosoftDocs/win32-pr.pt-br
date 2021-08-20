---
title: Usando o Windows DRM de Mídia 10 para o Protocolo de Dispositivos de Rede
description: Usando o Windows DRM de Mídia 10 para o Protocolo de Dispositivos de Rede
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows SDK de formato de mídia, Windows DRM de mídia 10 para dispositivos de rede
- Windows SDK de formato de mídia, DRM 10 para dispositivos de rede
- ASF (Advanced Systems Format), Windows MEDIA DRM 10 para dispositivos de rede
- ASF (formato de sistemas avançados), Windows DRM de mídia 10 para dispositivos de rede
- ASF (Advanced Systems Format), DRM 10 for Network Devices
- ASF (formato de sistemas avançados), DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows DRM de mídia 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows DRM de mídia 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- Windows DRM de mídia 10 para dispositivos de rede, protocolos
- DRM 10 para dispositivos de rede, protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b22f87fcb6a6f6d9ee7f8ab7765c7023295d031996eb7ea9359782e040024b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118028500"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a>Usando o Windows DRM de Mídia 10 para o Protocolo de Dispositivos de Rede

O SDK Windows Formato de Mídia do Windows fornece alguns recursos para dar suporte ao protocolo de dispositivo de rede seguro, Windows DRM de Mídia 10 para Dispositivos de Rede. Esse protocolo define as mensagens enviadas entre um dispositivo de reprodução de mídia digital, como um player de vídeo set-top, e o computador que serve dados para o dispositivo. Os dados de mídia enviados entre o servidor e o dispositivo são criptografados para protegê-los contra interceptação.

A comunicação entre seu aplicativo e dispositivos que dá suporte Windows DRM de Mídia 10 para Dispositivos de Rede pode usar qualquer protocolo de rede que você preferir. O Windows SDK de Formato de Mídia não fornece nenhum objeto que execute as comunicações de rede para você. Em vez disso, os objetos desse SDK processam algumas Windows DRM de Mídia 10 para mensagens de Dispositivos de Rede depois que seu aplicativo as recebe.

Os recursos que suportam Windows DRM de Mídia 10 para Dispositivos de Rede são registro de dispositivo, detecção de proximidade e conversão de arquivos protegidos por DRM. Esses recursos são descritos nas seções a seguir.



| Seção                                                                                                                                                                          | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Registro de dispositivo](device-registration.md)                                                                                                                                   | Descreve como processar mensagens de solicitação de registro de dispositivos.                                                                       |
| [Executando a detecção de proximidade](performing-proximity-detection.md)                                                                                                             | Descreve o processo de detecção de proximidade.                                                                                                 |
| [Convertendo um arquivo DRM-Protected em um Windows drm de mídia 10 para fluxo de dispositivos de rede](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | Descreve como converter um arquivo protegido por DRM em um fluxo que pode ser enviado para um dispositivo que usa Windows DRM de Mídia 10 para Dispositivos de Rede. |



 

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




